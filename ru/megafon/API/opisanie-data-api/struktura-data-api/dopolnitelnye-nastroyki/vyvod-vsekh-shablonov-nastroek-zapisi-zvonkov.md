---
order: 1.28
title: Получить все настройки записи разговоров
---

### `GET /settings/recording`

**Определение:** этот метод предоставляет пользователю полную информацию о всех существующих настройках записи звонков.

## Параметры метода

{% table %}

---

*  {% colwidth=[155] isHeader=true %}

   **Название**

*  {% isHeader=true %}

   **Тип**

*  {% isHeader=true %}

   **Допустимые значения**

*  {% isHeader=true %}

   **Описание**

---

*  {% colwidth=[155] isHeader=true %}

   is_internal_calls_recording_enabled

*  Boolean

*  true, false

*  Включена или выключена запись внутренних звонков.

---

*  {% colwidth=[155] isHeader=true %}

   is_external_calls_recording_enabled

*  Boolean

*  true, false

*  Включена или выключена запись внешних звонков.

---

*  {% colwidth=[155] isHeader=true %}

   no_recording_employee_ids

*  Array

*  Массив идентификаторов сотрудников

*  Список идентификаторов сотрудников, чьи звонки не должны записываться.

---

*  {% colwidth=[155] isHeader=true %}

   is_talk_option_enabled

*  Boolean

*  true, false

*  Включена или выключена возможность включения записи разговора по клавише.

---

*  {% colwidth=[155] isHeader=true %}

   talk_option_button

*  String

*  “2”

*  Клавиша для Активация записи разговора по клавише. Всегда 2

---

*  {% colwidth=[155] isHeader=true %}

   is_recording_notification_enabled

*  Boolean

*  true, false

*  Включено или выключено уведомления о записи разговоров.

---

*  {% colwidth=[155] isHeader=true %}

   recording_notification_audio_message_type

*  String

*  system, custom

*  Тип аудиосообщения для уведомлений о записи: стандартное или Моя аудиотека

---

*  {% colwidth=[155] isHeader=true %}

   recording_notification_media_file_id

*  Integer

*  Целое число

*  Идентификатор медиафайла из Моя аудиотека для проигрывания уведомления о записи разговора.

---

*  {% colwidth=[155] isHeader=true %}

   recording_notification_text

*  String

*  Любая строка

*  Текст уведомления о записи звонка.(пока не используется)

---

*  {% colwidth=[155] isHeader=true %}

   recording_notification_text_voice_id

*  Integer

*  Целое число

*  Идентификатор голоса для текстового уведомления о записи.(пока не используется)

---

*  {% colwidth=[155] isHeader=true %}

   id

*  Integer

*  Целое число

*  Уникальный идентификатор настройки записи.

{% /table %}

## Структура запроса

**Пример запроса:**

```json
GET /settings/recording
```

## **Структура ответа**

```json
[
    {
        "is_internal_calls_recording_enabled": true,
        "is_external_calls_recording_enabled": true,
        "no_recording_employee_ids": [
            125
        ],
        "is_talk_option_enabled": true,
        "talk_option_button": "2",
        "is_recording_notification_enabled": true,
        "recording_notification_audio_message_type": "client",
        "recording_notification_media_file_id": 736,
        "recording_notification_text": null,
        "recording_notification_text_voice_id": null,
        "id": 51
    }
]
```

### 