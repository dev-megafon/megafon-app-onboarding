---
order: 0.7
title: Добавить мобильный номер
---

### `POST numbers/unconfirmed `

**Описание**: этот метод позволяет добавить мобильный номер.

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% isHeader=true %}

   Обязательный

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   number

*  string

*  Да

*  \-

*  Виртуального номера

---

*  {% isHeader=true %}

   dgn_number

*  string

*  Да

*  \-

*  ДГН виртуального номера

---

*  {% isHeader=true %}

   purpose

*  string

*  Да

*  `company`, `not_specified`

*  Назначение Виртуального номера

---

*  {% isHeader=true %}

   comment

*  string

*  Нет

*  \-

*  Заметка виртуального номера

---

*  {% isHeader=true %}

   type

*  string

*  Да

*  Строго только “`def`”

*  Тип Виртуального номера

{% /table %}

## Структура запроса

```json
POST numbers/unconfirmed 
{
  "number": "79268622332",
  "dgn_number": "74958042300",
  "purpose": "not_specified",
  "comment": "ЗаметкаАПИ",
  "type": "def"
}
```

## Структура ответа

## **Параметры метода**

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% colwidth=[176] isHeader=true %}

   Тип

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

*  {% isHeader=true %}

   

---

*  {% isHeader=true %}

   number

*  {% colwidth=[176] %}

   string

*  Любой номер телефона

*  Виртуальный номер телефона.

*  

---

*  {% isHeader=true %}

   comment

*  {% colwidth=[176] %}

   string

*  \-

*  Комментарий к номеру.

*  

---

*  {% isHeader=true %}

   type

*  {% colwidth=[176] %}

   string

*  `def`, `abc`, `sip_registration`, `sip_redirection`, `toll_free`

*  Тип виртуального номера.

*  

---

*  {% isHeader=true %}

   purpose

*  {% colwidth=[176] %}

   string

*  `сompany`, `employee`, `not_specified`

*  Назначение Виртуального номера

*  

---

*  {% isHeader=true %}

   scenario_id

*  {% colwidth=[176] %}

   integer

*  Положительное число

*  Идентификатор входящего сценария, который привязан к номеру

*  

---

*  {% isHeader=true %}

   group_scenario_id

*  {% colwidth=[176] %}

   integer или null

*  \-

*  Идентификатор Входящего сценария у группы номеров

*  

---

*  {% isHeader=true %}

   group_id

*  {% colwidth=[176] %}

   integer или null

*  \-

*  Идентификатор группы номеров для входящих сценариев.

*  

---

*  {% isHeader=true %}

   is_scenario_active

*  {% colwidth=[176] %}

   boolean

*  `true`, `false`

*  Активен ли входящий сценарий.

*  

---

*  {% isHeader=true %}

   is_group_scenario_active

*  {% colwidth=[176] %}

   boolean или null

*  `true`, `false`

*  Активен ли Входящий сценарий у группы номеров.

*  

---

*  {% isHeader=true %}

   id

*  {% colwidth=[176] %}

   integer

*  Положительное число

*  Уникальный идентификатор виртуального номера.

*  

---

*  {% isHeader=true %}

   state

*  {% colwidth=[176] %}

   string

*  `active`, `inactive`

*  Активен ли входящий сценарий у группы номеров.

*  

---

*  {% isHeader=true %}

   reason

*  {% colwidth=[176] %}

   string или null

*  \-

*  Причина изменения состояния.

*  

---

*  {% isHeader=true %}

   from_redirect_numbers

*  {% colwidth=[176] %}

   array of objects

*  \-

*  Список перенаправленных номеров.

*  

---

*  {% isHeader=true %}

   employee_id

*  {% colwidth=[176] %}

   integer

*  Положительное число

*  Идентификатор сотрудника, на которого назначен номер.

*  

---

*  {% isHeader=true %}

   redirect_number

*  {% colwidth=[176] %}

   string

*  Любой номер телефона

*  Номер для перенаправления.

*  

---

*  {% isHeader=true %}

   dgn_number

*  {% colwidth=[176] %}

   string

*  Да

*  \-

*  ДГН виртуального номера

---

*  {% isHeader=true %}

   region_name

*  {% colwidth=[176] %}

   string

*  \-

*  Название региона, к которому относится номер.

*  

---

*  {% isHeader=true %}

   app_id

*  {% colwidth=[176] %}

   integer

*  Положительное число

*  Идентификатор Личного кабинета

*  

---

*  {% isHeader=true %}

   sip_uri

*  {% colwidth=[176] %}

   string или null

*  \-

*  SIP URI для виртуального номера “Sip-переадресации”.

*  

{% /table %}

```json
{
    "number": "79261234567",
    "comment": "ЗаметкаАПИ",
    "type": "def",
    "purpose": "not_specified",
    "scenario_id": null,
    "group_scenario_id": null,
    "group_id": null,
    "is_scenario_active": null,
    "is_group_scenario_active": null,
    "id": 331,
    "state": "activation",
    "reason": null,
    "from_redirect_numbers": null,
    "employee_id": null,
    "dgn_number": "74951234567",
    "region_name": "регион Москва"
}
```