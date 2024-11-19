---
order: 2
title: "Получение информации об отделе "
---

### `GET /employee-group/{id}`

**Описание**: этот метод позволяет получить информацию  об отделе по его уникальному идентификатору.

## Параметры метода

{% table %}

---

*  {% colwidth=[184] isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% colwidth=[127] isHeader=true %}

   Допустимые значения

*  {% colwidth=[240] isHeader=true %}

   Описание

---

*  {% colwidth=[184] isHeader=true %}

   name

*  string

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Название отдела

---

*  {% colwidth=[184] isHeader=true %}

   short_phone

*  string

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Внутренний номер  отдела

---

*  {% colwidth=[184] isHeader=true %}

   is_managers_enabled

*  boolean

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Включена ли настройка “Руководитель отдела

---

*  {% colwidth=[184] isHeader=true %}

   manager_ids

*  integer

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Идентификаторы Руководителей отдела.

---

*  {% colwidth=[184] isHeader=true %}

   distribution_type

*  string

*  {% colwidth=[127] %}

   `parallel`, `evenly`, `in_turn`, `increasingly`

*  {% colwidth=[240] %}

   Тип распределения звонков между сотрудниками.

---

*  {% colwidth=[184] isHeader=true %}

   distribution_delay

*  integer

*  {% colwidth=[127] %}

   5,10,15,20,25,30,35,40,45,50,55,60

*  {% colwidth=[240] %}

   Задержка распределения сотрудников.

---

*  {% colwidth=[184] isHeader=true %}

   employees

*  Employee\[\]

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Список сотрудников отдела.

---

*  {% colwidth=[184] isHeader=true %}

   employee_id

*  integer

*  {% colwidth=[127] %}

   

*  {% colwidth=[240] %}

   Уникальный идентификатор сотрудника

---

*  {% colwidth=[184] isHeader=true %}

   priority

*  integer

*  {% colwidth=[127] %}

   Целое число (стартовое - 0)

*  {% colwidth=[240] %}

   Приоритет сотрудника

---

*  {% colwidth=[184] isHeader=true %}

   is_active

*  boolean

*  {% colwidth=[127] %}

   `true`,`false`

*  {% colwidth=[240] %}

   Включен прием звонков сотрудника в отделе

---

*  {% colwidth=[184] isHeader=true %}

   fail_dialing_action

*  string

*  {% colwidth=[127] %}

   \[`voice_mail`, `redirect_to_number`, `redirect_to_employee`, `redirect_to_group`, `play_message`\]

*  {% colwidth=[240] %}

   Действия, если в отделе никто не ответил

---

*  {% colwidth=[184] isHeader=true %}

   fail_dialing_timeout

*  integer

*  {% colwidth=[127] %}

   15, 30, 60, 120, 300, 600

*  {% colwidth=[240] %}

   Время ожидания ответа в отделе

---

*  {% colwidth=[184] isHeader=true %}

   voice_message_type

*  string

*  {% colwidth=[127] %}

   `system`, `client`, `text`

*  {% colwidth=[240] %}

   Тип голосового сообщения

---

*  {% colwidth=[184] isHeader=true %}

   media_file_id

*  integer

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Идентификатор медиафайла.

---

*  {% colwidth=[184] isHeader=true %}

   text

*  string

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Текст сообщения.

---

*  {% colwidth=[184] isHeader=true %}

   redirect_number

*  string

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Номер для перенаправления.

---

*  {% colwidth=[184] isHeader=true %}

   redirect_employee_id

*  integer

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Идентификатор сотрудника для перенаправления.

---

*  {% colwidth=[184] isHeader=true %}

   redirect_employee_group_id

*  integer

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Идентификатор отдела сотрудников для перенаправления.

---

*  {% colwidth=[184] isHeader=true %}

   id

*  integer

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Уникальный идентификатор отдела сотрудников.

{% /table %}

## **Структура запроса**

```http
GET /employee-group/123
```

## **Структура ответа**

```json
{
    "name": "Название Отдела",
    "short_phone": "12345",
    "is_managers_enabled": true,
    "manager_ids": [
        123,
        234
    ],
    "distribution_type": "parallel",
    "distribution_delay": 0,
    "employees": [
        {
            "employee_id": 123,
            "priority": 0,
            "is_active": true,
            "id": 577
        },
        {
            "employee_id": 234,
            "priority": 1,
            "is_active": true,
            "id": 579
        },
        {
            "employee_id": 345,
            "priority": 2,
            "is_active": true,
            "id": 581
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
    "id": 123,
    "app_id": 123456
}
```