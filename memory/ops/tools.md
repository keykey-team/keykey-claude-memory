# Інструменти та MCP
*Оновлено: 2026-06-09*

## Claude MCP підключення

### Notion
- Tasks DB ID: `1a6be50a-aef3-812b-a81f-000bdcc70894`
- Query: `mcp__dc05e372-d6a2-4191-9593-55cc59d1b91c__notion-query-database-view`
- Meetings: `mcp__dc05e372-d6a2-4191-9593-55cc59d1b91c__notion-query-meeting-notes`
- Fetch: `mcp__dc05e372-d6a2-4191-9593-55cc59d1b91c__notion-fetch`

**Notion Views:**
```
VIEW_DONE      = 'view://c999a4a9-940e-4d6a-8781-f7a7643c173a'
VIEW_DUE       = 'view://1a6be50a-aef3-81e2-8e55-000c1d027e1e'
VIEW_ACTIVE    = 'view://378be50a-aef3-81ad-baaf-000c327746f6'
VIEW_BY_PERSON = 'view://378be50a-aef3-81f8-baf1-000cebccc3a3'
```

**Tasks DB Full URL (для notion-query-database-view):**
`https://www.notion.so/keykeyua/1a6be50aaef380b9ab23c317a11ee710?v=1a6be50aaef3803b806f000c88ee0987`

**Поля задач (flattened формат MCP):**
- `Блок / Задача` — string (назва)
- `Статус задачи` — string: Активна, Принята, На правках, Проверка, На паузе, Жду от Клиента, Жду от Команды, Не начата, Завершена, Отменена, На потом
- `Исполнитель` — string JSON array: `"[\"user://UUID\"]"` → парсити через JSON.parse + replace user://
- `date:Дедлайн:start` — "YYYY-MM-DD" (або ISO datetime якщо is_datetime=1)
- `date:Дедлайн:is_datetime` — 0 або 1
- `Оценка` — string "1"-"5" (рідко заповнено)
- Активні статуси: Активна, Принята, На правках, Проверка, На паузе, Жду от Клиента, Жду от Команды

