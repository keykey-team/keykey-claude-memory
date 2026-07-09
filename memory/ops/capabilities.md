# Мої можливості — що я вмію робити для Влада
*Оновлено: 2026-06-10 · scheduled-tasks звірено 2026-06-26 (weekly-audit): 4 enabled, агенти призупинені 24.06*

> Читаю коли хочу запропонувати автоматизацію або коли Влад питає "чи можеш ти..."

---

## 🔧 Skills — каталоги для самовдосконалення (09.06.2026)

**Протокол (оновлено 09.06.2026):** скіли вмикаю САМ, без запиту дозволу. Перед задачею дивлюсь мапу нижче → вмикаю потрібний скіл. Нема скіла → шукаю в каталогах і пропоную встановити.

### 🗺️ Мапа: задача → скіл (автономний вибір)

| Задача | Скіл |
|--------|------|
| Аналіз конкурентів (звіт) | `product-management:competitive-brief` або `brightdata:competitive-intel` (live data) |
| Метрики продуктів | `product-management:metrics-review` |
| Roadmap FREEMO R / ONEQ / KEY SPACE | `product-management:roadmap-update` |
| Специфікація фічі | `product-management:write-spec` |
| Аналіз воронки продажів | `sales:pipeline-review` |
| Прогноз продажів | `sales:forecast` |
| Дослідження клієнта/ліда | `sales:account-research` |
| Підготовка до дзвінка | `sales:call-prep` |
| Battlecard конкурента | `sales:competitive-intelligence` |
| Аналіз даних/таблиць | `data:analyze` / `data:explore-data` |
| Дашборд | `data:build-dashboard` |
| Перевірка аналізу перед показом | `data:validate-data` |
| Глибоке дослідження ринку | `deep-research` або `brightdata:live-research` |
| Що кажуть про бренд у соцмережах | `brightdata:brand-listening` |
| Стратегічне рішення | `council` |
| Пошук лідів | `lead-research-assistant` |
| Зробити текст людським | `humanizer` |
| 🎬 ВІДЕО YouTube — аналіз | Higgsfield `video_analysis_create(youtube_url)` → poll status 3-5 хв. НЕ клікати по YouTube UI — повільно! (правило 10.06) |
| 🎬 Відео TikTok/Instagram/файл | Влад кидає файл → ffmpeg кадри + faster-whisper звук (~1 хв, відпрацьовано) або Higgsfield media_upload |
| Робота з людьми: фідбек, складна розмова, конфлікт, мотивація, жорстке повідомлення Влада | `people-mirror` ✅ (кастомний, встановлено 09.06) |
| Найм, перформанс-рев'ю, орг-структура, офери | `human-resources:*` ✅ встановлено |
| Контент Reels/TikTok, контент-стратегія, кампанії | `marketing:content-creation` / `content-strategy` / `campaign-plan` |
| Дотиснути оплати/дебіторку (Віктор UBC) | `small-business:invoice-chase` |
| Прогноз каси 30/60/90 днів | `small-business:cash-flow-snapshot` |
| Рев'ю договору з клієнтом | `small-business:contract-review` |
| Вакансія: пост + інтерв'ю-гайд + офер | `small-business:job-post-builder` + `human-resources:interview-prep` |

