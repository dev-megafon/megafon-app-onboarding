---
order: 1
title: Получить все настроенные персональные мелодии
---

### `GET /melodies/personal`

**Описание:** метод позволяет получить настроенные персональные мелодии, которые будут звучать при дозвоне до отделов/виртуальных номеров.

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

   number_capacity_ids

*  Array

*  Целые числа или null

*  Список идентификаторов номеров, для которых применяется персональная мелодия.

---

*  {% isHeader=true %}

   employee_group_ids

*  Array

*  Целые числа или null

*  Список идентификаторов отделов сотрудников, для которых применяется персональная мелодия.

---

*  {% isHeader=true %}

   source_type

*  String

*  client, system

*  Тип источника мелодии: клиентская или системная мелодия.

---

*  {% isHeader=true %}

   media_id

*  Integer

*  Целое число

*  Идентификатор медиафайла для персональной мелодии.

---

*  {% isHeader=true %}

   id

*  Integer

*  Целое число

*  Уникальный идентификатор настройки персональной мелодии.

{% /table %}

## Структура запроса:

`GET /melodies/personal`

## Структура ответа:

```json
[
    {
        "numbercapacityids": [
            250,
            256,
            258
        ],
        "employeegroupids": null,
        "source_type": "system",
        "media_id": 50,
        "id": 37
    },
    {
        "numbercapacityids": null,
        "employeegroupids": [
            79
        ],
        "source_type": "system",
        "media_id": 50,
        "id": 67
    },
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
        "id": 81
    }
]
```