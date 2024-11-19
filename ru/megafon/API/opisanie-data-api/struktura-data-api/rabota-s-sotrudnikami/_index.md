---
order: 1
title: Управление сотрудниками
---

:::info 

URL для доступа к API: <https://simple-api.cp.megafon.ru>

:::

Метод: `/employee` метод позволяет создавать, обновлять или получать информацию о сотрудниках в системе.

### Cотрудники

{% table %}

---

*  {% colwidth=[241] isHeader=true %}

   Метод

*  {% colwidth=[529] isHeader=true %}

   Описание

---

*  {% colwidth=[241] isHeader=true %}

   [Получить список всех сотрудников в системе](./get-employee)

*  {% colwidth=[529] %}

   Запрос возвращает список всех сотрудников в системе.

---

*  {% colwidth=[241] isHeader=true %}

   [Получить информацию о сотруднике](./get-employee-id)

*  {% colwidth=[529] %}

   Запрос возвращает информацию о сотруднике.

---

*  {% colwidth=[241] isHeader=true %}

   [Создать нового сотрудника](./post-employee)

*  {% colwidth=[529] %}

   Запрос создает нового сотрудника.

---

*  {% colwidth=[241] isHeader=true %}

   [Обновить информации о сотруднике](./put-employee)

*  {% colwidth=[529] %}

   Запрос обновляет информацию о сотруднике.

---

*  {% colwidth=[241] isHeader=true %}

   [Удалить сотрудника](./delete-empoyee-id)

*  {% colwidth=[529] %}

   Удаление сотрудника.

{% /table %}

### Роли

Метод `/role `предназначен для работы с ролями в системе. Он позволяет получить или изменить информацию о ролях, связанных с определёнными пользователями или функциями.

{% table %}

---

*  {% colwidth=[241] isHeader=true %}

   Метод

*  {% colwidth=[529] isHeader=true %}

   Описание

---

*  {% colwidth=[241] isHeader=true %}

   [Получить список всех ролей](./poluchenie-spiska-dostupnykh-roley)

*  {% colwidth=[529] %}

   Получение списка всех ролей в системе.

---

*  {% colwidth=[241] isHeader=true %}

   [Получить  роль](./get-role-id)

*  {% colwidth=[529] %}

   Запрос возвращает информацию о роли.

---

*  {% colwidth=[241] isHeader=true %}

   [Получить параметры роли по имени роли](./get-role-name-name)

*  {% colwidth=[529] %}

   Запрос возвращает информацию о роли по её названию.

{% /table %}

### Должности

{% table %}

---

*  {% colwidth=[247] isHeader=true %}

   Метод

*  {% colwidth=[529] isHeader=true %}

   Описание

---

*  {% colwidth=[247] isHeader=true %}

   [Получить список всех должностей](./rabota-so-spiskom-dostupnykh-dolzhnostey)

*  {% colwidth=[529] %}

   Получение списка всех доступных должностей.

---

*  {% colwidth=[247] isHeader=true %}

   [Получить должность](./poluchenie-konkretnoy-pozicii-po-id)

*  {% colwidth=[529] %}

   Запрос возвращает информацию о должности.

---

*  {% colwidth=[247] isHeader=true %}

   [Получить должность по имени](./poisk-po-imeni-pozicii)

*  {% colwidth=[529] %}

   Запрос возвращает информацию о должности по её имени.

---

*  {% colwidth=[247] isHeader=true %}

   [Создать должность](./sozdanie-novoy-pozicii)

*  {% colwidth=[529] %}

   Запрос создает новую должность по заданным параметрам.

{% /table %}
