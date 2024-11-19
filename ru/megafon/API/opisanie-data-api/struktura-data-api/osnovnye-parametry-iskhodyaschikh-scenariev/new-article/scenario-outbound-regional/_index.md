---
order: 0.3
title: "Получить список\_ исходящих региональных сценариев"
---

### `GET/scenario/outbound/regional`

## Параметры метода

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

   virtual_number_id

*  integer

*  Положительное целое

*  Идентификатор виртуального номера.

---

*  {% isHeader=true %}

   id

*  integer

*  Положительное целое

*  Идентификатор сценария.

---

*  {% isHeader=true %}

   region_id

*  integer

*  Положительное целое

*  Идентификатор региона.

---

*  {% isHeader=true %}

   substitute_number_capacity_id

*  integer

*  Положительное целое

*  Идентификатор номера, который будет показываться клиенту при исходящем звонке

---

*  {% isHeader=true %}

   numa_type

*  string

*  null, «def», «abc»

*  Настройка “Использовать для звонков”. null - На все номера; «def» - На мобильные номера; «abc» - На Городские номера

{% /table %}



## Структура запроса

`GET/scenario/outbound/regional`

## Структура ответа

```json
[
    {
        "virtual_number_id": 250,
        "id": 365,
        "numa_type": null,
        "substitute_number_capacity_id": 249,
        "region_id": 20205
    },
    {
        "virtual_number_id": 256,
        "id": 367,
        "numa_type": "def",
        "substitute_number_capacity_id": 255,
        "region_id": 20240
    },
    {
        "virtual_number_id": 250,
        "id": 465,
        "numa_type": "abc",
        "substitute_number_capacity_id": 250,
        "region_id": 20240
    }
]
```