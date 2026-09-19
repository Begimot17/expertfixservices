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

# WhatsApp: шаблоны и сценарий первой линии

Это рабочий инструмент менеджера. Всё готово к вставке в WhatsApp Business сразу после подключения linked device.

Цены помечены `€[X]` там, где ждём подтверждения Лёши (`pricing/price-draft.md`).

---

## 1. Автоприветствие (Greeting message)

Уходит автоматически на первое сообщение от нового контакта.

```
Hi, thanks for messaging Expert Fix Services.

To give you a price quickly, send us:
• what needs doing
• a photo or two if you can
• your area in Dublin

We'll come back to you with a price, usually within the hour.
```

## 2. Сообщение в нерабочее время (Away message)

Часы: вне Mon–Fri 08:00–18:00, Sat 09:00–15:00.

```
Thanks for your message — we're off the tools for the day and will reply first thing
tomorrow morning.

If you send a photo of the job now, we'll have a price ready for you when we're back.
```

## 3. Быстрые ответы (Quick replies)

Набираются через `/`.

| Команда | Текст |
|---|---|
`/price` | Happy to price that up. Could you send a photo of the job and let me know your area? That way I can give you a real figure rather than a guess.
`/visit` | For a job like this it's best we call out and see it — takes 20 minutes and the quote is free. I have [day] morning or [day] afternoon free, which suits you better?
`/insured` | Yes, we're fully insured with public liability cover. Happy to send the certificate over if you'd like to see it.
`/areas` | We cover Dublin and the surrounding areas — Dún Laoghaire, Swords, Malahide, Blackrock, Tallaght, Lucan, Bray and Maynooth. Whereabouts are you?
`/when` | We could get started on this within [3–5] working days. Would that suit you?
`/handyman` | Handyman work is booked in a 2-hour minimum slot at €[X] per hour. If you've a few jobs around the house, group them into one visit — works out a lot cheaper than separate call-outs.
`/bathroom` | A full bathroom refit starts from €[6,000] and takes 8–12 working days — that's strip-out, plumbing, waterproofing, tiling and fittings. Final figure depends on tile choice and whether the layout moves. Send a photo of the room and I'll give you a proper range.
`/kitchen` | Fitting a kitchen you've already bought starts from €[2,500] and takes 4–7 days. A full kitchen renovation is quoted after a site visit. Which are you looking at?
`/painting` | Interior rooms start from €[350] including full prep and two coats. Exterior repaints start from €[1,800]. How many rooms are we talking about?
`/deposit` | We take a [X]% deposit to book the date and order materials, and the balance on completion.
`/photos` | Here are a few photos of similar jobs we've done recently 👇
`/thanks` | Thanks a million. I'll get that written up and back to you today.
`/nope` | Sorry, that's not something we take on — we'd rather tell you straight than do a poor job of it. If you need [X] though, that's right up our street.

---

## 4. Сценарий первой линии

Цель: за 3–4 сообщения получить услугу, район, фото и срок — и передать Лёше готовую заявку.

**Шаг 1 · Ответить в течение 15 минут в рабочее время.** Скорость важнее формулировки: по home services первый ответивший забирает большинство заявок.

**Шаг 2 · Квалификация.** Нужны четыре вещи, спрашивать по две за раз, не анкетой:

```
Hi [Name], thanks for getting in touch.

Two quick things so I can price it properly:
1. What's the job — and roughly what size / how many rooms?
2. What area of Dublin are you in?

A photo or two helps a lot if you have them.
```

**Шаг 3 · Назвать вилку.** Никогда не молчать про деньги — это главная причина, по которой люди уходят.

```
Thanks. For a job like that we'd usually be looking at €[X] to €[Y], depending on
[конкретный фактор: tile choice / condition of the walls / access].

Happy to come out and give you an exact figure — the visit and the quote are free.
```

**Шаг 4 · Закрыть на замер или дату.** Всегда предлагать **два конкретных окна**, а не «когда вам удобно»:

```
I have Thursday morning or Saturday afternoon free this week — which suits you better?
```

**Шаг 5 · Передать Лёше.** Одним сообщением, всегда в одном формате:

```
ЗАЯВКА
Услуга: bathroom refit
Район: Rathmines, D6
Объём: полная переделка, 4 м²
Фото: есть (3)
Назвал вилку: €6-8k
Хочет: замер в четверг утром
Контакт: [имя, номер]
```

**Шаг 6 · Поставить метку** в воронке: `Новый` → `Ждёт фото` → `Замер назначен` → `Смета отправлена` → `Выиграли` / `Проиграли`.

**Шаг 7 · Догнать молчащих.** Через 48 часов без ответа — одно короткое сообщение, больше не писать:

```
Hi [Name], just checking you got my message — still happy to price that up whenever
you're ready. No rush.
```

---

## 5. Границы: что решаю сам, что через Лёшу

| Решаю сам | Только через Лёшу |
|---|---|
| Назвать вилку по прайсу | Любая скидка |
| Предложить дату из свободных окон | Точная смета по объекту |
| Ответить про страховку, зоны, сроки | Работа не из прайса |
| Отказать по услугам из списка «не берём» | Сложные сроки под конкретный объект |
| Попросить фото, уточнить объём | Обещание «сделаем за N дней» по крупному проекту |
| Догнать молчащего клиента | Аварийный выезд сегодня |

**Правило при сомнении:** «Уточню у мастера и вернусь к вам в течение часа» — и правда вернуться в течение часа.

---

## 6. Каталог услуг в WhatsApp Business

9 позиций, каждая = фото + название + цена «от» + 1 строка описания. Фото берём из Instagram (`assets/photo-inventory.md`).

| Позиция | Фото есть? |
|---|---|
| Bathroom Refit — from €[6,000] | ✅ есть |
| Kitchen Fitting — from €[2,500] | ✅ есть |
| Flooring — from €[25]/m² | ✅ есть |
| Carpentry & Built-ins — from €[600] | ✅ лестница |
| Interior Painting — from €[350]/room | ❌ ждём |
| Exterior Painting — from €[1,800] | ❌ ждём |
| Plastering — from €[18]/m² | ❌ ждём |
| Handyman — €[X]/hour, 2h min | ❌ ждём |
| Full Renovation — free quote | ✅ есть |

---

## 7. Чего не делать в переписке

- Не отвечать «зависит от многого» без цифры — это ответ, после которого уходят
- Не писать простыни: 2–4 строки на сообщение
- Не задавать больше двух вопросов за раз
- Не обещать сроки, не сверившись с загрузкой Лёши
- Не оставлять последнее сообщение за клиентом: всегда заканчивать вопросом или предложением даты
- Не переходить на звонок, даже если клиент предлагает — «I'm on site, message is easier, I'll get you a price faster this way»
