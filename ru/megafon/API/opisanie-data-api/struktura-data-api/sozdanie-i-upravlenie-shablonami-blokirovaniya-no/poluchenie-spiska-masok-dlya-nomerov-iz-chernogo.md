---
order: 0.5
title: Получить номера и маски из черного списка
---

### ` GET /black-nums/mask`

**Описание:**  метод позволяет получить текущий список номеров и масок из черного списка.

## Параметры метода

{% table %}

---

*  {% colwidth=[160] isHeader=true %}

   Название

*  {% colwidth=[157] isHeader=true %}

   Тип

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

*  {% isHeader=true %}

   

---

*  {% colwidth=[160] isHeader=true %}

   pattern

*  {% colwidth=[157] %}

   string

*  --

*  Номер/маска для блокировки звонков.

*  {% isHeader=true %}

   

---

*  {% colwidth=[160] isHeader=true %}

   comment

*  {% colwidth=[157] %}

   string

*  --

*  Комментарий к номеру/маске.

*  {% isHeader=true %}

   

---

*  {% colwidth=[160] isHeader=true %}

   id

*  {% colwidth=[157] %}

   integer

*  --

*  Уникальный идентификатор номера/маски из ЧС.

*  {% isHeader=true %}

   

---

*  {% colwidth=[160] isHeader=true %}

   upload_dt

*  {% colwidth=[157] %}

   string(\$date-time)

*  --

*  Дата и время добавления номера/маски в ЧС.

*  {% isHeader=true %}

   

---

*  {% colwidth=[160] isHeader=true %}

   last_7_days_count

*  {% colwidth=[157] %}

   integer

*  0 и выше

*  Количество заблокированных звонков с этого номера/маски за последние 7 дней.

*  {% isHeader=true %}

   

---

*  {% colwidth=[160] isHeader=true %}

   last_365_days_count

*  {% colwidth=[157] %}

   integer

*  0 и выше

*  Количество заблокированных звонков с этого номера/маски за последний год

*  

{% /table %}

## Cтруктура запроса

```
GET /black-nums/mask HTTP/1.1
Host: api.example.com
```

## **Структура ответа**

```json
[
    {
        "pattern": "7495805*",
        "comment": null,
        "id": 31,
        "upload_dt": "2024-09-16T12:50:29.018826+03:00",
        "last_7_days_count": 0,
        "last_365_days_count": 0
    },
    {
        "pattern": "79530500055",
        "comment": null,
        "id": 33,
        "upload_dt": "2024-09-16T12:50:33.904660+03:00",
        "last_7_days_count": 0,
        "last_365_days_count": 0
    },
    {
        "pattern": "79530500056",
        "comment": null,
        "id": 35,
        "upload_dt": "2024-09-16T12:50:33.904660+03:00",
        "last_7_days_count": 0,
        "last_365_days_count": 0
    },
    {
        "pattern": "79530500057",
        "comment": null,
        "id": 37,
        "upload_dt": "2024-09-16T12:50:33.904660+03:00",
        "last_7_days_count": 0,
        "last_365_days_count": 0
    },
    {
        "pattern": "79530500059",
        "comment": null,
        "id": 41,
        "upload_dt": "2024-09-16T12:50:33.904660+03:00",
        "last_7_days_count": 0,
        "last_365_days_count": 0
    },
    {
        "pattern": "79530500060",
        "comment": null,
        "id": 43,
        "upload_dt": "2024-09-16T12:50:33.904660+03:00",
        "last_7_days_count": 0,
        "last_365_days_count": 0
    },
    {
        "pattern": "79530500061",
        "comment": null,
        "id": 45,
        "upload_dt": "2024-09-16T12:50:33.904660+03:00",
        "last_7_days_count": 0,
        "last_365_days_count": 0
    },
    {
        "pattern": "79530500062",
        "comment": null,
        "id": 47,
        "upload_dt": "2024-09-16T12:50:33.904660+03:00",
        "last_7_days_count": 0,
        "last_365_days_count": 0
    },
    {
        "pattern": "749512345*",
        "comment": null,
        "id": 55,
        "upload_dt": "2024-10-09T09:54:21.566035+03:00",
        "last_7_days_count": 0,
        "last_365_days_count": 0
    }
]
```