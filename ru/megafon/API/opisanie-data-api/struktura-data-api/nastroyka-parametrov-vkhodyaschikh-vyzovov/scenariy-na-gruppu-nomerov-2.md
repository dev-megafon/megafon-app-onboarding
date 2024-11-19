---
order: 0.9
title: Получить настройки виртуальных номеров для входящих звонков
---

### `GET /scenario/inbound/virtual-number-group`

**Описание**: метод  предназначен для управления группами сценариев, связанных с виртуальными номерами. Он позволяет настраивать различные рабочие смены и их параметры.

## Параметры метода

{% table %}

---

*  {% colwidth=[217] isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[217] isHeader=true %}

   working_shift1

*  Object

*  --

*  Первая рабочая смена(настраивается по умолчанию при Круглосуточном режиме и по расписанию)

---

*  {% colwidth=[217] isHeader=true %}

   working_shift2

*  Object

*  

*  Вторая рабочая смена

---

*  {% colwidth=[217] isHeader=true %}

   working_shift3

*  Object

*  

*  Третья рабочая смена

---

*  {% colwidth=[217] isHeader=true %}

   scenario_type

*  String

*  `redirect_to_employee`

*  Тип сценария для обработки входящих звонков.

---

*  {% colwidth=[217] isHeader=true %}

   employee_group_id

*  Integer or null

*  --

*  Идентификатор отдела сотрудников для приема звонка.

---

*  {% colwidth=[217] isHeader=true %}

   employee_id

*  Integer

*  --

*  Идентификатор сотрудника, на которого будет перенаправлен звонок

---

*  {% colwidth=[217] isHeader=true %}

   external_numb

*  String or null

*  --

*  Внешний номер, если требуется.

---

*  {% colwidth=[217] isHeader=true %}

   menu_settings

*  Object or null

*  --

*  Настройки меню, если применимо.

---

*  {% colwidth=[217] isHeader=true %}

   is_welcome_enabled

*  Boolean

*  `true`, `false`

*  Флаг, указывающий, включено ли приветствие.

---

*  {% colwidth=[217] isHeader=true %}

   personal_manager_not_set

*  Boolean

*  `true`, `false`

*  Флаг, указывающий включена ли настройка “Если персональный менеджер не задан”.

---

*  {% colwidth=[217] isHeader=true %}

   media_file_id

*  Integer or null

*  --

*  Идентификатор медиафайла для воспроизведения.

---

*  {% colwidth=[217] isHeader=true %}

   text

*  String or null

*  --

*  Текст сообщения, которое будет произнесено.

---

*  {% colwidth=[217] isHeader=true %}

   media_type

*  String or null

*  `system`, `client`, `text `

*  Тип приветствия

---

*  {% colwidth=[217] isHeader=true %}

   url

*  String or null

*  --

*  URL для отправки HTTP-запроса в операции “Интерактивная обработка””

---

*  {% colwidth=[217] isHeader=true %}

   http_method

*  String or null

*  «GET», «POST», ...

*  Тип HTTP-метода для отправки запроса на URL.”

---

*  {% colwidth=[217] isHeader=true %}

   timeout

*  Integer or null

*  --

*  Таймаут для HTTP-запроса в секундах.

---

*  {% colwidth=[217] isHeader=true %}

   max_access_code_len

*  Integer or null

*  --

*  Максимальная длина кода доступа.

---

*  {% colwidth=[217] isHeader=true %}

   http_actions

*  Array or null

*  --

*  Действия HTTP, которые будут выполнены.

---

*  {% colwidth=[217] isHeader=true %}

   http_error_employee

*  Integer or null

*  --

*  Идентификатор сотрудника для обработки ошибок HTTP.

---

*  {% colwidth=[217] isHeader=true %}

   http_error_group

*  Integer or null

*  --

*  Идентификатор отдела для обработки ошибок HTTP.”

---

*  {% colwidth=[217] isHeader=true %}

   http_error_enabled

*  Boolean

*  `true`, `false`

*  Флаг, указывающий, включена ли обработка ошибок HTTP.

---

*  {% colwidth=[217] isHeader=true %}

   scheduler_id

*  Integer or null

*  --

*  Идентификатор расписания для сценария.

---

*  {% colwidth=[217] isHeader=true %}

   is_voicemail_enabled

*  Boolean

*  `true`, `false`

*  Флаг, указывающий, включена ли голосовая почта.

---

*  {% colwidth=[217] isHeader=true %}

   breaks

*  Array

*  --

*  Массив перерывов в графике работы.

---

*  {% colwidth=[217] isHeader=true %}

   is_active

*  Boolean or null

*  `true`, `false`

*  Указывает активность сценария, смены или перерыва

---

*  {% colwidth=[217] isHeader=true %}

   default_working_shift

*  String or null

*  \-

*  Настройки сценария для нерабочего времени

---

*  {% colwidth=[217] isHeader=true %}

   id

*  Integer

*  --

*  Уникальный идентификатор сценария.

---

*  {% colwidth=[217] isHeader=true %}

   virtual_number_id

*  Integer

*  --

*  Уникальный идентификатор виртуального номера, для которого настроен входящий сценарий

---

*  {% colwidth=[217] isHeader=true %}

   virtual_number_group_id

*  integer

*  \-

*  

   Уникальный идентификатор группы номеров.

{% /table %}

## Cтруктура запроса

`GET /scenario/inbound/virtual-number-group`

## Структура ответа

```json
[
      {
        "working_shift1": {
            "scenario_type": "redirect_to_employee",
            "employee_group_id": null,
            "employee_id": 129,
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
            "scheduler_id": null,
            "is_voice_mail_enabled": false,
            "breaks": [],
            "is_active": true
        },
        "working_shift2": null,
        "working_shift3": null,
        "default_working_shift": null,
        "id": 77,
        "is_active": null,
        "virtual_number_id": null,
        "virtual_number_group_id": 37
    }
]
```