**Task Fields:** `Блок / Задача`, `Статус задачи`, `Виконавець (Исполнитель)` (user://UUID), `Дедлайн`, `Приоритет` (1/2/3), `Направление`, `Спринт`, `Проект`

### Google Calendar
- Calendar ID: `v.naidyuk.keykey@gmail.com`
- Tool: `mcp__8955aa74-325e-4e9c-95e9-d6ec52b31092__list_events`
- Timezone: `Europe/Kiev`

### Telegram ✅ ПІДКЛЮЧЕНО І ПРАЦЮЄ
- Метод: mcp-telegram (Telethon, user account)
- API ID: `34197750`
- Phone: `+380663558448`
- Скрипт: `/Users/vlad/Claude/Projects/Асистент/tg-login.applescript`
- Статус: **повністю активно з 2026-06-09 о 10:50**
- Tools: `mcp__mcp-telegram__ListDialogs`, `mcp__mcp-telegram__ListMessages`

**Ключові чати (ID) — ✅ звірено з `list_chats` 09.07.2026:**
- `Операционка KEYKEY` = -5298456424 ✅ активний
- `CEO KEYKEY` = **-1003936897492** ✅ (мігрував у супергрупу 03.07; старий `-5170325075` мертвий)
- `TeamLead KEYKEY` = **-1003978041033** ✅ (мігрував 03.07; старий `-5248408551` мертвий)
- `VARUS (внутрянка)` = **-5492474632** 🆕 (робочий чат по головному проєкту)
- `SEO (projects)` = -1003946998757 ✅
- `KeySpace` = -1004290229957 ✅ · `KEY SPACE flud` = -5181932392
- `ONEQ` = **-1003813562578** ✅ (старий `-4994273943` не в списку діалогів)
- `FREEMO R` = -1003940370622 ✅
- `UBC (внутрянка)` = -1003841419313 · `UBC (корп. сайт + AI)` = -5204347620 · `AI Tutor (UBC)` = -1004435228243
- `Оркестр` = -1004382201296 · `Дизайн KEYKEY` = -1002600903312 · `IT Space` = -5159936872 · `Projects` = -1002574970806
- `General KEYKEY` = -1004394580514 (архівований)
- Внутрянки клієнтів: Rosteria -1004291995659 · Sana -1004216632074 · Travnitsa -1004477876077 · Power Pro -1004486121115 · Led Tech -1004497690305 · World of Heels -1003902713111 · Maloe Atelier -1004385156820 · 4Chesse -1004312711670

🔴 **НЕ ІСНУЮТЬ у списку діалогів (09.07) — прибрано з опитування, повертали GEN-ERR:**
- ~~`ОП KEYKEY` = -1003400194567~~ — GEN-ERR-386 (раніше -631/-434/-292/-183/-804). Не в `list_chats`.
- ~~`AI направление` = -1004438639966~~ — GEN-ERR-386. Не в `list_chats`. Найближчий за змістом активний: `AI Tutor (UBC)` -1004435228243.
- Старі ID до міграції 03.07: `-5170325075` (CEO), `-5248408551` (TeamLead), `-1002288266883` (General), `-4994273943` (ONEQ), `-5229784602` (KEY SPACE), `-1003845516218` (Проекти), `-5009876751`, `-5006249121`, `-1002844955236`.

**Особисті чати команди:** Артем Horobets `202483716` · Артем Лайф (@Horobets_KeyKey) `6280043224` · Лера `8925990080` (старий `748039166`) · Пучко `7263616652` · Нікіта `575632161` (новий `8906043835`) · Макс `7293016451` · Гордєєв `971605766` (новий @Gordienko_KeyKey `8239055391`) · Льоша `8872225599` · Алексей ONEQ `1049110033` · Влад (self) `8669951150`

## AI Інструменти для розробки

### Google Antigravity (Gemini-based)
*Обговорено 25.05.2026 на стендапі команди*
- **Сильні сторони:** Генерує 3D-моделі, анімації, великий набір ефектів. Хороший для дизайну корпоративних сайтів.
- **Слабкі сторони:** Слабший у коді порівняно з Claude/Gemini/GPT. Погано оптимізує код.
- **Як використовувати:** Завантажити правила розробки в GitHub репозиторій → Antigravity читає stack і пише по нашим правилам
- **Workflow:** Нікіта набрасує першу версію головної сторінки → команда дочищає код
- **Статус:** Потрібно протестувати на реальному проєкті

---

## Артефакти
- **IT Dashboard** — artifact `it-team-dashboard`, файл `it-dashboard-v3.html`
  - 6 вкладок: Сьогодні / Завтра / Тиждень / По людях / Всі активні / Зустрічі
- **Team Capacity** — artifact `team-capacity` (09.06.2026)
  - Live дашборд завантаженості: активні задачі по людях, прострочені, без виконавця
  - Пагінує всі задачі з Tasks DB, фільтр по кліку на людину

## Claude підписки в команді (09.06.2026)
| Співробітник | Тариф | Вартість |
|-------------|-------|---------|
| Максим Уваровський | Claude Pro ($20/міс) | $20/міс |
| Коляда (? — уточнити) | Claude Max ($100/міс) | $100/міс |
| **Разом** | | **$120/міс** |
*Оплачується з бюджету KeyKey*

## Scheduled Tasks
- `daily-memory-update` — щодня о 9:00, оновлює memory/*.md з Notion
- `telegram-login-reminder` — одноразово 2026-06-09 о 10:00


## 🐙 GitHub (підключено 10.06.2026)
- **Токен:** fine-grained від Влада Пучка, лежить у `.secrets/github.token` (НЕ в git — у .gitignore). Термін дії — перевірити через ~90 днів
- **Доступні репо (org keykey-team):** `key-space`, `oneq`, `ubc`. FREEMO R — назва репо невідома/нема доступу, уточнити у Пучка
- **Використання:** `TOKEN=$(cat .secrets/github.token)` → `git ls-remote https://x-access-token:${TOKEN}@github.com/keykey-team/REPO.git`
- **Призначення:** контроль "слова vs код" у брифах + бекап пам'яті
- **Бекап-репо `keykey-claude-memory`:** ✅ працює з 10.06. ДВА РІВНІ: локальний git = повна історія; хмара = ТІЛЬКИ фільтрований зріз через scripts/cloud-backup.sh (рішення Влада: особисте НЕ в хмару — виключаються memory/vlad/, telegram/keykey.md, failure-investigation.md, sessions.md, drafts/). Окремий write-токен: .secrets/github-backup.token. НІКОЛИ не пушити в хмару повз скрипт!
- Перший факт 10.06: Максим — коміти нумерації воронок і RBAC = рівно те, що обіцяв на онбординзі. Слова = код ✅


## 🌐 Зовнішні API (перевірено 10.06.2026)
- ✅ **Курс валют:** api.privatbank.ua/p24api/pubinfo?json&exchange&coursid=11 — працює (USD/EUR купівля/продаж). У ранковому брифі щодня.
- ⛔ **bank.gov.ua (НБУ)** — НЕ відповідає з sandbox (порожнє тіло, 3 спроби). Не використовувати.
- ⛔ **timeapi.io, cloudflare trace та будь-які часові API** — веб-канал sandbox КЕШУЄТЬСЯ проксі (доказ: cloudflare ts відстав на 4 дні). Час ТІЛЬКИ з sandbox date (точний) + серверні мітки Telegram (локальний MCP, без кешу).

## 📋 Notion: задачники (від Влада 10.06.2026)
- ЄДИНА база задач: collection://1a6be50a-aef3-812b-a81f-000bdcc70894 ("Основний задачник") — фільтрувати по Исполнитель=UUID (UUIDs у people/team.md)
- Пучко "Планер": https://app.notion.com/p/345be50aaef380318d76c047432edcb7 (inline view у його кабінеті)
- Лера в'юхи: https://www.notion.so/keykeyua/2eebe50aaef380e0a3c7ccf0cb59fdba (Сегодня/Будущие/Планер/Завершенные; фільтр me — для запитів використовувати UUID f0c98b8f-7b74-4488-8188-0828f1b90948)
- Поля для пульсу: Статус задачи · Дедлайн · Планер · Приоритет · Блокирующая + Статус блокирующей задачи (готовий блокер-граф: хто кого блокує!)


## 🟢 KEY SPACE API (підключено 11.06.2026 — Максим зробив)
Base: https://keyspace.keykey.com.ua/api · read-only · поки БЕЗ авторизації (закрити токеном перед публічним) · формат {count, data[]}, тільки isDeleted=false
- **GET /api/integrations/pipeline** — воронка: id, dealNumber, title, company, status{key,name}, value, currency, manager{name,email}, responsibles[], createdAt, statusChangedAt, updatedAt
- **GET /api/integrations/orders** — замовлення: orderNumber, serviceName, company, amount, currency, status (DRAFT/CONFIRMED/IN_PROGRESS/COMPLETED/CANCELLED), paymentStatus (NOT_PAID/PARTIAL/PAID), manager, deadline
- ⚠️ У scheduled-брифах читати ЧЕРЕЗ curl у bash, НЕ web_fetch (web_fetch блокує ці URL у авто-сесії — provenance, бо URL не від користувача). У живій сесії з Владом web_fetch працює (URL у контексті). Воронка 19 угод, замовлень 29 (станом 11.06)
- ⚠️ є тестові картки ("Тест 45", "вапвыпвап", "Тов тест 15") — фільтрувати при аналізі
- Менеджер у воронці = здебільшого Артем (створює картки); responsibles = реальний відповідальний


## 🔌 KEY SPACE API — карта (звірено 15.06.2026, curl)
Base: `https://keyspace.keykey.com.ua`
- ✅ `/api/integrations/pipeline` — воронка, БЕЗ auth. Поля: id, dealNumber, title, company, status{key,name}, manager{name,email}, responsibles[]{name,email}, createdAt, statusChangedAt, updatedAt. value=null (сум нема тут). 24 картки.
- ✅ `/api/integrations/orders` — замовлення, БЕЗ auth. orderNumber, serviceName, company, amount, budget, status, paymentStatus, manager, deadline.
- ⛔ Коментарі карток: integration API НЕ віддає (pipeline/orders/expand/include/card-detail — нема).
- 🔑 `/api/comments?dealId={id}` та `/api/deals/{id}` — ІСНУЮТЬ, але **401 (треба auth)**. Шлях до коментарів = основний API за токеном.
- ➡️ Для адресних сигналів у звітах: або Льоша додає `/api/integrations/pipeline/{id}/comments` (без auth, як pipeline), або джерело блокерів — Telegram-групи.
- 🔒 УТОЧНЕНО 16.06.2026 (Влад дав офіц. integration-api.md + curl): інтеграційний API = ТІЛЬКИ `pipeline` + `orders`. Коментарів там не буде. `/api/comments`→401 — це ВНУТРІШНІЙ API (сесійна auth), Bearer-токен інтеграції його НЕ відкриє → НЕ радити «.secrets/keyspace.token для коментарів» (хибно). Шар коментарів = лише через доробку Льоші.
- 🔀 voronka-monitor (16.06): pipeline-дельти (нові/зміна етапу) → Ассистент KeyKey `-5399016122` (без сум); orders-дельти (нові/статус/оплата, з сумами) → CEO KEYKEY `-5170325075`.

## ✅ KEY SPACE API — ОНОВЛЕНО 16.06 (Макс відкрив коментарі)
`GET /api/integrations/pipeline/{id}/comments` — БЕЗ auth → `{count, data:[{author{name,email}, text, createdAt}]}`, хронологічно. {id} = поле id картки з /pipeline. Стара примітка про 401/токен — ЗАСТАРІЛА, коментарі тепер відкриті. pipeline тепер віддає і value+currency. Вшито в voronka-monitor + team-hourly + ceo-full.

## KEY SPACE — логи змін (16.06): у платформі Є, в API ще НЕМАЄ
Перевірено curl: /logs, /activity, /history, /pipeline/{id}/history, /audit — усі 404. Влад каже на платформі логи змін є. Потрібен endpoint від Макса (ТЗ): `GET /api/integrations/pipeline/{id}/history` (або /logs) → події картки: {type (stage_change/comment), from, to, author{name,email}, createdAt}, без auth. Дасть точну подію (хто/коли/з→на) замість порівняння знімків. Поки — voronka-monitor визначає відкат за номером «Шаг N» (менший = назад).
