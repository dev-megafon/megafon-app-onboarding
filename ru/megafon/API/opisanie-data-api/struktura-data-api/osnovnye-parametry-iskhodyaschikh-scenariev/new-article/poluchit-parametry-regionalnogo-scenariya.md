---
order: 0.4
title: Получить настройки исходящего регионального сценария
---

### `GET /scenario/outbound/regional/{id}`

**Описание**: этот метод позволяет получить параметры исходящего регионального сценария

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

`GET /scenario/outbound/regional/365`

## Структура ответа

```
[
    {
        "virtual_number_id": 250,
        "id": 365,
        "numa_type": null,
        "substitute_number_capacity_id": 249,
        "region_id": 20205
    }
]
```