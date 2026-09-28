# Google Ads — поисковая кампания под Карлоу

Написано 28.09.2026 взамен `ads/google-search-plan.md`, который построен на Дублине и
отменённых фактах. Отсюда можно копировать в аккаунт как есть: каждая строка сверена с
`FACTS.md`, длины заголовков и описаний проверены скриптом (внизу файла).

**Не запускать, пока не выполнены условия `PLAN.md`, часть 6.** На 28.09 не хватает
одного-двух отзывов в профиле Карт и отмеченных ключевых событий в GA4.

## Куда

Аккаунт `229-754-1152` — тот, что уже привязан к профилю Карт. Там на паузе две старые
кампании (`PLAN.md`, часть 7) и €30 предоплаты. Старые не включать и не править:
новую завести рядом, старые удалить после первого месяца, когда история уже не нужна.

## Настройки кампании

```
Campaign name:      EF | Search | Carlow | Plastering+Handyman
Goal:               Leads
Type:               Search
Networks:           Search only — снять «Display Network» и «Search partners»
Locations:          Carlow town + radius 30 km
Location option:    Presence: people in or regularly in your targeted locations
Languages:          English
Budget:             €5/day (≈ €150/мес)
Bidding:            Maximise clicks, max CPC €2.00 — первые 2 недели
                    → Maximise conversions, когда наберётся 15 конверсий
Ad schedule:        Mon–Sun 07:00–22:00 — ровно часы ответа (FACTS); ночной клик
                    получит ответ утром, и за него не надо платить
Devices:            все
Conversions:        импорт из GA4: whatsapp_click, generate_lead — обе «основные»
Call asset:         НЕ подключать — звонков нет (FACTS, «Связь»)
```

**Почему 30 км, а не 150.** Штукатурный ремонт от €150 — это два часа работы; поездка
дальше 30–40 км его не окупает (`build/gbp-v2.md`, §4.2). Реклама на мелкие работы должна
ловить мелкие работы рядом. Ванные и кухни — отдельная кампания и только после первых
отзывов: там клиент сравнивает трёх подрядчиков и без отзывов не выбирает никого.

**Почему только две группы.** €150 в месяц при €1.5–2.5 за клик — это 60–100 кликов.
Чтобы понять, работает ли группа, нужно 30+ кликов в ней. Две группы — предел.

---

## Группа 1 — Plastering → `/plastering-carlow`

Приоритет №1 в FACTS. Посадочная — своя гео-страница, не главная.

**Keywords** (phrase и exact; broad не использовать):
```
"plasterer carlow"
[plasterer carlow]
"plastering carlow"
[plastering carlow]
"plaster repair carlow"
"plasterer near me"
"skimming walls carlow"
"ceiling repair carlow"
"crack in wall repair"
```

**Заголовки (≤30 символов):**
```
Plasterer In Carlow
Plaster Repairs From €150
Send A Photo, Get A Price
Written Price Before Work
Walls And Ceilings Skimmed
Cracks, Holes, Leak Patches
Reply Within The Hour
Open 7am–10pm, Every Day
6-Month Guarantee On Work
Message Us On WhatsApp
Prices Published Online
Emergency Jobs Taken
```

**Описания (≤90 символов):**
```
Send 1–2 photos on WhatsApp and get a written price back, usually within the hour.
Plaster repairs from €150. Patches after a leak, cracks, holes, full skim finishes.
Every price is agreed in writing before anything is booked. 6-month guarantee.
Carlow and nearby. Open 7am to 10pm, seven days, emergency jobs taken.
```

---

## Группа 2 — Handyman → `/handyman-carlow`

Приоритет №2. Самые дешёвые клики, самая короткая сделка.

**Keywords:**
```
"handyman carlow"
[handyman carlow]
"handyman near me"
"odd jobs carlow"
"tv wall mounting carlow"
"shelves fitted carlow"
"flat pack assembly carlow"
"small repairs carlow"
```

