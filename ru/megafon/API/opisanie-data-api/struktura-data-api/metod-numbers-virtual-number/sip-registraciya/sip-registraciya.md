---
order: 0.5
title: Добавить/создать номер (SIP-регистрация)
---

### `POST /numbers/virtual-number`

**Описание:** метод для регистрации нового SIP-номера в системе.

## Параметры метода

{% table %}

---

*  {% colwidth=[108] isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% isHeader=true %}

   Обязательный

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[108] isHeader=true %}

   number

*  string

*  Да

*  

*  Виртуальный номер телефона

---

*  {% colwidth=[108] isHeader=true %}

   login

*  string

*  Да

*  

*  Логин аккаунта для регистрации номера

---

*  {% colwidth=[108] isHeader=true %}

   password

*  string

*  Да

*  

*  Пароль аккаунта для регистрации номера

---

*  {% colwidth=[108] isHeader=true %}

   server_host

*  string

*  Да

*  

*  URL сервера для регистрации номера

---

*  {% colwidth=[108] isHeader=true %}

   server_port

*  string

*  Да

*  

*  Порт сервера для регистрации номера

---

*  {% colwidth=[108] isHeader=true %}

   purpose

*  string

*  Да

*  `сompany`

*  Назначение Виртуального номера

---

*  {% colwidth=[108] isHeader=true %}

   type

*  string

*  Да

*  `sip_registration`

*  Тип виртуального номера

---

*  {% colwidth=[108] isHeader=true %}

   comment

*  string

*  Нет

*  

*  Комментарий

{% /table %}

## Cтруктура запроса

```json
{
  "number": "74872003333",
  "login": "login",
  "password": "password",
  "server_host": "195.211.120.35",
  "server_port": 5060,
  "purpose": "company",
  "type": "sip_registration"
  "comment": "Заметка",
}
```

## Cтруктура ответа

```json
{
  "number": "74872003333",
  "login": "login",
  "password": "password",
  "server_host": "195.211.120.35",
  "server_port": 5060,
  "purpose": "company",
  "type": "sip_registration"
  "comment": "Заметка",
  "id": 51
}
```