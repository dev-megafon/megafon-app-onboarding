---
order: 11
title: "Получить\_должность по уникальному идентификатору"
---

### `GET /position?id={id}`

**Описание:** этот метод позволяет получить информацию о конкретной должности по ее уникальному идентификатору.

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

   name

*  string

*  Произвольный текст

*  Название должности

---

*  {% isHeader=true %}

   id

*  integer

*  Целое число

*  Уникальный идентификатор должности

{% /table %}

## **Структура запроса**

`POST /position`

## **Структура ответа**

```json
{
    "name": "Аналитик",
    "id": 101
}
```