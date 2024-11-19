---
order: 1
title: Получить все доступные настройки автоответчика
---

### ` GET /voice-mail`

**Описание:** этот метод позволяет получить все доступные настройки автоответчика.

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% colwidth=[243] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   employee_ids

*  array

*  {% colwidth=[243] %}

   Массив целых чисел (например, `1, 2, 3`)

*  Массив идентификаторов сотрудников

---

*  {% isHeader=true %}

   emails

*  array

*  {% colwidth=[243] %}

   Массив строк, соответствующих формату email (например, `example@mail.com`)

*  Массив дополнительных адресов электронной почты

---

*  {% isHeader=true %}

   employee_group_ids

*  array

*  {% colwidth=[243] %}

   Массив целых чисел (например, \[`10`, `20`\])

*  Массив идентификаторов отделов  сотрудников

---

*  {% isHeader=true %}

   id

*  integer

*  {% colwidth=[243] %}

   Целое число (например, `123`)

*  Уникальный идентификатор автоответчика компании

{% /table %}

## Структура запроса

```json
GET /voice-mail 
```

## Структура ответа

```json
[
    {
        "employee_ids": [
            125,
            129
        ],
        "emails": [
            "aaa@mail.ru",
            "aa33a@mail.ru"
        ],
        "employee_group_ids": [
            79,
            83,
            87
        ],
        "id": 51
    }
]
```

## 

## 