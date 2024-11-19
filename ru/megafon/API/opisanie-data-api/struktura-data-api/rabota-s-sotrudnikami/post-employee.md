---
order: 0.8
title: Создать нового сотрудника
---

### `POST /employee`

**Описание**: этот метод создает нового сотрудника с данными, указанными в теле запроса.

## Параметры метода

{% table %}

---

*  {% colwidth=[144] isHeader=true %}

   Название

*  {% colwidth=[81] isHeader=true %}

   Тип

*  {% colwidth=[132] isHeader=true %}

   Допустимые значения

*  {% colwidth=[194] isHeader=true %}

   Обязательный

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[144] isHeader=true %}

   first_name

*  {% colwidth=[81] %}

   string

*  {% colwidth=[132] %}

   --

*  {% colwidth=[194] %}

   Нет

*  Имя пользователя.

---

*  {% colwidth=[144] isHeader=true %}

   last_name

*  {% colwidth=[81] %}

   string

*  {% colwidth=[132] %}

   --

*  {% colwidth=[194] %}

   Да

*  Фамилия пользователя.

---

*  {% colwidth=[144] isHeader=true %}

   login

*  {% colwidth=[81] %}

   string

*  {% colwidth=[132] %}

   --

*  {% colwidth=[194] %}

   Да

*  Логин сотрудника.

---

*  {% colwidth=[144] isHeader=true %}

   password

*  {% colwidth=[81] %}

   string

*  {% colwidth=[132] %}

   --

*  {% colwidth=[194] %}

   Да

*  Пароль сотрудника.

---

*  {% colwidth=[144] isHeader=true %}

   position_id

*  {% colwidth=[81] %}

   integer

*  {% colwidth=[132] %}

   --

*  {% colwidth=[194] %}

   Да

*  Идентификатор должности.

---

*  {% colwidth=[144] isHeader=true %}

   role_id

*  {% colwidth=[81] %}

   integer

*  {% colwidth=[132] %}

   --

*  {% colwidth=[194] %}

   Да

*  Идентификатор роли.

---

*  {% colwidth=[144] isHeader=true %}

   short_phone

*  {% colwidth=[81] %}

   string

*  {% colwidth=[132] %}

   --

*  {% colwidth=[194] %}

   Да

*  Внутренний номер телефона.

---

*  {% colwidth=[144] isHeader=true %}

   email

*  {% colwidth=[81] %}

   string

*  {% colwidth=[132] %}

   --

*  {% colwidth=[194] %}

   Нет (обязательно если роль “Администратор”)

*  Электронная почта пользователя.

---

*  {% colwidth=[144] isHeader=true %}

   sim_number_capacity_id

*  {% colwidth=[81] %}

   integer

*  {% colwidth=[132] %}

   --

*  {% colwidth=[194] %}

   Нет

*  Идентификатор рабочей SIM-карты.

---

*  {% colwidth=[144] isHeader=true %}

   dialing_type

*  {% colwidth=[81] %}

   string

*  {% colwidth=[132] %}

   `parallel`, `first_sip`, `first_virtual_number`

*  {% colwidth=[194] %}

   Да, если заполнен параметр `sim_number_capacity_id`

*  Настройка «Звонить на рабочие номера» (по умолчанию: parallel).

---

*  {% colwidth=[144] isHeader=true %}

   delay

*  {% colwidth=[81] %}

   integer

*  {% colwidth=[132] %}

   5, 10, 15, 20, 25, 30

*  {% colwidth=[194] %}

   Да, если в параметре `dialing_type` выбраны `first_sip`, `first_virtual_number`\
   `phone` - Нет

*  Дозвон на второе устройство через заданное время.

---

*  {% colwidth=[144] isHeader=true %}

   phone

*  {% colwidth=[81] %}

   string

*  {% colwidth=[132] %}

   --

*  {% colwidth=[194] %}

   Нет

*  Личный мобильный номер.

---

*  {% colwidth=[144] isHeader=true %}

   is_phone_dialing_enabled

*  {% colwidth=[81] %}

   boolean

*  {% colwidth=[132] %}

   --

*  {% colwidth=[194] %}

   Да, если заполнен параметр `phone`

*  Включен ли набор номера на личный мобильный.

---

*  {% colwidth=[144] isHeader=true %}

   phone_dialing_type

*  {% colwidth=[81] %}

   string

*  {% colwidth=[132] %}

   `dialing_rule`,`only_phone`

*  {% colwidth=[194] %}

   Да, если параметр `is_phone_dialing_enabled` заполнен как `True`

*  Тип набора номера по телефону (по умолчанию: `dialing_rule`).

---

*  {% colwidth=[144] isHeader=true %}

   phone_delay

*  {% colwidth=[81] %}

   integer

*  {% colwidth=[132] %}

   0, 5, 10, 15, 20, 25, 30

*  {% colwidth=[194] %}

   Да, если параметр `phone_dialing_type` заполнен как `dialing_rule`

*  Задержка звонка на мобильный.

---

*  {% colwidth=[144] isHeader=true %}

   id

*  {% colwidth=[81] %}

   integer

*  {% colwidth=[132] %}

   --

*  {% colwidth=[194] %}

   \-

*  Уникальный идентификатор сотрудника.

---

*  {% colwidth=[144] isHeader=true %}

   is_sip_registered

*  {% colwidth=[81] %}

   boolean

*  {% colwidth=[132] %}

   --

*  {% colwidth=[194] %}

   \-

*  Зарегистрирован ли SIP.

---

*  {% colwidth=[144] isHeader=true %}

   photo_link

*  {% colwidth=[81] %}

   string

*  {% colwidth=[132] %}

   --

*  {% colwidth=[194] %}

   

*  Ссылка на фотографию пользователя.

{% /table %}

## Cтруктура запроса:

```json
POST /employee HTTP/1.1
Host: api.example.com
Content-Type: application/json

{
    "first_name": "ИмяСотрудника",
    "last_name": "Тест_создание_АПИ",
    "position_id": 45,
    "role_id": 273,
    "short_phone": "10077",
    "email": "112222200000@vats1200054.cp.megafon.ru",
    "sim_number_capacity_id": 548,
    "dialing_type": "first_sip",
    "delay": 5,
    "phone": "79105500323",
    "is_phone_dialing_enabled": true,
    "phone_dialing_type": "dialing_rule",
    "phone_delay": 20,
    "login": "testapi1200054@vats1200054.cp.megafon.ru",
    "password": "123456Mm"
}
```

## Cтруктура ответа

```json
{
    "first_name": "Имя",
    "last_name": "Фамилия",
    "position_id": 45,
    "role_id": 273,
    "short_phone": "12345",
    "email": "email@megafon.ru",
    "sim_number_capacity_id": 354,
    "dialing_type": "first_virtual_number",
    "delay": 5,
    "phone": "79201234567",
    "is_phone_dialing_enabled": true,
    "phone_dialing_type": "dialing_rule",
    "phone_delay": 30,
    "id": 315,
    "is_sip_registered": false,
    "photo_link": null,
    "password": "123456Mm",
    "login": "login@vats1200054.cp.megafon.ru"
}
```