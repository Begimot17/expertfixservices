> # 🛑 УСТАРЕЛО. Сайт переписан с нуля (11.09.2026)
>
> Правки отсюда внесены не в этот файл, а в новый сайт (`site/`). Сам файл остался
> в исходном виде и содержит то, что запрещено `FACTS.md`:
>
> - title/H1 с Dublin — база **Карлоу**;
> - «20+ years' experience, fully insured» — **старт 2025, страховки нет**;
> - FAQ «Are you insured? Yes…»;
> - `foundingDate` в JSON-LD и старый номер телефона.
>
> **Что реально стоит на сайте — `site/apps/web/index.html` и `site/apps/web/src/lib/site.js`.**
> Читать можно как историю решений. **Копировать в живой профиль, на сайт, в каталог
> или в переписку — нельзя.**

---

# On-page правки — готовые тексты

Как вносить в Hostinger Horizons: либо через SEO-поля страницы, либо промптом AI-чату Horizons (пример в конце файла).

Логика правок одна: сейчас на сайте нет слова **Dublin** ни в одном заголовке, поэтому по запросам «... Dublin» сайт не появится вообще. Добавляем город + конкретику услуг.

## Title и Meta Description по страницам

`/`
```
Title: Handyman & Renovations Dublin | Expert Fix Services
Meta:  Trusted handyman, renovation and painting services across Dublin. 20+ years'
       experience, fully insured, free quote within 24 hours. Message us on WhatsApp.
H1:    Handyman & Renovation Services in Dublin
```
(было: `Premium Construction & Handyman Services Ireland | Expert Fix` — без города и без запросов, которые люди реально вводят)

`/services`
```
Title: Our Services — Renovations, Painting, Handyman | Dublin
Meta:  Kitchens, bathrooms, painting, flooring, carpentry, plastering and general repairs
       across Dublin. Fully insured team, transparent pricing, free 24-hour quotes.
H1:    Construction & Handyman Services in Dublin
```

`/work`
```
Title: Our Recent Projects in Dublin | Expert Fix Services
Meta:  See completed kitchens, bathrooms, extensions and painting projects across Dublin
       and the Greater Dublin Area. Real before-and-after photos from our team.
H1:    Recent Projects Across Dublin
```

`/about`
```
Title: About Expert Fix Services — Dublin Builders & Handymen
Meta:  A small, fully insured Dublin team with 20+ years in construction and renovation.
       One point of contact, transparent quotes, guaranteed workmanship.
H1:    About Expert Fix Services
```

`/contact`
```
Title: Get a Free Quote in 24 Hours | Expert Fix Services Dublin
Meta:  Tell us about your project and get a detailed free quote within 24 hours.
       Call, WhatsApp or fill in the form. Serving Dublin and surrounding areas.
H1:    Get Your Free Quote
```

## Текстовые замены на сайте

| Где | Сейчас | Заменить на |
|---|---|---|
| Footer → Location | `Serving all of Ireland` | `Dublin & Greater Dublin Area` |
| Footer → описание | `...across Ireland` | `...across Dublin and the Greater Dublin Area` |
| Главная, подзаголовок H1 | `Trusted by homeowners across Ireland` | `Trusted by homeowners across Dublin for 20+ years` |
| Footer, нижняя строка | `Premium Construction Services Ireland` | `Handyman & Renovation Services — Dublin` |
| Шапка | WhatsApp мелкой ссылкой | сделать WhatsApp **главной кнопкой** с предзаполненным текстом (`local/whatsapp-first.md`) |
| Кнопки услуг | `Get Free Quote` → форма | добавить второй вариант `Message on WhatsApp` с текстом под конкретную услугу |

Плюс добавить в футер новый блок:
```
Areas we cover: Dublin 1–24, Rathmines, Ranelagh, Blackrock, Dún Laoghaire, Sandyford,
Stillorgan, Dundrum, Swords, Malahide, Clontarf, Drumcondra, Lucan, Tallaght, Bray, Maynooth.
```
Это и клиенту отвечает на вопрос «а вы к нам приедете?», и даёт Google локальные сигналы.

## JSON-LD — вставить в `<head>` (после аналитики)

