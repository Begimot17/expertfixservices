> # 🛑 УСТАРЕЛО И ОПАСНО. Не выполнять рекомендации (12.09.2026)
>
> Аудит от 17.08.2026 — он про **старый сайт**, который с тех пор переписан с нуля.
> Раздел «Быстрые победы» предписывает сделать ровно то, что `FACTS.md` запрещает:
>
> - заменить гео на «Dublin & Greater Dublin Area» — база **Карлоу**;
> - добавить `Dublin` в H1 и title;
> - п.10 — «добавить **номер полиса/страховщика**, VAT/CRO» — **ничего этого нет**.
>
> Плюс фактическая ошибка: «Нет Google Business Profile (не найден)». Профиль есть —
> «Carlow / Leinster Handyman Services», доступ менеджера получен 12.09.
>
> Технические наблюдения (robots, sitemap, отсутствие аналитики) верны **для старого
> сайта** и представляют только исторический интерес. Актуальное состояние нового
> сайта — в репозитории `site/`.
---

# Аудит expertfixservices.com

Дата: 2026-08-17. Метод: Playwright (рендер SPA), curl (robots/sitemap), анализ сетевых запросов.

## Что есть

- Платформа: Hostinger Horizons (React SPA), за Cloudflare.
- Страницы: `/`, `/services`, `/work`, `/about`, `/contact`, `/privacy-policy`, `/terms-of-services`.
- 9 услуг: Premium Renovations, Bespoke Kitchens, Luxury Bathrooms, High-End Painting, Premium Flooring, Custom Carpentry, Expert Plastering, Professional Handyman, General Maintenance.
- Контакты: WhatsApp `+353 87 491 9556`, email `info@expertfixservices.com`.
- CTA «Get Free Quote» → `/contact`, форма на главной (Name, Email, Phone, Service Type, Message).
- `robots.txt` и `sitemap.xml` есть и корректны (7 URL, sitemap объявлен в robots) — плюс платформы.
- Title'ы страниц уникальные и осмысленные.
- Дизайн приличный, доверие-блоки есть (Insured, 20+ Years, Guarantee, 24h response).

## Проблемы по приоритету

### P0 — теряем заявки прямо сейчас

1. **Нет аналитики вообще.** В сетевых запросах только Google Fonts: ни GA4, ни GTM, ни Meta Pixel, ни Clarity. Мы не знаем ни трафика, ни источников, ни числа заявок. Любая реклама до этого = деньги без обратной связи. → `tracking/gtm-ga4-setup.md`
2. **WhatsApp есть, но он не выделен как главный способ связи.** Ограничение владельца: разговоры по телефону даются тяжело, поэтому весь трафик сознательно ведём в **сообщения WhatsApp и заявки с формы**, а не в звонки (см. `local/whatsapp-first.md`). Значит WhatsApp должен быть самой заметной кнопкой на сайте, а не одной из трёх: sticky-кнопка на мобиле, кнопка в каждом блоке услуги, предзаполненный текст сообщения. Кликабельный `tel:` **не добавляем**.
3. **Нет города.** «Serving all of Ireland» / «Location: Serving all of Ireland». Google не понимает, где вы работаете; клиент не понимает, приедете ли вы к нему. Нужно: «Dublin & Greater Dublin Area» + список районов.
4. **Форма: 5 обязательных полей.** Каждое обязательное поле срезает конверсию. Оставить обязательными Name + Phone; Email и Service Type — опционально.

### P1 — рост трафика

5. **Ноль локальных сигналов.** Нет `LocalBusiness` JSON-LD, нет города в H1/title, нет страниц под гео+услугу. По запросам вида «handyman Dublin 8» сайт не появится. → `seo/onpage-fixes.md`, `seo/geo-pages.md`
6. **Нет Google Business Profile** (не найден в поиске). Это главный бесплатный источник заявок для местного сервиса — важнее сайта. → `local/gbp-setup.md`
7. **Портфолио без конкретики.** Нет «где, что, сколько заняло, сколько стоило». Кейс «Bathroom refit, Rathmines, 9 days, from €X» продаёт в разы лучше абстрактного фото.
8. **Нет цен вообще.** «Transparent Pricing» заявлено, но ни одной цифры. «От €X» по 5–6 типовым работам снимает главный барьер и отсекает нецелевые обращения.

### P2 — доверие и юридическое

9. **Отзывы не верифицируемы.** Declan/Sarah/Michael без фото, даты, ссылки. Заменить на настоящие Google-отзывы с ссылкой на профиль GBP (после сбора).
10. **«20+ years», «Fully Insured» без подтверждений.** Добавить: год основания, номер полиса/страховщика, RGI/CIRI/SEAI-регистрации если есть, VAT/CRO номер. Для Google Ads в тематике home services это ещё и снижает риск отклонения объявлений.
11. **GDPR.** Ирландия: перед GA4/Pixel нужен consent-баннер (Consent Mode v2) и упоминание cookies/аналитики в Privacy Policy. → `tracking/consent-banner.html`
12. **Cloudflare отдал 403 «Checking your browser»** на первый заход headless-браузера. Для верифицированного Googlebot обычно ок, но после настройки Search Console **обязательно проверить** «Проверка URL» → страница отрендерена. Если Google видит челлендж — сайт не индексируется.
13. **Нет NAP-консистентности** (Name/Address/Phone одинаково везде) — понадобится для каталогов, см. `local/directories.md`.

## Быстрые победы (сделать первыми, суммарно ~1 час)

1. Вставить код аналитики (`tracking/head-snippet.html`).
2. Sticky-кнопка WhatsApp на мобиле + предзаполненный текст сообщения (`local/whatsapp-first.md`).
3. Заменить «Serving all of Ireland» → «Dublin & Greater Dublin Area» + районы.
4. Title/H1 главной: добавить `Dublin`.
5. Обязательными в форме оставить только Name + Phone.
6. Создать Google Business Profile.
