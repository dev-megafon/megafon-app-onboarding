---
order: 1.9
title: Удалить перерыв
---

### `PUT scenario/inbound/virtual-number/{id}`

**Описание**: метод предназначен для удаления перерыва из сценария.

:::info 

Для удаления перерыва из сценария просто в параметр “breaks” указываете пустой массив ““breaks”: \[ \]”.

:::

## Структура запроса:

```json
{
    "working_shift1": {
        "scenario_type": "redirect_to_employee_group",
        "employee_group_id": 183,
        "is_welcome_enabled": false,
        "scheduler_id": 67,
        "breaks": [
        ],
        "is_active": true
    },
    "working_shift2": null,
    "working_shift3": null,
    "default_working_shift": {
        "scenario_type": "informer",
        "media_type": "system",
        "is_active": true
    },
    "id": 693
}
```

## Структура ответа

```json
{
    "working_shift1": {
        "scenario_type": "redirect_to_employee_group",
        "employee_group_id": 183,
        "is_welcome_enabled": false,
        "scheduler_id": 67,
        "breaks": [
        ],
        "is_active": true
    },
    "working_shift2": null,
    "working_shift3": null,
    "default_working_shift": {
        "scenario_type": "informer",
        "media_type": "system",
        "is_active": true
    },
    "id": 693
}
```