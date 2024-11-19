---
order: 0.5
title: Добавить исходящий региональный сценарий
---

### `POST /scenario/outbound/regional`

**Описание**: метод позволяет добавить исходящий региональный сценарий.

## Параметры метода

{% table %}

---

*  {% colwidth=[195] isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% colwidth=[137] isHeader=true %}

   Обязательный

*  {% colwidth=[160] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[195] isHeader=true %}

   virtual_number_id

*  integer

*  {% colwidth=[137] %}

   да

*  {% colwidth=[160] %}

   Положительное целое

*  Идентификатор виртуального номера.

---

*  {% colwidth=[195] isHeader=true %}

   region_id

*  integer

*  {% colwidth=[137] %}

   да

*  {% colwidth=[160] %}

   Положительное целое

*  Идентификатор региона.(ЗАПРЕЩЕНО указывать регион и тот же numa_type который уже настроен)

---

*  {% colwidth=[195] isHeader=true %}

   substitute_number_capacity_id

*  integer

*  {% colwidth=[137] %}

   да

*  {% colwidth=[160] %}

   Положительное целое

*  Идентификатор номера который будет показываться клиенту при исходящем звонке (Например можно указать id самого номера или id номера ДГН или id номера 8800 привязанный к данному номеру)

---

*  {% colwidth=[195] isHeader=true %}

   numa_type

*  string

*  {% colwidth=[137] %}

   Обязательный, если нужны настройки или для «def» - На мобильные номера или для «abc» - На Городские номера. Если для всех звонков, то параметр не обязательный

*  {% colwidth=[160] %}

   null, «def», «abc»

*  Настройка “Использовать для звонков”. null - На все номера; «def» - На мобильные номера; «abc» - На Городские номера (ЗАПРЕЩЕНО указывать регион и тот же numa_type который уже настроен)

{% /table %}

## Cтруктура запроса

```json
{
  "numa_type": "abc",
  "virtual_number_id": 256,
  "region_id": 20170,
  "substitute_number_capacity_id": 256
}
```

## Структура ответа

```json
{
    "virtual_number_id": 256,
    "region_id": 20170,
    "numa_type": "abc",
    "id": 533,
    "substitute_number_capacity_id": 256
}
```