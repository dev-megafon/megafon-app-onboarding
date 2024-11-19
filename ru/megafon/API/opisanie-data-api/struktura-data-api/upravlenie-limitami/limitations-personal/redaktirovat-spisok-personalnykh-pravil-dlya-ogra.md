---
order: 3
title: Редактировать список персональных правил для ограничения звонков
---

### `PUT /limitations/personal/{id}`

## Параметры метода

{% table %}

---

*  {% colwidth=[109] isHeader=true %}

   **Название**

*  {% colwidth=[88] isHeader=true %}

   **Тип**

*  {% isHeader=true %}

   **Обязательные**

*  {% colwidth=[111] isHeader=true %}

   **Допустимые значения**

*  {% isHeader=true %}

   **Описание**

---

*  {% colwidth=[109] isHeader=true %}

   is_mobile_allowed

*  {% colwidth=[88] %}

   boolean

*  да

*  {% colwidth=[111] %}

   true, false

*  Указывает, разрешены ли звонки на мобильные номера

---

*  {% colwidth=[109] isHeader=true %}

   is_country_allowed

*  {% colwidth=[88] %}

   boolean

*  да

*  {% colwidth=[111] %}

   true, false

*  Указывает, разрешены ли междугородние звонки.

---

*  {% colwidth=[109] isHeader=true %}

   is_internation_alallowed

*  {% colwidth=[88] %}

   boolean

*  да

*  {% colwidth=[111] %}

   true, false

*  Указывает, разрешены ли международные звонки

---

*  {% colwidth=[109] isHeader=true %}

   country_ids

*  {% colwidth=[88] %}

   array of integers

*  да, если указан параметр “`is_internation_allowed`” как “`true`”

*  {% colwidth=[111] %}

   Положительные числа или пустой массив

*  Список идентификаторов стран, в которые разрешены исходящие звонки .

---

*  {% colwidth=[109] isHeader=true %}

   is_satellite_allowed

*  {% colwidth=[88] %}

   Boolean

*  да

*  {% colwidth=[111] %}

   true, false

*  Указывает, разрешены ли спутниковые звонки.

---

*  {% colwidth=[109] isHeader=true %}

   is_local_allowed

*  {% colwidth=[88] %}

   Boolean

*  да

*  {% colwidth=[111] %}

   true, false

*  Указывает, разрешены ли звонки по городу.

---

*  {% colwidth=[109] isHeader=true %}

   is_internal_allowed

*  {% colwidth=[88] %}

   Boolean

*  да

*  {% colwidth=[111] %}

   true(всегда разрешено для Персональных правил)

*  Указывает, разрешены ли внутренние звонки.

---

*  {% colwidth=[109] isHeader=true %}

   employee_ids

*  {% colwidth=[88] %}

   array of integers

*  да, обязательный один из двух параметров employee_ids или employee_group_ids и указывается только 1 из них

*  {% colwidth=[111] %}

   Положительные числа

*  Список идентификаторов сотрудников. Используется для указания конкретных сотрудников, к которым применяются ограничения звонков

---

*  {% colwidth=[109] isHeader=true %}

   employee_group_ids

*  {% colwidth=[88] %}

   array of integers

*  да, обязательный один из двух параметров `employee_ids `или `employee_group_ids `и указывается только 1 из них

*  {% colwidth=[111] %}

   Положительные числа

*  Список идентификаторов отдела сотрудников. Позволяет указать отдел, к которым применяются ограничения звонков

---

*  {% colwidth=[109] isHeader=true %}

   id

*  {% colwidth=[88] %}

   integer

*  да

*  {% colwidth=[111] %}

   Положительные числа

*  Уникальный идентификатор персонального правила ограничения звонков

{% /table %}

## Cтруктура запроса

`PUT /limitations/personal/63`

```json
{
  "is_mobile_allowed": true,
  "is_country_allowed": true,
  "is_international_allowed": true,
  "country_ids": [
    20152
  ],
  "is_satellite_allowed": false,
  "is_local_allowed": false,
  "is_internal_allowed": true,
  "employee_ids": null,
  "employee_group_ids": [
    79,
    83
  ],
  "id": 63
}
```

## Структура ответа

```json
{
    "is_mobile_allowed": true,
    "is_country_allowed": true,
    "is_international_allowed": true,
    "country_ids": [
        20152
    ],
    "is_satellite_allowed": false,
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