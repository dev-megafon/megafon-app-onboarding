---
order: 4.3
title: Редактировать график активности по циклам
---

### `PUT /calendar/schedule/{id}`

**Описание:** редактирует данные графика активности по циклам.

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

*  {% colwidth=[240] isHeader=true %}

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

*  {% colwidth=[240] %}

   Название графика активности

---

*  {% colwidth=[164] isHeader=true %}

   type

*  {% colwidth=[110] %}

   string

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   `week_days`, `month_days`, `cycle`

*  {% colwidth=[240] %}

   Тип расписания (По дням недели, По числам, По циклу)

---

*  {% colwidth=[164] isHeader=true %}

   working_number_days

*  {% colwidth=[110] %}

   integer

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   Положительное число

*  {% colwidth=[240] %}

   Количество рабочих дней

---

*  {% colwidth=[164] isHeader=true %}

   holiday_number_days

*  {% colwidth=[110] %}

   integer

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   Положительное число

*  {% colwidth=[240] %}

   Количество нерабочих дней

---

*  {% colwidth=[164] isHeader=true %}

   start_date

*  {% colwidth=[110] %}

   string

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   Формат даты (YYYY-MM-DD)

*  {% colwidth=[240] %}

   Дата старта графика

---

*  {% colwidth=[164] isHeader=true %}

   working_schedule

*  {% colwidth=[110] %}

   array of strings

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   Формат времени (HH:MM:SS)

*  {% colwidth=[240] %}

   Расписание на рабочие дни.

---

*  {% colwidth=[164] isHeader=true %}

   id

*  {% colwidth=[110] %}

   целое число

*  {% colwidth=[146] %}

   Да

*  {% colwidth=[126] %}

   Положительное число

*  {% colwidth=[240] %}

   Уникальный идентификатор графика активности.

{% /table %}

## **Структура запроса**

```json
PUT /calendar/scheduler/251
{
    "name": "Название графика",
    "type": "cycle",
    "working_number_days": 5,
    "holiday_number_days": 3,
    "start_date": "2024-10-23",
    "working_schedule": [
        "07:00:00",
        "18:00:00"
    ],
   "id": 251
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
    "id": 251
}
```

## 