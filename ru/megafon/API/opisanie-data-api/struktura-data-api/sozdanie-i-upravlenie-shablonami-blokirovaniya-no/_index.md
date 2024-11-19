---
order: 8
title: Черный список
---

:::info 

URL для доступа к API: <https://simple-api.cp.megafon.ru>

:::

Метод `/black-nums/mask` используется для добавления и удаления номеров в/из списка черный список, для возможности блокировки звонков от абонентов с нежелательных номеров и масок.

{% table %}

---

*  {% colwidth=[251] isHeader=true %}

   Метод

*  {% colwidth=[529] isHeader=true %}

   Описание

---

*  {% colwidth=[251] isHeader=true %}

   [Получить маски для номеров из черного списка](./poluchenie-spiska-masok-dlya-nomerov-iz-chernogo)

*  {% colwidth=[529] %}

   Метод позволяет получить список масок (шаблонов) номеров, которые находятся в черном списке.

---

*  {% colwidth=[251] isHeader=true %}

   [Добавить номер или диапазон номера в черный список](./dobavit-nomer-ili-diapazon-nomera-v-chernyy-spiso)

*  {% colwidth=[529] %}

   Метод предназначен для добавления одного номера или диапазона номеров в черный список.

---

*  {% colwidth=[251] isHeader=true %}

   [Удалить номера или диапазоны номеров из черного списка](./udalit-nomera-ili-diapazony-nomerov-iz-chernogo-s)

*  {% colwidth=[529] %}

   Метод позволяет удалить указанные номера или диапазоны номеров из черного списка.

{% /table %}

## Управление настройками блокировки анонимных номеров в системе

Метод `/black-nums/settings` предназначен для управления настройками блокировки звонков с анонимных номеров..

:::info 

URL для доступа к API: <https://simple-api.cp.megafon.ru>

:::

{% table %}

---

*  {% colwidth=[251] isHeader=true %}

   Метод

*  {% colwidth=[529] isHeader=true %}

   Описание

---

*  {% colwidth=[251] isHeader=true %}

   [Получить состояние настройки  опции блокировки звонков с анонимных номеров](./blokirovka-zvonkov-s-anonimnykh-nomerov)

*  {% colwidth=[529] %}

   Метод позволяет узнать текущее состояние опции блокировки звонков с анонимных номеров.

---

*  {% colwidth=[251] isHeader=true %}

   [Включить опцию блокировки звонков с анонимных номеров](./vklyuchit-opciyu-blokirovki-zvonkov-s-anonimnykh)

*  {% colwidth=[529] %}

   Метод предназначен для активации функции блокировки звонков от анонимных номеров.

---

*  {% colwidth=[251] isHeader=true %}

   [Отключить опцию блокировки звонков с анонимных номеров](./otklyuchit-opciyu-blokirovki-zvonkov-s-anonimnykh)

*  {% colwidth=[529] %}

   Метод позволяет деактивировать функцию блокировки звонков от анонимных номеров

{% /table %}
