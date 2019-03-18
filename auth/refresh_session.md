# Обновление сессии :lock:

Продлевает сессию. Выдает новые токены для авторизации и продления сессии. Старые токены становятся недействительными.

## Запрос

`POST /api/v1/auth/refresh_session`

| Параметр     | Тип    | Описание                    |
|--------------|--------|-----------------------------|
| refreshToken | string | Токен для обновления сессии |

### Пример
```JSON
{
    "refreshToken": "yRQYnWzskCZUxPwaQupWkiUzKELZ49eM7oWxAQK_ZXw"
}
```

## Ответ

| Параметр           | Тип    | Описание                                        |
|--------------------|--------|-------------------------------------------------|
| token              | string | Токен                                           |
| expirationDate     | date   | Срок действия токена                            |
| refreshToken       | string | Токен для [обновления сессии](#refresh_session) |

### Пример
```JSON
{
    "ok": true,
    "token": "yRQYnWzskCZUxPwaQupWkiUzKELZ49eM7oWxAQK_ZXw",
    "expirationDate": "2012-04-23T18:25:43.511Z",
    "refreshToken": "yRQYnWzskCZUxPwaQupWkiUzKELZ49eM7oWxAQK_ZXw"
}
```

## Ошибки
| Код ошибки | Описание                               |
|------------|----------------------------------------|
| 3          | Несуществующий токен                   |
| 4          | Несуществующий токен обновления сессии |
