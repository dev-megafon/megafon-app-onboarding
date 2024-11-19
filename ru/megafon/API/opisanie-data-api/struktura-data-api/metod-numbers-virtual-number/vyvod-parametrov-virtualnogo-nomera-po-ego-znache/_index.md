---
order: 3
title: Поиск виртуального номера по его параметрам
---

### `GET numbers/virtual-number?{параметр}={значение}`

**Описание:** этот метод выводит все параметры номера по его значению.

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% colwidth=[144] isHeader=true %}

   Тип

*  {% colwidth=[198] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   number

*  {% colwidth=[144] %}

   string

*  {% colwidth=[198] %}

   Любой номер телефона

*  Виртуальный номер телефона.

---

*  {% isHeader=true %}

   comment

*  {% colwidth=[144] %}

   string

*  {% colwidth=[198] %}

   \-

*  Комментарий к номеру.

---

*  {% isHeader=true %}

   type

*  {% colwidth=[144] %}

   string

*  {% colwidth=[198] %}

   `def`, `abc`, `sip_registration`, `sip_redirection`, `toll_free`

*  Тип виртуального номера.

---

*  {% isHeader=true %}

   purpose

*  {% colwidth=[144] %}

   string

*  {% colwidth=[198] %}

   `сompany`, `employee`, `not_specified`

*  Назначение Виртуального номера

---

*  {% isHeader=true %}

   scenario_id

*  {% colwidth=[144] %}

   integer

*  {% colwidth=[198] %}

   Положительное число

*  Идентификатор входящего сценария, который привязан к номеру

---

*  {% isHeader=true %}

   group_scenario_id

*  {% colwidth=[144] %}

   integer или null

*  {% colwidth=[198] %}

   \-

*  Идентификатор Входящего сценария у группы номеров

---

*  {% isHeader=true %}

   group_id

*  {% colwidth=[144] %}

   integer или null

*  {% colwidth=[198] %}

   \-

*  Идентификатор группы номеров для входящих сценариев.

---

*  {% isHeader=true %}

   is_scenario_active

*  {% colwidth=[144] %}

   boolean

*  {% colwidth=[198] %}

   `true`, `false`

*  Активен ли входящий сценарий.

---

*  {% isHeader=true %}

   is_group_scenario_active

*  {% colwidth=[144] %}

   boolean или null

*  {% colwidth=[198] %}

   `true`, `false`

*  Активен ли Входящий сценарий у группы номеров.

---

*  {% isHeader=true %}

   id

*  {% colwidth=[144] %}

   integer

*  {% colwidth=[198] %}

   Положительное число

*  Уникальный идентификатор виртуального номера.

---

*  {% isHeader=true %}

   state

*  {% colwidth=[144] %}

   string

*  {% colwidth=[198] %}

   `active`, `activation`, `debt_lock`, `unconfirmed`, `freeze`

*  Состояние виртуального номера

---

*  {% isHeader=true %}

   reason

*  {% colwidth=[144] %}

   string или null

*  {% colwidth=[198] %}

   \-

*  Причина изменения состояния.

---

*  {% isHeader=true %}

   from_redirect_numbers

*  {% colwidth=[144] %}

   array of objects

*  {% colwidth=[198] %}

   \-

*  Список перенаправленных номеров.

---

*  {% isHeader=true %}

   employee_id

*  {% colwidth=[144] %}

   integer

*  {% colwidth=[198] %}

   Положительное число

*  Идентификатор сотрудника, на которого назначен номер.

---

*  {% isHeader=true %}

   dgn_number

*  {% colwidth=[144] %}

   string

*  {% colwidth=[198] %}

   Любой номер телефона

*  Номер для перенаправления.

---

*  {% isHeader=true %}

   region_name

*  {% colwidth=[144] %}

   string

*  {% colwidth=[198] %}

   \-

*  Название региона, к которому относится номер.

---

*  {% isHeader=true %}

   app_id

*  {% colwidth=[144] %}

   integer

*  {% colwidth=[198] %}

   Положительное число

*  Идентификатор Личного кабинета

---

*  {% isHeader=true %}

   sip_uri

*  {% colwidth=[144] %}

   string или null

*  {% colwidth=[198] %}

   \-

*  SIP URI для виртуального номера “Sip-переадресации”.

{% /table %}

## **Структура запроса (Поиск по номеру виртуального телефона)**

`GET numbers/virtual-number?number=79267053890`

## **Структура ответа**

```json
[
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
    }
]
```

## **Структура запроса (Поиск по типу виртуального номера)**

`GET numbers/virtual-number?type=def`

## Структура ответа

```json
[
    {
        "number": "79208547433",
        "comment": "ffff",
        "type": "def",
        "purpose": "employee",
        "scenario_id": 779,
        "group_scenario_id": null,
        "group_id": null,
        "is_scenario_active": true,
        "is_group_scenario_active": null,
        "id": 250,
        "state": "active",
        "reason": null,
        "from_redirect_numbers": [
            {
                "id": 678,
                "number": "78009966666"
            },
            {
                "id": 249,
                "number": "74994088157"
            }
        ],
        "employee_id": 125,
        "dgn_number": "74994088157",
        "region_name": "Брянская область",
        "nc_type": "custom+fmc",
        "sip_uri": null,
        "dgn_number": null,
        "app_id": 1200054
    }
```

## **Структура запроса (Поиск номеров по назначению виртуального номера)**

`GET numbers/virtual-number?purpose=employee`

## Структура ответа

```json
{
        "number": "79260476605",
        "comment": "компании22332",
        "type": "def",
        "purpose": "employee",
        "scenario_id": 737,
        "group_scenario_id": null,
        "group_id": null,
        "is_scenario_active": true,
        "is_group_scenario_active": null,
        "id": 542,
        "state": "active",
        "reason": null,
        "from_redirect_numbers": [
            {
                "id": 543,
                "number": "74955011265"
            }
        ],
        "employee_id": 281,
        "dgn_number": "74955011265",
        "region_name": "регион Москва",
        "nc_type": "custom+fmc",
        "sip_uri": null,
        "dgn_number": null,
        "app_id": 1200054
    }
]
```