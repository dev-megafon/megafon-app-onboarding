---
order: 9
title: Получить роль
---

### `GET /role/{id}`

**Описание**: этот метод позволяет получить параметры конкретной роли по её ID.

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

*  Текстовое описание

*  Название роли

---

*  {% isHeader=true %}

   id

*  integer

*  Целое число

*  Уникальный идентификатор роли

---

*  {% isHeader=true %}

   is_manager

*  boolean/null

*  true, false, null

*  Указывает, является ли роль менеджером

---

*  {% isHeader=true %}

   type

*  string

*  «`megafon_employee`», «`megafon_department_manager`», «`megafon_supervisor`», «`megafon_admin`»

*  Тип роли

---

*  {% isHeader=true %}

   api_permissions

*  array/null

*  Массив строк или null

*  Права доступа API, связанные с ролью

---

*  {% isHeader=true %}

   description

*  string/null

*  Текстовое описание или null

*  Описание роли

---

*  {% isHeader=true %}

   creation_date

*  string (ISO 8601)

*  Дата в формате ISO 8601

*  Дата создания роли

{% /table %}

## Cтруктура запроса

`GET /role/267`

## Cтруктура ответа

```json
  "name": "Сотрудник",
    "id": 267,
    "type": "megafon_employee",
    "api_permissions": null,
    "creation_date": "2024-09-16T10:15:57+03:00",
    "description": null
```