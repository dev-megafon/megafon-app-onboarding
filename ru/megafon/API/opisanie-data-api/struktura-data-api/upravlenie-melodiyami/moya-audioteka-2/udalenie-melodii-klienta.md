---
order: 0.8
title: Удалить мелодию из каталога “Моя аудиотека”
---

### `DELETE /melodies/client/{id}`

**Описание**: этот метод позволяет удалить мелодию из каталога “Моя аудиотека” по уникальному идентификатору.

:::danger 

Удалению подлежат только файлы из раздела «Моя аудиотека» и те, которые нигде не задействованы.

:::

## Структура запроса

`DELETE /melodies/client/123`

## Структура ответа

```json
{
   "id": 123
}
```