> # 🛑 УСТАРЕЛО. Гео-страницы написаны не под тот город (11.09.2026)
>
> Четыре страницы (`/handyman-dublin`, `/painters-dublin`, `/bathroom-renovation-dublin`,
> `/kitchen-fitting-dublin`) не опубликованы и в нынешнем виде опубликованы быть не могут:
>
> - гео — Дублин, а база **Карлоу + 150 км**;
> - в текстах «fully insured» — **страховки нет**.
>
> **Заменено 12.09.2026.** Идея гео-страниц оказалась верной, и они переписаны под Карлоу:
> `site/apps/web/src/lib/geo.js` — четыре страницы (`/plastering-carlow`, `/handyman-carlow`,
> `/bathroom-renovation-kilkenny`, `/handyman-portlaoise`), города из кольца 1
> `build/gbp-v2.md` блок 4. Дублинских страниц нет и не будет: метка стоит в Карлоу, и
> текстом её не подвинуть. Актуальная версия — код, не этот файл.
> Читать можно как историю решений. **Копировать в живой профиль, на сайт, в каталог
> или в переписку — нельзя.**

---

# Гео-страницы под Дублин — готовый контент

## Зачем

Люди ищут не «premium services», а «handyman dublin», «bathroom fitters dublin», «painters dublin». Одна общая страница не может ранжироваться по всем; отдельная страница под связку **услуга + город** может. Это единственный бесплатный способ получать поисковый трафик без рекламы.

Создать 4 страницы (по объёму спроса):

1. `/handyman-dublin`
2. `/painters-dublin`
3. `/bathroom-renovation-dublin`
4. `/kitchen-fitting-dublin`

Правила, чтобы это работало:
- Каждая страница — **минимум 600 слов уникального текста**. Копии одного шаблона с заменой слова Google игнорирует (doorway pages).
- В каждой — свои фото реальных работ именно этого типа.
- Ссылки: с `/services` на каждую гео-страницу, и обратно.
- Добавить новые URL в `sitemap.xml`.

---

## 1. `/handyman-dublin`

```
Title: Handyman Dublin — Repairs, Fixtures & Odd Jobs | Expert Fix Services
Meta:  Reliable handyman in Dublin for repairs, fixture installation and odd jobs.
       Fully insured, minimum 2-hour booking, free quote within 24 hours.
H1:    Handyman Services in Dublin
```

**Intro (2 абзаца)**
> Looking for a handyman in Dublin who turns up on time and finishes the job properly? Expert Fix Services handles the repairs and small installations that most contractors won't take on — from a door that won't close to a full day of accumulated jobs around the house.
>
> We work across Dublin and the Greater Dublin Area, we're fully insured, and we quote before we start. Handyman work is booked in a minimum two-hour slot, and most jobs can be scheduled within three to five working days.

**H2: What our handyman service covers**
- Door and window adjustments, locks and handles
- Shelving, mirrors, TV brackets and picture hanging
- Flat-pack furniture assembly and built-in units
- Tap, shower head and bathroom fixture replacement
- Skirting, architrave and trim repairs
- Curtain rails, blinds and light fittings
- Silicone sealing in kitchens and bathrooms
- Small plastering and paint touch-ups
- Fence, gate and garden shed repairs
- Leak investigation and minor plumbing fixes
- Attic access, insulation top-ups and storage boards
- Snag-list work before or after a house sale

**H2: How pricing works**
> Handyman work is charged hourly with a two-hour minimum, so you're never paying a large call-out fee for a small job. If you have several jobs, group them into one visit — it works out far cheaper than separate call-outs. We confirm the rate and the estimated time before we start, and if a job turns out to be bigger than expected we tell you before continuing, not after.

**H2: Areas we cover in Dublin**
> Dublin 1 to Dublin 24, plus Rathmines, Ranelagh, Blackrock, Dún Laoghaire, Sandyford, Stillorgan, Dundrum, Swords, Malahide, Clontarf, Drumcondra, Lucan, Tallaght, Bray and Maynooth.

**H2: Why homeowners in Dublin call us back**
> Most complaints about tradespeople in Dublin aren't about skill — they're about people not showing up, not answering the phone, and prices changing halfway through. We built this business around the opposite: one point of contact, a quote in writing, and a time we actually keep. Over 20 years, that's what has kept our work coming from repeat customers and referrals.

**CTA:** `Get a free quote within 24 hours` → форма + WhatsApp + телефон

---

## 2. `/painters-dublin`

```
Title: Painters & Decorators Dublin — Interior & Exterior | Expert Fix Services
Meta:  Professional painters in Dublin. Interior and exterior painting with proper
       surface preparation and premium low-VOC paints. Free quote in 24 hours.
H1:    Painters & Decorators in Dublin
```

**Intro**
> A paint job lasts as long as the preparation behind it. Most repaints that fail within two years in Dublin's damp climate fail because someone skipped filling, sanding or priming to save half a day. We don't — and that's the whole difference between a room that still looks fresh in five years and one that needs redoing.

