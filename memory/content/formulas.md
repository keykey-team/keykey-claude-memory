# Формули і рецепти що працюють
*Оновлено: 2026-06-08*

> Сюди потрапляє тільки те що вже ДОВЕЛО ефективність. Не теорія — практика.

---

## 📱 Вірусний Reel/TikTok про AI-інструмент

**Коли використовувати:** просування ONEQ, KeyKey, будь-якого AI-продукту

**Структура (30-60 сек):**
1. **Hook (0-3 сек):** "[Результат] без [страху/болю]" — наприклад "Преміум сайт без коду"
2. **Демо (3-40 сек):** split screen — обличчя + скрін продукту в дії
3. **Результат (40-50 сек):** показуєш що вийшло, не процес
4. **CTA (50-60 сек):** "Напиши [СЛОВО] в коментарях" → надаєш матеріал в DM/Telegram

**Правила:**
- Фон: lifestyle (кав'ярня, вулиця, природа) — НЕ офіс
- Субтитри: великі, 3-5 слів, контрастні
- Мова: українська
- Comment bait word: одне просте слово ("Старт", "Хочу", "Гайд")

**Референс:** @dashi_agent — 1804 ❤️ / 1949 💬 за 6 днів

---

## 🌐 3D преміум сайт (HTML/JS)

**Коли використовувати:** лендінги для продуктів KeyKey, клієнтські сайти

**Стек:**
- Three.js (CDN r128) — particle system, wireframe геометрія
- CSS glassmorphism — `backdrop-filter: blur()`, rgba borders
- Custom cursor — точка + trailing кільце
- Scroll reveal — IntersectionObserver
- Mouse parallax — camera.position слідує за мишею

**Ключові ефекти:**
- Particle system: 2000-3000 частинок, ShaderMaterial для кольору і руху
- Floating shapes: TorusGeometry, OctahedronGeometry, IcosahedronGeometry (wireframe, opacity 0.1-0.15)
- Glassmorphism: `background: rgba(255,255,255,0.04)`, `border: 1px solid rgba(255,255,255,0.08)`
- Gradient text: `-webkit-background-clip: text`, `-webkit-text-fill-color: transparent`

**Референс:** showcase-3d.html (2026-06-08)

---

## 📊 Comment Bait механіка (Instagram/TikTok)

**Як працює:**
1. В відео або описі: "Напиши [СЛОВО] — надішлю [матеріал]"
2. Люди пишуть → багато коментарів → алгоритм підсилює пост
3. Ти надсилаєш матеріал в DM або через ManyChat автоматично

**Чому ефективно:** Instagram/TikTok ранжують за engagement rate. Коментар = сильніший сигнал ніж лайк.

**Найкращі слова-тригери:** "Список", "Гайд", "Старт", "Хочу" — прості, без зусиль

---

## 🔔 Ранковий брифінг CEO (scheduled task)

**Формула:** Calendar → Notion tasks → Finance → Leads → Projects → Рішення потрібні
**Час:** 08:30 Пн-Пт
**Файл:** `/Users/vlad/Claude/Scheduled/ceo-daily-brief/SKILL.md`
