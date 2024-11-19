---
order: 3
title: Создать график активности по числам
---

### `POST /calendar/scheduler`

**Описание:** этот метод  создает график активности по числам

## Параметры метода

{% table %}

---

*  {% colwidth=[164] isHeader=true %}

   Название

*  {% colwidth=[110] isHeader=true %}

   Тип

*  {% colwidth=[146] isHeader=true %}

   Обязательный

*  {% colwidth=[126] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[164] isHeader=true %}

   name

*  {% colwidth=[110] %}

   string

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   \-

*  Название графика активности

---

*  {% colwidth=[164] isHeader=true %}

   type

*  {% colwidth=[110] %}

   string

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   `week_days`, `month_days`, `cycle`

*  Тип расписания (По дням недели, По числам, По циклу)

---

*  {% colwidth=[164] isHeader=true %}

   month_days_schedule

*  {% colwidth=[110] %}

   array of arrays of boolean

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   

*  В рамках данного проекта необходимо заполнить данные о графике работы за весь месяц (31 день) . Если в параметре `default_schedule` указано время работы, то для каждого дня месяца необходимо указать значение`True/False`. Если `default_schedule` равен `null`, то для рабочих дней необходимо указать время работы, а для нерабочих -- `null`.

---

*  {% colwidth=[164] isHeader=true %}

   default_schedule

*  {% colwidth=[110] %}

   array of strings или null

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   Формат времени (HH:MM:SS)

*  Расписание на рабочие дни.

{% /table %}

## **Структура запроса (Пример 1)**

```json
POST /calendar/scheduler/
{
    "name": "Название графика",
    "type": "month_days",
    "month_days_schedule": [
        true,
        true,
        true,
        true,
        true,
        true,
        true,
        true,
        true,
        true,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false
    ],
    "default_schedule": [
        "09:40:10",
        "19:00:00"
    ]
}
```

## **Структура ответа**

```json
{
    "name": "Название графика",
    "type": "month_days",
    "virtual_number_ids": [],
    "virtual_number_group_ids": [],
    "month_days_schedule": [
        true,
        true,
        true,
        true,
        true,
        true,
        true,
        true,
        true,
        true,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false,
        false
    ],
    "default_schedule": [
        "09:40:10",
        "19:00:00"
    ],
    "id": 219
}
```

## **Структура запроса (Пример 2)**

```json
{
    "name": "Название графика",
    "type": "month_days",
    "month_days_schedule": [
        [
            "09:00:00",
            "18:00:00"
        ],
        [
            "09:00:00",
            "18:00:00"
        ],
        [
            "09:00:00",
            "18:00:00"
        ],
        null,
        [
            "09:00:00",
            "18:00:00"
        ],
        [
            "09:00:00",
            "18:00:00"
        ],
        [
            "09:00:00",
            "18:00:00"
        ],
        null,
        [
            "09:00:00",
            "18:00:00"
        ],
        [
            "09:00:00",
            "18:00:00"
        ],
        [
            "09:00:00",
            "18:00:00"
        ],
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null
    ],
    "default_schedule": null
}
```

```json
{
    "name": "Название графика",
    "type": "month_days",
    "virtual_number_ids": [],
    "virtual_number_group_ids": [],
    "month_days_schedule": [
        [
            "09:00:00",
            "18:00:00"
        ],
        [
            "09:00:00",
            "18:00:00"
        ],
        [
            "09:00:00",
            "18:00:00"
        ],
        null,
        [
            "09:00:00",
            "18:00:00"
        ],
        [
            "09:00:00",
            "18:00:00"
        ],
        [
            "09:00:00",
            "18:00:00"
        ],
        null,
        [
            "09:00:00",
            "18:00:00"
        ],
        [
            "09:00:00",
            "18:00:00"
        ],
        [
            "09:00:00",
            "18:00:00"
        ],
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null,
        null
    ],
    "default_schedule": null,
    "id": 223
}
```