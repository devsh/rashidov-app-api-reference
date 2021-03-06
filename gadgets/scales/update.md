# Обновить данные весов :lock:

## Запрос

`UPDATE /api/v1/gadgets/scales/{id}`

| Параметр | Тип    | Описание             |
|----------|--------|----------------------|
| id (GET) | string | Идентификатор весов  |
| title    | string | Новое название весов |

### Пример
`UPDATE /api/v1/gadgets/scales/1`
```JSON
{
    "title": "Весы в поле"
}
```

## Ответ

| Параметр                 | Тип    | Описание                                         |
|--------------------------|--------|--------------------------------------------------|
| id                       | string | Идентификатор весов                              |
| title                    | string | Название весов                                   |
| lastOnline               | date   | Когда в последний раз были online (дата и время) |
| batteryLevel             | number | Уровень заряда батареи                           |
| batteryExpireDate        | date   | До какой даты приблизительно хватит батареи      |
| serialNumber             | string | Серийный номер                                   |
| firmwareVersion          | string | Текущая версия прошивки                          |
| avaliableFirmwareVersion | string | Доступная для обновления версия прошивки         |

### Пример
```JSON
{
    "ok": true,
    "id": "1",
    "title": "Весы в поле",
    "lastOnline": "2019-02-22T20:35:00.000Z",
    "batteryLevel": 3,
    "batteryExpireDate": "2019-03-15T00:00:00.000Z",
    "serialNumber": "001-160-10231234",
    "firmwareVersion": "2.3",
    "avaliableFirmwareVersion": "2.4"
}
```

## Ошибки
| Код ошибки | Описание                               |
|------------|----------------------------------------|
| 3          | Несуществующий токен                   |
| 5          | Неверный id                            |
