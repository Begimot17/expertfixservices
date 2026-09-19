# Установка аналитики — пошагово

Всё бесплатно. Займёт ~30 минут. Делать в этом порядке.

## 1. Google Analytics 4 (5 мин)

1. https://analytics.google.com → **Start measuring**.
2. Account name: `Expert Fix Services`. Галочки sharing — как есть.
3. Property name: `expertfixservices.com`, Reporting time zone: **(GMT+00:00) Dublin**, Currency: **Euro (€)**.
4. Industry: `Home & Garden`, Business size: `Small`.
5. Objectives: выбрать **Generate leads**.
6. Platform: **Web** → Website URL: `https://expertfixservices.com`, Stream name: `Main site`.
7. Скопировать **Measurement ID** вида `G-XXXXXXXXXX` → прислать мне.
8. В настройках потока: Enhanced measurement — **включено** (по умолчанию).

## 2. Google Tag Manager (5 мин)

Зачем GTM, а не просто GA4: через него ставятся клики по WhatsApp/телефону/email и Pixel — без правок сайта каждый раз.

1. https://tagmanager.google.com → **Create Account**.
2. Account: `Expert Fix Services`, Country: **Ireland**.
3. Container name: `expertfixservices.com`, Target platform: **Web**.
4. Скопировать **Container ID** вида `GTM-XXXXXXX` → прислать мне.
5. Код вставлять не нужно — я соберу единый сниппет.

## 3. Microsoft Clarity (5 мин)

Бесплатно, без лимитов. Показывает **записи сессий** и heatmap — увидим, где люди бросают форму.

1. https://clarity.microsoft.com → Sign in (Google-аккаунт подойдёт).
2. **New project**: Name `Expert Fix`, Website `https://expertfixservices.com`, Category `Services`.
3. Setup → **Install tracking code manually** → скопировать **Project ID** (строка вида `abcd1234ef`) → прислать мне.

## 4. Meta Pixel (10 мин)

Ставим **сейчас**, хотя рекламу не запускаем: пиксель начинает копить аудиторию посетителей уже сегодня. Через 2–3 месяца это будет готовая аудитория для ретаргетинга — накопление бесплатное, назад его не отмотать.

1. https://business.facebook.com → **Create account** (Business name: `Expert Fix Services`, ваш email).
2. Business Settings → **Data sources → Datasets → Add** → название `Expert Fix Web`.
3. Выбрать **Meta Pixel** / Web → Connect website manually.
4. Скопировать **Pixel ID** (15–16 цифр) → прислать мне.
5. Карту привязывать НЕ нужно — пиксель работает без рекламного аккаунта.

## 5. Google Search Console (3 мин)

1. https://search.google.com/search-console → Add property → **URL prefix** → `https://expertfixservices.com`.
2. Verification: выбрать **HTML tag** → скопировать `content="..."` значение → прислать мне (вставлю в сниппет).
   Либо, если Hostinger даёт DNS-доступ — способ **Domain** надёжнее.
3. После верификации: Sitemaps → добавить `sitemap.xml` (он уже существует).
4. **Важно:** URL Inspection → проверить `/` → «View crawled page» → убедиться, что Google видит контент, а не Cloudflare-челлендж.

## 6. Bing Webmaster Tools (2 мин, опционально)

https://www.bing.com/webmasters → импорт из Google Search Console одной кнопкой. Bing = ~5% трафика в Ирландии, но бесплатно.

## 7. Что прислать мне

```
GA4 Measurement ID:   G-
GTM Container ID:     GTM-
Clarity Project ID:
Meta Pixel ID:
GSC verification tag:
```

Плюс, если готовы: **read-доступ (Viewer)** в GA4 и Search Console на мой email — тогда я подключу read-only MCP и буду сам смотреть цифры и делать недельные отчёты.

## 8. Куда вставлять код (Hostinger Horizons)

1. Открыть проект в Horizons → **Settings** (шестерёнка) → раздел **Custom code** / **SEO & Analytics** → поле для `<head>`.
2. Вставить содержимое `tracking/head-snippet.html` (я пришлю с подставленными ID).
3. **Publish**.
4. Если поля custom code в вашем плане Horizons нет — альтернатива: попросить AI-чат Horizons вставить скрипты в `index.html` (`"Add this code to the <head> of index.html: ..."`). Второй вариант: подключить домен к Cloudflare и внедрить через **Cloudflare Zaraz** (бесплатно) — тогда сайт вообще не трогаем. Скажите, если понадобится этот путь.

## 9. Проверка (делаю я)

- Playwright: в сетевых запросах есть `googletagmanager.com/gtm.js`, `connect.facebook.net`, `clarity.ms`.
- GA4 → Admin → **DebugView**: виден `page_view`.
- Тестовая заявка + клик по WhatsApp → GA4 Realtime показывает `generate_lead` и `whatsapp_click`.
- Meta Events Manager → **Test Events**: `PageView` и `Lead`.
