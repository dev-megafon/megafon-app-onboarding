---
order: 0.5
title: "Получить\_ информацию о виртуальных номерах и настроек входящих сценариев для них"
---

### `GET /scenario/inbound/virtual-number`

**Описание**: метод используется для поиска виртуальных номеров(id) и настроек входящих сценариев для них.

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   working_shift1

*  Object

*  --

*  Первая рабочая смена(настраивается по умолчанию при Круглосуточном режиме и по расписанию)

---

*  {% isHeader=true %}

   working_shift2

*  Object

*  

*  Вторая рабочая смена

---

*  {% isHeader=true %}

   working_shift3

*  Object

*  

*  Третья рабочая смена

---

*  {% isHeader=true %}

   scenario_type

*  String

*  `redirect_to_employee`

*  Тип сценария для обработки входящих звонков.

---

*  {% isHeader=true %}

   employee_group_id

*  Integer or null

*  --

*  Идентификатор отдела сотрудников для приема звонка.

---

*  {% isHeader=true %}

   employee_id

*  Integer

*  --

*  Идентификатор сотрудника, на которого будет перенаправлен звонок

---

*  {% isHeader=true %}

   external_numb

*  String or null

*  --

*  Внешний номер, если требуется.

---

*  {% isHeader=true %}

   menu_settings

*  Object or null

*  --

*  Настройки меню, если применимо.

---

*  {% isHeader=true %}

   is_welcome_enabled

*  Boolean

*  `true`, `false`

*  Флаг, указывающий, включено ли приветствие.

---

*  {% isHeader=true %}

   personal_manager_not_set

*  Boolean

*  `true`, `false`

*  Флаг, указывающий включена ли настройка “Если персональный менеджер не задан”.

---

*  {% isHeader=true %}

   media_file_id

*  Integer or null

*  --

*  Идентификатор медиафайла для воспроизведения.

---

*  {% isHeader=true %}

   text

*  String or null

*  --

*  Текст сообщения, которое будет произнесено.

---

*  {% isHeader=true %}

   media_type

*  String or null

*  \[ `system`, `client`, `text `\]

*  Тип приветствия

---

*  {% isHeader=true %}

   url

*  String or null

*  --

*  URL для отправки HTTP-запроса в операции “Интерактивная обработка””

---

*  {% isHeader=true %}

   http_method

*  String or null

*  `GET`, `POST,` ...

*  Тип HTTP-метода для отправки запроса на URL.”

---

*  {% isHeader=true %}

   timeout

*  Integer or null

*  --

*  Таймаут для HTTP-запроса в секундах.

---

*  {% isHeader=true %}

   max_access_code_len

*  Integer or null

*  --

*  Максимальная длина кода доступа.

---

*  {% isHeader=true %}

   http_actions

*  Array or null

*  --

*  Действия HTTP, которые будут выполнены.

---

*  {% isHeader=true %}

   http_error_employee

*  Integer or null

*  --

*  Идентификатор сотрудника для обработки ошибок HTTP.

---

*  {% isHeader=true %}

   http_error_group

*  Integer or null

*  --

*  Идентификатор отдела для обработки ошибок HTTP.”

---

*  {% isHeader=true %}

   http_error_enabled

*  Boolean

*  `true`, `false`

*  Флаг, указывающий, включена ли обработка ошибок HTTP.

---

*  {% isHeader=true %}

   scheduler_id

*  Integer or null

*  --

*  Идентификатор расписания для сценария.

---

*  {% isHeader=true %}

   is_voicemail_enabled

*  Boolean

*  `true`, `false`

*  Флаг, указывающий, включена ли голосовая почта.

---

*  {% isHeader=true %}

   breaks

*  Array

*  --

*  Массив перерывов в графике работы.

---

*  {% isHeader=true %}

   is_active

*  Boolean or null

*  `true`, `false`

*  Указывает активность сценария, смены или перерыва/

---

*  {% isHeader=true %}

   default_working_shift

*  String or null

*  \-

*  Настройки сценария для нерабочего времени

---

*  {% isHeader=true %}

   id

*  Integer

*  --

*  Уникальный идентификатор сценария.

---

*  {% isHeader=true %}

   virtual_number_id

*  Integer

*  --

*  Уникальный идентификатор виртуального номера, для которого настроен входящий сценарий

{% /table %}

## Структура запроса

`GET /scenario/inbound/virtual-number`

## Структура ответа

```json
{
    "working_shift1": {
        "scenario_type": "redirect_to_employee",
        "employee_group_id": null,
        "employee_id": 125,
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
    "id": 773,
    "is_active": null,
    "virtual_number_id": 649
}
```