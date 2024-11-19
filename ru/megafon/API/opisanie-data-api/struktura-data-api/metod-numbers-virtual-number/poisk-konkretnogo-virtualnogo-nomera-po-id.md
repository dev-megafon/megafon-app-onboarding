---
order: 2
title: Поиск виртуального номера
---

### `GET /numbers/virtual-number/{id}`

**Описание**: этот метод позволяет найти виртуальный номер по его уникальному идентификатору.

## **Параметры метода**

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% colwidth=[131] isHeader=true %}

   Тип

*  {% colwidth=[158] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   number

*  {% colwidth=[131] %}

   string

*  {% colwidth=[158] %}

   Любой номер телефона

*  Виртуальный номер телефона.

---

*  {% isHeader=true %}

   comment

*  {% colwidth=[131] %}

   string

*  {% colwidth=[158] %}

   \-

*  Комментарий к номеру.

---

*  {% isHeader=true %}

   type

*  {% colwidth=[131] %}

   string

*  {% colwidth=[158] %}

   `def`, `abc`, `sip_registration`, `sip_redirection`, `toll_free`

*  Тип виртуального номера.

---

*  {% isHeader=true %}

   purpose

*  {% colwidth=[131] %}

   string

*  {% colwidth=[158] %}

   `сompany`, `employee`, `not_specified`

*  Назначение Виртуального номера

---

*  {% isHeader=true %}

   scenario_id

*  {% colwidth=[131] %}

   integer

*  {% colwidth=[158] %}

   Положительное число

*  Идентификатор входящего сценария, который привязан к номеру

---

*  {% isHeader=true %}

   group_scenario_id

*  {% colwidth=[131] %}

   integer или null

*  {% colwidth=[158] %}

   \-

*  Идентификатор Входящего сценария у группы номеров

---

*  {% isHeader=true %}

   group_id

*  {% colwidth=[131] %}

   integer или null

*  {% colwidth=[158] %}

   \-

*  Идентификатор группы номеров для входящих сценариев.

---

*  {% isHeader=true %}

   is_scenario_active

*  {% colwidth=[131] %}

   boolean

*  {% colwidth=[158] %}

   `true`, `false`

*  Активен ли входящий сценарий.

---

*  {% isHeader=true %}

   is_group_scenario_active

*  {% colwidth=[131] %}

   boolean или null

*  {% colwidth=[158] %}

   `true`, `false`

*  Активен ли Входящий сценарий у группы номеров.

---

*  {% isHeader=true %}

   id

*  {% colwidth=[131] %}

   integer

*  {% colwidth=[158] %}

   Положительное число

*  Уникальный идентификатор виртуального номера.

---

*  {% isHeader=true %}

   state

*  {% colwidth=[131] %}

   string

*  {% colwidth=[158] %}

   `active`, `activation`, `debt_lock`, `unconfirmed`, `freeze`

*  Состояние виртуального номера

---

*  {% isHeader=true %}

   reason

*  {% colwidth=[131] %}

   string или null

*  {% colwidth=[158] %}

   \-

*  Причина изменения состояния.

---

*  {% isHeader=true %}

   from_redirect_numbers

*  {% colwidth=[131] %}

   array of objects

*  {% colwidth=[158] %}

   \-

*  Список перенаправленных номеров.

---

*  {% isHeader=true %}

   employee_id

*  {% colwidth=[131] %}

   integer

*  {% colwidth=[158] %}

   Положительное число

*  Идентификатор сотрудника, на которого назначен номер.

---

*  {% isHeader=true %}

   dgn_number

*  {% colwidth=[131] %}

   string

*  {% colwidth=[158] %}

   Любой номер телефона

*  Номер для перенаправления.

---

*  {% isHeader=true %}

   region_name

*  {% colwidth=[131] %}

   string

*  {% colwidth=[158] %}

   \-

*  Название региона, к которому относится номер.

---

*  {% isHeader=true %}

   app_id

*  {% colwidth=[131] %}

   integer

*  {% colwidth=[158] %}

   Положительное число

*  Идентификатор Личного кабинета

---

*  {% isHeader=true %}

   sip_uri

*  {% colwidth=[131] %}

   string или null

*  {% colwidth=[158] %}

   \-

*  SIP URI для виртуального номера “Sip-переадресации”.

{% /table %}

## Структура запроса

`GET /numbers/virtual-number/250`

## Структура ответа

```json
{
    "number": "79208547433",
    "comment": "ffff",
    "type": "def",
    "purpose": "employee",
    "scenario_id": 723,
    "group_scenario_id": null,
    "group_id": null,
    "is_scenario_active": true,
    "is_group_scenario_active": null,
    "id": 250,
    "state": "active",
    "reason": null,
    "from_redirect_numbers": [
        {
            "id": 249,
            "number": "74994088157"
        }
    ],
    "employee_id": 125,
    "dgn_number": "74994088157",
    "region_name": "Брянская область",
    "app_id": 1200054,
    "nc_type": "custom+fmc",
    "sip_uri": null
}
``` «sip_uri»: null
}
```ll
}
```