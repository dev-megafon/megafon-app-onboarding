---
order: 2
title: "Включить/выключить настройку блокировки звонков с\_анонимных номеров"
---

### `PUT /black-nums/settings/{id}`

**Описание:** этот метод позволяет включить/выключить настройку блокировки звонков с анонимных номеров.

## Параметры метода

{% table %}

---

*  {% colwidth=[133] isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% colwidth=[110] isHeader=true %}

   Обязательный

*  {% colwidth=[145] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[133] isHeader=true %}

   is_block_anonymous_calls

*  boolean

*  {% colwidth=[110] %}

   Да

*  {% colwidth=[145] %}

   `true`, `false`

*  Указывает, блокируются ли звонки с анонимным АОНом.

---

*  {% colwidth=[133] isHeader=true %}

   id

*  integer

*  {% colwidth=[110] %}

   Да

*  {% colwidth=[145] %}

   любое неотрицательное целое число

*  Уникальный идентификатор для настройки.

{% /table %}

## **Структура запроса**

```json
PUT /black-nums/settings/1

{
    "is_block_anonymous_calls": true, 
    "id": 1
}
```

## **Структура ответа**

```json
{
    "is_block_anonymous_calls": true,
    "id": 1
}
```

### 