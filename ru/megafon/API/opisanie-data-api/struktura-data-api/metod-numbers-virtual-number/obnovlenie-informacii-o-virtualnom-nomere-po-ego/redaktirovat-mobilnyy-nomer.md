---
order: 0.5
title: Редактировать мобильный номер
---

### `PUT /numbers/virtual-number/{id}`

**Описание:** Обновление информации о мобильном номере по его уникальному идентификатору.

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% colwidth=[176] isHeader=true %}

   Тип

*  {% colwidth=[140] isHeader=true %}

   Обязательный

*  {% colwidth=[171] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   comment

*  {% colwidth=[176] %}

   string

*  {% colwidth=[140] %}

   Нет

*  {% colwidth=[171] %}

   \-

*  Комментарий к номеру.

---

*  {% isHeader=true %}

   purpose

*  {% colwidth=[176] %}

   string

*  {% colwidth=[140] %}

   Да

*  {% colwidth=[171] %}

   `сompany`, `employee`, `not_specified`

*  Назначение Виртуального номера

---

*  {% isHeader=true %}

   id

*  {% colwidth=[176] %}

   integer

*  {% colwidth=[140] %}

   Да

*  {% colwidth=[171] %}

   Положительное число

*  Уникальный идентификатор виртуального номера.

---

*  {% isHeader=true %}

   employee_id

*  {% colwidth=[176] %}

   integer

*  {% colwidth=[140] %}

   Да, если в параметре `purpose` указано значение `employee`

*  {% colwidth=[171] %}

   Положительное число

*  Идентификатор сотрудника, на которого назначен номер.

{% /table %}

## Структура запроса

`PUT /numbers/virtual-number/542`

```json
{
  "comment": "Заметка",
  "purpose": "employee",
  "employee_id": 123,
  "id": 542
}
```

## **Структура ответа**

```json
{
  "comment": "Заметка",
  "purpose": "employee",
  "employee_id": 123,
  "id": 542
}
```