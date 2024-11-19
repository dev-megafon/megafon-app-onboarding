---
order: 1
title: Редактировать параметры регионального исходящего сценария
---

### `PUT /scenario/outbound/regional/{id}`

**Описание**: этот метод позволяет редактировать параметры регионального исходящего сценария.

## Параметры метода

{% table %}

---

*  {% colwidth=[146] isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% colwidth=[145] isHeader=true %}

   Обязательные

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[146] isHeader=true %}

   virtual_number_id

*  integer

*  {% colwidth=[145] %}

   да

*  Положительное целое

*  Идентификатор виртуального номера.

---

*  {% colwidth=[146] isHeader=true %}

   id

*  integer

*  {% colwidth=[145] %}

   да

*  Положительное целое

*  Идентификатор сценария.

---

*  {% colwidth=[146] isHeader=true %}

   region_id

*  integer

*  {% colwidth=[145] %}

   да

*  Положительное целое

*  Идентификатор региона.(**ЗАПРЕЩЕНО** менять в исходящем сценарии регион. )

---

*  {% colwidth=[146] isHeader=true %}

   substitute_number_capacity_id

*  integer

*  {% colwidth=[145] %}

   да

*  Положительное целое

*  Идентификатор номера который будет показываться клиенту при исходящем звонке (Например можно указать id самого номера или id номера ДГН или id номера 8800 привязанный к данному номеру)

---

*  {% colwidth=[146] isHeader=true %}

   numa_type

*  string

*  {% colwidth=[145] %}

   Обязательный, если нужны настройки или для «`def`» - На мобильные номера или для «`abc`» - На Городские номера. Если для всех звонков, то параметр не обязательный

*  `null`, «`def`», «`abc`»

*  Настройка “Использовать для звонков”. null - На все номера; «def» - На мобильные номера; «abc» - На Городские номера

{% /table %}



## Структура запроса

`PUT /scenario/outbound/regional/529`

```json
{
  "virtual_number_id": 256,
  "region_id": 20165,
  "numa_type": "abc",
  "id": "529",
  "substitute_number_capacity_id": 676
}
```

## Структура ответа

```json
{
    "virtual_number_id": 256,
    "region_id": 20165,
    "numa_type": "abc",
    "id": 529,
    "substitute_number_capacity_id": 676
}
```