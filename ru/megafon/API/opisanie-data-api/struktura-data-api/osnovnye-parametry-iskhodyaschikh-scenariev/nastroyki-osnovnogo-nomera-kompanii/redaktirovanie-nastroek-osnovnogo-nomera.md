---
order: 1
title: Редактировать настройки основного номера
---

## `PUT /scenario/outbound/main/{id}`

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

   id

*  integer

*  да

*  Положительное целое

*  Идентификатор правила исходящего сценария(получить можно методом GET /scenario/outbound/main)

---

*  {% isHeader=true %}

   substitute_number_capacity_id

*  integer

*  да

*  Положительное целое

*  Идентификатор номера который будет показываться клиенту при исходящем звонке (Например можно указать id самого номера или id номера ДГН или id номера 8800 привязанный к данному номеру)

{% /table %}

## Cтруктура запроса

`PUT /scenario/outbound/main/123`

```json
{
  "virtual_number_id": 123,
  "id": 185,
  "substitute_number_capacity_id": 321
}
```

## Структура ответа

```json
{
  "virtual_number_id": 123,
  "id": 185,
  "substitute_number_capacity_id": 321
}
```