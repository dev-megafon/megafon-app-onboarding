---
order: 2
title: Добавить персональную мелодию
---

### `POST /melodies/personal`

**Описание:** метод позволяет добавить персональную мелодию, которая будет звучать при дозвоне до отделов/виртуальных номеров.

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% colwidth=[159] isHeader=true %}

   Обязательный

*  {% colwidth=[114] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   number_capacity_ids

*  Array

*  {% colwidth=[159] %}

   Да, обязательный один из параметров `number_capacity_ids `или employee_group_ids

*  {% colwidth=[114] %}

   Целые числа

*  Список идентификаторов номеров, для которых применяется персональная мелодия. (**ЗАПРЕЩЕНО** добавлять правила на те ВН, по которым уже есть правила)

---

*  {% isHeader=true %}

   employee_group_ids

*  Array

*  {% colwidth=[159] %}

   Да, обязательный один из параметров `number_capacity_ids `или `employee_group_ids`

*  {% colwidth=[114] %}

   Целые числа

*  Список идентификаторов отделов сотрудников, для которых применяется персональная мелодия. (**ЗАПРЕЩЕНО** добавлять правила на те отделы, по которым уже есть правила)

---

*  {% isHeader=true %}

   source_type

*  String

*  {% colwidth=[159] %}

   Да

*  {% colwidth=[114] %}

   client, system

*  Тип источника мелодии: клиентская или системная мелодия.

---

*  {% isHeader=true %}

   media_id

*  Integer

*  {% colwidth=[159] %}

   Да

*  {% colwidth=[114] %}

   Целое число

*  Идентификатор медиафайла для персональной мелодии.

{% /table %}

## Структура запроса:

`POST /melodies/personal`

```json
{
  "numbercapacityids": [
    352,
    446,
    448
  ],
  "employeegroupids": [
    93,
    103
  ],
  "source_type": "system",
  "media_id": 50
}
```

## Структура ответа:

```json

{
    "numbercapacityids": [
        352,
        446,
        448
    ],
    "employeegroupids": [
        93,
        103
    ],
    "source_type": "system",
    "media_id": 50,
    "id": 83
}
```