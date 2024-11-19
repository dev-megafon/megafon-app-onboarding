---
order: 0.8
title: Редактировать настройку правила ограничения звонков для всех сотрудников
---

### `PUT /limitations/main/{id}`

**Описание:**

## Параметры метода

{% table %}

---

*  {% colwidth=[139] isHeader=true %}

   **Название**

*  {% colwidth=[92] isHeader=true %}

   **Тип**

*  {% isHeader=true %}

   **Обязательный**

*  {% colwidth=[189] isHeader=true %}

   **Допустимые значения**

*  {% isHeader=true %}

   **Описание**

---

*  {% colwidth=[139] isHeader=true %}

   is_mobile_allowed

*  {% colwidth=[92] %}

   Boolean

*  да

*  {% colwidth=[189] %}

   true, false

*  Указывает, разрешены ли звонки на мобильные номера

---

*  {% colwidth=[139] isHeader=true %}

   is_country_allowed

*  {% colwidth=[92] %}

   Boolean

*  да

*  {% colwidth=[189] %}

   true, false

*  Указывает, разрешены ли междугородние звонки

---

*  {% colwidth=[139] isHeader=true %}

   is_international_allowed

*  {% colwidth=[92] %}

   Boolean

*  да

*  {% colwidth=[189] %}

   true, false

*  Указывает, разрешены ли международные звонки

---

*  {% colwidth=[139] isHeader=true %}

   country_ids

*  {% colwidth=[92] %}

   Array of Integers

*  да

*  {% colwidth=[189] %}

   Положительные целые числа или пустой массив(если в параметре “`is_international_allowed`” стоит значение `false`)

*  Список идентификаторов стран, в которые разрешены исходящие звонки .

---

*  {% colwidth=[139] isHeader=true %}

   is_satellite_allowed

*  {% colwidth=[92] %}

   Boolean

*  да

*  {% colwidth=[189] %}

   true, false

*  Указывает, разрешены ли спутниковые звонки.

---

*  {% colwidth=[139] isHeader=true %}

   is_local_allowed

*  {% colwidth=[92] %}

   Boolean

*  да

*  {% colwidth=[189] %}

   true(всегда разрешено для Общих настроек компании)

*  Указывает, разрешены ли звонки по городу.

---

*  {% colwidth=[139] isHeader=true %}

   is_internal_allowed

*  {% colwidth=[92] %}

   Boolean

*  да

*  {% colwidth=[189] %}

   true(всегда разрешено для Общих настроек компании)

*  Указывает, разрешены ли внутренние звонки.

---

*  {% colwidth=[139] isHeader=true %}

   id

*  {% colwidth=[92] %}

   Integer

*  

*  {% colwidth=[189] %}

   Положительное целое число

*  Уникальный идентификатор правила ограничения.

{% /table %}

## Структура запроса

`PUT /limitations/main/1`

```json
{
  "is_mobile_allowed": true,
  "is_country_allowed": true,
  "is_international_allowed": false,
  "country_ids": [
    20152,
    21824,
    21902
  ],
  "is_satellite_allowed": true,
  "is_local_allowed": true,
  "is_internal_allowed": true,
  "id": "1"
}
```

## Структура ответа

```json
{
    "is_mobile_allowed": true,
    "is_country_allowed": true,
    "is_international_allowed": false,
    "country_ids": [
        21824,
        20152,
        21902
    ],
    "is_satellite_allowed": true,
    "is_local_allowed": true,
    "is_internal_allowed": true,
    "id": 1
}
```