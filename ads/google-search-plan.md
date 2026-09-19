> # 🛑 НЕ ЗАПУСКАТЬ. Файл построен на отменённых допущениях (07.09.2026)
>
> Ниже — рабочий план, но **каждая его посылка недействительна**. Копипаст из этого файла
> в живой аккаунт нарушит `FACTS.md` и повторит ровно те 197 заявлений, которые снимали
> с сайта в PR #3.
>
> **Что именно сломано:**
>
> | Что в файле | Почему нельзя |
> |---|---|
> | Гео — Дублин, радиус 20 км от центра | База — Карлоу (R93AD98). Кольцо работ — `build/gbp-v2.md`, блок 4 |
> | CPC и CPL по дублинской выдаче | Замер дублинский, к Карлоу отношения не имеет. Рынок на два порядка меньше |
> | «fully insured» | Страховки нет — `FACTS.md`, блок «Доверие» |
> | «20+ years at it» | Работа в Ирландии с 2025 года |
> | «One team» / «our team» | Исполнитель один |
> | «Free itemised quote within 24 hours» | SLA по времени ответа нигде не зафиксирован, обещать нельзя |
> | «This one took 10 working days» | Сроки в днях не подтверждены |
> | Отзывы, рейтинги, звёзды в креативах | Отзывов нет ни одного |
> | Цены ванной / кухни / фасада | Не выяснено, работа это или всё включено — `audit/bench-carlow.md`, блок 2 |
>
> **Что переиспользуется без правки:** структура кампаний, логика Click-to-WhatsApp,
> минусовые слова, порядок подключения форматов. Ломается только гео, цифры и тексты.
>
> Переписывать **после** ответа владельца по ценам (`outreach/lesha-prices.md`) — иначе
> объявления придётся переделывать дважды.

# Google Ads — готовая кампания (запускать при бюджете €150+/мес)

Всё ниже готово к копипасту. Пока не запускаем — см. `ads/budget-math.md`.

## Настройки кампании

```
Campaign name:      EF | Search | Dublin | Renovations
Goal:               Leads
Type:               Search
Networks:           Search only (Display network — ВЫКЛЮЧИТЬ, он сливает бюджет)
Locations:          Dublin, Ireland + radius 20 km around Dublin city centre
Location option:    "Presence: People in or regularly in your targeted locations"
                    (НЕ "Presence or interest" — иначе платите за людей из других стран)
Languages:          English
Bidding:            Manual CPC (max €4) первые 2 недели → Maximize Conversions после 15 конверсий
Budget:             €5–8/day
Ad rotation:        Optimise for best performing ads
Ad schedule:        Mon–Sat 07:00–20:00 (ночью заявок нет, а клики есть)
Devices:            все; mobile bid adjustment +20% (WhatsApp пишут с мобильных)
Conversions:        generate_lead, whatsapp_click (из GA4)
Extensions:         sitelinks, callouts, structured snippets
                    call extension — НЕ подключаем, звонки не наш канал (local/whatsapp-first.md)
```

---

## Ad group 1 — Bathrooms

**Keywords** (phrase `"..."` и exact `[...]` — broad НЕ использовать при малом бюджете):
```
"bathroom renovation dublin"
[bathroom renovation dublin]
"bathroom refit dublin"
"bathroom fitters dublin"
[bathroom fitters dublin]
"bathroom remodelling dublin"
"new bathroom installation dublin"
"wet room installation dublin"
"walk in shower installation dublin"
"bathroom tiling dublin"
"en suite installation dublin"
"bathroom renovation cost dublin"
"small bathroom renovation dublin"
```

**Headlines (макс. 30 символов каждая):**
```
Bathroom Renovation Dublin
Full Bathroom Refits
Dublin Bathroom Fitters
Free Quote In 24 Hours
20+ Years Experience
Fully Insured Team
Fixed Price, No Surprises
Refit Done In 8-12 Days
Tiling & Waterproofing
Walk-In Showers Fitted
Guaranteed Workmanship
One Team, One Contact
Book A Free Site Visit
Wet Rooms & En Suites
Trusted Dublin Builders
```

