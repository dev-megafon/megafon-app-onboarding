---
order: 0.5
title: Получение настроек основного номера компании
---

### `GET /scenario/outbound/main`

**Описание**: метод  позволяет задавать основной номер кампании, а так же какой номер будет видеть Абонент при исходящем звонке ему.

## Параметры метода

{% table %}

---

*  {% colwidth=[250] isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[250] isHeader=true %}

   virtual_number_id

*  integer

*  Положительное целое

*  Идентификатор виртуального номера.

---

*  {% colwidth=[250] isHeader=true %}

   id

*  integer

*  Положительное целое

*  Идентификатор правила исходящего сценария

---

*  {% colwidth=[250] isHeader=true %}

   substitute_number_capacity_id

*  integer

*  Положительное целое

*  Идентификатор номера который будет показываться клиенту при исходящем звонке.

{% /table %}

## Структура запроса

`GET /scenario/outbound/main`

## Cтруктура ответа

```json
[
    {
        "virtual_number_id": 256,
        "id": 185,
        "substitute_number_capacity_id": 677
    }
]
```