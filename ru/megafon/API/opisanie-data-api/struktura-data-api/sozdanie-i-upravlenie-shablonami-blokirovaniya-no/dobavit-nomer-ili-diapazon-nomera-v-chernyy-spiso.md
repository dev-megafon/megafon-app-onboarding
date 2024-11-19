---
order: 1
title: Добавить номер или диапазон номеров в черный список
---

### `POST /black-nums/mask`

**Описание:** метод позволяет добавить номер или диапазон номеров  в черный список

## Параметры метода

{% table %}

---

*  {% colwidth=[100] isHeader=true %}

   Название

*  {% colwidth=[125] isHeader=true %}

   Тип

*  {% colwidth=[136] isHeader=true %}

   Обязательный

*  {% colwidth=[162] isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% colwidth=[100] isHeader=true %}

   pattern

*  {% colwidth=[125] %}

   string

*  {% colwidth=[136] %}

   Да

*  {% colwidth=[162] %}

   Допустимо указывать только цифры и `*`*.* Если нужно заблокировать диапазон (диапазон блокируется только для РФ номеров), то в конце указывается `*`, например `792012345*`.

   **Примечание**: РФ- номера всегда начинаются с 7 и состоят из 11 цифр, например `79201234567*`.Международные номера указываются без 810 и состоят из 8-20 цифр.

*  Номер/маска для блокировки звонков.

---

*  {% colwidth=[100] isHeader=true %}

   comment

*  {% colwidth=[125] %}

   string

*  {% colwidth=[136] %}

   Нет

*  {% colwidth=[162] %}

   --

*  Комментарий к номеру/маске.

---

*  {% colwidth=[100] isHeader=true %}

   id

*  {% colwidth=[125] %}

   integer

*  {% colwidth=[136] %}

   \-

*  {% colwidth=[162] %}

   --

*  Уникальный идентификатор номера/маски из ЧС.

---

*  {% colwidth=[100] isHeader=true %}

   upload_dt

*  {% colwidth=[125] %}

   string(\$date-time)

*  {% colwidth=[136] %}

   \-

*  {% colwidth=[162] %}

   --

*  Дата и время добавления номера/маски в ЧС.

---

*  {% colwidth=[100] isHeader=true %}

   last_7_days_count

*  {% colwidth=[125] %}

   integer

*  {% colwidth=[136] %}

   \-

*  {% colwidth=[162] %}

   0 и выше

*  Количество заблокированных звонков с этого номера/маски за последние 7 дней.

---

*  {% colwidth=[100] isHeader=true %}

   last_365_days_count

*  {% colwidth=[125] %}

   integer

*  {% colwidth=[136] %}

   \-

*  {% colwidth=[162] %}

   0 и выше

*  Количество заблокированных звонков с этого номера/маски за последний год

{% /table %}

## Cтруктура запроса

`POST /black-nums/mask`

```json
{
    "pattern": "792012345*",
    "comment": "ЗаметкаАпи"
}
```

## **Структура ответа**

```json
{
    "pattern": "792012345*",
    "comment": "ЗаметкаАпи",
    "id": 123,
    "upload_dt": "2024-10-30T14:10:38.531612+03:00",
    "last_7_days_count": 0,
    "last_365_days_count": 0
}
```