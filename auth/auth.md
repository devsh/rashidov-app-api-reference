# Авторизация

После авторизации Токен, Срок действия и Токен обновления сессии сохраняйте в local storage.
## Запрос

`POST /api/v1/auth/`

| Параметр | Тип    | Описание            |
|----------|--------|---------------------|
| username | string | логин пользователя  |
| password | string | пароль пользователя |

### Пример
```JSON
{
    "username": "username",
    "password": "password"
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
| Код ошибки | Описание             |
|------------|----------------------|
| 1          | Неверный логин       |
| 2          | Неверный пароль      |
