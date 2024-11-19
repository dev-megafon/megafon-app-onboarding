---
order: 1
title: Получить список всех звонков
---

### `get_mgf_calls`

**Описание**: метод позволяет получить историю звонков

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% colwidth=[137] isHeader=true %}

   Обязательный

*  {% colwidth=[215] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   report_id

*  number

*  {% colwidth=[137] %}

   да

*  {% colwidth=[215] %}

   Уникальный идентификатор отчета пользователя. Для получения списка отчетов пользователей необходимо использовать метод `get.reportslist.`

*  Уникальный идентификатор отчета пользователя.

---

*  {% isHeader=true %}

   date_from

*  iso8601

*  {% colwidth=[137] %}

   да

*  {% colwidth=[215] %}

   YYYY-MM-DD hh:mm:ss

*  Дата начала основной выборки (ограничение 366 дней).

---

*  {% isHeader=true %}

   date_till

*  iso8601

*  {% colwidth=[137] %}

   да

*  {% colwidth=[215] %}

   YYYY-MM-DD hh:mm:ss

*  Дата окончания основной выборки.

---

*  {% isHeader=true %}

   fields

*  array

*  {% colwidth=[137] %}

   Да

*  {% colwidth=[215] %}

   «`communication_id`»

   «`call_start_date`»

   «`call_start_time`»

   «`contact_phone_number`»

   «`call_direction`»

   «`call_status`»

   «`call_type`»

   «`virtual_phone_number`»

   «`employees`»

   «`call_total_duration`»

   «`call_await_talk_duration`»

   «`call_talk_duration`»

   «`call_is_internal`»

   «`call_finish_reason`»

   «`employee_rating`»

   «`call_records`»

   «`communication_comment`»

   «`communication_comment_author`»

   «`received_call`»

   «`first_employee_for_internal_call`»

   «`second_employee_for_internal_call`»

   «`call_finish_date_time`»

   «`coaches`»

   «`is_coach_handled_call`»

   «`virtual_number_comment`»

   «`is_blacklisted_phone`»

   «`call_start_date_time`»

   «`call_is_internal`»

   «`tags`»

   «`call_processed_mark_duration`»

*  Список идентификаторов пользовательских столбцов, разделенных запятой.

---

*  {% isHeader=true %}

   filter

*  object

*  {% colwidth=[137] %}

   нет

*  {% colwidth=[215] %}

   Допустимо использовать не более 2 уровней вложенности. Смотри примеры ниже

*  Фильтры, применяемые в отчете. Логика построения аналогична «Критерии фильтрации».

---

*  {% isHeader=true %}

   filters

*  array

*  {% colwidth=[137] %}

   Да, если применяется фильтрация(используется параметр “`filter`”)

*  {% colwidth=[215] %}

   Выражение, может содержать как простые фильтры, так и дерево фильтров.

*  Список фильтров, применяемых в отчете.

---

*  {% isHeader=true %}

   field

*  string

*  {% colwidth=[137] %}

   

*  {% colwidth=[215] %}

   Поле сущности, к которой будет применяться фильтрация (список заранее определён для метода).

*  Поле сущности для фильтрации.

---

*  {% isHeader=true %}

   operator

*  enum

*  {% colwidth=[137] %}

   \-

*  {% colwidth=[215] %}

   \-

*  Оператор фильтрации. Список всех операторов можно получить в разделе «Операторы фильтрации»

---

*  {% isHeader=true %}

   value

*  string

*  {% colwidth=[137] %}

   \-

*  {% colwidth=[215] %}

   \-

*  Значение для оператора фильтрации. Необязательное поле, если оно отсутствует, то считается пустота.

{% /table %}

## Структура запроса:

```json
{
  "jsonrpc":"2.0",
  "id":"number",
  "method":"get.mgf_calls",
  "params":{
    "report_id": 1015,
    "date_from": "2024-10-21 00:00:00",
    "date_till": "2024-10-21 23:59:59",
    "fields": [
        "communication_id",
        "call_start_date",
        "call_start_time",
        "contact_phone_number",
        "call_direction",
        "call_status",
        "call_type",
        "virtual_phone_number",
        "employees",
        "call_total_duration",
        "call_await_talk_duration",
        "call_talk_duration",
        "call_is_internal",
        "call_finish_reason",
        "employee_rating",
        "call_records",
        "communication_comment",
        "communication_comment_author",
        "received_call",
        "first_employee_for_internal_call",
        "second_employee_for_internal_call",
        "call_finish_date_time",
        "coaches",
        "is_coach_handled_call",
        "virtual_number_comment",
        "is_blacklisted_phone",
        "call_start_date_time",
        "call_is_internal",
        "tags",
        "call_processed_mark_duration"
        ]
  }
}
 
```

### Параметры ответа

{% table %}

---

*  {% colwidth=[202] isHeader=true %}

   Название

*  {% colwidth=[86] isHeader=true %}

   Тип

*  {% colwidth=[125] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Фильтрация

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[202] isHeader=true %}

   communication_id

*  {% colwidth=[86] %}

   string

*  {% colwidth=[125] %}

   

*  да

*  Уникальный идентификатор Звонка.ID сессии звонка

---

*  {% colwidth=[202] isHeader=true %}

   call_start_date

*  {% colwidth=[86] %}

   iso8601

*  {% colwidth=[125] %}

   `YYYY-MM-DD`

*  да

*  Дата звонка

---

*  {% colwidth=[202] isHeader=true %}

   call_start_time

*  {% colwidth=[86] %}

   iso8601

*  {% colwidth=[125] %}

   `hh:mm:ss`

*  да

*  Время звонка

---

*  {% colwidth=[202] isHeader=true %}

   contact_phone_number

*  {% colwidth=[86] %}

   string

*  {% colwidth=[125] %}

   

*  да

*  Номер Клиента от которого поступил звонок в случае входящего звонка или номер контакта на который совершили звонок в случае исходящего звонка.

---

*  {% colwidth=[202] isHeader=true %}

   call_direction

*  {% colwidth=[86] %}

   object

*  {% colwidth=[125] %}

   `Входящий звонок`/`Исходящий звонок`

*  да

*  Направление звонка

---

*  {% colwidth=[202] isHeader=true %}

   call_status

*  {% colwidth=[86] %}

   object

*  {% colwidth=[125] %}

   `Потерянный`/`Принятый`

*  да

*  Статус звонка

---

*  {% colwidth=[202] isHeader=true %}

   call_type

*  {% colwidth=[86] %}

   object

*  {% colwidth=[125] %}

   `Звонок ВАТС`\
   `Исходящий с SIP`\
   `Исходящий с FMC`\
   `Call API` `Базовый набор`”\
   `amoCRM`\
   `Bitrix24`\
   `Megaplan`\
   `retailCRM`\
   `Лидогенератор`\
   `Омниканальный виджет`\
   `Партнёрская интеграция`\
   `Сайтфон`\
   и т.д

*  да

*  Тип звонка

---

*  {% colwidth=[202] isHeader=true %}

   virtual_phone_number

*  {% colwidth=[86] %}

   string

*  {% colwidth=[125] %}

   

*  да

*  Виртуальный номер/Через номер

---

*  {% colwidth=[202] isHeader=true %}

   employees

*  {% colwidth=[86] %}

   array

*  {% colwidth=[125] %}

   

*  да

*  Сотрудники, которые участвовали в звонке

---

*  {% colwidth=[202] isHeader=true %}

   call_total_duration

*  {% colwidth=[86] %}

   iso8601

*  {% colwidth=[125] %}

   hh:mm:ss

*  да

*  Длительность звонка

---

*  {% colwidth=[202] isHeader=true %}

   call_await_talk_duration

*  {% colwidth=[86] %}

   iso8601

*  {% colwidth=[125] %}

   hh:mm:ss

*  да

*  Длительность ожидания начала разговора

---

*  {% colwidth=[202] isHeader=true %}

   call_talk_duration

*  {% colwidth=[86] %}

   iso8601

*  {% colwidth=[125] %}

   hh:mm:ss

*  да

*  Длительность разговора

---

*  {% colwidth=[202] isHeader=true %}

   call_is_internal

*  {% colwidth=[86] %}

   string

*  {% colwidth=[125] %}

   Внешний/Внутренний

*  да

*  Внешний/внутренний

---

*  {% colwidth=[202] isHeader=true %}

   call_finish_reason

*  {% colwidth=[86] %}

   object

*  {% colwidth=[125] %}

   `Абонент положил трубку`;\
   `Вызов перенаправлен`;\
   `Не дозвонились до абонента`;\
   `Не дозвонились до сотрудника`;\
   `Сотрудник разорвал соединение;`\
   `и т.д`

*  да

*  Результат/Причина завершения звонка

---

*  {% colwidth=[202] isHeader=true %}

   employee_rating

*  {% colwidth=[86] %}

   numeric

*  {% colwidth=[125] %}

   

*  да

*  Рейтинг на звонке

---

*  {% colwidth=[202] isHeader=true %}

   call_records

*  {% colwidth=[86] %}

   array

*  {% colwidth=[125] %}

   

*  да

*  Уникальный идентификатор ссылки на записанный разговор.

---

*  {% colwidth=[202] isHeader=true %}

   communication_comment

*  {% colwidth=[86] %}

   string

*  {% colwidth=[125] %}

   

*  да

*  Комментарий

---

*  {% colwidth=[202] isHeader=true %}

   communication_comment_author

*  {% colwidth=[86] %}

   string

*  {% colwidth=[125] %}

   

*  да

*  Автор комментария

---

*  {% colwidth=[202] isHeader=true %}

   received_call

*  {% colwidth=[86] %}

   string

*  {% colwidth=[125] %}

   

*  да

*  Кто принял/совершил звонок. Последняя операция во входящем пропущенном звонке или первый ответивший /первый сотрудник в исходящем

---

*  {% colwidth=[202] isHeader=true %}

   first_employee_for_internal_call

*  {% colwidth=[86] %}

   string

*  {% colwidth=[125] %}

   

*  да

*  Инициатор звонка. Только для внутренних звонков

---

*  {% colwidth=[202] isHeader=true %}

   second_employee_for_internal_call

*  {% colwidth=[86] %}

   string

*  {% colwidth=[125] %}

   

*  да

*  Кому звонил. Только для внутренних звонков

---

*  {% colwidth=[202] isHeader=true %}

   call_finish_date_time

*  {% colwidth=[86] %}

   iso8601

*  {% colwidth=[125] %}

   `YYYY-MM-DD hh:mm:ss`

*  да

*  Время завершения звонка

---

*  {% colwidth=[202] isHeader=true %}

   coaches

*  {% colwidth=[86] %}

   array

*  {% colwidth=[125] %}

   

*  да

*  ФИО сотрудника, который являлся тренером у сотрудника, участвовавшего в звонке

---

*  {% colwidth=[202] isHeader=true %}

   is_coach_handled_call

*  {% colwidth=[86] %}

   object

*  {% colwidth=[125] %}

   

*  да

*  Статус подключения тренера. Показывает, что в звонке в одном из вызовов был участвовал Тренер

---

*  {% colwidth=[202] isHeader=true %}

   virtual_number_comment

*  {% colwidth=[86] %}

   string

*  {% colwidth=[125] %}

   

*  да

*  Заметка на виртуальном номере

---

*  {% colwidth=[202] isHeader=true %}

   is_blacklisted_phone

*  {% colwidth=[86] %}

   object

*  {% colwidth=[125] %}

   

*  да

*  Является ли номер абонента в черном списке

---

*  {% colwidth=[202] isHeader=true %}

   call_start_date_time

*  {% colwidth=[86] %}

   iso8601

*  {% colwidth=[125] %}

   `YYYY-MM-DD hh:mm:ss`

*  да

*  Дата и Время звонка

---

*  {% colwidth=[202] isHeader=true %}

   call_is_internal

*  {% colwidth=[86] %}

   object

*  {% colwidth=[125] %}

   

*  да

*  Направление звонка(Внешний/внутренний)

---

*  {% colwidth=[202] isHeader=true %}

   tags

*  {% colwidth=[86] %}

   iso8601

*  {% colwidth=[125] %}

   `hh:mm:ss`

*  да

*  Теги у звонка

---

*  {% colwidth=[202] isHeader=true %}

   call_processed_mark_duration

*  {% colwidth=[86] %}

   iso8601

*  {% colwidth=[125] %}

   да

*  да

*  Длительность обработки звонка

{% /table %}

## Структура ответа:

```json
{
    "jsonrpc": "2.0",
    "id": "number",
    "result": {
        "data": [
            {
                "tags": {
                    "items": [
                        {
                            "id": 24498,
                            "name": "Обработано",
                            "color": "color2"
                        }
                    ],
                    "communication_id": 26016,
                    "communication_type": "call"
                },
                "coaches": null,
                "call_type": {
                    "value": "Звонок ВАТС",
                    "value_id": "va"
                },
                "employees": [
                    "Иванов Иван"
                ],
                "call_status": {
                    "value": "Пропущенный",
                    "value_id": "lost"      
                },
                "call_records": null,
                "received_call": null,
                "call_direction": {
                    "value": "Входящий звонок",
                    "value_id": "in"
                },
                "call_start_date": "2024-10-21",
                "call_start_time": "16:08:19",
                "employee_rating": null,
                "call_is_internal": {
                    "value": "Внешний",
                    "value_id": "external"
                },
                "communication_id": 26016,
                "call_finish_reason": {
                    "value": "Не дозвонились до сотрудника",
                    "value_id": "no_success_operator_call"
                },
                "call_talk_duration": "00:00:00",
                "call_total_duration": "00:00:24",
                ],
                "call_start_date_time": "2024-10-21 16:08:19",
                "contact_phone_number": {
                    "extra": {
                        "call_status": "lost",
                        "call_direction": "in"
                    },
                    "value": "74950230625"
                },
                "is_blacklisted_phone": {
                    "value": "Нет",
                    "value_id": false
                },
                "virtual_phone_number": "79201234567",
                "call_finish_date_time": "2024-10-21 16:08:43",
                "communication_comment": {
                    "comment": null,
                    "communication_id": 26016,
                    "communication_type": "call"
                },
                "is_coach_handled_call": {
                    "value": "Нет",
                    "value_id": false
                },
                "virtual_number_comment": "Заметка о ВН",
                "call_await_talk_duration": null,
                "call_processed_mark_duration": "00:01:51",
                "communication_comment_author": null,
                "first_employee_for_internal_call": null,
                "second_employee_for_internal_call": null
            }
        ],
        "metadata": {
            "total_items": 1,
            "version": null,
            "limits": {}
        }
    }
}
```