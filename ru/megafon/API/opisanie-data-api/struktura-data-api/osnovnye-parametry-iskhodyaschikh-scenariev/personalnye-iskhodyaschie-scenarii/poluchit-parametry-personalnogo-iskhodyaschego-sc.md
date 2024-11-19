---
order: 0.8
title: Получить настройки персонального исходящего сценария
---

### `GET /scenario/outbound/personal/{id}`

**Описание:** Получение информации о параметрах персонального исходящего сценария

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

`GET /scenario/outbound/personal/155`

## Cтруктура ответа

```json
[
    {
        "virtual_number_id": 256,
        "id": 155,
        "employee_group_id": null,
        "employee_id": 137,
        "substitute_number_capacity_id": 677
    }
]
```