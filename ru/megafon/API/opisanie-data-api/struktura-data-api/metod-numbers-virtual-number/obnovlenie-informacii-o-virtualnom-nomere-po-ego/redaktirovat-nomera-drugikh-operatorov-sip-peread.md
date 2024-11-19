---
order: 0.9
title: Редактировать номера других операторов Sip-регистрации
---

### `PUT /numbers/virtual-number/{id}`

**Описание:** Обновление информации о номере других операторов Sip-регистрации по его уникальному идентификатору.

## Параметры метода

{% table %}

---

*  {% colwidth=[117] isHeader=true %}

   Название

*  {% colwidth=[144] isHeader=true %}

   Тип

*  {% colwidth=[198] isHeader=true %}

   Обязательный

*  {% colwidth=[152] isHeader=true %}

   Допустимые значения

*  {% colwidth=[152] isHeader=true %}

   Описание

---

*  {% colwidth=[117] isHeader=true %}

   login

*  {% colwidth=[144] %}

   string

*  {% colwidth=[198] %}

   Нет

*  {% colwidth=[152] %}

   

*  {% colwidth=[152] %}

   Логин аккаунта для регистрации номера

---

*  {% colwidth=[117] isHeader=true %}

   password

*  {% colwidth=[144] %}

   string

*  {% colwidth=[198] %}

   Нет

*  {% colwidth=[152] %}

   

*  {% colwidth=[152] %}

   Пароль аккаунта для регистрации номера

---

*  {% colwidth=[117] isHeader=true %}

   server_host

*  {% colwidth=[144] %}

   string

*  {% colwidth=[198] %}

   Нет

*  {% colwidth=[152] %}

   

*  {% colwidth=[152] %}

   URL сервера для регистрации номера

---

*  {% colwidth=[117] isHeader=true %}

   server_port

*  {% colwidth=[144] %}

   string

*  {% colwidth=[198] %}

   Нет

*  {% colwidth=[152] %}

   

*  {% colwidth=[152] %}

   Порт сервера для регистрации номера

---

*  {% colwidth=[117] isHeader=true %}

   purpose

*  {% colwidth=[144] %}

   string

*  {% colwidth=[198] %}

   Да

*  {% colwidth=[152] %}

   `сompany`

*  {% colwidth=[152] %}

   Назначение Виртуального номера

---

*  {% colwidth=[117] isHeader=true %}

   comment

*  {% colwidth=[144] %}

   string

*  {% colwidth=[198] %}

   Нет

*  {% colwidth=[152] %}

   

*  {% colwidth=[152] %}

   Комментарий

---

*  {% colwidth=[117] isHeader=true %}

   id

*  {% colwidth=[144] %}

   integer

*  {% colwidth=[198] %}

   Да

*  {% colwidth=[152] %}

   Положительное число

*  {% colwidth=[152] %}

   

   Уникальный идентификатор виртуального номера.

{% /table %}

## Структура запроса

`DELETE /numbers/virtual-number/101`

```json
{
  "login": "login",
  "password": "password123",
  "comment": "Заметка по АПИ",
  "purpose": "company",
  "server_host": "195.211.120.35",
  "server_port": 5060,
  "id": 608
}
```

## **Структура ответа**

```json
{
  "login": "login",
  "password": "password123",
  "comment": "Заметка по АПИ",
  "purpose": "company",
  "server_host": "195.211.120.35",
  "server_port": 5060,
  "id": 608
}
```

### 