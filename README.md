# liteExchange. Синхронизация с 1с

#liteExchange - это технология для выполнения задач синхронизации и интеграции на платформе 1с.

Ключевая особенность - практически мгновенный обмен, недостижимая скорость для привычных инструментов.
В основе - http сервисы.

## Решаемые задачи:

1. Организация Backend на платформе 1с.
2. Обработка WebHook
3. Отправка данных на сторонний сервер для обработки.
4. Синхронизация баз 1с с возможностью описать код конвертации объектов:
   * Одинаковые базы 1с
   * Похожие базы 1с
   * Разные базы 1с
   * Риб (ускорение до онлайн)

## Компоненты фреймворка:

1. Легкий HTTP коннектор.
2. Продвинутый JSON сериализатор
3. Продвинутый конвертер объектов 1с в простые типы и обратно
4. Анализатор данных, формирующий массив ссылок на объект
5. GZIP распаковщик для обработки ответов серверов
6. Модуль обработки входящих и формирования исходящих запросов HTTP

## Особенности и тебования

Поставляется в виде расширения

Минимальные требования - платформа 8.3.9 или режим совместимости 8.3.9 для устаревших конфигураций
Подробнее о том, как в УПП 1.3. получить режим совместимости 8.3.9 и чем это грозит тут: <..>

## Концепция решения


* DATAREON MQ - содержит встроенный коннектор с 1с, реализует обмен в формате XML. Решает часть задач, как liteExchange, но ео надо уметь готовить.
* Rabbit MQ - для высоконагруженных систем. Требоует коннектора и внешней компоненты для работы с 1с
* Универсальный обмен данными XML - невероятно медленный
* Правила обмена КД2 - еще более медленные
* Правила обмена КД3 и омбен через универсальный формат - быстрее КД2, но надо уметь из готовить. Обмен опять через XML.

## Примеры решаемых задач.

1. Обмен с AMO CRM, Битрикс 24, Интернет магазинами в реальном времени.
2. Передача данных для обработки на удаленные сервера и системы.
3. Синхронизация с другой 1с.
4. Параллельная работа в нескольких копиях 1с (почти РИБ)

Больше кейсов в канале телеграмм:
https://t.me/liteExchange_channel

## Документация
[тут:][1]

[1]: https://github.com/liteappsru/liteExchange/wiki/liteExchange.%D0%94%D0%BE%D0%BA%D1%83%D0%BC%D0%B5%D0%BD%D1%82%D0%B0%D1%86%D0%B8%D1%8F/        "документация"
