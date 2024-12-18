---
order: 0.5
title: Основные особенности структуры
---

#### Базовый URL

Все запросы к API следует отправлять на следующий базовый URL:

`https://callapi.cp.megafon.ru/v4.0`

#### Формат возвращаемых данных

По умолчанию используется формат JSON. Заголовок Accept игнорируется, и все ответы будут возвращены в формате MIME Type: `application/json`

#### Общие поля для всех методов

| Название | Тип               | Обязательный | Допустимые значения | Описание                                                                                                                                           |
|----------|-------------------|--------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| id       | string или number | да           | --                  | Уникальный идентификатор запроса к API. Не передается в уведомлениях. Фигурирует только в статистике и отчетах (параметр "Идентификатор запроса"). |
| method   | string            | да           | --                  | Вызываемый метод (см. Список методов).                                                                                                             |
| jsonrpc  | string            | да           | 2\.0                | Номер спецификации JSON-RPC.                                                                                                                       |
| params   | object            | да           | --                  | Содержит тело запроса к API. В зависимости от вызываемого метода тело запроса меняется.                                                            |