**Descriptions (макс. 90 символов):**
```
Complete bathroom refits across Dublin. Waterproofing, tiling and fixtures done right.
Free itemised quote within 24 hours. Fully insured, workmanship guaranteed in writing.
One team from strip-out to finish. Day-by-day schedule agreed before we start.
20+ years renovating Dublin bathrooms. Message us on WhatsApp - we reply within the hour.
```

**Final URL:** `https://expertfixservices.com/bathroom-renovation-dublin`
**Display path:** `/Bathrooms/Dublin`

---

## Ad group 2 — Kitchens

**Keywords:**
```
"kitchen fitters dublin"
[kitchen fitters dublin]
"kitchen fitting dublin"
"kitchen installation dublin"
"kitchen renovation dublin"
"kitchen refit dublin"
"ikea kitchen fitters dublin"
"howdens kitchen fitting dublin"
"kitchen worktop installation dublin"
"kitchen cabinet fitting dublin"
```

**Headlines:**
```
Kitchen Fitters Dublin
Kitchen Fitting From €2500
Any Supplier Fitted
IKEA Kitchens Fitted
Free Quote In 24 Hours
Worktops & Splashbacks
Fitted In 4-7 Days
Fully Insured Fitters
20+ Years Experience
Appliances Installed Too
Fixed Price Before We Start
Old Kitchen Removed Free
Dublin & Surrounding Areas
Guaranteed Workmanship
Book A Free Site Visit
```

**Descriptions:**
```
Kitchen fitting across Dublin. Bought anywhere - IKEA, Howdens, bespoke. We fit it right.
Cabinetry, worktops, tiling and appliances. Free itemised quote within 24 hours.
Fitting-only from €2,500 in 4-7 days, or a full renovation project managed end to end.
Fully insured Dublin team, 20+ years. Message us on WhatsApp to arrange a free site visit.
```

**Final URL:** `https://expertfixservices.com/kitchen-fitting-dublin`

---

## Ad group 3 — Painting (добавлять на месяц 2)

**Keywords:**
```
"painters dublin"
[painters dublin]
"painters and decorators dublin"
[painters and decorators dublin]
"house painters dublin"
"interior painting dublin"
"exterior painting dublin"
"house painting cost dublin"
"kitchen cabinet painting dublin"
"professional painters dublin"
```

**Headlines:**
```
Painters & Decorators Dublin
Interior & Exterior Painting
Rooms From €350
Proper Prep, Lasting Finish
Free Quote In 24 Hours
Fully Insured Painters
Low-VOC Premium Paints
Clean, Tidy, On Time
20+ Years Experience
Cabinet Respraying Too
Exterior Repaints Dublin
Guaranteed Workmanship
Furniture Moved & Covered
Colour Advice Included
Book A Free Quote Today
```

**Descriptions:**
```
Professional painters across Dublin. Filling, sanding and priming as standard, not optional.
Interior rooms from €350 including full prep and two coats of premium low-VOC paint.
Exterior repaints built for Irish weather - power wash, repair, breathable masonry paint.
Fully insured, 20+ years, free quote in 24 hours. Message us on WhatsApp today.
```

**Final URL:** `https://expertfixservices.com/painters-dublin`

---

## Ad group 4 — Handyman (только если бюджет €300+)

CPL низкий, но чек маленький — окупается слабее остальных (`ads/budget-math.md`). При малом бюджете handyman ведём через GBP бесплатно.

**Keywords:**
```
"handyman dublin"
[handyman dublin]
"handyman services dublin"
"local handyman dublin"
"odd job man dublin"
"handyman near me dublin"
```

**Headlines:**
```
Handyman Dublin
Repairs & Odd Jobs Done
2-Hour Minimum Booking
Fully Insured Handyman
Free Quote In 24 Hours
Start In 3-5 Days
One Visit, Many Jobs
Turn Up When We Say
20+ Years Experience
Flat-Pack, Shelves, Doors
Dublin & Nearby Areas
No Job Too Small
```

