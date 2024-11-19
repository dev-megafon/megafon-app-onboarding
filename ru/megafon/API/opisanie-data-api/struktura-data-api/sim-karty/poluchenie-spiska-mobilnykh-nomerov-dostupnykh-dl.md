---
order: 0.6
title: >-
  Получить список мобильных номеров доступных для подключения со своего лицевого
  счёта
---

### `GET numbers/def-virtual-number-capacity`

**Описание:** Этот метод позволяет найти номера, которые можно подключить к своему лицевому счёту в  Личном кабинете.

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

   id

*  string

*  \-

*  Уникальный идентификатор виртуального номера

---

*  {% isHeader=true %}

   number

*  string

*  \-

*  Виртуальный номер

---

*  {% isHeader=true %}

   dgn_number

*  string

*  \-

*  Номер ДГН, привязанный к виртуальному номеру

---

*  {% isHeader=true %}

   state

*  string

*  `active`, `activation`, `debt_lock`, `unconfirmed`, `freeze`, `error`

*  Текущее состояние виртуального номера

{% /table %}

## Структура запроса

`GET numbers/def-virtual-number-capacity`

## Структура ответа

```json
[
    {
        "id": "79261234567",
        "number": "79261234567",
        "dgn_number": "74951234567",
        "state": "freeze"
    },
    {
        "id": "79267654321",
        "number": "79267654321",
        "dgn_number": "",
        "state": "freeze"
    }
]
```