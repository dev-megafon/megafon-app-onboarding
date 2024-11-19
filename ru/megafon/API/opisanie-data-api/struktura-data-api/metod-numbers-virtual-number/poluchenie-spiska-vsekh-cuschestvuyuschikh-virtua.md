---
order: 1
title: Получить список всех виртуальных номеров
---

### `GET /numbers/virtual-number`

**Описание**: этот метод получает список всех имеющихся виртуальных номеров.

## **Параметры метода**

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% colwidth=[176] isHeader=true %}

   Тип

*  {% colwidth=[171] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   number

*  {% colwidth=[176] %}

   string

*  {% colwidth=[171] %}

   Любой номер телефона

*  Виртуальный номер телефона.

---

*  {% isHeader=true %}

   comment

*  {% colwidth=[176] %}

   string

*  {% colwidth=[171] %}

   \-

*  Комментарий к номеру.

---

*  {% isHeader=true %}

   type

*  {% colwidth=[176] %}

   string

*  {% colwidth=[171] %}

   `def`, `abc`, `sip_registration`, `sip_redirection`, `toll_free`

*  Тип виртуального номера.

---

*  {% isHeader=true %}

   purpose

*  {% colwidth=[176] %}

   string

*  {% colwidth=[171] %}

   `сompany`, `employee`, `not_specified`

*  Назначение Виртуального номера

---

*  {% isHeader=true %}

   scenario_id

*  {% colwidth=[176] %}

   integer

*  {% colwidth=[171] %}

   Положительное число

*  Идентификатор входящего сценария, который привязан к номеру

---

*  {% isHeader=true %}

   group_scenario_id

*  {% colwidth=[176] %}

   integer или null

*  {% colwidth=[171] %}

   \-

*  Идентификатор Входящего сценария у группы номеров

---

*  {% isHeader=true %}

   group_id

*  {% colwidth=[176] %}

   integer или null

*  {% colwidth=[171] %}

   \-

*  Идентификатор группы номеров для входящих сценариев.

---

*  {% isHeader=true %}

   is_scenario_active

*  {% colwidth=[176] %}

   boolean

*  {% colwidth=[171] %}

   `true`, `false`

*  Активен ли входящий сценарий.

---

*  {% isHeader=true %}

   is_group_scenario_active

*  {% colwidth=[176] %}

   boolean или null

*  {% colwidth=[171] %}

   `true`, `false`

*  Активен ли Входящий сценарий у группы номеров.

---

*  {% isHeader=true %}

   id

*  {% colwidth=[176] %}

   integer

*  {% colwidth=[171] %}

   Положительное число

*  Уникальный идентификатор виртуального номера.

---

*  {% isHeader=true %}

   state

*  {% colwidth=[176] %}

   string

*  {% colwidth=[171] %}

   `active`, `activation`, `debt_lock`, `unconfirmed`, `freeze`

*  Состояние виртуального номера.

---

*  {% isHeader=true %}

   reason

*  {% colwidth=[176] %}

   string или null

*  {% colwidth=[171] %}

   \-

*  Причина изменения состояния.

---

*  {% isHeader=true %}

   from_redirect_numbers

*  {% colwidth=[176] %}

   array of objects

*  {% colwidth=[171] %}

   \-

*  Список перенаправленных номеров.

---

*  {% isHeader=true %}

   employee_id

*  {% colwidth=[176] %}

   integer

*  {% colwidth=[171] %}

   Положительное число

*  Идентификатор сотрудника, на которого назначен номер.

---

*  {% isHeader=true %}

   dgn_number

*  {% colwidth=[176] %}

   string

*  {% colwidth=[171] %}

   Любой номер телефона

*  Номер для перенаправления.

---

*  {% isHeader=true %}

   region_name

*  {% colwidth=[176] %}

   string

*  {% colwidth=[171] %}

   \-

*  Название региона, к которому относится номер.

---

*  {% isHeader=true %}

   app_id

*  {% colwidth=[176] %}

   integer

*  {% colwidth=[171] %}

   Положительное число

*  Идентификатор Личного кабинета

---

*  {% isHeader=true %}

   sip_uri

*  {% colwidth=[176] %}

   string или null

*  {% colwidth=[171] %}

   \-

*  SIP URI для виртуального номера “Sip-переадресации”.

{% /table %}

## **Структура запроса**

```
GET /numbers/virtual-number
```

## **Структура ответа**

```json
[
    {
        "number": "79208547433",
        "comment": "ffff",
        "type": "def",
        "purpose": "company",
        "scenario_id": null,
        "group_scenario_id": null,
        "group_id": null,
        "is_scenario_active": null,
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
        "employee_id": null,
        "redirect_number": "74994088157",
        "region_name": "Брянская область",
        "app_id": 1200054,
        "nc_type": "custom",
        "sip_uri": null
    },
    {
        "number": "79267053890",
        "comment": null,
        "type": "def",
        "purpose": "company",
        "scenario_id": 561,
        "group_scenario_id": null,
        "group_id": null,
        "is_scenario_active": true,
        "is_group_scenario_active": null,
        "id": 256,
        "state": "active",
        "reason": null,
        "from_redirect_numbers": [
            {
                "id": 255,
                "number": "74954789551"
            }
        ],
        "employee_id": null,
        "dgn_number": "74954789551",
        "region_name": "регион Москва",
        "app_id": 1200054,
        "nc_type": "custom",
        "sip_uri": null
    },
```