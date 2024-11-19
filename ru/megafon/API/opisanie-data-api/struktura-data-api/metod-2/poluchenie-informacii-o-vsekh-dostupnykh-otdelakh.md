---
order: 1
title: Получить список всех отделов
---

### `GET /employee-group/`

**Описание**: этот метод позволяет получить информацию о всех существующих в системе отделах.

## Параметры метода

{% table %}

---

*  {% colwidth=[181] isHeader=true %}

   Название

*  {% colwidth=[102] isHeader=true %}

   Тип

*  {% colwidth=[127] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[181] isHeader=true %}

   name

*  {% colwidth=[102] %}

   string

*  {% colwidth=[127] %}

   --

*  Название отдела

---

*  {% colwidth=[181] isHeader=true %}

   short_phone

*  {% colwidth=[102] %}

   string

*  {% colwidth=[127] %}

   --

*  Внутренний номер  отдела

---

*  {% colwidth=[181] isHeader=true %}

   is_managers_enabled

*  {% colwidth=[102] %}

   boolean

*  {% colwidth=[127] %}

   --

*  Включена ли настройка “Руководитель отдела”

---

*  {% colwidth=[181] isHeader=true %}

   manager_ids

*  {% colwidth=[102] %}

   integer

*  {% colwidth=[127] %}

   --

*  Идентификаторы Руководителей отдела.

---

*  {% colwidth=[181] isHeader=true %}

   distribution_type

*  {% colwidth=[102] %}

   string

*  {% colwidth=[127] %}

   `parallel`, `evenly`, `in_turn`, `increasingly`

*  Тип распределения звонков между сотрудниками

---

*  {% colwidth=[181] isHeader=true %}

   distribution_delay

*  {% colwidth=[102] %}

   integer

*  {% colwidth=[127] %}

   5,10,15,20,25,30,35,40,45,50,55,60

*  Задержка распределения сотрудников.

---

*  {% colwidth=[181] isHeader=true %}

   employees

*  {% colwidth=[102] %}

   Employee\[\]

*  {% colwidth=[127] %}

   --

*  Список сотрудников отдела.

---

*  {% colwidth=[181] isHeader=true %}

   employee_id

*  {% colwidth=[102] %}

   integer

*  {% colwidth=[127] %}

   \-

*  Уникальный идентификатор сотрудника

---

*  {% colwidth=[181] isHeader=true %}

   priority

*  {% colwidth=[102] %}

   integer

*  {% colwidth=[127] %}

   Целое число (стартовое - 0)

*  Приоритет сотрудника

---

*  {% colwidth=[181] isHeader=true %}

   is_active

*  {% colwidth=[102] %}

   boolean

*  {% colwidth=[127] %}

   `true,false`

*  Включен прием звонков сотрудника в отделе

---

*  {% colwidth=[181] isHeader=true %}

   fail_dialing_action

*  {% colwidth=[102] %}

   string

*  {% colwidth=[127] %}

   \[`voice_mail`, `redirect_to_number`, `redirect_to_employee`, `redirect_to_group`, `play_message`\]

*  Действия, если в отделе никто не ответил

---

*  {% colwidth=[181] isHeader=true %}

   fail_dialing_timeout

*  {% colwidth=[102] %}

   integer

*  {% colwidth=[127] %}

   15, 30, 60, 120, 300, 600

*  Время ожидания ответа в отделе

---

*  {% colwidth=[181] isHeader=true %}

   voice_message_type

*  {% colwidth=[102] %}

   string

*  {% colwidth=[127] %}

   `system`, `client`, `text`

*  Тип голосового сообщения.

---

*  {% colwidth=[181] isHeader=true %}

   media_file_id

*  {% colwidth=[102] %}

   integer

*  {% colwidth=[127] %}

   --

*  Идентификатор медиафайла.

---

*  {% colwidth=[181] isHeader=true %}

   text

*  {% colwidth=[102] %}

   string

*  {% colwidth=[127] %}

   --

*  Текст сообщения.

---

*  {% colwidth=[181] isHeader=true %}

   redirect_number

*  {% colwidth=[102] %}

   string

*  {% colwidth=[127] %}

   --

*  Номер для перенаправления.

---

*  {% colwidth=[181] isHeader=true %}

   redirect_employee_id

*  {% colwidth=[102] %}

   integer

*  {% colwidth=[127] %}

   --

*  Идентификатор сотрудника для перенаправления.

---

*  {% colwidth=[181] isHeader=true %}

   redirect_employee_group_id

*  {% colwidth=[102] %}

   integer

*  {% colwidth=[127] %}

   \-

*  Идентификатор группы для перенаправления.

---

*  {% colwidth=[181] isHeader=true %}

   id

*  {% colwidth=[102] %}

   integer

*  {% colwidth=[127] %}

   --

*  Уникальный идентификатор отдела сотрудников.

{% /table %}

## **Структура запроса**

```http
GET /employee-group/
```

## **Структура ответа**

```json
[
    {
        "name": "22_2",
        "short_phone": "33333",
        "is_managers_enabled": false,
        "manager_ids": null,
        "distribution_type": "in_turn",
        "distribution_delay": 15,
        "employees": [
            {
                "employee_id": 137,
                "priority": 0,
                "is_active": true,
                "id": 209
            },
            {
                "employee_id": 129,
                "priority": 1,
                "is_active": true,
                "id": 205
            },
            {
                "employee_id": 125,
                "priority": 2,
                "is_active": true,
                "id": 207
            }
        ],
        "fail_dialing_action": "voice_mail",
        "fail_dialing_timeout": 120,
        "voice_message_type": "system",
        "media_file_id": 63,
        "text": null,
        "text_voice_id": 12,
        "redirect_number": null,
        "redirect_employee_id": null,
        "redirect_employee_group_id": null,
        "is_use_group_phone": false,
        "id": 79,
        "app_id": 1200054
    },
    {
        "name": "333",
        "short_phone": "55555",
        "is_managers_enabled": false,
        "manager_ids": null,
        "distribution_type": "in_turn",
        "distribution_delay": 60,
        "employees": [
            {
                "employee_id": 129,
                "priority": 0,
                "is_active": true,
                "id": 201
            }
        ],
        "fail_dialing_action": "voice_mail",
        "fail_dialing_timeout": 120,
        "voice_message_type": "system",
        "media_file_id": 63,
        "text": null,
        "text_voice_id": 12,
        "redirect_number": null,
        "redirect_employee_id": null,
        "redirect_employee_group_id": null,
        "is_use_group_phone": false,
        "id": 83,
        "app_id": 1200054
    },
    {
        "name": "444",
        "short_phone": "44444",
        "is_managers_enabled": false,
        "manager_ids": null,
        "distribution_type": "parallel",
        "distribution_delay": 0,
        "employees": [
            {
                "employee_id": 125,
                "priority": 0,
                "is_active": true,
                "id": 199
            }
        ],
        "fail_dialing_action": "play_message",
        "fail_dialing_timeout": 120,
        "voice_message_type": "client",
        "media_file_id": null,
        "text": null,
        "text_voice_id": null,
        "redirect_number": null,
        "redirect_employee_id": null,
        "redirect_employee_group_id": null,
        "is_use_group_phone": false,
        "id": 87,
        "app_id": 1200054
    },
```,
        «app_id»: 1200054
    }
```