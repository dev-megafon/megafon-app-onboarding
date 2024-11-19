---
order: 0.8
title: Редактирование настроек мелодии “Для всей компании”
---

### `PUT /melodies/main/{id}`

**Описание:** метод позволяет отредактировать настройки мелодии для всей компании.

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% isHeader=true %}

   Обязательный

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   dialing_source_type

*  string

*  Да

*  `beeps`, `client`, `system`

*  Тип источника мелодии.

---

*  {% isHeader=true %}

   dialing_media_id

*  integer

*  Да

*  \-

*  Идентификатор медиа.

---

*  {% isHeader=true %}

   hold_source_type

*  string

*  Да

*  `beeps`, `client`, `system`

*  Тип источника мелодии для удержания звонка.

---

*  {% isHeader=true %}

   hold_media_id

*  integer

*  Да

*  \-

*  Идентификатор медиа для мелодии удержания звонка.

---

*  {% isHeader=true %}

   id

*  integer

*  Да

*  \-

*  Уникальный идентификатор записи.

{% /table %}

## Структура запроса:

`PUT /melodies/main/1`

## Структура ответа:

```json

{
    "dialingsourcetype": "client",
    "dialingmediaid": 818,
    "holdsourcetype": "system",
    "holdmediaid": 53,
    "id": 1
}
```