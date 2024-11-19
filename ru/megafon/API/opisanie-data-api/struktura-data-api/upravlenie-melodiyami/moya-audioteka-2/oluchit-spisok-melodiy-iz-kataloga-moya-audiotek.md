---
order: 0.3
title: Получить список мелодий из каталога “Моя аудиотека”
---

### `GET /melodies/client`

**Описание**: этот метод позволяет получить список мелодий из каталога «Моя аудиотека».

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

`GET /melodies/client`

## Структура ответа

```json
[
    {
        "name": "Музыка переадресации 1",
        "id": 50,
        "url": "https://vcc.cp.megafon.ru/system/media/user_media/50/41050dc7719ee8c182e0d703102d9699/"
    },
    {
        "name": "Музыка переадресации 2",
        "id": 51,
        "url": "https://vcc.cp.megafon.ru/system/media/user_media/51/6050c7a3abc0e148821cc3d0b33f87c6/"
    },
...
```