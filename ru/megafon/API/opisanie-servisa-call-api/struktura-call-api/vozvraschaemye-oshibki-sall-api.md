---
order: 4
title: Коды ошибок Сall API
---

При работе с **Call API** могут возникать следующие ошибки. Каждая ошибка содержит текстовое сообщение, код и мнемонику для удобства обработки:

{% table %}

---

*  {% isHeader=true %}

   Текст ошибки

*  {% isHeader=true %}

   Код ошибки

*  {% isHeader=true %}

   Мнемоника

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   The maximum length of Text-to-Speech message is {tts_message_max_length}. The length of your message is {sent_tts_message_length}

*  \-32602

*  tts_text_exceeded

*  Длина сообщения превысила допустимое ограничение, установленное тарифным планом.

---

*  {% isHeader=true %}

   The media file with id {media_file_id} not found

*  \-32602

*  media_file_not_found

*  Файл не найден.

---

*  {% isHeader=true %}

   Virtual phone number {virtual_phone_number} not found. It is not your virtual phone number.

*  \-32007

*  virtual_phone_number_not_found

*  Используется виртуальный номер, не принадлежащий клиенту.

---

*  {% isHeader=true %}

   Employee with id {employee_id} not found. It is not your employee.

*  \-32602

*  employee_not_found

*  Сотрудник не найден.

---

*  {% isHeader=true %}

   The phone number does not exist or inactive

*  \-32602

*  no_active_phone_number

*  У сотрудника нет активных номеров в настройках.

---

*  {% isHeader=true %}

   Parameter contact can not contain own virtual phone number

*  \-32602

*  own_virtual_phone_number_not_allowed

*  Звонок на собственный виртуальный номер запрещен.

---

*  {% isHeader=true %}

   The contact {contact} has been found in the blacklist

*  \-32002

*  contact_in_blacklist

*  Контакт находится в Черном списке.

---

*  {% isHeader=true %}

   The character encoding must be UTF-8

*  \-32602

*  character_encoding_not_allowed

*  Кодировка символов должна быть UTF-8.

{% /table %}
