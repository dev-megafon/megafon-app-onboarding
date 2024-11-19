---
order: 0.8
title: Получить информацию о группах входящих сценариев
---

### `GET /scenario/inbound/group`

**Описание**: метод  используется для работы с группами номеров, настроенных во входящих сценариях. Он позволяет найти информацию о группе номеров.

:::info 

URL для доступа к API: <https://simple-api.cp.megafon.ru>

:::

### Параметры

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   `name`

*  string

*  --

*  Уникальное имя группы сценариев.

---

*  {% isHeader=true %}

   `is_active`

*  boolean

*  `true`, `false`

*  Указывает активность сценария, смены или перерыва

---

*  {% isHeader=true %}

   `comment`

*  string

*  --

*  Заметка для группы номеров.

---

*  {% isHeader=true %}

   `virtual_number_ids`

*  array of int

*  --

*  Массив идентификаторов виртуальных номеров, добавленных в группу.

---

*  {% isHeader=true %}

   `scenario_id`

*  integer

*  --

*  Идентификатор Входящего сценарий настроенный для группы номеров.

---

*  {% isHeader=true %}

   `id`

*  integer

*  --

*  Уникальный идентификатор группы номеров

{% /table %}

## Пример запроса

`GET /scenario/inbound/group`

## Пример ответа

```json
[
    {
        "name": "Имя группы",
        "is_active": true,
        "comment": "Заметка о группе",
        "virtual_number_ids": [
            546
        ],
        "scenario_id": 73,
        "id": 35
    },
    {
        "name": "Имя группы2",
        "is_active": false,
        "comment": null,
        "virtual_number_ids": [
            585,
            817,
            611,
            600
        ],
        "scenario_id": null,
        "id": 39
    }
]
```