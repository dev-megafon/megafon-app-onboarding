---
order: 3
title: Получить список регионов для исходящих сценариев
---

### `GET /limitations/region?_order=asc&_sort=name&parent_id=20151&type=region`

**Описание:** метод поможет найти все Регионы и их id, которые можно использовать для настройки исходящих сценариев.

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

   id

*  integer

*  \-

*  Идентификатор региона.

---

*  {% isHeader=true %}

   name

*  string

*  \-

*  Название региона.

{% /table %}

## Структура запроса

`GET /limitations/region?_order=asc&_sort=name&parent_id=20151&type=region`

## Структура ответа

```json
[
    {
        "id": 20195,
        "name": "Алтайский край",
        "type": "region"
    },
    {
        "id": 20240,
        "name": "Амурская область",
        "type": "region"
    },
...
]
```