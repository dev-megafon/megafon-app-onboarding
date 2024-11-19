---
order: 1
title: Добавить/редактировать перерыв в уже созданном сценарии.
---

### `PUT scenario/inbound/virtual-number/{id}`

**Описание:** данный метод помогает отредактировать уже созданный сценарий и добавить/отредактировать в нем перерывы, параметр “breaks”.

## Параметры метода:

{% table %}

---

*  {% colwidth=[131] isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% colwidth=[158] isHeader=true %}

   Обязательный

*  {% colwidth=[147] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[131] isHeader=true %}

   scenario_type

*  String

*  {% colwidth=[158] %}

   Да

*  {% colwidth=[147] %}

   “informer”, “duty_informer”, “duty”

*  Тип перерыва(Автоответчик, Сообщение о нерабочем времени, Дежурный)

---

*  {% colwidth=[131] isHeader=true %}

   name

*  String

*  {% colwidth=[158] %}

   да

*  {% colwidth=[147] %}

   

*  Название перерыва(не должны повторяться в рамках сценария)

---

*  {% colwidth=[131] isHeader=true %}

   start

*  string

*  {% colwidth=[158] %}

   Да

*  {% colwidth=[147] %}

   Формат времени (HH:MM)

*  Время начала перерыва

---

*  {% colwidth=[131] isHeader=true %}

   stop

*  string

*  {% colwidth=[158] %}

   Да

*  {% colwidth=[147] %}

   Формат времени (HH:MM)

*  Время начала перерыва

---

*  {% colwidth=[131] isHeader=true %}

   media_type

*  string

*  {% colwidth=[158] %}

   Да, если в параметре “scenario_type” выбраны значения “informer”, “duty_informer” и в параметре “duty” включен параметр “is_welcome_enabled: true”

*  {% colwidth=[147] %}

   \[ system, client, text \]

*  Голосовое сообщение абоненту или приветствие перед звонком дежурного.

---

*  {% colwidth=[131] isHeader=true %}

   is_welcome_enabled

*  boolean

*  {% colwidth=[158] %}

   Нет

*  {% colwidth=[147] %}

   

*  Приветствие для абонента перед звонком дежурного(можно указать только есть параметр `scenario_type` имеет значение “`duty`”)

---

*  {% colwidth=[131] isHeader=true %}

   media_file_id

*  integer

*  {% colwidth=[158] %}

   Да, если в параметре media_type выбрано значение client

*  {% colwidth=[147] %}

   

*  Идентификатор медиафайла.

---

*  {% colwidth=[131] isHeader=true %}

   “text”

*  string

*  {% colwidth=[158] %}

   Да, если в параметре media_type выбрано значение client

*  {% colwidth=[147] %}

   text

*  Текст сообщения которое будет проиграно Абоненту

---

*  {% colwidth=[131] isHeader=true %}

   employee_group_id

*  integer

*  {% colwidth=[158] %}

   При выборе значения “duty” в параметре “scenario_type” нужно указать обязательно один из трех параметров \[employee_group_id, employee_id, external_numb \]

*  {% colwidth=[147] %}

   

*  Идентификатор отдела сотрудников

---

*  {% colwidth=[131] isHeader=true %}

   employee_id

*  integer

*  {% colwidth=[158] %}

   При выборе значения “duty” в параметре “scenario_type” нужно указать обязательно один из трех параметров \[employee_group_id, employee_id, external_numb \]

*  {% colwidth=[147] %}

   

*  Идентификатор сотрудника

---

*  {% colwidth=[131] isHeader=true %}

   external_numb

*  string

*  {% colwidth=[158] %}

   При выборе значения “duty” в параметре “scenario_type” нужно указать обязательно один из трех параметров \[employee_group_id, employee_id, external_numb \]

*  {% colwidth=[147] %}

   

*  Внешний номер

{% /table %}

## Структура запроса

`PUT scenario/inbound/virtual-number/693`

```json
{
    "working_shift1": {
        "scenario_type": "redirect_to_employee_group",
        "employee_group_id": 183,
        "is_welcome_enabled": false,
        "scheduler_id": 67,
        "breaks": [
            {
                "scenario_type": "informer",
                "media_type": "system",
                "name": "Перерыв1111",
                "start": "11:11",
                "stop": "11:21"
            },
            {
                 "scenario_type": "informer",
                "media_type": "client",
                "media_file_id":27,
                "name": "Перерыв222",
                "start": "12:22",
                "stop": "12:23"
            },
                        {
                "scenario_type": "duty_informer",
                "name": "Перерыв333",
                "media_type": "system",
                "start": "13:33",
                "stop": "13:34"
            },
            {
                "scenario_type": "duty",
                "employee_id": 253,
                "is_welcome_enabled": false,
                "name": "Перерыв555",
                "start": "15:44",
                "stop": "15:45"
            },
            {
                "scenario_type": "duty",
                "employee_group_id": 183,
                "is_welcome_enabled": true,
                "media_type": "system",
                "name": "Перерыв666",
                "start": "16:05",
                "stop": "16:10"
            },
                        {
                "scenario_type": "duty",
                "external_numb": "79105846224",
                "is_welcome_enabled": true,
                "media_type": "system",
                "name": "Перерыв777",
                "start": "17:07",
                "stop": "17:55"
            }
        ],
        "is_active": true
    },
    "working_shift2": null,
    "working_shift3": null,
    "default_working_shift": {
        "scenario_type": "informer",
        "media_type": "system",
        "is_active": true
    },
    "id": 693
}
```

## Структура ответа

