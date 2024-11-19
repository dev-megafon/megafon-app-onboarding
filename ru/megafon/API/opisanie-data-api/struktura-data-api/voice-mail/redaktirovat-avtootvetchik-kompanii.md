---
order: 2.3
title: Редактировать автоответчик компании
---

### `PUT /employee/{id}`

**Описание**: метод позволяет отредактировать настройку «Автоответчик компании».

## Параметры метода

{% table %}

---

*  {% colwidth=[108] isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% colwidth=[220] isHeader=true %}

   Обязательный

*  {% colwidth=[156] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[108] isHeader=true %}

   id

*  integer

*  {% colwidth=[220] %}

   Да

*  {% colwidth=[156] %}

   Целое число (например, 123)

*  Уникальный идентификатор Автоответчика компании

---

*  {% colwidth=[108] isHeader=true %}

   employee_ids

*  array

*  {% colwidth=[220] %}

   Нет(обязательно указывать хотя бы один из параметров `employee_ids`, `emails`, `employee_group_ids`)

*  {% colwidth=[156] %}

   Массив целых чисел (например, \[1, 2, 3\])

*  Массив идентификаторов сотрудников

---

*  {% colwidth=[108] isHeader=true %}

   emails

*  array

*  {% colwidth=[220] %}

   Нет

   (обязательно указывать хотя бы один из параметров `employee_ids`,`emails`,`employee_group_ids`)

*  {% colwidth=[156] %}

   Массив строк, соответствующих формату email (например, \[“[example@mail.com](mailto:example@mail.com)”\])

*  Массив дополнительных адресов электронной почты

---

*  {% colwidth=[108] isHeader=true %}

   employee_group_ids

*  array

*  {% colwidth=[220] %}

   Нет(обязательно указывать хотя бы один из параметров `employee_ids`, `emails`” `employee_group_ids`)

*  {% colwidth=[156] %}

   Массив целых чисел (например, \[10, 20\])

*  Массив идентификаторов отделов сотрудников

{% /table %}

## Структура запроса

\
`PUT https://simple-api.cp.megafon.ru/voice-mail/89`

```json
{
    "employee_ids": [
        253,
        259
    ],
    "emails": [
        "email1@megafom.ru",
        "email2@megafom.ru",
        "email3@megafom.ru"
    ],
    "employee_group_ids": [
        193,
        215
    ],
    "id": 89
}
```

## Структура ответа

```json
{
    "employee_ids": [
        253,
        259
    ],
    "emails": [
        "email1@megafom.ru",
        "email2@megafom.ru",
        "email3@megafom.ru"
    ],
    "employee_group_ids": [
        193,
        215
    ],
    "id": 89
}
```