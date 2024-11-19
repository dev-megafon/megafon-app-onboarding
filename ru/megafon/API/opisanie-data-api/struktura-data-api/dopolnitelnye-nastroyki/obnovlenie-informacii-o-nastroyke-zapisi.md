---
order: 3.8
title: Редактировать настройки записей разговоров
---

### `PUT /settings/recording/{id}`

**Описание:** этот метод позволяет пользователю обновить параметры существующей настройки записи звонков, передавая уникальный идентификатор и новые значения параметров.

## Параметры метода

{% table %}

---

*  {% colwidth=[165] isHeader=true %}

   **Название**

*  {% isHeader=true %}

   **Тип**

*  {% colwidth=[142] isHeader=true %}

   **Обязательный**

*  {% colwidth=[155] isHeader=true %}

   **Допустимые значения**

*  {% isHeader=true %}

   **Описание**

---

*  {% colwidth=[165] isHeader=true %}

   is_internal_calls_recording_enabled

*  Boolean

*  {% colwidth=[142] %}

   да

*  {% colwidth=[155] %}

   `true`, `false`

*  Включена или выключена запись внутренних звонков.

---

*  {% colwidth=[165] isHeader=true %}

   is_external_calls_recording_enabled

*  Boolean

*  {% colwidth=[142] %}

   да

*  {% colwidth=[155] %}

   `true`, `false`

*  Включена или выключена запись внешних звонков.

---

*  {% colwidth=[165] isHeader=true %}

   no_recording_employee_ids

*  Array

*  {% colwidth=[142] %}

   да

*  {% colwidth=[155] %}

   Массив идентификаторов сотрудников или пустой массив

*  Список идентификаторов сотрудников, чьи звонки не должны записываться.

---

*  {% colwidth=[165] isHeader=true %}

   is_talk_option_enabled

*  Boolean

*  {% colwidth=[142] %}

   да

*  {% colwidth=[155] %}

   `true`, `false`

*  Включена или выключена возможность включения записи разговора по клавише.

---

*  {% colwidth=[165] isHeader=true %}

   talk_option_button

*  String

*  {% colwidth=[142] %}

   да

*  {% colwidth=[155] %}

   Только “`2`”

*  Клавиша для активации записи разговора по клавише. Всегда 2

---

*  {% colwidth=[165] isHeader=true %}

   is_recording_notification_enabled

*  Boolean

*  {% colwidth=[142] %}

   да

*  {% colwidth=[155] %}

   true, false

*  Включено или выключено уведомления о записи разговоров.

---

*  {% colwidth=[165] isHeader=true %}

   recording_notification_audio_message_type

*  String

*  {% colwidth=[142] %}

   Да, если параметр “`is_recording_notification_enabled`” стоит “`true`”

*  {% colwidth=[155] %}

   `system`, `custom`

*  Тип аудиосообщения для уведомлений о записи: стандартное или Моя аудиотека

---

*  {% colwidth=[165] isHeader=true %}

   recording_notification_media_file_id

*  Integer

*  {% colwidth=[142] %}

   Да, если параметр “`recording_notification_audio_message_type`” стоит “`custom`”

*  {% colwidth=[155] %}

   Целое число

*  Идентификатор медиафайла из Моя аудиотека для проигрывания уведомления о записи разговора.

---

*  {% colwidth=[165] isHeader=true %}

   recording_notification_text

*  String

*  {% colwidth=[142] %}

   Нет

*  {% colwidth=[155] %}

   Любая строка

*  Текст уведомления о записи звонка.(пока не используется)

---

*  {% colwidth=[165] isHeader=true %}

   recording_notification_text_voice_id

*  Integer

*  {% colwidth=[142] %}

   Нет

*  {% colwidth=[155] %}

   Целое число

*  Идентификатор голоса для текстового уведомления о записи.(пока не используется)

---

*  {% colwidth=[165] isHeader=true %}

   id

*  Integer

*  {% colwidth=[142] %}

   Да

*  {% colwidth=[155] %}

   Целое число

*  Уникальный идентификатор настройки записи.

{% /table %}

**Пример запроса:**

`PUT settings/recording/51`

```json

{
  "is_internal_calls_recording_enabled": true,
  "is_external_calls_recording_enabled": true,
  "no_recording_employee_ids": [
    125
  ],
  "is_talk_option_enabled": true,
  "talk_option_button": "2",
  "is_recording_notification_enabled": false,
  "recording_notification_audio_message_type": "client",
  "recording_notification_media_file_id": 736,
  "id": "51"
}
```

**Ответ:**

```json
{
    "is_internal_calls_recording_enabled": true,
    "is_external_calls_recording_enabled": true,
    "no_recording_employee_ids": [
        125
    ],
    "is_talk_option_enabled": true,
    "talk_option_button": "2",
    "is_recording_notification_enabled": false,
    "recording_notification_audio_message_type": "client",
    "recording_notification_media_file_id": null,
    "recording_notification_text": null,
    "recording_notification_text_voice_id": null,
    "id": 51
}
```