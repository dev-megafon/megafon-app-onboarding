---
order: 0.5
title: "Получить список\_ персональных исходящих сценариев"
---

### `GET /scenario/outbound/personal`

**Описание:** Получение информации о параметрах персональных исходящих сценариях звонков.

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

   employee_group_id

*  integer

*  null или положительное целое

*  Идентификатор отдела сотрудников

---

*  {% isHeader=true %}

   employee_id

*  integer

*  null или положительное целое

*  Идентификатор сотрудника.

---

*  {% isHeader=true %}

   substitute_number_capacity_id

*  integer

*  null или положительное целое

*  Идентификатор номера который будет показываться клиенту при исходящем звонке

{% /table %}

## Структура запроса

`GET /scenario/outbound/personal`

## Cтруктура ответа

```json
[
    {
        "virtual_number_id": 256,
        "id": 347,
        "substitute_number_capacity_id": 677,
        "employee_group_id": null,
        "employee_id": 137
    },
    {
        "virtual_number_id": 250,
        "id": 467,
        "substitute_number_capacity_id": 250,
        "employee_group_id": 83,
        "employee_id": null
    }
]
```