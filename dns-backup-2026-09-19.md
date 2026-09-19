# Резервная копия DNS-зоны expertfixservices.com

Снято 19.09.2026 из hPanel, до каких-либо изменений. Нужно на случай, если при
отключении домена от Hostinger AI Builder / Horizons хостинг-панель пересоздаст
зону DNS с нуля — тогда эти записи восстанавливаются вручную за несколько минут.

Nameservers на момент снятия: `ns1.dns-parking.com`, `ns2.dns-parking.com`

## Записи

| Тип | Имя | Приоритет | Значение | TTL |
|---|---|---|---|---|
| CNAME | hostingermail-c._domainkey | — | hostingermail-c.dkim.mail.hostinger.com | 300 |
| CNAME | hostingermail-b._domainkey | — | hostingermail-b.dkim.mail.hostinger.com | 300 |
| CNAME | hostingermail-a._domainkey | — | hostingermail-a.dkim.mail.hostinger.com | 300 |
| CNAME | www | — | www.expertfixservices.com.cdn.hstgr.net | 300 |
| CNAME | autodiscover | — | autodiscover.mail.hostinger.com | 300 |
| CNAME | autoconfig | — | autoconfig.mail.hostinger.com | 300 |
| TXT | _dmarc | — | "v=DMARC1; p=none" | 3600 |
| ALIAS | @ | — | expertfixservices.com.cdn.hstgr.net | 300 |
| TXT | @ | — | "v=spf1 include:_spf.mail.hostinger.com ~all" | 3600 |
| MX | @ | 10 | mx2.hostinger.com | 14400 |
| MX | @ | 5 | mx1.hostinger.com | 14400 |

## Что из этого — почта, что — сайт

- **Почта (не трогать, восстановить в первую очередь при потере):** три CNAME
  `hostingermail-*._domainkey` (DKIM), `autodiscover`, `autoconfig`, `TXT _dmarc`,
  `TXT @` (SPF), оба `MX @`.
- **Сайт (то, что мы меняем):** `ALIAS @` и `CNAME www` — сейчас указывают на
  Horizons (`*.cdn.hstgr.net`), после перевода должны указывать на наш хостинг.

## Как восстановить, если зона слетела

В hPanel → Домени → expertfixservices.com → DNS / Сервери імен → Управління
DNS-записями → добавить каждую запись из таблицы выше вручную, тип/имя/значение/
TTL — как в таблице. Приоритет указывается только у MX.
