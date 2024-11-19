---
order: 3.5
title: Редактировать график активности по дням
---

### `PUT /calendar/scheduler/{id}`

**Описание:**  этот метод редактирует данные графика активности по дням.

## Параметры метода

{% table %}

---

*  {% colwidth=[159] isHeader=true %}

   Название

*  {% colwidth=[110] isHeader=true %}

   Тип

*  {% colwidth=[148] isHeader=true %}

   Обязательный

*  {% colwidth=[126] isHeader=true %}

   Допустимые значения

*  {% colwidth=[240] isHeader=true %}

   Описание

---

*  {% colwidth=[159] isHeader=true %}

   name

*  {% colwidth=[110] %}

   string

*  {% colwidth=[148] %}

   Да

*  {% colwidth=[126] %}

   \-

*  {% colwidth=[240] %}

   Название графика активности

---

*  {% colwidth=[159] isHeader=true %}

   type

*  {% colwidth=[110] %}

   string

*  {% colwidth=[148] %}

   Да

*  {% colwidth=[126] %}

   `week_days`, `month_days`, `cycle`

*  {% colwidth=[240] %}

   Тип расписания (По дням недели, По числам, По циклу)

---

*  {% colwidth=[159] isHeader=true %}

   virtual_number_ids

*  {% colwidth=[110] %}

   array of integers

*  {% colwidth=[148] %}

   Нет

*  {% colwidth=[126] %}

   \-

*  {% colwidth=[240] %}

   Идентификаторы виртуальных номеров.

---

*  {% colwidth=[159] isHeader=true %}

   virtual_number_group_ids

*  {% colwidth=[110] %}

   array of integers

*  {% colwidth=[148] %}

   Нет

*  {% colwidth=[126] %}

   \-

*  {% colwidth=[240] %}

   Идентификаторы групп виртуальных номеров.

---

*  {% colwidth=[159] isHeader=true %}

   production_holidays

*  {% colwidth=[110] %}

   array of strings

*  {% colwidth=[148] %}

   Нет

*  {% colwidth=[126] %}

   \-

*  {% colwidth=[240] %}

   Уникальные дни для графика: Нерабочие дни

---

*  {% colwidth=[159] isHeader=true %}

   production_workdays

*  {% colwidth=[110] %}

   array of strings

*  {% colwidth=[148] %}

   Нет

*  {% colwidth=[126] %}

   \-

*  {% colwidth=[240] %}

   Уникальные дни для графика: рабочие дни

---

*  {% colwidth=[159] isHeader=true %}

   week_end_schedule

*  {% colwidth=[110] %}

   array of strings или null

*  {% colwidth=[148] %}

   Нет (Обязательное, если параметр “`use_public_days_difference`” или “`is_use_days_difference_day_type`” стоит “`True`”)

*  {% colwidth=[126] %}

   Формат времени (HH:MM:SS)

*  {% colwidth=[240] %}

   Расписание на дополнительные рабочие дни согласно Производственному календарю или Уникальным рабочим дням.

---

*  {% colwidth=[159] isHeader=true %}

   week_days_schedule

*  {% colwidth=[110] %}

   array of arrays of strings

*  {% colwidth=[148] %}

   Да

*  {% colwidth=[126] %}

   Формат времени (HH:MM:SS)

*  {% colwidth=[240] %}

   Расписание на рабочие дни. Необходимо обязательно указывать время для всех дней недели. Если день считается выходным, то вместо времени следует указать значение «`null`».

---

*  {% colwidth=[159] isHeader=true %}

   use_public_days_difference

*  {% colwidth=[110] %}

   boolean

*  {% colwidth=[148] %}

   Да, только если в параметре “`type`” выбрано значение “`week_days`”

*  {% colwidth=[126] %}

   `true`, `false`

*  {% colwidth=[240] %}

   Учитывать производственный календарь.

---

*  {% colwidth=[159] isHeader=true %}

   is_use_days_difference_day_type

*  {% colwidth=[110] %}

   boolean

*  {% colwidth=[148] %}

   Да, только если в параметре “`type`” выбрано значение “`week_days`”

*  {% colwidth=[126] %}

   `true`, `false`

*  {% colwidth=[240] %}

   Установить уникальные дни для графика.

---

*  {% colwidth=[159] isHeader=true %}

   id

*  {% colwidth=[110] %}

   целое число

*  {% colwidth=[148] %}

   \-

*  {% colwidth=[126] %}

   Положительное число

*  {% colwidth=[240] %}

   Уникальный идентификатор графика активности.

{% /table %}

## **Структура запроса**

```json
PUT /calendar/scheduler/51

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
    "is_use_days_difference_day_type": true,
    "id": 51
}
```

## **Структура ответа**

```json
{
    "name": "тест",
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
    "id": 51
}
```