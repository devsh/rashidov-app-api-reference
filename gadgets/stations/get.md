# Получить данные станции :lock:

## Запрос

`GET /api/v1/gadgets/stations/{id}`

| Параметр | Тип    | Описание              |
|----------|--------|-----------------------|
| id       | string | Идентификатор станции |

### Пример
`GET /api/v1/gadgets/stations/1`

## Ответ

| Параметр                 | Тип    | Описание                                         |
|--------------------------|--------|--------------------------------------------------|
| id                       | string | Идентификатор станции                            |
| title                    | string | Название станции                                 |
| lastOnline               | date   | Когда в последний раз были online (дата и время) |
| gsmSignalLevel           | number | Уровень сигнала gsm                              |
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
    "title": "Липовый лес",
    "lastOnline": "2019-02-22T20:35:00.000Z",
    "gsmSignalLevel": 1,
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