```
{
    "working_shift1": {
        "scenario_type": "redirect_to_employee_group",
        "employee_group_id": 183,
        "employee_id": null,
        "external_numb": null,
        "menu_settings": null,
        "is_welcome_enabled": false,
        "personal_manager_not_set": true,
        "text_voice_id": null,
        "media_file_id": null,
        "text": null,
        "media_type": null,
        "url": null,
        "http_method": null,
        "timeout": null,
        "max_access_code_len": null,
        "http_actions": null,
        "http_error_employee": null,
        "http_error_group": null,
        "http_error_enabled": false,
        "scheduler_id": 67,
        "is_voice_mail_enabled": false,
        "breaks": [
            {
                "scenario_type": "informer",
                "employee_group_id": null,
                "employee_id": null,
                "external_numb": null,
                "menu_settings": null,
                "is_welcome_enabled": false,
                "personal_manager_not_set": false,
                "text_voice_id": null,
                "media_file_id": null,
                "text": null,
                "media_type": "system",
                "url": null,
                "http_method": null,
                "timeout": null,
                "max_access_code_len": null,
                "http_actions": null,
                "http_error_employee": null,
                "http_error_group": null,
                "http_error_enabled": false,
                "name": "Перерыв1111",
                "start": "11:11:00",
                "stop": "11:21:00",
                "scheduler_id": 67,
                "is_active": true
            },
            {
                "scenario_type": "informer",
                "employee_group_id": null,
                "employee_id": null,
                "external_numb": null,
                "menu_settings": null,
                "is_welcome_enabled": false,
                "personal_manager_not_set": false,
                "text_voice_id": null,
                "media_file_id": 27,
                "text": null,
                "media_type": "client",
                "url": null,
                "http_method": null,
                "timeout": null,
                "max_access_code_len": null,
                "http_actions": null,
                "http_error_employee": null,
                "http_error_group": null,
                "http_error_enabled": false,
                "name": "Перерыв222",
                "start": "12:22:00",
                "stop": "12:23:00",
                "scheduler_id": 67,
                "is_active": true
            },
            {
                "scenario_type": "duty_informer",
                "employee_group_id": null,
                "employee_id": null,
                "external_numb": null,
                "menu_settings": null,
                "is_welcome_enabled": true,
                "personal_manager_not_set": false,
                "text_voice_id": null,
                "media_file_id": null,
                "text": null,
                "media_type": "system",
                "url": null,
                "http_method": null,
                "timeout": null,
                "max_access_code_len": null,
                "http_actions": null,
                "http_error_employee": null,
                "http_error_group": null,
                "http_error_enabled": false,
                "name": "Перерыв333",
                "start": "13:33:00",
                "stop": "13:34:00",
                "scheduler_id": 67,
                "is_active": true
            },
            {
                "scenario_type": "duty",
                "employee_group_id": null,
                "employee_id": 253,
                "external_numb": null,
                "menu_settings": null,
                "is_welcome_enabled": false,
                "personal_manager_not_set": true,
                "text_voice_id": null,
                "media_file_id": null,
                "text": null,
                "media_type": null,
                "url": null,
                "http_method": null,
                "timeout": null,
                "max_access_code_len": null,
                "http_actions": null,
                "http_error_employee": null,
                "http_error_group": null,
                "http_error_enabled": false,
                "name": "Перерыв555",
                "start": "15:44:00",
                "stop": "15:45:00",
                "scheduler_id": 67,
                "is_active": true
            },
            {
                "scenario_type": "duty",
                "employee_group_id": 183,
                "employee_id": null,
                "external_numb": null,
                "menu_settings": null,
                "is_welcome_enabled": true,
                "personal_manager_not_set": true,
                "text_voice_id": null,
                "media_file_id": null,
                "text": null,
                "media_type": "system",
                "url": null,
                "http_method": null,
                "timeout": null,
                "max_access_code_len": null,
                "http_actions": null,
                "http_error_employee": null,
                "http_error_group": null,
                "http_error_enabled": false,
                "name": "Перерыв666",
                "start": "16:05:00",
                "stop": "16:10:00",
                "scheduler_id": 67,
                "is_active": true
            },
            {
                "scenario_type": "duty",
                "employee_group_id": null,
                "employee_id": null,
                "external_numb": "79105846224",
                "menu_settings": null,
                "is_welcome_enabled": true,
                "personal_manager_not_set": false,
                "text_voice_id": null,
                "media_file_id": null,
                "text": null,
                "media_type": "system",
                "url": null,
                "http_method": null,
                "timeout": null,
                "max_access_code_len": null,
                "http_actions": null,
                "http_error_employee": null,
                "http_error_group": null,
                "http_error_enabled": false,
                "name": "Перерыв777",
                "start": "17:07:00",
                "stop": "17:55:00",
                "scheduler_id": 67,
                "is_active": true
            }
        ],
        "is_active": true
    },
    "working_shift2": null,
    "working_shift3": null,
    "default_working_shift": {
        "scenario_type": "informer",
        "employee_group_id": null,
        "employee_id": null,
        "external_numb": null,
        "menu_settings": null,
        "is_welcome_enabled": false,
        "personal_manager_not_set": false,
        "text_voice_id": null,
        "media_file_id": null,
        "text": null,
        "media_type": "system",
        "url": null,
        "http_method": null,
        "timeout": null,
        "max_access_code_len": null,
        "http_actions": null,
        "http_error_employee": null,
        "http_error_group": null,
        "http_error_enabled": false,
        "scheduler_id": null,
        "is_voice_mail_enabled": false,
        "breaks": [],
        "is_active": true
    },
    "id": 693,
    "is_active": null,
    "virtual_number_id": 28
}
```