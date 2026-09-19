> # 🛑 УСТАРЕЛО в части номера и гео (11.09.2026)
>
> Стратегия верна и остаётся в силе: звонков нет, всё в переписку.
> Недействительны конкретные строки:
>
> - номер `+353 87 491 9556` во всех `wa.me`-ссылках — **актуальный `+353 89 983 1680`**;
> - быстрый ответ `/insured` «Yes, we're fully insured» — **страховки нет**;
> - гео в примерах текстов — Дублин вместо Карлоу.
>
> **Актуальные шаблоны — `build/whatsapp-v4.md`.**
> Читать можно как историю решений. **Копировать в живой профиль, на сайт, в каталог
> или в переписку — нельзя.**

---

# WhatsApp-first: стратегия без звонков

## Ограничение

Владелец: говорить по телефону тяжело, особенно с незнакомыми (вживую и на рабочие темы — нормально). Значит **звонки как канал заявок мы не используем**. Всё ведём в:

1. **Сообщение в WhatsApp** — главный канал
2. **Заявка с формы на сайте** — второй канал
3. Живая встреча / замер на объекте — там разговор уже не проблема

Это не компромисс и не «слабое место». В Ирландии по home services переписка часто конвертит лучше звонка: человек может написать в 23:00, приложить фото проблемы, не «ловить момент». Многие конкуренты не отвечают на сообщения вообще — это и есть преимущество.

## Что меняется в плане

| Было | Стало |
|---|---|
| `tel:`-ссылка в шапке как P0-задача | **отменено**, вместо неё — крупная кнопка WhatsApp |
| Sticky-панель «Позвонить + WhatsApp» на мобиле | Sticky-кнопка **только WhatsApp** |
| Call extension в Google Ads (было «обязательно») | **не подключаем** |
| «Call or WhatsApp today» в объявлениях | «Message us on WhatsApp» |
| Кнопка «Call now» в постах Google-профиля | «Message» / «Learn more» |
| Meta: Lead Ads с формой | **Click-to-WhatsApp Ads** становятся главным форматом |
| Конверсия `phone_call` в GA4 | остаётся в коде, но не является целью |

## Сайт: как оформить WhatsApp правильно

**1. Предзаполненный текст сообщения.** Человеку психологически трудно написать первым в пустоту. Ссылка с готовым текстом снимает барьер и сразу даёт вам контекст:

```
https://wa.me/353874919556?text=Hi%2C%20I%27d%20like%20a%20quote%20for%20
```

Под каждую услугу — свой текст:

| Где кнопка | Ссылка |
|---|---|
| Шапка / общая | `https://wa.me/353874919556?text=Hi%2C%20I%27d%20like%20a%20free%20quote` |
| Bathrooms | `...?text=Hi%2C%20I%27d%20like%20a%20quote%20for%20a%20bathroom%20refit` |
| Kitchens | `...?text=Hi%2C%20I%27d%20like%20a%20quote%20for%20kitchen%20fitting` |
| Painting | `...?text=Hi%2C%20I%27d%20like%20a%20quote%20for%20painting` |
| Handyman | `...?text=Hi%2C%20I%20have%20a%20few%20small%20jobs%20that%20need%20doing` |

В аналитике это тоже плюс: по тексту сообщения сразу видно, с какой страницы человек пришёл.

**2. Sticky-кнопка на мобиле.** Зелёная, внизу справа, видна всегда. 70–80% трафика в этой тематике — мобильный.

**3. Формулировки на сайте.** Заменить «Call us» → тексты, которые прямо приглашают писать и снимают ожидание звонка:

```
Message us on WhatsApp — we usually reply within an hour
Send a photo of the job and we'll come back with a price
Prefer to write instead of call? Message us on WhatsApp
No phone tag. Send us a message and we'll take it from there
```

**4. «Пришлите фото» — сильный приём.** Для handyman/ремонта фото задачи ускоряет оценку и делает переписку естественной. Добавить в форму опциональную загрузку фото и текст «Send a photo of the problem for a faster quote».

**5. Форма: убрать обязательный email, оставить имя + WhatsApp-номер.** Плюс галочка «Contact me on WhatsApp» (по умолчанию включена) — так клиент сам соглашается на переписку, и это снимает ожидание звонка с обеих сторон.

## Google Business Profile: как убрать звонки

Профиль уже создан. Что настроить:

1. **Включить Messaging** (Messages в приложении Google Business Profile). Клиент пишет прямо из карт, приходит в приложение как чат. Ответ можно писать текстом — то, что нужно.
2. **Включить автоответ на сообщения** (Welcome message):
   ```
   Thanks for getting in touch with Expert Fix Services. Send us a few details or a photo
   of the job and we'll come back to you with a price, usually within the hour.
   ```
3. **Телефон.** Google требует либо телефон, либо сайт — можно оставить **только сайт**, и тогда кнопки «Позвонить» в профиле не будет. Но: номер повышает доверие и участвует в локальном ранжировании, а часть клиентов всё равно захочет позвонить. Мой совет: **номер оставить**, но приоритетом сделать Messaging, а в описание и в услуги добавить прямую строку «WhatsApp preferred». Если звонки всё равно будут напрягать — убираем номер, оставляем сайт; на ранжирование это влияет слабее, чем отзывы и фото.
4. **Посты в профиле** — кнопка «Learn more» на сайт, а не «Call now».
5. В описание профиля добавить строку:
   ```
   WhatsApp is the fastest way to reach us — message us a photo of the job for a quick price.
   ```

