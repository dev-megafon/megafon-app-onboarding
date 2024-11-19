---
order: 2.5
title: Создать график активности по дням
---

### `POST /calendar/scheduler`

**Описание:** этот метод создает график активности.

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

   virtual_number_ids

*  {% colwidth=[110] %}

   array of integers

*  {% colwidth=[146] %}

   Нет

*  {% colwidth=[126] %}

   \-

*  Идентификаторы виртуальных номеров.

---

*  {% colwidth=[164] isHeader=true %}

   virtual_number_group_ids

*  {% colwidth=[110] %}

   array of integers

*  {% colwidth=[146] %}

   Нет

*  {% colwidth=[126] %}

   \-

*  Идентификаторы групп виртуальных номеров.

---

*  {% colwidth=[164] isHeader=true %}

   production_holidays

*  {% colwidth=[110] %}

   array of strings

*  {% colwidth=[146] %}

   Нет

*  {% colwidth=[126] %}

   \-

*  Уникальные дни для графика: Нерабочие дни

---

*  {% colwidth=[164] isHeader=true %}

   production_workdays

*  {% colwidth=[110] %}

   array of strings

*  {% colwidth=[146] %}

   Нет

*  {% colwidth=[126] %}

   \-

*  Уникальные дни для графика: рабочие дни

---

*  {% colwidth=[164] isHeader=true %}

   week_end_schedule

*  {% colwidth=[110] %}

   array of strings или null

*  {% colwidth=[146] %}

   Нет (Обязательное, если параметр “`use_public_days_difference`” или “`is_use_days_difference_day_type`” стоит “`True`”)

*  {% colwidth=[126] %}

   Формат времени (HH:MM:SS)

*  Расписание на дополнительные рабочие дни согласно Производственному календарю или Уникальным рабочим дням.

---

*  {% colwidth=[164] isHeader=true %}

   week_days_schedule

*  {% colwidth=[110] %}

   array of arrays of strings

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   Формат времени (HH:MM:SS)

*  Расписание на рабочие дни. Необходимо обязательно указывать время для всех дней недели. Если день считается выходным, то вместо времени следует указать значение «`null`».

---

*  {% colwidth=[164] isHeader=true %}

   use_public_days_difference

*  {% colwidth=[110] %}

   boolean

*  {% colwidth=[146] %}

   Да, только если в параметре “`type`” выбрано значение “`week_days`”

*  {% colwidth=[126] %}

   true, false

*  Учитывать производственный календарь.

---

*  {% colwidth=[164] isHeader=true %}

   is_use_days_difference_day_type

*  {% colwidth=[110] %}

   boolean

*  {% colwidth=[146] %}

   Да, только если в параметре “`type`” выбрано значение “`week_days`”

*  {% colwidth=[126] %}

   true, false

*  Установить уникальные дни для графика.

---

*  {% colwidth=[164] isHeader=true %}

   id

*  {% colwidth=[110] %}

   integer

*  {% colwidth=[146] %}

   \-

*  {% colwidth=[126] %}

   Положительное число

*  Уникальный идентификатор графика активности.

{% /table %}

## **Структура запроса**

```json
POST /calendar/scheduler/
{
    "name": "Название графика",
    "type": "week_days",
    "production_holidays": [
        "2024-10-29",
        "2024-10-28"
    ],
    "production_workdays": [
        "2024-10-27",
        "2024-10-26"
    ],
    "day_before_holidays_schedule": [
        "09:00:00",
        "18:00:00"
    ],
    "week_end_schedule": [
        "09:00:00",
        "17:00:00"
    ],
    "week_days_schedule": [
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
        null
    ],
    "use_public_days_difference": true,
    "is_use_days_difference_day_type": true
}
```

**Ответ**:

```json
{
    "name": "Название_графика",
    "type": "week_days",
    "virtual_number_ids": [],
    "virtual_number_group_ids": [],
    "production_holidays": [],
    "production_workdays": [],
    "day_before_holidays_schedule": [
        "09:00:00",
        "18:00:00"
    ],
    "week_end_schedule": null,
    "week_days_schedule": [
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
        [
            "09:00:00",
            "18:00:00"
        ]
    ],
    "use_public_days_difference": true,
    "is_use_days_difference_day_type": false,
    "id": 203
}
```