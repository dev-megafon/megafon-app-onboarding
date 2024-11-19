---
order: 0.8
title: Редактировать городской номер
---

### `PUT /numbers/virtual-number/{id}`

**Описание:** Обновление информации о городском номере по его уникальному идентификатору.

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% colwidth=[176] isHeader=true %}

   Тип

*  {% isHeader=true %}

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

*  Да

*  {% colwidth=[171] %}

   \-

*  Комментарий к номеру.

---

*  {% isHeader=true %}

   purpose

*  {% colwidth=[176] %}

   string

*  Да

*  {% colwidth=[171] %}

   `сompany`

*  Назначение Виртуального номера

---

*  {% isHeader=true %}

   id

*  {% colwidth=[176] %}

   integer

*  Да

*  {% colwidth=[171] %}

   Положительное число

*  Уникальный идентификатор виртуального номера.

{% /table %}

## Структура запроса

`PUT /numbers/virtual-number/569`

```json
{
  "comment": "компании22332",
  "purpose": "company",
  "id": 569
}
```

## **Структура ответа**

```json
{
  "comment": "компании22332",
  "purpose": "company",
  "id": 569
}
```