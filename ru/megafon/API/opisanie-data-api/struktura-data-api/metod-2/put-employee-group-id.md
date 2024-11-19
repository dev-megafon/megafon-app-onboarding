---
order: 4
title: Редактировать отдел
---

### `PUT /employee-group/{id}`

**Описание**: этот метод позволяет редактировать информацию об отделе по его уникальному идентификатору.

## Параметры метода

{% table %}

---

*  {% colwidth=[181] isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% colwidth=[145] isHeader=true %}

   Обязательный

*  {% colwidth=[127] isHeader=true %}

   Допустимые значения

*  {% colwidth=[240] isHeader=true %}

   Описание

---

*  {% colwidth=[181] isHeader=true %}

   name

*  string

*  {% colwidth=[145] %}

   Да

*  {% colwidth=[127] %}

   Любая строка

*  {% colwidth=[240] %}

   Название отдела.

---

*  {% colwidth=[181] isHeader=true %}

   short_phone

*  string

*  {% colwidth=[145] %}

   Да

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Внутренний номер  отдела

---

*  {% colwidth=[181] isHeader=true %}

   is_managers_enabled

*  boolean

*  {% colwidth=[145] %}

   Нет

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Включена ли настройка “Руководитель отдела” (по умолчанию: `false`)

---

*  {% colwidth=[181] isHeader=true %}

   manager_ids

*  array

*  {% colwidth=[145] %}

   Нет

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Идентификаторы Руководителей отдела.

---

*  {% colwidth=[181] isHeader=true %}

   distribution_type

*  string

*  {% colwidth=[145] %}

   Нет

*  {% colwidth=[127] %}

   `parallel`, `evenly`, `in_turn`, `increasingly`

*  {% colwidth=[240] %}

   Тип распределения звонков между сотрудниками (по умолчанию: `parallel`)

---

*  {% colwidth=[181] isHeader=true %}

   distribution_delay

*  integer

*  {% colwidth=[145] %}

   Нет (Обязательно, если в параметре `distribution_type `выбраны “`evenly`”, “`in_turn`”, “`increasingly`”)

*  {% colwidth=[127] %}

   5,10,15,20,25,30,35,40,45,50,55,60

*  {% colwidth=[240] %}

   Задержка распределения сотрудников.

---

*  {% colwidth=[181] isHeader=true %}

   employees

*  array

*  {% colwidth=[145] %}

   Нет

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Список сотрудников отдела.

---

*  {% colwidth=[181] isHeader=true %}

   employee_id

*  integer

*  {% colwidth=[145] %}

   Да ( если есть параметр `employees`)

*  {% colwidth=[127] %}

   

*  {% colwidth=[240] %}

   Уникальный идентификатор сотрудника

---

*  {% colwidth=[181] isHeader=true %}

   priority

*  integer

*  {% colwidth=[145] %}

   Да ( если есть параметр `employees`)

*  {% colwidth=[127] %}

   Целое число (стартовое - 0)

*  {% colwidth=[240] %}

   Приоритет сотрудника

---

*  {% colwidth=[181] isHeader=true %}

   is_active

*  boolean

*  {% colwidth=[145] %}

   Да (если есть параметр `employees)`

*  {% colwidth=[127] %}

   true,false

*  {% colwidth=[240] %}

   Включен прием звонков сотрудника в отделе

---

*  {% colwidth=[181] isHeader=true %}

   fail_dialing_action

*  string

*  {% colwidth=[145] %}

   Да

*  {% colwidth=[127] %}

   \[`voice_mail`, `redirect_to_number`, `redirect_to_employee`, `redirect_to_group`, `play_message`\]

*  {% colwidth=[240] %}

   Действия, если в отделе никто не ответил

---

*  {% colwidth=[181] isHeader=true %}

   fail_dialing_timeout

*  integer

*  {% colwidth=[145] %}

   Да

*  {% colwidth=[127] %}

   15, 30, 60, 120, 300, 600

*  {% colwidth=[240] %}

   Время ожидания ответа в отделе

---

*  {% colwidth=[181] isHeader=true %}

   voice_message_type

*  string

*  {% colwidth=[145] %}

   Да

*  {% colwidth=[127] %}

   `system`, `client`, `text`

*  {% colwidth=[240] %}

   Тип голосового сообщения.

---

*  {% colwidth=[181] isHeader=true %}

   media_file_id

*  integer

*  {% colwidth=[145] %}

   Нет (обязательное при заполнении “`voice_message_type`” как “`client`”)”

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Идентификатор медиафайла.

---

*  {% colwidth=[181] isHeader=true %}

   text

*  string

*  {% colwidth=[145] %}

   Нет (обязательное при заполнении “`voice_message_type`” как “`text`”)”

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Текст сообщения.

---

*  {% colwidth=[181] isHeader=true %}

   redirect_number

*  string

*  {% colwidth=[145] %}

   Нет (обязательный при заполнении “`fail_dialing_action`” как “`redirect_to_number`

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Номер для перенаправления.

---

*  {% colwidth=[181] isHeader=true %}

   redirect_employee_id

*  integer

*  {% colwidth=[145] %}

   Нет (обязательный при заполнении “`fail_dialing_action`” как “`redirect_to_employee`”)

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Идентификатор сотрудника для перенаправления.

---

*  {% colwidth=[181] isHeader=true %}

   redirect_employee_group_id

*  integer

*  {% colwidth=[145] %}

   Нет (обязательный при заполнении “`fail_dialing_action`” как “`redirect_to_group`”)

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Идентификатор отдела сотрудников для перенаправления.

---

*  {% colwidth=[181] isHeader=true %}

   id

*  integer

*  {% colwidth=[145] %}

   Да

*  {% colwidth=[127] %}

   --

*  {% colwidth=[240] %}

   Уникальный идентификатор отдела

{% /table %}

## **Структура запроса**

`PUT /employee-group/12356`

```json
{
  "name": "Название отдела2",
  "short_phone": "12345",
  "is_managers_enabled": true,
  "manager_ids": [
    123
  ],
  "distribution_type": "parallel",
  "distribution_delay": 0,
  "employees": [
    {
      "employee_id": 123,
      "priority": 0,
      "is_active": true
    }
  ],
  "fail_dialing_action": "voice_mail",
  "fail_dialing_timeout": 120,
  "voice_message_type": "system",
  "media_file_id": 123,
  "text": "Перезвоните позднее",
  "text_voice_id": 123,
  "redirect_number": "79201234567",
  "redirect_employee_id": 123,
  "redirect_employee_group_id": 123
}
```

## **Структура ответа**

```json
{
    "name": "Название отдела2",
    "short_phone": "12345",
    "is_managers_enabled": true,
    "manager_ids": [
        123
    ],
    "distribution_type": "parallel",
    "distribution_delay": 0,
    "employees": [
        {
            "employee_id": 123,
            "priority": 0,
            "is_active": true,
            "id": 583
        }
    ],
    "fail_dialing_action": "voice_mail",
    "fail_dialing_timeout": 120,
    "voice_message_type": "system",
    "media_file_id": 63,
    "text": "Перезвоните позднее",
    "text_voice_id": 12,
    "redirect_number": "79201234567",
    "redirect_employee_id": 123,
    "redirect_employee_group_id": 123,
    "is_use_group_phone": false,
    "id": 123,
    "app_id": 123456
}
```