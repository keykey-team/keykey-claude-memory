# KEY SPACE — Integration API (довідка)
*Оновлено: 2026-06-16 · джерело: [Макс, integration-api.md 16.06] + перевірено наживо curl*

Базовий URL: `https://keyspace.keykey.com.ua/api`
Авторизація: **немає** (поки відкриті, read-only). Формат: `{ "count": <n>, "data": [...] }`. Лише не видалені (`isDeleted=false`).
⚠️ Перед публічним використанням Макс планує закрити токеном (`Authorization: Bearer <token>`).

## 1. GET /api/integrations/pipeline — картки воронки
Поля: `id` (cuid), `dealNumber` (людський №), `title`, `company|null`, `status.key`, `status.name` («Шаг N: …»), `value|null`, `currency` (UAH/USD/EUR), `manager{id,name,email}|null`, `responsibles[]{id,name,email}`, `createdAt`, `statusChangedAt` (зміна етапу; fallback updatedAt), `updatedAt`.

## 2. GET /api/integrations/pipeline/{id}/comments — коментарі картки
`{id}` = id картки з #1. Хронологічно (старі→нові). Поля: `author{name,email}|null`, `text`, `createdAt`. Нема → `{count:0,data:[]}`.

## 3. GET /api/integrations/pipeline/{id}/logs — ЖУРНАЛ ЗМІН картки ⭐ (Макс додав 16.06)
`{id}` = id картки з #1. Усі зафіксовані зміни: створення, редагування полів, зміна етапу, задачі, коментарі. Хронологічно. Поля: `action`, `entityType` (Deal/Task/Comment), `entityName|null`, `details|null`, `user{name,email}|null`, `createdAt`.

**Реальні значення `action` / `details` (перевірено наживо):**
- `Створено угоду` — створення картки. details=null.
- `Змінено статус угоди` — **зміна етапу**. details = `OLD_KEY → NEW_KEY` (ключі статусів, напр. `СОГЛАСОВАНИЕ_ТЗ_mq84sgg6 → ФОРМИРОВАНИЕ_ТЗ_mq84s849`). user = хто перемістив. ← точний напрям руху, не треба вгадувати.
- `Оновлено угоду` — редагування поля. ⚠️ details на практиці = **null** (яке саме поле — НЕ вказано; перевірено на 24 подіях, усі null). Тобто зміну СУМИ з логу не видно — лови порівнянням `value`/`currency` зі знімком pipeline (#1), не з логом. `user` = хто редагував (можна назвати виконавця, зіставивши за часом).
- `comment_added` — коментар. entityName=null, details = повний текст коментаря, user = автор.

Щоб визначити напрям (вперед/відкат) зі зміни статусу: ключі мапляться на «Шаг N» через назви етапів (status.name з #1). Тримати словник key→«Шаг N» у voronka-state. NEW крок < OLD → відкат 🔙; > → вперед ✅.

## 4. GET /api/integrations/orders — замовлення
Поля: `id`, `orderNumber`, `serviceName`, `company|null`, `amount|null` (totalUAH або budget), `currency`, `status` (DRAFT/CONFIRMED/IN_PROGRESS/COMPLETED/CANCELLED), `paymentStatus` (NOT_PAID/PARTIAL/PAID), `manager{id,name,email}|null`, `createdAt`, `deadline|null`. (Логів/коментарів по orders НЕМАЄ — лише знімок-діф.)

## Хто використовує
- `voronka-monitor` (кожні 30 хв) — #1 + #4 знімок-діф + #3 logs (дельти етапів/коментарів з автором).
- `team-hourly-brief`, `ceo-full-snapshot` — #1 + #4. Потенційно можуть використати #3 logs для «що змінилось за годину» (поки не підключено — кандидат на апгрейд).
