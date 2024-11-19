---
order: 1.5
title: "Получить состояние настройки блокировки звонков с\_анонимных номеров"
---

### `GET /black-nums/settings`

## Параметры метода

{% table %}

---

*  {% colwidth=[146] isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% colwidth=[174] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[146] isHeader=true %}

   is_block_anonymous_calls

*  boolean

*  {% colwidth=[174] %}

   `true`, `false`

*  Указывает, блокируются ли звонки с анонимным АОНом.

---

*  {% colwidth=[146] isHeader=true %}

   id

*  integer

*  {% colwidth=[174] %}

   любое неотрицательное целое число

*  Уникальный идентификатор для настройки.

{% /table %}

## Структура запроса

**Пример запроса:**

```
GET /black-nums/settings 
```

## **Структура ответа**

```json
[
    {
        "is_block_anonymous_calls": false,
        "id": 1
    }
]
```

### 