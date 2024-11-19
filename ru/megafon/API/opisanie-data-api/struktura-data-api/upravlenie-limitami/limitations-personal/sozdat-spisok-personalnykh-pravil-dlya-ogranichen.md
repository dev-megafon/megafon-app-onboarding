---
order: 2
title: Создать список персональных правил для ограничения звонков
---

### `POST /limitations/personal`

**Описание**: метод помогает создать персональное правило сотрудников или отделов для ограничения звонков

## Параметры метода

{% table %}

---

*  {% colwidth=[119] isHeader=true %}

   **Название**

*  {% isHeader=true %}

   **Тип**

*  {% colwidth=[164] isHeader=true %}

   **Обязательные**

*  {% colwidth=[148] isHeader=true %}

   **Допустимые значения**

*  {% isHeader=true %}

   **Описание**

---

*  {% colwidth=[119] isHeader=true %}

   is_mobile_allowed

*  boolean

*  {% colwidth=[164] %}

   да

*  {% colwidth=[148] %}

   true, false

*  Указывает, разрешены ли звонки на мобильные номера

---

*  {% colwidth=[119] isHeader=true %}

   is_country_allowed

*  boolean

*  {% colwidth=[164] %}

   да

*  {% colwidth=[148] %}

   true, false

*  Указывает, разрешены ли междугородние звонки

---

*  {% colwidth=[119] isHeader=true %}

   is_internation_alallowed

*  boolean

*  {% colwidth=[164] %}

   да

*  {% colwidth=[148] %}

   true, false

*  Указывает, разрешены ли международные звонки

---

*  {% colwidth=[119] isHeader=true %}

   country_ids

*  array of integers

*  {% colwidth=[164] %}

   да, если указан параметр “`is_internation_allowed`” как “`true`”

*  {% colwidth=[148] %}

   Положительные числа или пустой массив

*  Список идентификаторов стран, в которые разрешены исходящие звонки .

---

*  {% colwidth=[119] isHeader=true %}

   is_satellite_allowed

*  Boolean

*  {% colwidth=[164] %}

   да

*  {% colwidth=[148] %}

   true, false

*  Указывает, разрешены ли спутниковые звонки.

---

*  {% colwidth=[119] isHeader=true %}

   is_local_allowed

*  Boolean

*  {% colwidth=[164] %}

   да

*  {% colwidth=[148] %}

   true, false

*  Указывает, разрешены ли Звонки по городу.

---

*  {% colwidth=[119] isHeader=true %}

   is_internal_allowed

*  Boolean

*  {% colwidth=[164] %}

   да

*  {% colwidth=[148] %}

   `true`(всегда разрешено для Персональных правил)

*  Указывает, разрешены ли внутренние звонки.

---

*  {% colwidth=[119] isHeader=true %}

   employee_ids

*  array of integers

*  {% colwidth=[164] %}

   да, обязательный один из двух параметров `employee_ids `или `employee_group_ids `и указывается только 1 из них

*  {% colwidth=[148] %}

   Положительные числа

*  Список идентификаторов сотрудников. Используется для указания конкретных сотрудников, к которым применяются ограничения звонков

---

*  {% colwidth=[119] isHeader=true %}

   employee_group_ids

*  array of integers

*  {% colwidth=[164] %}

   да, обязательный один из двух параметров `employee_ids `или `employee_group_ids `и указывается только 1 из них

*  {% colwidth=[148] %}

   Положительные числа

*  Список идентификаторов отдела сотрудников. Позволяет указать отдел, к которым применяются ограничения звонков

{% /table %}

## Структура запроса:

`POST /limitations/personal`

```json
{
  "is_mobile_allowed": true,
  "is_country_allowed": true,
  "is_international_allowed": true,
  "country_ids": [
    20152
  ],
  "is_satellite_allowed": true,
  "is_local_allowed": false,
  "is_internal_allowed": true,
  "employee_ids": null,
  "employee_group_ids": [
    79,
    83
  ]
}
```

## Структура ответа:

```json
{
    "is_mobile_allowed": true,
    "is_country_allowed": true,
    "is_international_allowed": true,
    "country_ids": [
        20152
    ],
    "is_satellite_allowed": true,
    "is_local_allowed": false,
    "is_internal_allowed": true,
    "employee_ids": [],
    "employee_group_ids": [
        79,
        83
    ],
    "id": 63
}
```