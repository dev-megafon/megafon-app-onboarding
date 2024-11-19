---
order: 1
title: Поиск международных id стран
---

### `GET /limitations/region?_order=asc&_sort=name&type=country`

**Описание**: метод помогает найти id стран для настройки правил ограничения звонков для международных звонков.

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   **Название**

*  {% isHeader=true %}

   **Тип**

*  {% isHeader=true %}

   **Допустимые значения**

*  {% isHeader=true %}

   **Описание**

---

*  {% isHeader=true %}

   id

*  integer

*  Целое число

*  Уникальный идентификатор страны.

---

*  {% isHeader=true %}

   name

*  string

*  Название Страны

*  Название страны.

{% /table %}

## Структура запроса

`GET /limitations/region?_order=asc&_sort=name&type=country`

## Структура ответа

```json
{
        "id": 20152,
        "name": "Абхазия",
        "type": "country"
    },
    {
        "id": 21824,
        "name": "Австралия",
        "type": "country"
    },
    {
        "id": 21902,
        "name": "Австрия",
        "type": "country"
    }
```