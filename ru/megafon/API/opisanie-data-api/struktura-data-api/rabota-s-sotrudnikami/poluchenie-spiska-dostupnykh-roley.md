---
order: 1
title: Получить список всех ролей
---

### `GET /role`

**Описание:** этот метод позволяет получить список всех ролей  в системе.

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% colwidth=[240] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   name

*  string

*  {% colwidth=[240] %}

   «Сотрудник», «Руководитель отдела», «Супервизор», «Администратор»

*  Название роли

---

*  {% isHeader=true %}

   id

*  integer

*  {% colwidth=[240] %}

   Целое число

*  Уникальный идентификатор роли

---

*  {% isHeader=true %}

   is_manager

*  boolean или null

*  {% colwidth=[240] %}

   true, false, null

*  Указывает, является ли роль менеджером

---

*  {% isHeader=true %}

   type

*  string

*  {% colwidth=[240] %}

   «`megafon_employee`», «`megafon_department_manager`», «`megafon_supervisor`», «`megafon_admin`»

*  Тип роли

---

*  {% isHeader=true %}

   api_permissions

*  array или null

*  {% colwidth=[240] %}

   Массив строк или null

*  Права доступа API, связанные с ролью

---

*  {% isHeader=true %}

   description

*  string или null

*  {% colwidth=[240] %}

   Текстовое описание или null

*  Описание роли

---

*  {% isHeader=true %}

   creation_date

*  string (ISO 8601)

*  {% colwidth=[240] %}

   Дата в формате ISO 8601

*  Дата создания роли

{% /table %}

## Cтруктура запроса

`GET /role`

## **Структура ответа**

```json

[
  {
    "name": "Сотрудник",
    "id": 196,
    "is_manager": null,
    "type": "megafon_employee",
    "api_permissions": null,
    "description": null,
    "creation_date": "2024-09-16T12:00:37+03:00"
  },
  {
    "name": "Руководитель отдела",
    "id": 198,
    "is_manager": null,
    "type": "megafondepartmentmanager",
    "api_permissions": null,
    "description": null,
    "creation_date": "2024-09-16T12:00:37+03:00"
  },
  {
    "name": "Супервизор",
    "id": 200,
    "is_manager": null,
    "type": "megafon_supervisor",
    "api_permissions": null,
    "description": null,
    "creation_date": "2024-09-16T12:00:37+03:00"
  },
  {
    "name": "Администратор",
    "id": 202,
    "is_manager": null,
    "type": "megafon_admin",
    "api_permissions": null,
    "description": null,
    "creation_date": "2024-09-16T12:00:37+03:00"
  }
]
```