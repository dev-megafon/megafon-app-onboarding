---
order: 0.5
title: Добавить мелодию в каталог “Моя аудиотека”
---

### `POST /melodies/client`

**Описание:** этот метод позволяет добавить новую мелодию  в каталог “Моя аудиотека”

## Параметры метода

{% table %}

---

*  {% isHeader=true %}

   Название

*  {% isHeader=true %}

   Тип

*  {% isHeader=true %}

   Обязательный

*  {% isHeader=true %}

   Допустимые значения

*  {% isHeader=true %}

   Описание

---

*  {% isHeader=true %}

   file

*  {% isHeader=true %}

   string

*  {% isHeader=true %}

   Да

*  {% isHeader=true %}

   Файл закодированный в Base64

*  {% isHeader=true %}

   Здесь необходимо ввести код, который присваивается аудиофайлу после его кодирования в формате Base64.

---

*  name

*  string

*  

*  Название

*  Имя аудиофайла

{% /table %}

## Структура запроса

`POST /melodies/client`

```json
{
"file": "SUQzBAAAAAAAI1RTU0UAAAAPAAADTGF2ZjU3LjcxLjEwMAAAA...",
"name": "АПИ.mp3"
}
```

## Структура ответа

```json
{
    "name": "АПИ.mp3",
    "id": 123,
    "url": "https://vcc.cp.megafon.ru/system/media/user_media/123/6abd7a5b632ff220f3fef702408e1b7a/"
}
```