---
order: 3
title: Редактировать настройки персональных мелодий
---

### `PUT /melodies/personal/{id}`

**Описание**: Метод позволяет отредактировать персональную мелодию, которая будет звучать при дозвоне до отделов/виртуальных номеров

## Параметры метода

{% table %}

---

*  {% colwidth=[106] isHeader=true %}

   **Название**

*  {% isHeader=true %}

   **Тип**

*  {% isHeader=true %}

   **Обязательный**

*  {% colwidth=[118] isHeader=true %}

   **Допустимые значения**

*  {% isHeader=true %}

   **Описание**

---

*  {% colwidth=[106] isHeader=true %}

   number_capacity_ids

*  Array

*  Да, обязательный один из параметров `number_capacity_ids `или `employee_group_ids`

*  {% colwidth=[118] %}

   Целые числа

*  Список идентификаторов номеров, для которых применяется персональная мелодия.(**ЗАПРЕЩЕНО** добавлять правила на те ВН по которым уже есть правила)

---

*  {% colwidth=[106] isHeader=true %}

   employee_group_ids

*  Array

*  Да, обязательный один из параметров `number_capacity_ids` или `employee_group_ids`

*  {% colwidth=[118] %}

   Целые числа

*  Список идентификаторов отделов сотрудников, для которых применяется персональная мелодия.(**ЗАПРЕЩЕНО** добавлять правила на те Отделы по которым уже есть правила)

---

*  {% colwidth=[106] isHeader=true %}

   source_type

*  String

*  Да

*  {% colwidth=[118] %}

   client, system

*  Тип источника мелодии: клиентская или системная мелодия.

---

*  {% colwidth=[106] isHeader=true %}

   media_id

*  Integer

*  Да

*  {% colwidth=[118] %}

   Целое число

*  Идентификатор медиафайла для персональной мелодии.

---

*  {% colwidth=[106] isHeader=true %}

   id

*  Integer

*  Да

*  {% colwidth=[118] %}

   Целое число

*  Уникальный идентификатор настройки персональной мелодии.

{% /table %}

## Структура запроса

`PUT /melodies/personal/77`

```json
{
    "number_capacity_ids": [
        352,
        446,
        448
    ],
    "employee_group_ids": [
        93,
        103
    ],
    "source_type": "system",
    "media_id": 50,
    "id": 77
}
```

## Структура ответа

```json
{
    "number_capacity_ids": [
        352,
        446,
        448
    ],
    "employee_group_ids": [
        93,
        103
    ],
    "source_type": "system",
    "media_id": 50,
    "id": 77
}
```