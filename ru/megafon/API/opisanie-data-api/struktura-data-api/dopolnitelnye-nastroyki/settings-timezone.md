---
order: 0.5
title: Список часовых поясов
---

### `GET /settings/timezone`

**Описание:** этот метод предоставляет пользователю полную информацию о всех доступных часовых поясах, включая их названия и смещения относительно UTC

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% colwidth=[72] isHeader=true %}

   Тип

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   id

*  {% colwidth=[72] %}

   string

*  Любая строка

*  Уникальный идентификатор временной зоны.

---

*  {% isHeader=true %}

   name

*  {% colwidth=[72] %}

   string

*  Любая строка

*  Название временной зоны.

{% /table %}

## Структура запроса

` GET /settings/timezone`

## **Структура ответа**

```json

    {
        "id": "Etc/GMT+12",
        "name": "(UTC-12) UTC-12"
    },
    {
        "id": "Etc/GMT+11",
        "name": "(UTC-11) UTC-11"
    },
    {
        "id": "Pacific/Midway",
        "name": "(UTC-11) Pacific/Midway"
    },
    {
        "id": "Pacific/Niue",
        "name": "(UTC-11) Pacific/Niue"
    },
    {
        "id": "Pacific/Pago_Pago",
        "name": "(UTC-11) Pacific/Pago_Pago"
    },
```

### 