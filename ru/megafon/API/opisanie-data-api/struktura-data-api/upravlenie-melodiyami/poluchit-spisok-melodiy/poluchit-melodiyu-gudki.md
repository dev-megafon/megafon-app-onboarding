---
order: 0.5
title: "Получить мелодию\_“Гудки”"
---

### `GET /melodies/beeps`

**Описание**: этот метод позволяет получить настройки мелодии «Гудки».

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   name

*  string

*  Любое имя файла

*  Название аудиофайла (например, «[2223\.mp](http://2223.mp)3»).

---

*  {% isHeader=true %}

   id

*  integer

*  Положительное число

*  Уникальный идентификатор аудиофайла.

---

*  {% isHeader=true %}

   url

*  string

*  URL-адрес

*  Ссылка на аудиофайл, доступный для загрузки или воспроизведения.

{% /table %}

## Структура запроса

`GET /melodies/beeps`

## Структура ответа

```json
[
    {
        "name": "Стандартные телефонные гудки",
        "id": 123,
        "url": "https://vcc.cp.megafon.ru/system/media/system_media/143/7e1b4a0bc7286768c049120ecedbace3/"
    }
]
```