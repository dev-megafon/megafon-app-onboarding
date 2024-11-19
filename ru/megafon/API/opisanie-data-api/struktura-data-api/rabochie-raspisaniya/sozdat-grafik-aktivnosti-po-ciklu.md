---
order: 3.3
title: Создать график активности по циклу
---

### `POST /calendar/scheduler`

**Описание:** этот метод  создает график активности по циклу

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

   working_number_days

*  {% colwidth=[110] %}

   integer

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   Положительное число

*  Количество рабочих дней

---

*  {% colwidth=[164] isHeader=true %}

   holiday_number_days

*  {% colwidth=[110] %}

   integer

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   Положительное число

*  Количество нерабочих дней

---

*  {% colwidth=[164] isHeader=true %}

   start_date

*  {% colwidth=[110] %}

   string

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   Формат даты (YYYY-MM-DD)

*  Дата старта графика

---

*  {% colwidth=[164] isHeader=true %}

   working_schedule 

*  {% colwidth=[110] %}

   array of strings

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   Формат времени (HH:MM:SS)

*  

   Расписание на рабочие дни.

{% /table %}

## **Структура запроса**

```json
POST /calendar/scheduler/
{
    "name": "Название графика",
    "type": "cycle",
    "working_number_days": 5,
    "holiday_number_days": 3,
    "start_date": "2024-10-23",
    "working_schedule": [
        "07:00:00",
        "18:00:00"
    ]
}
```

## **Структура ответа**

```json
{
    "name": "Название графика",
    "type": "cycle",
    "virtual_number_ids": [],
    "virtual_number_group_ids": [],
    "working_number_days": 5,
    "holiday_number_days": 3,
    "start_date": "2024-10-23",
    "working_schedule": [
        "07:00:00",
        "18:00:00"
    ],
    "id": 227
}
```

## 