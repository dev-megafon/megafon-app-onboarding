---
order: 0.5
title: "Получить настройки мелодии\_ “Для всей компании”"
---

### GET /melodies/main

**Описание:** метод позволяет получить настройки мелодии “Для всей компании”.

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   dialing_source_type

*  string

*  `beeps`, `client`, `system`

*  Тип источника мелодии.

---

*  {% isHeader=true %}

   dialing_media_id

*  integer

*  \-

*  Идентификатор медиа.

---

*  {% isHeader=true %}

   hold_source_type

*  string

*  `beeps`, `client`, `system`

*  Тип источника мелодии для удержания звонка.

---

*  {% isHeader=true %}

   hold_media_id

*  integer

*  \-

*  Идентификатор медиа для мелодии удержания звонка.

---

*  {% isHeader=true %}

   id

*  integer

*  \-

*  Уникальный идентификатор записи.

{% /table %}

## Структура запроса:

`GET /melodies/main`

## Структура ответа:

```json

[
    {
        "dialingsourcetype": "client",
        "dialingmediaid": 818,
        "holdsourcetype": "client",
        "holdmediaid": 804,
        "id": 1
    }
]
```