**Descriptions:**
```
Reliable handyman across Dublin. Repairs, fixtures, flat-pack, doors, shelves and more.
Booked in 2-hour slots so a small job never costs a big call-out fee. Free quote in 24h.
Group your jobs into one visit and save. Fully insured, price agreed before we start.
```

**Final URL:** `https://expertfixservices.com/handyman-dublin`

---

## Assets (общие для кампании)

**Sitelink extensions:**
```
Free Quote        | Detailed quote within 24 hours | /contact
Our Services      | Kitchens, bathrooms, painting  | /services
Recent Projects   | Real before-and-after photos   | /work
About Our Team    | Fully insured, 20+ years       | /about
```

**Callout extensions (макс. 25 символов):**
```
Fully Insured
20+ Years Experience
Free Quotes
Fixed Price Quotes
Work Guaranteed
Dublin Based
```

**Structured snippets** (Header: Services):
```
Bathrooms, Kitchens, Painting, Flooring, Carpentry, Plastering, Repairs, Extensions
```

**Call extension:** не подключаем — заявки идут в WhatsApp и форму, не в звонки.

**Вместо него** — sitelink `WhatsApp Us` → на гео-страницу, где WhatsApp вынесен главной кнопкой. Google не разрешает `wa.me` как финальный URL, поэтому переход только через свою страницу.

**Заголовки с призывом писать** (добавить в каждую группу, заменив варианты со словом Call):
```
Message Us On WhatsApp
Text Us For A Price
Send A Photo, Get A Price
Reply Within The Hour
No Phone Tag, Just Answers
```

---

## Negative keywords — подключить ДО запуска

Это самая важная часть при малом бюджете: без списка 30–40% денег уйдёт на «как сделать самому» и «вакансии».

```
# работа/вакансии
jobs
job
vacancy
vacancies
hiring
apprentice
apprenticeship
career
careers
salary
wages
"rates of pay"
cv
recruitment
employment
labourer wanted

# DIY / обучение
diy
"do it yourself"
how to
tutorial
youtube
video
course
courses
training
college
qualification
guide
tips

# бесплатное / дешёвое
free
cheap
cheapest
budget
grant
grants
"government scheme"
seai grant

# не наши услуги
plumber
electrician
electrical
roofer
roofing
gutter cleaning
chimney
locksmith
gardener
landscaping
"tree surgeon"
pest control
"window cleaning"
"solar panel"
"heat pump"
boiler
"septic tank"
driveway
paving
tarmac
scaffolding
"skip hire"
removals
"man with a van"
cleaning services
"end of tenancy"

# не то гео
belfast
cork
galway
limerick
waterford
kilkenny
sligo
"northern ireland"
uk
london
usa

# товары, не услуги
buy
shop
store
b&q
woodies
screwfix
"for sale"
supplier
suppliers
wholesale
tools
paint colours
"colour chart"
b2b

# инфо-запросы без намерения
salary
definition
meaning
"what is"
reviews of
complaints
"planning permission"
regulations
"building regs"
insurance claim
```

## Первые 30 дней — рутина

| Когда | Что |
|---|---|
| День 1 | проверить, что конверсии регистрируются (тестовая заявка) |
| День 3 | Search terms report → добавить негативы |
| Каждые 3 дня, недели 1–2 | Search terms → негативы; выключить ключи с 0 конверсий и 15+ кликами |
| День 14 | сравнить CPL по ad group, перераспределить бюджет |
| День 21 | отключить объявления с CTR ниже половины среднего по группе |
| День 30 | при 15+ конверсиях → Maximize Conversions; иначе остаёмся на Manual CPC |

## Чего НЕ делать

- Не включать **Display network** в Search-кампании (галочка стоит по умолчанию — снять).
- Не запускать **Performance Max** первой кампанией: он требует данных о конверсиях и на малом бюджете уходит в дешёвый мусорный трафик.
- Не использовать **broad match** до €500/мес.
- Не менять ставки чаще раза в 3 дня — статистика не успевает накопиться.
- Не гнать трафик на главную: под каждый ad group — своя гео-страница (`seo/geo-pages.md`), иначе конверсия падает вдвое.
- Не запускать до того, как аналитика подтверждённо считает конверсии.