| Ресурс | Скіли | Особливість |
|--------|-------|-------------|
| [skills.sh](https://www.skills.sh/) | 692K | Офіційний реєстр Vercel, top-leaderboard |
| [skillhub.club](https://skillhub.club/) | 87K | AI-оцінка S/A/B, curated stacks |
| [skillsmp.com](https://skillsmp.com/) | 1.6M | Найбільший каталог, пошук по категоріях |

**Як встановлюю:** fetch SKILL.md з GitHub → пакую як .skill → Влад натискає "Save skill"

### Встановлені скіли (09.06.2026)

| Скіл | Джерело | Функція |
|------|---------|---------|
| `council` | custom | 5-advisor LLM Council для складних рішень |
| `systematic-debugging` | obra/superpowers | Iron Law: без root cause — без fix |
| `brainstorming` | obra/superpowers | HARD-GATE: дизайн до коду |
| `ui-ux-pro-max` | nextlevelbuilder | 67 стилів, 161 палітра, 99 UX-правил |
| `writing-plans` | obra/superpowers | Плани реалізації з TDD-завданнями |
| `test-driven-development` | obra/superpowers | Red-Green-Refactor, Iron Law |
| `subagent-driven-development` | obra/superpowers | Свіжий субагент на кожне завдання |
| `lead-research-assistant` | davepoon/buildwithclaude | Пошук лідів: ICP → скоринг → стратегія |

### Встановлені плагіни (09.06.2026) — Cowork
| Плагін | Скіли |
|--------|-------|
| `product-management` | competitive-brief, metrics-review, roadmap-update, write-spec, sprint-planning, stakeholder-update, synthesize-research, product-brainstorming |
| `sales` | competitive-intelligence, pipeline-review, account-research, forecast, call-prep, call-summary, daily-briefing, draft-outreach |
| `data` | analyze, build-dashboard, create-viz, explore-data, sql-queries, statistical-analysis, validate-data |
| `brightdata` | competitive-intel, live-research, brand-listening, scrape, search, price-comparison, seo-audit (потребує BRIGHTDATA_API_KEY для частини функцій) |
| `human-resources` | performance-review, org-planning, interview-prep, comp-analysis, draft-offer, onboarding, recruiting-pipeline, people-report |
| `marketing` | content-creation, content-strategy (через draft-content), campaign-plan, email-sequence, performance-report, brand-review, competitive-brief, seo-audit |
| `small-business` | invoice-chase, cash-flow-snapshot, contract-review, business-pulse, monday-brief, margin-analyzer, job-post-builder, customer-pulse, month-end-prep + ~20 інших |
| `people-mirror` | кастомний скіл для роботи з командою: фрейми фідбеку, шпаргалка по команді |

---

## 📅 Google Calendar
- Переглядати події на день/тиждень
- Створювати нагадування і події
- **Проактивно:** якщо є важлива дата — одразу пропоную нагадування

## 📋 Notion
- Читати задачі, проєкти, зустрічі
- Оновлювати статуси задач
- Шукати по базі, фільтрувати по людині/проєкту/статусу
- **Проактивно:** після аналізу задач — повідомляю про блокери

## 💾 Google Drive
- Читати файли (Excel, Docs, PDF)
- Аналізувати фін-таблицю KeyKey
- **Проактивно:** якщо >7 днів без оновлення фін-таблиці — нагадую

## 📧 Gmail
- Шукати листи, читати threads
- Створювати чернетки листів
- **Проактивно:** можу допомогти з текстом КП або follow-up листа

## 🎨 Higgsfield (AI генерація)
- **Зображення:** безкоштовно — генерую банери, рекламу, ілюстрації
- **Відео:** потребує PLUS план ($49/міс) — поки недоступно
- **Проактивно:** якщо потрібна графіка для контенту — пропоную

## 🎨 Canva
- Створювати і редагувати дизайни
- Генерувати з шаблонів
- Експортувати файли
- **Проактивно:** альтернатива Higgsfield для статичних матеріалів

## 💬 Telegram MCP (chigwell/telegram-mcp) — оновлено 10.06.2026
- **🎙️ ГОЛОСОВІ: транскрибація працює** (тест 10.06: download_media → faster-whisper base/int8 у sandbox, мова авто, якість бойова). Вшито в ceo-hourly-brief. Сліпа зона голосових ЗАКРИТА.
- **Встановлено:** ~/telegram-mcp-chigwell (uv, session string)
- **get_history / list_messages** → повертає: `sender`, `date`, `sender_id`, `text`, `media`
- **list_chats** → chat_id, title, type, unread, muted
- 80+ інструментів: читання, пошук, відправка, реакції, медіа
- **Відмінність від старого:** старий (sparfenyuk) повертав тільки text без metadata

## ⏰ Scheduled Tasks — РЕАЛЬНИЙ стан (звірено 26.06.2026 через list_scheduled_tasks)
> 🔴 ВАЖЛИВО: 24.06 Влад призупинив частину агентів (ліміт Claude вичерпано + проектується нова архітектура AI-агентів, перенос на сервер) [focus.md 24–25.06]. Звітні агенти й оркестратор/критик/CEO ВИМКНЕНІ. Працює лише інфраструктура пам'яті + розвідка.

**✅ ENABLED (4, станом на 26.06):**
| Задача | Коли | Що |
|--------|------|-----|
| `daily-memory-update` | Пн-Пт 08:00 | оновлення пам'яті з Notion+Drive + git/хмара бекап |
| `claude-self-audit` | Пн-Пт 20:00 | аудит МОЇХ сесій (джерела/факти) + звіт росту |
| `oneq-competitor-scan` | Пн/Ср/Пт 10:00 | AI-розвідка (конкуренти+ідеї+тренди) → гілка 🌍 Ринок супергрупи Оркестр |
| `weekly-memory-audit` | Пт 18:00 | аудит пам'яті: суперечності + приватність хмари + патерни тижня |

**⛔ DISABLED — призупинено 24.06 (ліміт Claude / нова архітектура):** `agent-orchestrator` (картина дня 08/18), `agent-critic` (тінь агентів, кожні 30хв), `ceo-growth` (драйвер до $1М, 2×/день), `voronka-monitor` (моніторинг KEY SPACE 30хв), `team-hourly-brief` (опер. звіт 09/17).
**⛔ DISABLED раніше:** `ceo-full-snapshot` (ВИМКНЕНО 22.06 — Влад: «у CEO-групу звіти більше не слати, повну картину дає оркестратор»), `weekly-ideas-scan` (→ oneq-competitor-scan), `weekly-metrics-snapshot` (metrics прибрано).
**🗑️ ВИДАЛЕНО раніше:** ceo-hourly-brief, ceo-daily-brief, puchko-control, telegram-memory-update, weekly-business-report, daily-personal-session, telegram-setup/login-reminder.

## 🌐 Chrome / Браузер
- Відкривати сайти, читати контент
- Аналізувати Instagram, TikTok (без авторизації — читаю публічне)
- Заповнювати форми (з дозволу Влада)
- **Обмеження:** не можу кликати якщо вимагає авторизацію

## 💻 Bash / Код
- Запускати Python, Node.js скрипти
- Аналізувати відео (ffmpeg, ffprobe)
- Обробляти файли, конвертувати формати
- Встановлювати пакети

## 📄 Файли
- Читати і редагувати будь-які файли в папці проєкту
- Створювати HTML сайти, Excel таблиці, Word документи, PDF, PowerPoint
- **Проактивно:** якщо результат зручніше у файлі — роблю файл без запиту

## 🧠 Пам'ять
- Читати і оновлювати всі memory/ файли
- Фіксувати рішення, інсайти, помилки в реальному часі
- Відстежувати контекст між сесіями через sessions.md

## ❌ Що НЕ можу (або потребує дозволу Влада)
- Відправляти листи або повідомлення ІНШИМ ЛЮДЯМ (тільки чернетки — відправляє Влад). Виняток: звіти самому Владу в його Telegram Saved Messages — дозволено 09.06.2026
- Переводити гроші або підтверджувати платежі
- Видаляти файли назавжди
- Входити в акаунти (вводити паролі)

## ⏰ Scheduled — НОВА СТРУКТУРА (16.06.2026, чистка 16→ядро)
Звіти 2, обидва Пн-Пт 09:00 і 17:00:
- ceo-full-snapshot → CEO-звіт, повний доступ (фінанси) → CEO KEYKEY (-5170325075)
- team-hourly-brief → Операційний звіт, без фінансів/особистого → Ассистент KeyKey (-5399016122)
Моніторинг: voronka-monitor — кожні 30хв (Пн-Пт 9-19) воронка+коментарі+блокери → Ассистент KeyKey з тегом відповідальних карток.
Інфраструктура: daily-memory-update (8:00), weekly-memory-audit (Пт 18:00) — гігієна пам'яті + аналіз патернів компанії за тиждень (люди/клієнти/проблеми).
ВИМКНЕНО/прибрано: ceo-hourly-brief, + 7 мертвих (telegram-reminder×2, daily-personal-session, ceo-daily-brief, puchko-control, weekly-business-report, telegram-memory-update).
РІШЕННЯ 16.06: metrics+ideas прибрано; oneq-competitor-scan → тижнева AI-розвідка (конкуренти+ідеї, Пн→Saved Messages); claude-self-audit лишено.
