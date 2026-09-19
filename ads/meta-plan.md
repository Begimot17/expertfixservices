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

# Meta (Facebook/Instagram) — план

**Изменение приоритета:** изначально Meta шла вторым каналом после Google. Из-за ограничения по звонкам (`local/whatsapp-first.md`) Meta поднимается наравне с Google Search, потому что у неё есть формат **Click-to-WhatsApp** — объявление открывает переписку напрямую, без формы и без звонка. Это ровно то, что нужно.

Плюс: Instagram уже наполняется (instagram.com/expertfixservices) — креативы для объявлений фактически готовы, снимать заново ничего не надо.

Порядок подключения: **Click-to-WhatsApp** → **ретаргетинг** (аудитория копится Pixel'ом бесплатно с сегодня) → холодные Lead Ads с формой, если понадобится.

## Кампания 0 — Click-to-WhatsApp (главный формат)

```
Objective:      Engagement → WhatsApp (или Leads → WhatsApp)
Destination:    WhatsApp
Geo:            Dublin + 25 км
Age:            30–65
Placements:     Advantage+ (Reels и Stories работают хорошо на до/после)
Budget:         €5–10/day
Prefilled text: "Hi, I saw your ad — I'd like a quote for "
```

Почему это лучше Instant Form в вашем случае: лид приходит сразу в переписку, отвечаете текстом когда удобно, можно тут же отправить фото похожих работ, история сохраняется. И CTWA-лиды обычно дешевле, потому что человеку не надо заполнять поля.

Обязательное условие: настроенный **WhatsApp Business** с автоприветствием и быстрыми ответами (`local/whatsapp-first.md`), иначе поток сообщений станет нагрузкой вместо помощи.

## Что делаем прямо сейчас, бесплатно

1. **Pixel уже стоит** (см. `tracking/head-snippet.html`) — начинает копить аудиторию посетителей сайта. Это единственная невосполнимая вещь: аудиторию нельзя «досоздать» задним числом.
2. **Facebook Page + Instagram Business** — создать, заполнить, публиковать 2–3 поста в неделю (фото до/после). Органика для ремонта работает: локальные группы Дублина активно шарят такие посты.
3. **Custom Audiences** создать сразу, они наполняются сами:
   - `Website — all visitors 180 days`
   - `Website — /contact visitors 180 days` (самая горячая)
   - `Instagram/Facebook engagers 365 days`

## Кампания 1 — Ретаргетинг (первая при появлении бюджета)

Дешёвая и самая эффективная: человек уже был на сайте.

```
Objective:      Leads (или Traffic, если лидов мало для оптимизации)
Audience:       Website visitors 180 days + page engagers 365 days
Exclude:        те, кто отправил заявку (Lead event 90 days)
Placements:     Advantage+ placements (авто)
Geo:            Dublin + 25 km
Age:            30–65+
Budget:         €3–5/day
Optimisation:   Leads (если <50/нед — на Landing Page Views)
```

Запускать, когда в аудитории накопилось **минимум 300–500 человек** — иначе показывать некому.

## Кампания 2 — Холодный трафик, Lead Ads

Форма заполняется внутри Facebook — конверсия выше, чем при переходе на сайт, но лиды холоднее (человек мог нажать не думая). Обязательно добавить квалифицирующий вопрос.

```
Objective:      Leads → Instant Form
Geo:            Dublin + 25 km (исключить центр, если там мало частного жилья)
Age:            30–65
Detailed targeting:
  - Behaviours: Homeowners / Likely to move
  - Interests: Home improvement, Home renovation, Interior design, DIY
Placements:     Advantage+
Budget:         €5–10/day
```

**Instant Form — поля:**
1. Full name
2. Phone number
3. **What do you need? (multiple choice)** — Bathroom refit / Kitchen fitting / Painting / Renovation / Small repairs
4. **When do you want the work done? (multiple choice)** — Within 1 month / 1–3 months / Just researching
   ← это поле фильтрует «просто смотрю» и экономит вам часы звонков
5. Postcode / area

Screening: включить **Higher intent** (лишний шаг подтверждения) — лидов меньше, качество выше.

## Креативы

Что работает в этой тематике, по убыванию:

1. **До/после, одна фотография с разделением** — самый сильный формат
2. **Видео 15–30 с**: панорама «до» → таймлапс работы → панорама «после», без музыки, с подписями
3. **Карусель 5 фото** одного проекта: до → процесс → детали → после
4. Отзыв клиента на фоне готовой работы

Требования: снимать вертикально (4:5 и 9:16), дневной свет, **никакого стока** — стоковые кухни в этой нише убивают доверие мгновенно, люди хотят видеть реальные ирландские дома.

## Тексты объявлений

**Вариант A — до/после, bathroom**
```
Primary text:
That bathroom you've been putting off? This one took 10 working days, start to finish —
strip-out, waterproofing, tiling, the lot. One team, one price agreed before we started.

We're a fully insured Dublin team, 20+ years at it. Free itemised quote within 24 hours,
and we tell you what it costs before anything is torn out.

Headline: Bathroom Refits Across Dublin
Description: Free quote in 24 hours. Fully insured.
CTA: Get quote
```

**Вариант B — handyman, боль «никто не приходит»**
```
Primary text:
Waiting three weeks for someone to return a call about a job that takes two hours?

We do the small stuff: doors that won't close, shelves, taps, flat-pack, the silicone
in the bathroom that's gone black. Booked in 2-hour slots, price agreed up front,
and we turn up on the day we said.

Dublin and surrounding areas. Fully insured.

Headline: Dublin Handyman — Small Jobs Done
Description: 2-hour minimum. Insured. On time.
CTA: Send WhatsApp message
```

**Вариант C — painting, сезонный (весна/лето для exterior)**
```
Primary text:
Most exterior paint jobs in Dublin fail in two years because someone skipped the prep.

We power wash, treat the moss, repair the cracks, then use breathable masonry paint
built for Irish weather. It's a day longer and it lasts years more.

Free quote within 24 hours. Fully insured, 20+ years.

Headline: Exterior Painting Dublin
Description: Proper prep. Lasting finish.
CTA: Get quote
```

**Вариант D — ретаргетинг (для тех, кто был на сайте)**
```
Primary text:
Still thinking about that project? Happy to just give you a number to work with —
no pressure, no obligation.

Free itemised quote within 24 hours. Fully insured Dublin team, 20+ years.

Headline: Your Free Quote Is Waiting
CTA: Get quote
```

## Правила ведения

- Минимум **3 креатива** на ad set — Meta сама найдёт рабочий.
- **Не трогать** кампанию первые 4–5 дней (learning phase); правки перезапускают обучение.
- Обновлять креативы каждые 3–4 недели: в узком гео аудитория выгорает быстро.
- Отвечать на лид в **первые 5 минут** — по home services конверсия падает в разы после первого часа. Настроить уведомления Meta на телефон.
- Instant Form лиды выгружать в CRM/таблицу сразу, они не приходят на email автоматически.

## Чего избегать

- Не запускать холодные lead ads раньше ретаргетинга — дороже и хуже качеством.
- Не выбирать objective «Engagement»/«Awareness» — соберёте лайки, не заявки.
- Не ставить бюджет ниже €3/день на ad set — алгоритм не обучится.
- Не использовать один креатив на все аудитории.
- Не обещать в объявлении цену, которую не держите — Meta банит за несоответствие лендингу, и клиент приходит злым.
