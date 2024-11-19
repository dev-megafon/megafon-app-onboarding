---
order: 0.7
title: Получить информацию о сотруднике
---

### `GET /employee/{id}`

**Описание:** этот метод возвращает информацию о сотруднике по его уникальному идентификатору (ID).

## Параметры метода

{% table %}

---

*  {% colwidth=[118] isHeader=true %}

   Название

*  {% colwidth=[81] isHeader=true %}

   Тип

*  {% colwidth=[133] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[118] isHeader=true %}

   first_name

*  {% colwidth=[81] %}

   string

*  {% colwidth=[133] %}

   --

*  Имя пользователя.

---

*  {% colwidth=[118] isHeader=true %}

   last_name

*  {% colwidth=[81] %}

   string

*  {% colwidth=[133] %}

   --

*  Фамилия пользователя.

---

*  {% colwidth=[118] isHeader=true %}

   login

*  {% colwidth=[81] %}

   string

*  {% colwidth=[133] %}

   \-

*  Логин сотрудника

---

*  {% colwidth=[118] isHeader=true %}

   password

*  {% colwidth=[81] %}

   string

*  {% colwidth=[133] %}

   \-

*  Пароль сотрудника

---

*  {% colwidth=[118] isHeader=true %}

   position_id

*  {% colwidth=[81] %}

   integer

*  {% colwidth=[133] %}

   --

*  Идентификатор должности.

---

*  {% colwidth=[118] isHeader=true %}

   role_id

*  {% colwidth=[81] %}

   integer

*  {% colwidth=[133] %}

   --

*  Идентификатор роли.

---

*  {% colwidth=[118] isHeader=true %}

   short_phone

*  {% colwidth=[81] %}

   string

*  {% colwidth=[133] %}

   --

*  Внутренний номер телефона.

---

*  {% colwidth=[118] isHeader=true %}

   email

*  {% colwidth=[81] %}

   string

*  {% colwidth=[133] %}

   --

*  Электронная почта пользователя.

---

*  {% colwidth=[118] isHeader=true %}

   sim_number_capacity_id

*  {% colwidth=[81] %}

   integer

*  {% colwidth=[133] %}

   --

*  Идентификатор рабочей SIM-карты

---

*  {% colwidth=[118] isHeader=true %}

   dialing_type

*  {% colwidth=[81] %}

   string

*  {% colwidth=[133] %}

   `parallel`\- Звонить одновременно\
   “`first_sip`” - Сначала на SIP-регистрацию\
   “`first_virtual_number`” - Сначала на SIM-карту

*  Настройка «Звонить на рабочие номера»\
   (по умолчанию: `parallel`)

---

*  {% colwidth=[118] isHeader=true %}

   delay

*  {% colwidth=[81] %}

   integer

*  {% colwidth=[133] %}

   --

*  Дозвон на второе устройство через

---

*  {% colwidth=[118] isHeader=true %}

   phone

*  {% colwidth=[81] %}

   string

*  {% colwidth=[133] %}

   --

*  Личный мобильный номер

---

*  {% colwidth=[118] isHeader=true %}

   is_phone_dialing_enabled

*  {% colwidth=[81] %}

   boolean

*  {% colwidth=[133] %}

   --

*  Включен ли набор номера на личный мобильный (по умолчанию: `false`).

---

*  {% colwidth=[118] isHeader=true %}

   phone_dialing_type

*  {% colwidth=[81] %}

   string

*  {% colwidth=[133] %}

   `dialing_rule`\
   `only_phone`

*  Тип набора номера по телефону (по умолчанию: `dialing_rule`).

---

*  {% colwidth=[118] isHeader=true %}

   phone_delay

*  {% colwidth=[81] %}

   integer

*  {% colwidth=[133] %}

   --

*  Задержка звонка на мобильный.

---

*  {% colwidth=[118] isHeader=true %}

   id

*  {% colwidth=[81] %}

   integer

*  {% colwidth=[133] %}

   --

*  Уникальный идентификатор сотрудника.

---

*  {% colwidth=[118] isHeader=true %}

   is_sip_registered

*  {% colwidth=[81] %}

   boolean

*  {% colwidth=[133] %}

   --

*  Зарегистрирован ли SIP

---

*  {% colwidth=[118] isHeader=true %}

   photo_link

*  {% colwidth=[81] %}

   string

*  {% colwidth=[133] %}

   --

*  Ссылка на фотографию пользователя.

{% /table %}

## **Структура запроса**

`GET /employee/125`

## Cтруктура ответа

Возвращает объект с данными о сотруднике, включая имя, фамилию, должность, контактные данные и другую информацию.

```json
{
    "first_name": null,
    "last_name": "Администратор1111",
    "position_id": 45,
    "role_id": 273,
    "short_phone": "700",
    "email": "m.malinin1@comagic.dev",
    "sim_number_capacity_id": 250,
    "dialing_type": "parallel",
    "delay": null,
    "phone": "79151621545",
    "is_phone_dialing_enabled": false,
    "phone_dialing_type": "dialing_rule",
    "phone_delay": null,
    "id": 125,
    "is_sip_registered": false,
    "photo_link": null,
    "role": "employee",
    "role_name": "Администратор",
    "app_id": 1200054,
    "user_id": 145,
    "full_name": "Администратор1111",
    "login": "admin@vats1200054.cp.megafon.ru",
    "sim_phone": "79208547433",
    "position_name": "Test"
}
```