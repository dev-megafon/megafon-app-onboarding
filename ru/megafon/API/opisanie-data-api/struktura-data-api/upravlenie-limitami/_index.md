---
order: 17
title: Ограничения звонков
---

:::info 

URL для доступа к API: <https://simple-api.cp.megafon.ru>

:::

## Ограничения звонков - общие правила

Метод `/limitations/main `используется для определения ограничений звонков для всех сотрудников. Он позволяет установить, какие направления звонков будут доступны для сотрудников всей компании, таких как “Звонки на мобильные”, “Междугородние звонки”, “Спутниковые звонки” и “Международные звонки.

{% table %}

---

*  {% colwidth=[253] isHeader=true %}

   Метод

*  {% colwidth=[529] isHeader=true %}

   Описание

---

*  {% colwidth=[253] isHeader=true %}

   [Получить настройки правила ограничения звонков для всех сотрудников](./ogranichenie-zvonkov-obschie-pravila/limitations-main)

*  {% colwidth=[529] %}

   Метод  позволяет извлекать текущие параметры и настройки, касающиеся прав доступа пользователей к ресурсам системы.

---

*  {% colwidth=[253] isHeader=true %}

   [Редактировать настройку правила ограничения звонков для всех сотрудников](./ogranichenie-zvonkov-obschie-pravila/redaktirovat-nastroyku-pravila-ogranicheniya-zvon)

*  {% colwidth=[529] %}

   Метод внесения изменений в уже существующие правила,  ограничения на звонки для всех сотрудников

{% /table %}

## Ограничения звонков - персональные правила

Метод `/limitations/personal `используется для установки ограничений доступов конкретных пользователей. Он позволяет управлять доступом в зависимости от различных условий, таких как мобильный доступ, международные или внутренние ограничения, а также доступ для определённых сотрудников и групп.

{% table %}

---

*  {% colwidth=[253] isHeader=true %}

   Метод

*  {% colwidth=[529] isHeader=true %}

   Описание

---

*  {% colwidth=[253] isHeader=true %}

   [Получить список персональных правил для ограничения звонков](./limitations-personal/poluchit-spisok-personalnykh-pravil-dlya-ogranich)

*  {% colwidth=[529] %}

   Метод извлечения всех существующих правил, установленных пользователем для ограничения  звонков.

---

*  {% colwidth=[253] isHeader=true %}

   [Создать список персональных правил для ограничения звонков](./limitations-personal/sozdat-spisok-personalnykh-pravil-dlya-ogranichen)

*  {% colwidth=[529] %}

   Метод добавления нового правила, регулирующего ограничения звонков.

---

*  {% colwidth=[253] isHeader=true %}

   [Редактировать список персональных правил для ограничения звонков](./limitations-personal/redaktirovat-spisok-personalnykh-pravil-dlya-ogra)

*  {% colwidth=[529] %}

   Метод внесения изменений в уже существующие правила,  ограничения на звонки.

---

*  {% colwidth=[253] isHeader=true %}

   [Удалить список персональных правил для ограничения звонков](./limitations-personal/udalit-spisok-personalnykh-pravil-dlya-ogranichen)

*  {% colwidth=[529] %}

   Метод для удаления  персональных правил сотрудников или отделов для ограничения звонков.

---

*  {% colwidth=[253] isHeader=true %}

   [Поиск международных id стран](./metod-pomogaet-nayti-id-stran-dlya-nastrpoyki-pra)

*  {% colwidth=[529] %}

   Метод для  получения уникальных идентификаторов стран.

{% /table %}

## Международные id стран

Метод `GET /limitations/region?_order=asc&_sort=name&type=country ` помогает найти id стран для настройки правил ограничения звонков для международных звонков.

{% table %}

---

*  {% colwidth=[253] isHeader=true %}

   Метод

*  {% colwidth=[529] isHeader=true %}

   Описание

---

*  {% colwidth=[253] isHeader=true %}

   [Поиск международных id стран](./metod-pomogaet-nayti-id-stran-dlya-nastrpoyki-pra)

*  {% colwidth=[529] %}

   Метод для  получения уникальных идентификаторов стран.

{% /table %}
