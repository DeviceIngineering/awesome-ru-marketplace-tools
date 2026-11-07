# Awesome Russian Marketplace Tools [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Открытые инструменты для продавцов на Ozon, Wildberries и Яндекс.Маркете: клиенты API, MCP-серверы, репрайсеры, аналитика.

Слой «достучаться до API» сообществом закрыт хорошо — по Ozon и Wildberries в сумме больше трёхсот репозиториев. Слой «принять решение» почти пуст: во всём GitHub семь репозиториев с тегом `repricer`. Этот список — попытка собрать в одном месте то, что действительно работает, и честно показать, где ничего нет.

**Что попадает в список:** открытый исходный код, публичный репозиторий, понятно, что оно делает. Коммерческие сервисы вынесены в отдельный раздел без оценок — как ориентир по рынку, не как рекомендация.

**Отметки:** ⭐ — звёзды на момент обновления списка · 🗄️ — архивирован автором · 💤 — без коммитов больше года.

---

## Содержание

- [Клиенты API](#клиенты-api)
  - [Ozon](#ozon)
  - [Wildberries](#wildberries)
  - [Яндекс.Маркет](#яндексмаркет)
  - [Несколько площадок](#несколько-площадок)
- [MCP-серверы](#mcp-серверы)
- [Ценообразование и репрайсеры](#ценообразование-и-репрайсеры)
- [Инструменты вокруг](#инструменты-вокруг)
- [Коммерческие сервисы](#коммерческие-сервисы)
- [Официальная документация площадок](#официальная-документация-площадок)
- [Чего пока нет](#чего-пока-нет)
- [Как добавить проект](#как-добавить-проект)

---

## Клиенты API

### Ozon

- [gam6itko/ozon-seller](https://github.com/gam6itko/ozon-seller) — PHP, MIT, ⭐131. Самый зрелый клиент Ozon Seller API, живёт с 2018 года и до сих пор обновляется. Де-факто эталон в нише.
- [matacoder/wildberries-rest-api](https://github.com/matacoder/wildberries-rest-api) 💤 — Python, ⭐66. Несмотря на название, покрывает и Ozon. Последний коммит в 2024-м.
- [diPhantxm/ozon-api-client](https://github.com/diPhantxm/ozon-api-client) — Go, MIT, ⭐50. Полный типизированный клиент Seller API.
- [a-ulianov/OzonAPI](https://github.com/a-ulianov/OzonAPI) — Python, MIT, ⭐33. Асинхронный клиент с лимитами, автоповторами и документацией.
- [googlesheets-ru/OzonFromGAS](https://github.com/googlesheets-ru/OzonFromGAS) — TypeScript, ⭐31. Ozon API из Google Apps Script — практично, если учёт живёт в таблицах.
- [salacoste/ozon-daytona-seller-api](https://github.com/salacoste/ozon-daytona-seller-api) — TypeScript, MIT, ⭐15. 278 методов в 33 категориях.

### Wildberries

- [glmn/wb-private-api](https://github.com/glmn/wb-private-api) — JavaScript, ⭐111. Непубличное API WB: карточки, цены, поисковая выдача. Без ключей продавца, но и без гарантий стабильности.
- [Dakword/WBSeller](https://github.com/Dakword/WBSeller) 🗄️ — PHP, ⭐49. Архивирован автором в 2025-м, но код остаётся полезным справочником по структуре API.
- [RTHeLL/wbsdk](https://github.com/RTHeLL/wbsdk) — Python, MIT, ⭐12. Неофициальный SDK.

### Яндекс.Маркет

- [yandex-market/yandex-market-partner-api](https://github.com/yandex-market/yandex-market-partner-api) — BSD-3, ⭐39. **Официальная** OpenAPI-спецификация Партнёрского API. Из неё генерируется клиент на любом языке.

### Несколько площадок

- [dev-ik/seller-sdk](https://github.com/dev-ik/seller-sdk) — TypeScript, MIT. Ozon, Wildberries и Яндекс в одном типобезопасном SDK. Молодой проект.

---

## MCP-серверы

[Model Context Protocol](https://modelcontextprotocol.io/) даёт языковой модели доступ к данным. Сегмент делится надвое: серверы, читающие публичную витрину (запускаются мгновенно, ключи не нужны), и серверы, работающие с кабинетом продавца (нужен API-ключ, зато можно управлять).

**Чтение витрины**

- [Vladimir-Human/ru-marketplace-mcp](https://github.com/Vladimir-Human/ru-marketplace-mcp) — Python, MIT, ⭐82. Одиннадцать российских площадок, сравнение цен, ключи не требуются.
- [eduard256/ozon-mcp-server](https://github.com/eduard256/ozon-mcp-server) — JavaScript, ⭐58. Покупательский сценарий: поиск товаров, цены, доставка.

**Работа с кабинетом продавца**

- [ilyautov/marketplaces-mcp-ru](https://github.com/ilyautov/marketplaces-mcp-ru) — Python, MIT, ⭐22. WB и Ozon, 793 метода, генерация из схемы, отдельный гейт на операции записи.
- [PCDCK/ozon-mcp](https://github.com/PCDCK/ozon-mcp) 💤 — Python, MIT, ⭐20. Ozon Seller и Performance API.
- [theYahia/wildberries-mcp](https://github.com/theYahia/wildberries-mcp) — TypeScript, MIT, ⭐13. Заказы, аналитика, остатки WB.
- [DeviceIngineering/ozon-mcp-server](https://github.com/DeviceIngineering/ozon-mcp-server) — Python, MIT, ⭐4. 151 инструмент, Seller и Performance API, веб-панель, самодиагностика, мультимагазинность, SSE. Есть в [официальном реестре MCP](https://registry.modelcontextprotocol.io/).
- [DeviceIngineering/wb-mcp-server](https://github.com/DeviceIngineering/wb-mcp-server) — Python, MIT, ⭐3. То же для Wildberries, 202 инструмента.

**От площадок и сервисов**

- [mpstats-io/claude-code-skills](https://github.com/mpstats-io/claude-code-skills) — Shell, MIT, ⭐10. Единственный подтверждённый открытый релиз от коммерческого сервиса аналитики.

Официальных MCP-серверов от Ozon, Wildberries или Яндекс.Маркета на сентябрь 2026 нет.

---

## Ценообразование и репрайсеры

Самый пустой участок. Во всём GitHub семь репозиториев с тегом [`repricer`](https://github.com/topics/repricer), и почти все — учебные.

- [DeviceIngineering/ozon-wildberries-repricer](https://github.com/DeviceIngineering/ozon-wildberries-repricer) — Node.js + React, MIT. Ozon, Wildberries и Яндекс.Маркет: удержание эталонной цены, безубыточность по реальным тарифам каждой площадки (три разные модели), автовывод из акций, байесовский подбор цены экспериментом, кокпит решений, HTTP-API для LLM-агентов. Запускается на демо-данных без подключения магазина.
- [abrenmarie/ozon-marketplace-agent](https://github.com/abrenmarie/ozon-marketplace-agent) — Python, лицензии нет, ⭐2. Юнит-экономика по SKU и margin guard для Ozon. Компактный, читается за вечер.
- [execut/ozon-promotions](https://github.com/execut/ozon-promotions) — Go, лицензии нет. Ротация товаров в «Эластичном бустинге» — единственный найденный проект, посвящённый акциям Ozon.

---

## Инструменты вокруг

- [pashabaranov/Wildberries_Dashboard](https://github.com/pashabaranov/Wildberries_Dashboard) — дашборд по данным WB.
- [victorprogrammist/scrape_marketplaces](https://github.com/victorprogrammist/scrape_marketplaces) — MIT. Клиент к стороннему парсеру Ozon.

- [kosoyyagent/card-audit](https://github.com/kosoyyagent/card-audit) — Python, MIT. Аудит карточек WB/Ozon: отзывы, фото, рейтинг → Excel-отчёт с флагами.
- [kosoyyagent/ozon-seller-sync](https://github.com/kosoyyagent/ozon-seller-sync) — PHP, MIT. Синхронизация заказов и ПВЗ из Ozon Seller API в MySQL.
- [kosoyyagent/wb-ozon-ip-evidence](https://github.com/kosoyyagent/wb-ozon-ip-evidence) — Python, MIT. Пакет доказательств копирования карточек: метаданные, фото, скриншоты → Excel.
- [kosoyyagent/wb-photo-insert](https://github.com/kosoyyagent/wb-photo-insert) — Python, MIT. Массовая подстановка фото в карточки WB по списку артикулов.
- [kosoyyagent/wb-reviews-digest](https://github.com/kosoyyagent/wb-reviews-digest) — Python, MIT. Дайджест новых отзывов WB/Ozon в Excel для селлеров.

---

## Коммерческие сервисы

Без оценок и рекомендаций — как ориентир по рынку. Тарифы меняются, проверяйте на сайтах.

| Сервис | Что делает | Публичный API |
|---|---|---|
| [MPStats](https://mpstats.io/) | Аналитика, репрайсер WB и Ozon | да, + MCP |
| [MP Manager](https://mpmgr.ru/) | Управление ценами с учётом скидок площадок | да, + бесплатный MCP |
| [SalesFinder](https://salesfinder.ru/) | Аналитика и репрайсер | да |
| [Priceva](https://priceva.ru/) | Мониторинг цен, рекомендации | да, [PHP SDK](https://github.com/priceva/priceva-sdk-php) |
| [Imprice](https://imprice.ru/) | Репрайсер с юнит-экономикой, три площадки | не указан |
| [Moneyplace](https://moneyplace.io/) | Аналитика, репрайсер | да |
| [WBCON](https://wbcon.ru/) | Работа с ценами WB, синхронизация между площадками | да, Swagger |
| [ГуруСеллер](https://guruseller.ru/) | Репрайсер трёх площадок, юнит-экономика | не указан |

С февраля 2026 [собственный репрайсер есть и у самого Ozon](https://oborot.ru/blogs/ozon-zapustil-reprajser-avtomaticheskoe-upravlenie-cenami-na-dvuh-marketplejsah-i263193.html) — кросс-платформенный, для Ozon и Wildberries.

---

## Официальная документация площадок

- [Ozon Seller API](https://docs.ozon.ru/api/seller/) · [dev.ozon.ru](https://dev.ozon.ru/) · [как избежать блокировок](https://dev.ozon.ru/start/298-Seller-API-kak-izbezhat-blokirovok/)
- [Ozon Performance API](https://docs.ozon.ru/api/performance/) — реклама, отдельные учётные данные
- [Wildberries API](https://dev.wildberries.ru/) · [что это такое](https://seller.wildberries.ru/instructions/ru/ru/material/wb-api)
- [Яндекс.Маркет Partner API](https://yandex.ru/dev/market/partner-api/)

> **Важно.** Правила Ozon прямо запрещают автоматический парсинг витрины вне разрешённых доменов и работу через VPN, а ответственность за действия по API несёт владелец кабинета. Прежде чем подключать инструмент из этого списка к боевому аккаунту, прочитайте правила площадки.

---

## Чего пока нет

Честный список пробелов — если вы ищете, что написать, здесь свободно:

- **Мультиплатформенный автовывод из акций.** Автовход есть у нескольких коммерческих сервисов, автовыход по правилу — почти нигде.
- **Открытый инструмент для Яндекс.Маркета.** Есть официальная спека API и ни одного заметного приложения поверх неё.
- **Работа с отчётами о реализации.** Ни один открытый проект не разбирает финансовые отчёты площадок, а именно там видна настоящая экономика.
- **Подбор цены экспериментом.** По запросу `bayesian pricing experiment` на GitHub два репозитория, оба без звёзд.
- **Официальные MCP-серверы площадок.** Всё, что есть, написано сообществом.

---

## Как добавить проект

Пул-реквест с одной строкой в нужный раздел. Просьбы, которые экономят время ревью:

- проект открыт и работает — не заготовка и не архив без пометки;
- одно предложение о том, что он делает, без маркетинга;
- укажите язык и лицензию;
- свои проекты добавлять можно и нужно — просто скажите об этом в описании PR.

Порядок внутри разделов — по звёздам, чтобы не спорить о вкусах. Цифры обновляются периодически и могут отставать.

---

## Лицензия

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

Список распространяется под [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/). Лицензии самих проектов — у их авторов.