**Заголовки:**
```
Handyman In Carlow
€50/Hour, 2-Hour Minimum
Shelves, Doors, TV Brackets
Small Jobs Welcome
Group Jobs Into One Visit
Send A Photo, Get A Price
Written Price Before Work
Reply Within The Hour
Open 7am–10pm, Every Day
Message Us On WhatsApp
Emergency Jobs Taken
6-Month Guarantee On Work
```

**Описания:**
```
€50 an hour, two-hour minimum. Send the whole list and we tell you how many hours.
Shelves, curtain rails, TV brackets, doors, sealant, flat-pack and the small jobs.
Send photos on WhatsApp and get a written price back, usually within the hour.
Carlow and nearby. Open 7am to 10pm, seven days, emergency jobs taken.
```

---

## Группа 3 — Painting → `/prices` (месяц 2, не раньше)

Только если группы 1–2 дают заявки дешевле €60. Ключи: `"painter carlow"`,
`[painter carlow]`, `"painter decorator carlow"`, `"room painting carlow"`.
Заголовки — `Painter In Carlow`, `Room Painted From €250`, остальное из группы 1.

---

## Ассеты кампании

**Sitelinks:**
```
Prices         | Nine jobs, nine prices    | /prices
Recent Work    | Before and after photos   | /work
Plastering     | Repairs from €150         | /plastering-carlow
Handyman       | €50/hour, 2-hour minimum  | /handyman-carlow
```

**Callouts (≤25):**
```
Written Price First
6-Month Guarantee
Reply Within The Hour
Open 7 Days
Emergency Jobs Taken
Prices Published Online
```

**Structured snippet** — Services:
```
Plastering, Painting, Repairs, Carpentry, Flooring, Kitchen Fitting, Bathrooms
```

WhatsApp как финальный URL Google не пускает, поэтому все объявления ведут на свои
страницы — там WhatsApp главной кнопкой, и клик по ней засчитывается как конверсия.

## Чего в текстах нет и не будет

По `FACTS.md`, «Прямые запреты»: insured, «registered», годы опыта, «our team», отзывы и
звёзды, «certified electrician», «Free Quote within 24 hours», сроки работ в днях. Плитки
отдельной услугой и «for businesses» тоже нет — это было в старой кампании Search-1 и
не соответствует прайсу.

## Минус-слова

Из `ads/google-search-plan.md`, блоки «работа/вакансии», «DIY», «бесплатное», «не наши
услуги», «товары», «инфо-запросы» — без изменений. Блок «не то гео» заменить на:
```
dublin
belfast
cork
galway
limerick
sligo
"northern ireland"
uk
london
```
Kilkenny и Waterford из старого списка убраны: Kilkenny в радиусе, Waterford — кольцо 2.
Плюс свои: `gas`, `boiler`, `electrician`, `rewire`, `plumber` — этого не берём (FACTS).

## Первые 30 дней

| Когда | Что |
|---|---|
| День 0 | Тестовая заявка с телефона: клик по WhatsApp виден в GA4 и в Ads (до 24 ч) |
| День 3 | Отчёт по поисковым запросам → минус-слова |
| Каждые 3 дня | То же; выключить ключи с 15+ кликами и 0 конверсий |
| День 14 | Сравнить цену заявки по группам, бюджет — в лучшую |
| День 30 | 15+ конверсий → Maximise conversions; иначе остаёмся на кликах |

Считать не только клики в WhatsApp, но и чем они кончились: метки в WhatsApp
(Новый → … → Выиграли/Проиграли). Без этого через месяц будет цена клика, но не цена заказа.

## Проверка длин

Проверено скриптом 28.09.2026 по блокам этого файла: все заголовки ≤30 символов,
описания ≤90, callouts ≤25, тексты sitelinks ≤25. После любой правки текстов —
перепроверить: Google режет молча, и объявление уходит на модерацию обрезанным.
