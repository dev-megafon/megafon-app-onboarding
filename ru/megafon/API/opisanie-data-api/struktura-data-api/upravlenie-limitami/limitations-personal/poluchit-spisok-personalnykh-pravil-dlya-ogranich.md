---
order: 1
title: Получить список персональных правил для ограничения звонков
---

### `GET /limitations/personal`

**Описание**: метод помогает получить настройки персональных правил для сотрудников/отделов.

## Параметры метода

{% table %}

---

*  {% colwidth=[201] isHeader=true %}

   **Название**

*  {% isHeader=true %}

   **Тип**

*  {% colwidth=[151] isHeader=true %}

   **Допустимые значения**

*  {% isHeader=true %}

   **Описание**

---

*  {% colwidth=[201] isHeader=true %}

   is_mobile_allowed

*  boolean

*  {% colwidth=[151] %}

   true, false

*  Указывает, разрешены ли звонки на Мобильные номера.

---

*  {% colwidth=[201] isHeader=true %}

   is_country_allowed

*  boolean

*  {% colwidth=[151] %}

   true, false

*  Указывает, разрешены ли междугородние звонки.

---

*  {% colwidth=[201] isHeader=true %}

   is_internation_alallowed

*  boolean

*  {% colwidth=[151] %}

   true, false

*  Указывает, разрешены ли международные звонки

---

*  {% colwidth=[201] isHeader=true %}

   country_ids

*  array of integers

*  {% colwidth=[151] %}

   Положительные числа

*  Список идентификаторов стран, в которые разрешены исходящие звонки .

---

*  {% colwidth=[201] isHeader=true %}

   is_satellite_allowed

*  Boolean

*  {% colwidth=[151] %}

   true, false

*  Указывает, разрешены ли спутниковые звонки.

---

*  {% colwidth=[201] isHeader=true %}

   is_local_allowed

*  Boolean

*  {% colwidth=[151] %}

   true, false

*  Указывает, разрешены ли звонки по городу.

---

*  {% colwidth=[201] isHeader=true %}

   is_internal_allowed

*  Boolean

*  {% colwidth=[151] %}

   true(всегда разрешено для Общих настроек компании)

*  Указывает, разрешены ли внутренние звонки.

---

*  {% colwidth=[201] isHeader=true %}

   employee_ids

*  array of integers

*  {% colwidth=[151] %}

   Положительные числа

*  Список идентификаторов сотрудников. Используется для указания конкретных сотрудников, к которым применяются ограничения звонков

---

*  {% colwidth=[201] isHeader=true %}

   employee_group_ids

*  array of integers

*  {% colwidth=[151] %}

   Положительные числа

*  Список идентификаторов отдела сотрудников. Позволяет указать отдел, к которым применяются ограничения звонков

---

*  {% colwidth=[201] isHeader=true %}

   id

*  integer

*  {% colwidth=[151] %}

   Положительные числа

*  Уникальный идентификатор персонального правила ограничения звонков

{% /table %}

## Пример запроса:

`GET /limitations/personal`

## Пример ответа:

```json
[
    {
        "is_mobile_allowed": true,
        "is_country_allowed": true,
        "is_international_allowed": true,
        "country_ids": [
            1,
            21961
        ],
        "is_satellite_allowed": true,
        "is_local_allowed": false,
        "is_internal_allowed": true,
        "employee_ids": [],
        "employee_group_ids": [
            79
        ],
        "id": 52
    }
]
```