**H2: Interior painting**
- Full room repaints: walls, ceilings, woodwork
- Filling, sanding and priming as standard
- Wallpaper removal and wall repair
- Staircases, hallways and high ceilings
- Kitchen cabinet respraying
- Radiator, door and skirting finishing
- Premium low-VOC paints — safe to occupy the same day

**H2: Exterior painting**
- Render, pebbledash and masonry painting
- Window frames, fascia, soffits and gutters
- Front doors and railings
- Power washing and moss/algae treatment before painting
- Masonry crack repair and weatherproofing
- Breathable masonry paint suited to Irish weather

**H2: What a professional job includes**
> Furniture moved and covered, floors protected, edges taped, and the room left cleaner than we found it. We agree the exact colours and finishes before starting — and if you're not sure, we'll bring sample pots rather than guessing.

**H2: Typical pricing**
> Interior rooms start from around €350 including full preparation and two coats; exterior repaints depend on access and the condition of the render. Every quote is itemised so you can see what the preparation, materials and labour each cost.

**H2: Areas we cover** — [тот же список районов]

---

## 3. `/bathroom-renovation-dublin`

```
Title: Bathroom Renovation Dublin — Full Refits & Wet Rooms | Expert Fix
Meta:  Complete bathroom renovations in Dublin. Waterproofing, tiling, walk-in showers
       and fixture installation, project managed start to finish. Free quote.
H1:    Bathroom Renovations in Dublin
```

**Intro**
> A bathroom refit is the job where shortcuts cost the most. Poor waterproofing behind tiles doesn't show for a year, then shows up as damp in the room below. We do bathrooms as a fully managed project: strip-out, plumbing, waterproofing, tiling, fixtures and finishing — one team, one point of contact, one price agreed up front.

**H2: What's included in a full refit**
- Strip-out and disposal of the old bathroom
- Plumbing and electrical alterations (certified)
- Tanking and waterproofing to the wet areas
- Wall and floor tiling, including large-format tiles
- Walk-in showers and wet room installations
- Bath, basin, WC and vanity unit fitting
- Underfloor heating
- Extraction and ventilation to regulations
- Lighting, mirrors and finishing details

**H2: How long it takes**
> A standard Dublin bathroom takes 8–12 working days from strip-out to finished. We give you a day-by-day schedule before starting, so you know which days there's no water and when the tiler is in.

**H2: What it costs**
> Full refits typically start around €6 000 including labour and standard fittings, with the final figure driven by tile choice, whether the layout moves, and fixture spec. We itemise the quote so you can see exactly where money goes and adjust the spec rather than the quality of the work.

**H2: Common Dublin bathroom problems we fix**
> Older Dublin housing stock brings recurring issues: single-glazed windows causing condensation, no extraction fan, lead or old copper pipework, sloping floors in period houses, and shower trays installed without proper tanking. We check for all of these at the quote stage — it's cheaper to find them then than mid-project.

---

## 4. `/kitchen-fitting-dublin`

```
Title: Kitchen Fitting Dublin — Installation & Renovation | Expert Fix Services
Meta:  Kitchen fitting and renovation in Dublin. Cabinetry, worktops, tiling and
       appliance installation. Fully insured, free quote within 24 hours.
H1:    Kitchen Fitting & Renovation in Dublin
```

**Intro**
> Whether you've bought a kitchen and need it fitted properly, or want the whole room reworked, we handle it end to end: strip-out, first fix, cabinetry, worktops, tiling, appliances and finishing.

**H2: What we do**
- Fitting kitchens bought from any supplier (IKEA, Howdens, DIY-store, bespoke)
- Custom cabinetry and made-to-measure units
- Granite, quartz and laminate worktop installation
- Splashback tiling and glass panels
- Integrated appliance installation
- Plumbing for sinks, dishwashers and washing machines
- Extractor fans and ducting
- Under-cabinet lighting and sockets
- Flooring: tile, LVT or engineered wood
- Old kitchen removal and disposal

**H2: Fitting only vs full renovation**
> If your layout stays as is and you've already bought the units, fitting-only starts from around €2 500 and takes 4–7 days. A full renovation — moving plumbing, replacing flooring, new electrics, replastering — is quoted after a site visit, because layout changes are what actually drive the cost.

**H2: Areas we cover** — [тот же список районов]

---

## Внутренние ссылки

- `/services` → блок «Popular in Dublin» со ссылками на все 4 гео-страницы
- Каждая гео-страница → `/work` («see similar projects») и `/contact`
- Каждая гео-страница → 1–2 ссылки на другие гео-страницы («planning a kitchen at the same time?»)
- Футер: ссылки на все 4 страницы

## После публикации

- [ ] Добавить 4 URL в `sitemap.xml`
- [ ] Search Console → URL Inspection → **Request indexing** для каждой
- [ ] Проверить, что титулы не дублируются между страницами
- [ ] Через 3–4 недели: Search Console → Performance → какие запросы появились. По ним допишем контент.
