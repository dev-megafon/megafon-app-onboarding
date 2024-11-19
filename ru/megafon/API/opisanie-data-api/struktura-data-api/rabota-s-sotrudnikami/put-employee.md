---
order: 0.9
title: Редактировать сотрудника
---

### `PUT /employee/{id}`

**Описание**: этот метод обновляет информацию о сотруднике с указанным ID. Все поля в теле запроса могут быть изменены.

## Параметры метода

{% table %}

---

*  {% colwidth=[196] isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% colwidth=[139] isHeader=true %}

   Допустимые значения

*  {% colwidth=[127] isHeader=true %}

   Обязательный

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[196] isHeader=true %}

   first_name

*  string

*  {% colwidth=[139] %}

   --

*  {% colwidth=[127] %}

   Нет

*  Имя пользователя.

---

*  {% colwidth=[196] isHeader=true %}

   last_name

*  string

*  {% colwidth=[139] %}

   --

*  {% colwidth=[127] %}

   Да

*  Фамилия пользователя.

---

*  {% colwidth=[196] isHeader=true %}

   login

*  string

*  {% colwidth=[139] %}

   --

*  {% colwidth=[127] %}

   Да

*  Логин сотрудника. **Внимание**!  Его нельзя изменить.

---

*  {% colwidth=[196] isHeader=true %}

   password

*  string

*  {% colwidth=[139] %}

   --

*  {% colwidth=[127] %}

   Да

*  Пароль сотрудника.

---

*  {% colwidth=[196] isHeader=true %}

   position_id

*  integer

*  {% colwidth=[139] %}

   --

*  {% colwidth=[127] %}

   Да

*  Идентификатор должности.

---

*  {% colwidth=[196] isHeader=true %}

   role_id

*  integer

*  {% colwidth=[139] %}

   --

*  {% colwidth=[127] %}

   Да

*  Идентификатор роли.

---

*  {% colwidth=[196] isHeader=true %}

   short_phone

*  string

*  {% colwidth=[139] %}

   --

*  {% colwidth=[127] %}

   Да

*  Внутренний номер телефона.

---

*  {% colwidth=[196] isHeader=true %}

   email

*  string

*  {% colwidth=[139] %}

   --

*  {% colwidth=[127] %}

   Нет (обязательно если роль “Администратор”)

*  Электронная почта пользователя.

---

*  {% colwidth=[196] isHeader=true %}

   sim_number_capacity_id

*  integer

*  {% colwidth=[139] %}

   --

*  {% colwidth=[127] %}

   Нет

*  Идентификатор рабочей SIM-карты.

---

*  {% colwidth=[196] isHeader=true %}

   dialing_type

*  string

*  {% colwidth=[139] %}

   `parallel`, `first_sip`, `first_virtual_number`

*  {% colwidth=[127] %}

   Да, если заполнен параметр “`sim_number_capacity_id`”

*  Настройка «Звонить на рабочие номера» (по умолчанию: `parallel`).

---

*  {% colwidth=[196] isHeader=true %}

   delay

*  integer

*  {% colwidth=[139] %}

   5, 10, 15, 20, 25, 30

*  {% colwidth=[127] %}

   Да/ если в параметре “`dialing_type`” выбраны “`first_sip`”, “`first_virtual_number`”

*  Дозвон на второе устройство через заданное время.

---

*  {% colwidth=[196] isHeader=true %}

   phone

*  string

*  {% colwidth=[139] %}

   --

*  {% colwidth=[127] %}

   Нет

*  Личный мобильный номер.

---

*  {% colwidth=[196] isHeader=true %}

   is_phone_dialing_enabled

*  boolean

*  {% colwidth=[139] %}

   --

*  {% colwidth=[127] %}

   Да ( если заполнен параметр «`phone`)

*  Включен ли набор номера на личный мобильный (по умолчанию: `false`).

---

*  {% colwidth=[196] isHeader=true %}

   phone_dialing_type

*  string

*  {% colwidth=[139] %}

   `dialing_rule`, `only_phone`

*  {% colwidth=[127] %}

   Да, если параметр “`is_phone_dialing_enabled`” заполнен как “`True`”

*  Тип набора номера по телефону (по умолчанию: `dialing_rule`).

---

*  {% colwidth=[196] isHeader=true %}

   phone_delay

*  integer

*  {% colwidth=[139] %}

   0, 5, 10, 15, 20, 25, 30

*  {% colwidth=[127] %}

   Да, если параметр “`phone_dialing_type`” заполнен как “`dialing_rule`”

*  Задержка звонка на мобильный.

---

*  {% colwidth=[196] isHeader=true %}

   id

*  integer

*  {% colwidth=[139] %}

   --

*  {% colwidth=[127] %}

   Да

*  Уникальный идентификатор сотрудника.

---

*  {% colwidth=[196] isHeader=true %}

   is_sip_registered

*  boolean

*  {% colwidth=[139] %}

   --

*  {% colwidth=[127] %}

   \-

*  Зарегистрирован ли SIP.

---

*  {% colwidth=[196] isHeader=true %}

   photo_link

*  string

*  {% colwidth=[139] %}

   --

*  {% colwidth=[127] %}

   Нет

*  Ссылка на фотографию пользователя.

---

*  {% colwidth=[196] isHeader=true %}

   app_id

*  integer

*  {% colwidth=[139] %}

   Да

*  {% colwidth=[127] %}

   \-

*  Идентификатор Личного кабинета

{% /table %}

## Cтруктура запроса

```json
PUT /employee/317


{
    "first_name": "Имя",
    "last_name": "Фамилия",
    "position_id": 45,
    "role_id": 273,
    "short_phone": "12345",
    "email": "email@megafon.ru",
    "sim_number_capacity_id": 464,
    "dialing_type": "first_sip",
    "delay": 15,
    "login": "login@vats1200054.cp.megafon.ru",
    "phone": "79201234567",
    "is_phone_dialing_enabled": true,
    "phone_dialing_type": "dialing_rule",
    "phone_delay": 25,
    "id": 317,
    "app_id": 1200054
}
```

## Cтруктура ответа

Возвращает сообщение с настройками

```json
{
    "first_name": "Имя",
    "last_name": "Фамилия",
    "position_id": 45,
    "role_id": 273,
    "short_phone": "12345",
    "email": "email@megafon.ru",
    "sim_number_capacity_id": 464,
    "dialing_type": "first_sip",
    "delay": 15,
    "phone": "79201234567",
    "is_phone_dialing_enabled": true,
    "phone_dialing_type": "dialing_rule",
    "phone_delay": 25,
    "id": 317,
    "is_sip_registered": false,
    "photo_link": null,
    "login": "login@vats1200054.cp.megafon.ru",
    "role": "employee",
    "sim_phone": "79263169708",
    "app_id": 1200054,
    "full_name": "Фамилия Имя",
    "role_name": "Администратор",
    "user_id": 357,
    "position_name": "Test"
}
```