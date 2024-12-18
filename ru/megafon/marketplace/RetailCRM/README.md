## Интеграция с  RetailCRM <br />

Решение позволяет интегрировать функционал телефонии и передавать данные по звонкам из нашего Личного кабинета в RetailCRM.<br /> 

**Возможности интеграции**  <br />

- всплывающие уведомления о входящих звонках;
- звонок в один клик из RetailCRM;
- сохранение истории и записей звонков в RetailCRM.

<br />
<br />
<br />


## Подключение интеграции  <br />

1. Укажите **Учетные данные** <br />

- если ранее добавляли учетные данные RetailCRM, то выберите их из списка;
- если нет, то нажмите **Подключить учетную запись** и заполните значения:
    - название;
    - URL (домен RetailCRM ) в формате YOURDOMAIN.retailcrm.ru , часть 'YOURDOMAIN' у каждого клиента уникальна;
    - API key - ключ API RetailCRM (Настройки - > Интеграция → Ключи доступа к API -> Добавить).  <br />
    
Создайте новый ключ с доступом ко всем магазинам и методам. Добавьте данный ключ в настройки интеграции. <br />

<br /> 

![image](retailCRM.gif)

<br />

После добавления учетных данных на странице появятся **Параметры интеграции**.

<br />

2. **Фильтровать по виртуальным номерам** - выберите настройку, если требуется фильтрация по виртуальным номерам (в случае подключения нескольких интеграций CRM). <br /> 

При нажатии будет выведена дополнительная настройка с выбором виртуальных номеров. <br />

**Список виртуальных номеров** - укажите виртуальные номера, по которым необходимо отображать данные по звонкам в RetailCRM. <br /> 

3. **Сопоставьте пользователей** - укажите соответствие сотрудников из RetailCRM и МегаФон. <br /> 

4. **Ответственный по умолчанию** - если звонок потерян или поступил на сотрудника, который отсутствует в RetailCRM, то выбранный сотрудник будет назначен ответственным при автоматическом создании контакта.<br />


5. Выберите дополнительный функционал обработки звонков, при необходимости: <br /> 

- включить переадресацию на персонального менеджера; <br />

**Важно**: переадресация на персонального менеджера из CRM будет работать при настроенном сценарии с соответствующей операцией в ЛК МегаФон, а также при настроенном сопоставлении в п.3. <br /> 

 - создавать контакт при исходящем звонке на неизвестный номер; <br />

 - создавать контакт при входящем звонке с неизвестного номера.

<br /> 

6. Заполните сопоставление магазинов в RetailCRM и виртуального номера АТС . <br />  
Это потребуется при создании контакта и отображении магазина в статистике по звонкам. <br />

7. Активируйте интеграцию. <br /> 

8. Нажмите **Сохранить**


Для проверки работы интеграции на тестовых звонках проверьте работу пунктов, указанных в разделе **Возможности интеграции**.
