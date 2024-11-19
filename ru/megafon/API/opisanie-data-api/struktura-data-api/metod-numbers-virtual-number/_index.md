---
order: 2.5
title: Управление виртуальными номерами
---

:::info 

URL для доступа к API: <https://simple-api.cp.megafon.ru>

:::

Метод `/numbers/virtual-number` используется для управления виртуальными номерами в системе, включая их назначение, сценарии использования и состояние

{% table %}

---

*  {% isHeader=true %}

   Метод

*  {% colwidth=[535] isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   [Получить список всех виртуальных номеров](./poluchenie-spiska-vsekh-cuschestvuyuschikh-virtua)

*  {% colwidth=[535] %}

   Получение списка всех имеющихся виртуальных номеров.

---

*  {% isHeader=true %}

   [Поиск виртуального номера](./poisk-konkretnogo-virtualnogo-nomera-po-id)

*  {% colwidth=[535] %}

   Получение информации о виртуальном номере по его уникальному идентификатору.

---

*  {% isHeader=true %}

   [Поиск виртуального номера по его параметрам](./vyvod-parametrov-virtualnogo-nomera-po-ego-znache/_index)

*  {% colwidth=[535] %}

   Получение параметров виртуального номера по заданным критериям.

---

*  {% colspan=2 colwidth=[0,535] isHeader=true %}

   SIP-регистрация и SIP-переадрессация

---

*  {% isHeader=true %}

   [Добавить/создать номер (SIP-регистрация)](./sip-registraciya/sip-registraciya)

*  {% colwidth=[535] %}

   Метод для регистрации нового SIP-номера в системе.

---

*  {% isHeader=true %}

   [Добавить/создать номер (SIP-переадрессация)](./sip-registraciya/dobavit-sozdat-nomer-sip-pereadressaciya)

*  {% colwidth=[535] %}

   Метод для создания нового номера с настройкой переадресации вызовов на другой номер или устройство, позволяющий перенаправлять входящие звонки.

---

*  {% colspan=2 colwidth=[0,535] isHeader=true %}

   Редактировать виртуальный номер

---

*  [Редактировать мобильный номер](./obnovlenie-informacii-o-virtualnom-nomere-po-ego/redaktirovat-mobilnyy-nomer)

*  {% colwidth=[535] %}

   Метод для изменения информации о зарегистрированном мобильном номере.

---

*  [Редактировать городской номер](./obnovlenie-informacii-o-virtualnom-nomere-po-ego/redaktirovat-gorodskoy-nomer)

*  {% colwidth=[535] %}

   Метод для изменения параметров городского номера.

---

*  [Редактировать номера других операторов Sip-регистрации](./obnovlenie-informacii-o-virtualnom-nomere-po-ego/redaktirovat-nomera-drugikh-operatorov-sip-peread)

*  {% colwidth=[535] %}

   Метод для изменения настроек SIP-регистрации для номеров, принадлежащих другим операторам.

---

*  [Редактировать номера других операторов Sip-переадрессации](./obnovlenie-informacii-o-virtualnom-nomere-po-ego/redaktirovat-nomera-drugikh-operatorov-sip-peread-2)

*  {% colwidth=[535] %}

   Метод для изменения настроек переадресации для номеров других операторов.

{% /table %}
