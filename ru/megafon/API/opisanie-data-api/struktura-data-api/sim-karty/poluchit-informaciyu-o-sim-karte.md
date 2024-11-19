---
order: 0.4
title: Получить информацию о мобильном номере
---

### `GET /numbers/virtual-number/{id}`

**Описание**: этот метод позволяет получить информацию о мобильном номере.

## Параметры метода

{% table %}

---

*  {% colwidth=[142] isHeader=true %}

   Название

*  {% colwidth=[106] isHeader=true %}

   Тип

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[142] isHeader=true %}

   number

*  {% colwidth=[106] %}

   string

*  Любой номер телефона

*  Виртуальный номер телефона.

---

*  {% colwidth=[142] isHeader=true %}

   comment

*  {% colwidth=[106] %}

   string

*  \-

*  Комментарий к номеру.

---

*  {% colwidth=[142] isHeader=true %}

   type

*  {% colwidth=[106] %}

   string

*  `def`, `abc`, `sip_registration`, `sip_redirection`, `toll_free`

*  Тип виртуального номера.

---

*  {% colwidth=[142] isHeader=true %}

   purpose

*  {% colwidth=[106] %}

   string

*  `сompany`, `employee`, `not_specified`

*  Назначение Виртуального номера

---

*  {% colwidth=[142] isHeader=true %}

   scenario_id

*  {% colwidth=[106] %}

   integer

*  Положительное число

*  Идентификатор входящего сценария, который привязан к номеру

---

*  {% colwidth=[142] isHeader=true %}

   group_scenario_id

*  {% colwidth=[106] %}

   integer или null

*  \-

*  Идентификатор Входящего сценария у группы номеров

---

*  {% colwidth=[142] isHeader=true %}

   group_id

*  {% colwidth=[106] %}

   integer или null

*  \-

*  Идентификатор группы номеров для входящих сценариев.

---

*  {% colwidth=[142] isHeader=true %}

   is_scenario_active

*  {% colwidth=[106] %}

   boolean

*  `true`, `false`

*  Активен ли входящий сценарий.

---

*  {% colwidth=[142] isHeader=true %}

   is_group_scenario_active

*  {% colwidth=[106] %}

   boolean или null

*  `true`, `false`

*  Активен ли Входящий сценарий у группы номеров.

---

*  {% colwidth=[142] isHeader=true %}

   id

*  {% colwidth=[106] %}

   integer

*  Положительное число

*  Уникальный идентификатор виртуального номера.

---

*  {% colwidth=[142] isHeader=true %}

   state

*  {% colwidth=[106] %}

   string

*  `active`, `inactive`

*  Активен ли входящий сценарий у группы номеров.

---

*  {% colwidth=[142] isHeader=true %}

   reason

*  {% colwidth=[106] %}

   string или null

*  \-

*  Причина изменения состояния.

---

*  {% colwidth=[142] isHeader=true %}

   from_redirect_numbers

*  {% colwidth=[106] %}

   array of objects

*  \-

*  Список перенаправленных номеров.

---

*  {% colwidth=[142] isHeader=true %}

   employee_id

*  {% colwidth=[106] %}

   integer

*  Положительное число

*  Идентификатор сотрудника, на которого назначен номер.

---

*  {% colwidth=[142] isHeader=true %}

   redirect_number

*  {% colwidth=[106] %}

   string

*  Любой номер телефона

*  Номер для перенаправления.

---

*  {% colwidth=[142] isHeader=true %}

   **dgn_number**

*  {% colwidth=[106] isHeader=true %}

   **string**

*  {% isHeader=true %}

   Любой номер телефона

*  {% isHeader=true %}

   Дополнительный городской номер

---

*  {% colwidth=[142] isHeader=true %}

   region_name

*  {% colwidth=[106] %}

   string

*  \-

*  Название региона, к которому относится номер.

---

*  {% colwidth=[142] isHeader=true %}

   app_id

*  {% colwidth=[106] %}

   integer

*  Положительное число

*  Идентификатор Личного кабинета

---

*  {% colwidth=[142] isHeader=true %}

   sip_uri

*  {% colwidth=[106] %}

   string или null

*  \-

*  SIP URI для виртуального номера “Sip-переадресации”.

{% /table %}

## Структура запроса

`GET /numbers/virtual-number/123`

## Структура ответа

```json
{
    "number": "79201234567",
    "comment": "Заметка",
    "type": "def",
    "purpose": "employee",
    "scenario_id": 779,
    "group_scenario_id": null,
    "group_id": null,
    "is_scenario_active": true,
    "is_group_scenario_active": null,
    "id": 123,
    "state": "active",
    "reason": null,
    "from_redirect_numbers": [
        {
            "id": 678,
            "number": "78001234567"
        },
        {
            "id": 249,
            "number": "74991234567"
        }
    ],
    "employee_id": 125,
    "dgn_number": "74991234567",
    "region_name": "Московская область",
    "nc_type": "custom+fmc",
    "sip_uri": null,
    "redirect_number": null,
    "app_id": 1200054
}
```