## Meta: Click-to-WhatsApp — теперь главный формат

Это прямое попадание в ваше ограничение: объявление открывает чат WhatsApp с предзаполненным текстом. Ни звонков, ни формы.

```
Objective:      Engagement → WhatsApp  (или Leads → WhatsApp)
Destination:    WhatsApp
Geo:            Dublin + 25 км
Age:            30–65
Placements:     Advantage+
Prefilled text: "Hi, I saw your ad — I'd like a quote for ..."
```

Плюсы для вас конкретно: лид приходит уже в переписке, отвечаете текстом когда удобно, история сохраняется, можно отправить фото прошлых работ прямо в чат. Обычно CTWA-лиды дешевле лидов через Instant Form, потому что человеку не надо заполнять поля.

Поэтому приоритет каналов при появлении бюджета меняется: **Meta CTWA идёт наравне с Google Search**, а не после него (было: Meta вторым номером).

## Google Ads: без звонков

- **Не подключаем** call extension и call-only кампании.
- Убрать «Call» из заголовков объявлений, заменить на «Message Us On WhatsApp», «Text Us For A Quote».
- Трафик ведём на гео-страницу, где главная кнопка — WhatsApp.
- В расширениях: sitelink «WhatsApp Us» → на страницу с крупной кнопкой (Google не разрешает `wa.me` как финальный URL — нужен переход через свою страницу).
- Конверсии: `generate_lead` + `whatsapp_click`. Оптимизация идёт по ним, и это корректно — это и есть ваши заявки.

## WhatsApp Business — настроить обязательно

Бесплатное приложение, ставится вместо обычного WhatsApp на тот же номер. Решает ровно вашу задачу — отвечать быстро и не формулировать каждый раз с нуля.

**1. Приветственное сообщение** (уходит автоматически на первое сообщение):
```
Hi, thanks for messaging Expert Fix Services.

To give you a price quickly, send us:
- what needs doing
- a photo or two if you can
- your area in Dublin

We'll come back to you with a price, usually within the hour.
```

**2. Сообщение в нерабочее время:**
```
Thanks for your message. We're finishing up for the day and will reply first thing
tomorrow morning. If it's urgent, send a photo and we'll look at it tonight.
```

**3. Быстрые ответы** (набираются через `/` — экономят силы и время):

| Команда | Текст |
|---|---|
| `/price` | Happy to give you a price. Could you send a photo of the job and your area? That way I can quote properly rather than guess. |
| `/visit` | For a job like this it's best I call out and look at it. I'm free [day] morning or [day] afternoon — which suits? |
| `/insured` | Yes, we're fully insured — happy to send the certificate over if you'd like to see it. |
| `/areas` | We cover Dublin and the surrounding areas — Dún Laoghaire, Swords, Malahide, Blackrock, Tallaght, Lucan and Bray. |
| `/when` | We could start on this within [3–5] working days. Would that work for you? |
| `/handyman` | Handyman work is booked in a 2-hour minimum slot at €[X]/hour. If you have a few jobs, group them into one visit — works out cheaper. |
| `/deposit` | We take a [X]% deposit to book the date and materials, the rest on completion. |
| `/photos` | Here are a few photos of similar jobs we've done recently. |
| `/thanks` | Thanks a million. I'll get that written up and sent over to you today. |

**4. Каталог (Catalogue)** — витрина услуг с фото и ценами «от» прямо в WhatsApp. Клиент листает сам, вам не надо ничего объяснять текстом.

**5. Метки (Labels)** — воронка прямо в приложении: `Новый` → `Ждёт фото` → `Замер назначен` → `Смета отправлена` → `Выиграли` / `Проиграли`. Раз в неделю по меткам видно, где заявки застревают.

**6. Ссылка и QR-код бизнеса** — из настроек, кидать в Instagram bio, в профиль карт, на визитки.

## Instagram

Аккаунт уже пополняется: https://www.instagram.com/expertfixservices/ — это готовый источник фото для профиля в картах, сайта и объявлений (ничего не надо снимать заново).

Что настроить:
- Перевести в **Professional / Business** аккаунт (если ещё нет) — даёт статистику и кнопку WhatsApp
- В профиле: кнопка **WhatsApp** (появляется после привязки номера в Business-аккаунте) + ссылка на сайт
- Bio: `Construction & handyman · Dublin · Message us on WhatsApp for a quote`
- В каждом посте — район («Bathroom refit in Rathmines») и призыв писать в WhatsApp
- Связать аккаунт с Facebook Page — нужно для запуска CTWA-объявлений

## Что говорим клиенту (позиционирование)

Не «мы не берём звонки», а формулировка, которая звучит как сервис:

> **We work by message, not phone tag.** Send us a photo of the job and we'll come back with a price — usually within the hour. No waiting on hold, no missed calls, everything in writing.

Это ещё и снимает реальную боль рынка: главная жалоба на ирландских тредсменов — «не берут трубку, не перезванивают». Вы отвечаете письменно и быстро — это выглядит лучше, чем звонок.
