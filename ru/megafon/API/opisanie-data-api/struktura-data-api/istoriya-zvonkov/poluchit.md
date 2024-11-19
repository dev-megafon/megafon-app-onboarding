---
order: 2
title: Получить список отчётов пользователей
---

**Описание**: Каждый пользователь видит свой отчет с уникальным идентификатором (id). Это значение потом используется в параметре «`report_id`» в методе `get_mgf_calls`

## Структура запроса

```json
{
  "jsonrpc":"2.0",
  "id":"number",
  "method":"get.reports_list",
  "params":{
        "filter":{
            "field":"name",
            "operator":"=",
            "value":"История звонков"
    }
  }
}
 
```

## Структура ответа

```json
{
    "jsonrpc": "2.0",
    "id": "number",
    "result": {
        "data": [
            {
                "id": 1015,
                "name": "История звонков",
                "sort": 9300,
                "type": "mgf_calls",
                "group_id": 9,
                "is_mobile": false,
                "is_system": false,
                "description": null,
                "is_editable": true,
                "is_favorite": false,
                "is_deletable": false,
                "date_time_added_to_favorite": null
            }
        ],
        "metadata": {
            "total_items": 2,
            "version": null,
            "limits": {}
        }
    }
}
```