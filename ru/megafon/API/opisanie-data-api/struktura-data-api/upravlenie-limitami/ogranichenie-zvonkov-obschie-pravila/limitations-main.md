---
order: 0.5
title: Получить настройки правила ограничения звонков для всех сотрудников
---

### `GET /limitations/main`

**Описание**: этот метод позволяет получить основные настройки разрешений.

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   **Название**

*  {% isHeader=true %}

   **Тип**

*  {% isHeader=true %}

   **Допустимые значения**

*  {% isHeader=true %}

   **Описание**

---

*  {% isHeader=true %}

   is_mobile_allowed

*  Boolean

*  `true`, `false`

*  Указывает, разрешены ли звонки на мобильные номера

---

*  {% isHeader=true %}

   is_country_allowed

*  Boolean

*  `true`, `false`

*  Указывает, разрешены ли междугородние звонки

---

*  {% isHeader=true %}

   is_international_allowed

*  Boolean

*  `true`, `false`

*  Указывает, разрешены ли международные звонки

---

*  {% isHeader=true %}

   country_ids

*  Array of Integers

*  Положительные целые числа

*  Список идентификаторов стран, в которые разрешены исходящие звонки .

---

*  {% isHeader=true %}

   is_satellite_allowed

*  Boolean

*  `true`, `false`

*  Указывает, разрешены ли спутниковые звонки.

---

*  {% isHeader=true %}

   is_local_allowed

*  Boolean

*  `true`

*  Указывает, разрешены ли звонки по городу.

---

*  {% isHeader=true %}

   is_internal_allowed

*  Boolean

*  `true`

*  Указывает, разрешены ли внутренние звонки

---

*  {% isHeader=true %}

   id

*  Integer

*  Положительное целое число

*  Уникальный идентификатор правила ограничения.

{% /table %}

## Структура запроса

```
GET /limitations/main 
```

## **Структура ответа**

```json
[
    {
        "is_mobile_allowed": true,
        "is_country_allowed": true,
        "is_international_allowed": true,
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
]
```

### 