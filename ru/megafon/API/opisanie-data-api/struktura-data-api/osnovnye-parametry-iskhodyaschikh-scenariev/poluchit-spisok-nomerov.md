---
order: 2
title: Получить список номеров для исходящих сценариев
---

### `GET /numbers/virtual-number?purpose__ne=not_specified&state=active&type=def&type=abc`

**Описание:** этот метод позволяет получить список номеров для исходящих сценариев

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% colwidth=[192] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   number

*  string

*  {% colwidth=[192] %}

   

*  Виртуального номера.

---

*  {% isHeader=true %}

   comment

*  string

*  {% colwidth=[192] %}

   

*  Заметка о Виртуальном номере

---

*  {% isHeader=true %}

   purpose

*  string

*  {% colwidth=[192] %}

   `сompany`, `employee`, `not_specified`

*  Назначение Виртуального номера

---

*  {% isHeader=true %}

   id

*  integer

*  {% colwidth=[192] %}

   Положительное число

*  Уникальный идентификатор виртуального номера.

---

*  {% isHeader=true %}

   from_redirect_numbers

*  array of objects

*  {% colwidth=[192] %}

   \-

*  Список перенаправленных номеров.

{% /table %}

## Пример запроса:

`GET /numbers/virtual-number?purpose__ne=not_specified&state=active&type=def&type=abc`

## Пример ответа:

```json
[
    {
        "number": "79201234567",
        "comment": "Заметка",
        "type": "def",
        "purpose": "employee",
        "scenario_id": 779,
        "group_scenario_id": null,
        "group_id": null,
        "is_scenario_active": true,
        "is_group_scenario_active": null,
        "id": 250,
        "state": "active",
        "reason": null,
        "from_redirect_numbers": [
            {
                "id": 678,
                "number": "78009966666"
            },
            {
                "id": 249,
                "number": "74994088157"
            }
        ],
        "employee_id": 125,
        "dgn_number": "74994088157",
        "region_name": "Брянская область",
        "sip_uri": null,
        "nc_type": "custom+fmc",
        "redirect_number": null,
        "app_id": 1200054
    }
]
```