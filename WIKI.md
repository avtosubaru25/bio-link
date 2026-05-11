# 📖 WIKI — Bio Link страница для Instagram

## 🗂️ Структура папки

```
bio-link/
├── index.html          ← Главный файл страницы (ВСЁ здесь)
├── README.md           ← Краткое описание проекта
├── WIKI.md             ← Этот файл — полная документация
├── netlify.toml        ← Конфиг для деплоя на Netlify
└── .gitignore          ← Исключения для Git
```

---

## 🚀 Как задеплоить (бесплатно, 2 минуты)

### Способ 1 — Vercel (рекомендуется)

```powershell
cd c:\Pyton\hh-applicant-tool\instogram\bio-link
npx vercel
```

При первом запуске:
1. Откроется браузер → войди через GitHub/Google
2. Vercel спросит настройки → жми Enter на всё (defaults)
3. Получишь ссылку вида `https://kazdev-biolink.vercel.app`

Повторный деплой после изменений:
```powershell
npx vercel --prod
```

### Способ 2 — Перетащить папку (ещё проще)

1. Зайди на [vercel.com](https://vercel.com) → Sign Up (бесплатно)
2. Нажми **"Add New → Project"**
3. Выбери **"Browse"** → укажи папку `bio-link`
4. Нажми **Deploy** → готово!

### Способ 3 — Netlify drag & drop

1. Зайди на [app.netlify.com/drop](https://app.netlify.com/drop)
2. **Перетащи папку** `bio-link` прямо на страницу
3. Получишь ссылку за 30 секунд — без регистрации!

---

## ✏️ Что и где менять в index.html

### 👤 Имя и описание профиля (строки ~851-853)

```html
<h1 class="name">Python-разработчик</h1>
<p class="title">🤖 AI-боты • ⚙️ Автоматизация • 💻 Full Stack</p>
<p class="tagline">Помогаю бизнесу в Казахстане...</p>
```

### 📊 Статистика (строки ~855-875)

```html
<div class="stat-value">50+</div>
<div class="stat-label">Проектов</div>
```

Меняй цифры под себя: проекты, часы, клиенты, рейтинг.

### 💰 Цены на услуги (строки ~885-940)

Цены указаны в тенге (₸). Найди и замени:
```html
<span class="service-price">от 60 000 ₸</span>
```

Текущие цены:
| Услуга | Цена |
|--------|------|
| Telegram-боты | от 60 000 ₸ |
| Instagram-автоматизация | от 90 000 ₸ |
| Бизнес-автоматизация | от 120 000 ₸ |
| Веб-разработка | от 180 000 ₸ |

### 📞 Кнопки связи (строки ~870-877)

```html
<a href="https://t.me/ВАШ_USERNAME" class="btn btn-primary">
<a href="https://wa.me/77XXXXXXXXX" class="btn btn-secondary">
```

Замени `ВАШ_USERNAME` на твой Telegram и номер WhatsApp.

### 🎨 Аватарка

Сейчас используется автогенерация через DiceBear API:
```html
<img src="https://api.dicebear.com/7.x/avataaars/svg?seed=developer&backgroundColor=b6e3f4">
```

Чтобы поставить своё фото:
```html
<img src="https://i.imgur.com/ТВОЯ_ССЫЛКА.jpg" alt="Фото">
```
Загрузи фото на [imgur.com](https://imgur.com) или используй прямую ссылку.

---

## 📋 Структура кейсов (Реальные кейсы)

Каждый кейс состоит из 4 блоков:

```html
<div class="case-card">
  <div class="case-icon">🏪</div>
  <div class="case-content">

    <!-- Заголовок -->
    <h3 class="case-title">Название кейса</h3>

    <!-- Вводная история (курсив) -->
    <p class="case-story">1-2 предложения о клиенте</p>

    <!-- БЫЛО — оранжевый блок -->
    <div class="case-step case-before">
      <span class="step-label">Было</span>
      Описание ситуации до...
    </div>

    <!-- СДЕЛАЛИ — голубой блок -->
    <div class="case-step case-did">
      <span class="step-label">Сделали</span>
      Что именно было реализовано...
    </div>

    <!-- СТАЛО — зелёный блок -->
    <div class="case-step case-after">
      <span class="step-label">Стало</span>
      Результат после...
    </div>

    <!-- Метрики -->
    <div class="case-result">
      <span class="result-tag">+40% продаж</span>
      <span class="result-tag">Окупилось за 2 недели</span>
    </div>

  </div>
</div>
```

Для **featured** кейса (выделенного) добавь класс и бейдж:
```html
<div class="case-card featured">
  <div class="case-badge">🔥 Хит</div>
  ...
</div>
```

---

## 💬 Отзывы клиентов

Найди блок `<!-- Reviews Section -->`. Каждый отзыв:

```html
<div class="review-card">
  <div class="review-header">
    <div class="reviewer-avatar" style="background: linear-gradient(135deg, #667eea, #764ba2)">А</div>
    <div>
      <div class="reviewer-name">Имя Фамилия</div>
      <div class="reviewer-info">Должность, Компания</div>
    </div>
  </div>
  <p class="review-text">"Текст отзыва"</p>
</div>
```

---

## 🔗 Кнопки соцсетей (Quick Links)

Найди блок с кнопками-ссылками после заголовка:

```html
<a href="https://github.com/ВАШ_GITHUB" class="social-link">
<a href="https://hh.ru/resume/ВАШ_ID" class="social-link">
```

---

## 🎨 Цветовая схема

Все цвета в переменных CSS в начале файла (`<style>`):

```css
:root {
    --primary: #00d4ff;      /* Голубой акцент */
    --secondary: #a855f7;    /* Фиолетовый */
    --accent: #10b981;       /* Зелёный (успех) */
    --bg-primary: #0a0a0f;   /* Фон страницы */
    --text-primary: #f8fafc; /* Основной текст */
    --text-secondary: #94a3b8; /* Серый текст */
}
```

Поменяй `--primary` и `--secondary` чтобы изменить всю цветовую схему.

---

## 📱 Вставка ссылки в Instagram

После деплоя получишь ссылку вида:
- Vercel: `https://kazdev-biolink.vercel.app`
- Netlify: `https://amazing-name-123.netlify.app`

**Как вставить в Instagram:**
1. Instagram → профиль → **Редактировать профиль**
2. Поле **"Website"** → вставить ссылку
3. Сохранить

В Bio напиши что-то вроде:
```
🤖 AI-боты | Автоматизация бизнеса
📦 Kaspi • Wildberries • Bitrix24
👇 Кейсы и цены:
```

---

## 🔄 Рабочий процесс (обновление страницы)

1. Открыть `index.html` в редакторе (VS Code / Windsurf)
2. Внести изменения
3. Посмотреть локально: двойной клик на файл → откроется в браузере
4. Задеплоить обновление:
   ```powershell
   cd c:\Pyton\hh-applicant-tool\instogram\bio-link
   npx vercel --prod
   ```
5. Изменения появятся на сайте через ~30 секунд

---

## ❓ FAQ

**Q: Как проверить страницу локально?**
```powershell
cd c:\Pyton\hh-applicant-tool\instogram\bio-link
start index.html
```

**Q: Форма отправки заявок не работает — куда идут данные?**
Сейчас форма работает на фронтенде (заглушка). Чтобы получать заявки:
- Подключи [Formspree.io](https://formspree.io) (бесплатно): `<form action="https://formspree.io/f/ВАШ_ID">`
- Или Telegram Bot через webhook

**Q: Как добавить Google Analytics?**
Вставь перед `</head>`:
```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
```

**Q: Можно ли использовать свой домен?**
Да, бесплатно на Vercel:
- Settings → Domains → Add Domain
- Пример: `dev.yourname.kz`

**Q: Страница не индексируется в Google?**
Это нормально для Bio Link — главная цель трафик из Instagram, не SEO.
Но если нужно, добавь в `<head>`:
```html
<meta name="robots" content="index, follow">
```
