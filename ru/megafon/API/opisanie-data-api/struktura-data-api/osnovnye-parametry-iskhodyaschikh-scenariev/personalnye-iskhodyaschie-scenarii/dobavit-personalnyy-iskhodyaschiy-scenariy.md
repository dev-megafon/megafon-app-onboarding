---
order: 1
title: Добавить персональный исходящий сценарий
---

### `POST /scenario/outbound/personal`

**Описание:** метод позволяет добавить персональный исходящий сценарий.

## Параметры метода:

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% isHeader=true %}

   Обязательный

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   virtual_number_id

*  integer

*  да

*  Положительное целое

*  Идентификатор виртуального номера.

---

*  {% isHeader=true %}

   employee_group_id

*  integer

*  Обязательный один из двух параметров: employee_group_id или employee_id

*  положительное целое

*  Идентификатор отдела сотрудников (ЗАПРЕЩЕНО указывать ID отдела по которой уже есть правила )

---

*  {% isHeader=true %}

   employee_id

*  integer

*  Обязательный один из двух параметров: employee_group_id или employee_id

*  положительное целое

*  Идентификатор сотрудника.(ЗАПРЕЩЕНО указывать IDсотрудника по которому уже есть правила)

---

*  {% isHeader=true %}

   substitute_number_capacity_id

*  integer

*  да

*  положительное целое

*  Идентификатор номера который будет показываться клиенту при исходящем звонке (Например можно указать id самого номера или id номера ДГН или id номера 8800 привязанный к данному номеру)

{% /table %}

## Структура запроса:

```json
{
  "virtual_number_id": 256,
  "employee_id": 293,
  "substitute_number_capacity_id": 255
}
```

## Структура ответа:

```json
{
    "virtual_number_id": 256,
    "employee_id": 293,
    "employee_group_id": null,
    "substitute_number_capacity_id": 255,
    "id": 527
}
```