Заполнить поля в квадратных скобках реальными данными.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "HomeAndConstructionBusiness",
  "@id": "https://expertfixservices.com/#business",
  "name": "Expert Fix Services",
  "description": "Premium construction, renovation and handyman services across Dublin and the Greater Dublin Area.",
  "url": "https://expertfixservices.com",
  "telephone": "+353874919556",
  "email": "info@expertfixservices.com",
  "foundingDate": "[YYYY]",
  "priceRange": "€€",
  "image": "https://expertfixservices.com/[путь-к-обложке.jpg]",
  "address": {
    "@type": "PostalAddress",
    "addressLocality": "Dublin",
    "addressRegion": "County Dublin",
    "addressCountry": "IE"
  },
  "areaServed": [
    { "@type": "City", "name": "Dublin" },
    { "@type": "City", "name": "Dún Laoghaire" },
    { "@type": "City", "name": "Swords" },
    { "@type": "City", "name": "Malahide" },
    { "@type": "City", "name": "Blackrock" },
    { "@type": "City", "name": "Tallaght" },
    { "@type": "City", "name": "Lucan" },
    { "@type": "City", "name": "Bray" }
  ],
  "openingHoursSpecification": [
    { "@type": "OpeningHoursSpecification",
      "dayOfWeek": ["Monday","Tuesday","Wednesday","Thursday","Friday"],
      "opens": "08:00", "closes": "18:00" },
    { "@type": "OpeningHoursSpecification",
      "dayOfWeek": "Saturday", "opens": "09:00", "closes": "15:00" }
  ],
  "sameAs": [
    "[ссылка на Google Business Profile]",
    "[ссылка на Facebook]",
    "[ссылка на Instagram]"
  ],
  "hasOfferCatalog": {
    "@type": "OfferCatalog",
    "name": "Services",
    "itemListElement": [
      { "@type": "Offer", "itemOffered": { "@type": "Service", "name": "Handyman & Repairs" } },
      { "@type": "Offer", "itemOffered": { "@type": "Service", "name": "Interior & Exterior Painting" } },
      { "@type": "Offer", "itemOffered": { "@type": "Service", "name": "Bathroom Renovation" } },
      { "@type": "Offer", "itemOffered": { "@type": "Service", "name": "Kitchen Fitting" } },
      { "@type": "Offer", "itemOffered": { "@type": "Service", "name": "Flooring Installation" } },
      { "@type": "Offer", "itemOffered": { "@type": "Service", "name": "Carpentry" } },
      { "@type": "Offer", "itemOffered": { "@type": "Service", "name": "Plastering & Skimming" } },
      { "@type": "Offer", "itemOffered": { "@type": "Service", "name": "Full Home Renovation" } }
    ]
  }
}
</script>
```

**Не добавлять** `aggregateRating` вручную — рейтинг без реальных отзывов Google расценивает как spam и может наложить ручную санкцию. Появится сам, когда будут отзывы в GBP.

## FAQ-блок на `/contact` (даёт rich snippet в выдаче)

Добавить видимый текстовый блок с этими вопросами (текст должен быть на странице, не только в разметке):

- **Do you charge for quotes?** No. All quotes are free and detailed, usually within 24 hours.
- **Which areas do you cover?** Dublin and the Greater Dublin Area, including Dún Laoghaire, Swords, Malahide, Blackrock, Tallaght, Lucan and Bray.
- **Are you insured?** Yes, we carry full public liability insurance — certificate available on request.
- **Do you take small jobs?** Yes. Handyman work is booked in a minimum 2-hour slot.
- **How quickly can you start?** Small jobs usually within 3–5 working days; larger renovations are scheduled after a site visit.
- **Do you provide a warranty?** Yes, our workmanship is guaranteed in writing.

Затем ту же информацию продублировать разметкой `FAQPage`.

## Технические проверки (после Search Console)

- [ ] URL Inspection на `/` → Google видит контент, а не Cloudflare-челлендж (**критично**, см. `audit/site-audit.md` п.12)
- [ ] Sitemap `sitemap.xml` отправлен и принят
- [ ] Все 7 URL проиндексированы (Pages → Indexed)
- [ ] PageSpeed Insights мобильный: LCP < 2.5 c (проверю сам)
- [ ] У каждой картинки заполнен `alt` с услугой и городом: `Bathroom refit in Rathmines, Dublin`
- [ ] Открыть `expertfixservices.com` без `https` и с `www` → редирект на канонический адрес

## Промпт для AI-чата Hostinger Horizons

Если правки удобнее внести через чат Horizons, скопируйте ему это:

```
Please make the following changes:

1. Update page titles and meta descriptions:
   - Home: title "Handyman & Renovations Dublin | Expert Fix Services"
   - Services: title "Our Services — Renovations, Painting, Handyman | Dublin"
   - Work: title "Our Recent Projects in Dublin | Expert Fix Services"
   - About: title "About Expert Fix Services — Dublin Builders & Handymen"
   - Contact: title "Get a Free Quote in 24 Hours | Expert Fix Services Dublin"

2. Change the home page H1 to "Handyman & Renovation Services in Dublin".

3. Replace every occurrence of "across Ireland" and "Serving all of Ireland" with
   "Dublin & Greater Dublin Area".

4. Make WhatsApp the primary contact button in the header. Do NOT add a tel: phone link
   anywhere — we deliberately route enquiries to WhatsApp and the form, not to calls.
   Header button: "Message on WhatsApp" linking to
   https://wa.me/353874919556?text=Hi%2C%20I%27d%20like%20a%20free%20quote

5. On mobile, add a sticky bottom bar with ONE full-width green WhatsApp button:
   "Message us on WhatsApp — reply within the hour".

6. In the footer, add a line: "Areas we cover: Dublin 1–24, Rathmines, Ranelagh,
   Blackrock, Dún Laoghaire, Sandyford, Stillorgan, Dundrum, Swords, Malahide,
   Clontarf, Drumcondra, Lucan, Tallaght, Bray, Maynooth."

7. In the quote form, make only "Full Name" and "Phone Number" required; make Email,
   Service Type and Message optional.
```
