---
order: 2
title: Получить настройки графика активности по названию
---

### `GET /calendar/scheduler?name={name}`

**Описание:** этот метод выводит список всех доступных графиков активности по названию.

## Параметры метода

{% table %}

---

*  {% colwidth=[164] isHeader=true %}

   Название

*  {% colwidth=[110] isHeader=true %}

   Тип

*  {% colwidth=[126] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[164] isHeader=true %}

   name

*  {% colwidth=[110] %}

   string

*  {% colwidth=[126] %}

   \-

*  Название графика активности

---

*  {% colwidth=[164] isHeader=true %}

   type

*  {% colwidth=[110] %}

   string

*  {% colwidth=[126] %}

   `week_days`, `month_days`, `cycle`

*  Тип расписания (По дням недели, По числам, По циклу)

---

*  {% colwidth=[164] isHeader=true %}

   virtual_number_ids

*  {% colwidth=[110] %}

   array of integers

*  {% colwidth=[126] %}

   \-

*  Идентификаторы виртуальных номеров.

---

*  {% colwidth=[164] isHeader=true %}

   virtual_number_group_ids

*  {% colwidth=[110] %}

   array of integers

*  {% colwidth=[126] %}

   \-

*  Идентификаторы групп виртуальных номеров.

---

*  {% colwidth=[164] isHeader=true %}

   production_holidays

*  {% colwidth=[110] %}

   array of strings

*  {% colwidth=[126] %}

   \-

*  Уникальные дни для графика: Нерабочие дни

---

*  {% colwidth=[164] isHeader=true %}

   production_workdays

*  {% colwidth=[110] %}

   array of strings

*  {% colwidth=[126] %}

   \-

*  Уникальные дни для графика: рабочие дни

---

*  {% colwidth=[164] isHeader=true %}

   week_end_schedule

*  {% colwidth=[110] %}

   array of strings или null

*  {% colwidth=[126] %}

   Формат времени (HH:MM:SS)

*  Расписание на дополнительные рабочие дни согласно Производственному календарю или Уникальным рабочим дням.

---

*  {% colwidth=[164] isHeader=true %}

   week_days_schedule

*  {% colwidth=[110] %}

   array of arrays of strings

*  {% colwidth=[126] %}

   Формат времени (HH:MM:SS)

*  Расписание на рабочие дни.

---

*  {% colwidth=[164] isHeader=true %}

   use_public_days_difference

*  {% colwidth=[110] %}

   boolean

*  {% colwidth=[126] %}

   `true`, `false`

*  Учитывать производственный календарь.

---

*  {% colwidth=[164] isHeader=true %}

   is_use_days_difference_day_type

*  {% colwidth=[110] %}

   boolean

*  {% colwidth=[126] %}

   `true`, `false`

*  Установить уникальные дни для графика.

---

*  {% colwidth=[164] isHeader=true %}

   id

*  {% colwidth=[110] %}

   целое число

*  {% colwidth=[126] %}

   Положительное число

*  Уникальный идентификатор графика активности.

{% /table %}

## **Структура запроса**

```
GET /calendar/scheduler?name=тест
```

**Ответ**:

```json
[
    {
        "name": "3332",
        "type": "week_days",
        "virtual_number_ids": [
            258
        ],
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
        "use_public_days_difference": false,
        "is_use_days_difference_day_type": false,
        "id": 49
    },
    {
        "name": "по числам",
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
    },
```

#### 