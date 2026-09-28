# WhatsApp Business — профиль и автоответы

**Статус: linked device подключён 23.09.2026.** Профиль, быстрые ответы и метки-воронка
настроены через web.whatsapp.com в тот же день — ниже зафиксировано, что именно стоит
в системе, чтобы не расходиться с фактическим состоянием.

Источник фактов: `FACTS.md`. Правила набора — `build/whatsapp-v4.md`, раздел
«Жёсткие правила набора» (без верхних границ цены, без обещаний сроков сверх
подтверждённых, без слова «insured», Карлоу + 150 км, а не «вся Ирландия»).

---

## ✅ Сделано 23.09.2026 через web.whatsapp.com

### Профиль компании (Business tools → Профиль компании)

| Поле | Значение |
|---|---|
| Имя | Expert Fix Services |
| Описание | Plastering, painting, bathrooms, kitchens & general handyman work across Carlow and within 150km. Quotes in writing from a photo — no calls needed. |
| Категория | Строительная компания (уже стояла, ближайшая из списка WhatsApp) |
| Сайт | https://expertfixservices.com |
| Email | info@expertfixservices.com |
| Номер | +353 89 983 1680 (уже был верный) |
| Часы | Открыто в определённые часы, Пн–Вс 07:00–22:00 (было «Открыто круглосуточно» — исправлено) |
| Адрес | Не заполнен намеренно — автокомплит поля предлагает только точные улицы (пин по умолчанию стоял в Калифорнии), а точный адрес по правилам проекта не публикуется |

### Быстрые ответы (Settings → Быстрые ответы) — 9 штук, плюс дефолтный «спасибо»

| Ярлык | Текст |
|---|---|
| `price` | Happy to price that up — send a photo of the job and your area and I'll give you a real figure, not a guess. |
| `bathroom` | A full bathroom refit starts from €6,500, all-inclusive — materials, fittings and labour. Send photos of the room and I'll put a figure in writing. |
| `kitchen` | Fitting a kitchen you've already bought starts from €2,500, labour only. A full kitchen renovation starts from €10,000, all-inclusive. Which are you after? |
| `painting` | Interior painting starts from €250 a room. Facade (exterior) painting starts from €2,500, all-inclusive. How many rooms, or is it the outside? |
| `plastering` | Small plastering repairs start from €150. Send a photo and I'll give you a proper figure. |
| `handyman` | It's €50/hour with a 2-hour minimum. Send me the full list of jobs and I'll tell you honestly how many hours it is. |
| `areas` | We cover Carlow and up to 150km around it. Whereabouts are you? |
| `deposit` | We take a 30% deposit to book the date, the rest on the day the work finishes. The deposit isn't refundable if the job's cancelled after that. |
| `emergency` | We take emergency call-outs. Send your address and I'll get a start time back to you here. |

В чате набираются через `/` + ярлык (напр. `/bathroom`).

### Метки-воронка (Settings → Списки — в этой версии WhatsApp «Ярлыки» переименованы в «Списки»)

Новый → Ждёт фото → Замер назначен → Смета отправлена → Выиграли / Проиграли (6 списков, все пустые, готовы к использованию).

---

## Не сделано — требует телефона, не веба

Перепроверено 23.09.2026: искал «Приветственное сообщение» и «Сообщение об отсутствии»
во всех разделах web.whatsapp.com — «Инструменты для бизнеса», «Настройки» (включая
поиск по настройкам), «Списки». Нигде нет. В мобильном приложении WhatsApp Business
это есть (Настройки → Инструменты для бизнеса → Приветственное сообщение / Сообщение
об отсутствии) — значит два этих поля настраиваются только с телефона, где стоит
приложение (у Лёши). Готовые тексты — вставить как есть:

**Приветственное сообщение:**
```
Hi, thanks for messaging Expert Fix Services. Send a photo of the job, what needs doing, and your area, and we'll come back with a price in writing — usually within the hour (7am–10pm, every day).
```

**Сообщение вне часов работы (07:00–22:00):**
```
Thanks for your message — we're off the tools right now, back online at 7am. Send a photo and the details now and you'll have a price waiting for you when we're back.
```

- **Каталог услуг** (Business tools → Каталог): проверено 23.09.2026 — кнопка
  «Добавить в каталог» остаётся неактивной, даже когда название и цена заполнены;
  фото обязательно. Фото по трём приоритетным услугам (штукатурка, handyman, покраска)
  всё ещё не прислал Лёша (`outreach/lesha-whatsapp-setup.md`) — раньше этого не начать.
- Полный сценарий первой линии (что спрашивать, в каком порядке, когда называть
  вилку, когда передавать Лёше) — не автоответ, а инструкция для менеджера:
  `build/whatsapp-v4.md`, разделы 1–11 целиком.
