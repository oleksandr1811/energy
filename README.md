# API Прикарпаттяобленерго (unofficial)

Цей проєкт дозволяє отримувати інформацію про відключення електроенергії в Івано-Франківську через API та Telegram-бота.

## API

### Способи використання

1. **(Рекомендовано)** Використання API без завантаження файлу:
   - URL: `https://oleksandr1811.pp.ua/api/energy.php`
   - Метод: POST
   - Параметри:
     - `accountNumber`: номер особового рахунку.

2. **Використання локального файлу**:
   - Завантажте файл `energy.php` на вебхостинг із підтримкою PHP.
   - Налаштуйте режим роботи у файлі:
     - `1`: Використання POST-запиту з параметром `accountNumber`.
     - `2`: Використання статичного особового рахунку. Укажіть значення в змінній `accountNumber`.

---

## Telegram Bot

### Способи використання

1. **(Рекомендовано)** Використання API для Telegram-бота без завантаження файлу:
   - URL: `https://oleksandr1811.pp.ua/api/energy-tg.php`
   - Метод: POST
   - Параметри:
     - `accountNumber`: номер особового рахунку.
     - `botToken`: токен Telegram-бота.
     - `chatID`: ID вашого чату.

2. **Використання локального файлу**:
   - Завантажте файл `energy.php` на вебхостинг із підтримкою PHP.
   - Налаштуйте режим роботи у файлі:
     - `1`: Використання POST-запиту з параметрами `accountNumber`, `botToken` та `chatID`.
     - `2`: Використання статичних даних. Укажіть значення змінних:
       - `accountNumber`: номер особового рахунку.
       - `botToken`: токен Telegram-бота.
       - `chatID`: ID вашого чату.

---

## Приклад запиту до API

### Для отримання інформації про відключення світла

#### Запит
```
POST https://oleksandr1811.pp.ua/api/energy.php
Content-Type: application/json

{
    "accountNumber": "123456789"
}
```

#### Відповідь
```
{
  "current": {
    "note": "За вказаним особовим рахунком '1234567' споживач підпадає під чергу '5.2' Графіку погодинних вимкнень(ГПВ)",
    "hasQueue": "yes",
    "subqueue": 2,
    "queue": 5
  },
  "graphs": {
    "today": {
      "scheduleApprovedSince": "16-12-2024 11:47",
      "hoursList": [
        {
          "hour": "0",
          "electricity": 0,
          "description": "00:00-00:30",
          "from": "00:00",
          "to": "00:30",
          "periodLimitValue": 0.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "00:30-01:00",
          "from": "00:30",
          "to": "01:00",
          "periodLimitValue": 1
        },
        {
          "hour": "1",
          "electricity": 0,
          "description": "01:00-01:30",
          "from": "01:00",
          "to": "01:30",
          "periodLimitValue": 1.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "01:30-02:00",
          "from": "01:30",
          "to": "02:00",
          "periodLimitValue": 2
        },
        {
          "hour": "2",
          "electricity": 0,
          "description": "02:00-02:30",
          "from": "02:00",
          "to": "02:30",
          "periodLimitValue": 2.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "02:30-03:00",
          "from": "02:30",
          "to": "03:00",
          "periodLimitValue": 3
        },
        {
          "hour": "3",
          "electricity": 0,
          "description": "03:00-03:30",
          "from": "03:00",
          "to": "03:30",
          "periodLimitValue": 3.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "03:30-04:00",
          "from": "03:30",
          "to": "04:00",
          "periodLimitValue": 4
        },
        {
          "hour": "4",
          "electricity": 0,
          "description": "04:00-04:30",
          "from": "04:00",
          "to": "04:30",
          "periodLimitValue": 4.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "04:30-05:00",
          "from": "04:30",
          "to": "05:00",
          "periodLimitValue": 5
        },
        {
          "hour": "5",
          "electricity": 0,
          "description": "05:00-05:30",
          "from": "05:00",
          "to": "05:30",
          "periodLimitValue": 5.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "05:30-06:00",
          "from": "05:30",
          "to": "06:00",
          "periodLimitValue": 6
        },
        {
          "hour": "6",
          "electricity": 0,
          "description": "06:00-06:30",
          "from": "06:00",
          "to": "06:30",
          "periodLimitValue": 6.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "06:30-07:00",
          "from": "06:30",
          "to": "07:00",
          "periodLimitValue": 7
        },
        {
          "hour": "7",
          "electricity": 0,
          "description": "07:00-07:30",
          "from": "07:00",
          "to": "07:30",
          "periodLimitValue": 7.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "07:30-08:00",
          "from": "07:30",
          "to": "08:00",
          "periodLimitValue": 8
        },
        {
          "hour": "8",
          "electricity": 0,
          "description": "08:00-08:30",
          "from": "08:00",
          "to": "08:30",
          "periodLimitValue": 8.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "08:30-09:00",
          "from": "08:30",
          "to": "09:00",
          "periodLimitValue": 9
        },
        {
          "hour": "9",
          "electricity": 0,
          "description": "09:00-09:30",
          "from": "09:00",
          "to": "09:30",
          "periodLimitValue": 9.5
        },
        {
          "hour": "",
          "electricity": 1,
          "description": "09:30-10:00",
          "from": "09:30",
          "to": "10:00",
          "periodLimitValue": 10
        },
        {
          "hour": "10",
          "electricity": 1,
          "description": "10:00-10:30",
          "from": "10:00",
          "to": "10:30",
          "periodLimitValue": 10.5
        },
        {
          "hour": "",
          "electricity": 1,
          "description": "10:30-11:00",
          "from": "10:30",
          "to": "11:00",
          "periodLimitValue": 11
        },
        {
          "hour": "11",
          "electricity": 1,
          "description": "11:00-11:30",
          "from": "11:00",
          "to": "11:30",
          "periodLimitValue": 11.5
        },
        {
          "hour": "",
          "electricity": 1,
          "description": "11:30-12:00",
          "from": "11:30",
          "to": "12:00",
          "periodLimitValue": 12
        },
        {
          "hour": "12",
          "electricity": 1,
          "description": "12:00-12:30",
          "from": "12:00",
          "to": "12:30",
          "periodLimitValue": 12.5
        },
        {
          "hour": "",
          "electricity": 1,
          "description": "12:30-13:00",
          "from": "12:30",
          "to": "13:00",
          "periodLimitValue": 13
        },
        {
          "hour": "13",
          "electricity": 0,
          "description": "13:00-13:30",
          "from": "13:00",
          "to": "13:30",
          "periodLimitValue": 13.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "13:30-14:00",
          "from": "13:30",
          "to": "14:00",
          "periodLimitValue": 14
        },
        {
          "hour": "14",
          "electricity": 0,
          "description": "14:00-14:30",
          "from": "14:00",
          "to": "14:30",
          "periodLimitValue": 14.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "14:30-15:00",
          "from": "14:30",
          "to": "15:00",
          "periodLimitValue": 15
        },
        {
          "hour": "15",
          "electricity": 0,
          "description": "15:00-15:30",
          "from": "15:00",
          "to": "15:30",
          "periodLimitValue": 15.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "15:30-16:00",
          "from": "15:30",
          "to": "16:00",
          "periodLimitValue": 16
        },
        {
          "hour": "16",
          "electricity": 0,
          "description": "16:00-16:30",
          "from": "16:00",
          "to": "16:30",
          "periodLimitValue": 16.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "16:30-17:00",
          "from": "16:30",
          "to": "17:00",
          "periodLimitValue": 17
        },
        {
          "hour": "17",
          "electricity": 0,
          "description": "17:00-17:30",
          "from": "17:00",
          "to": "17:30",
          "periodLimitValue": 17.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "17:30-18:00",
          "from": "17:30",
          "to": "18:00",
          "periodLimitValue": 18
        },
        {
          "hour": "18",
          "electricity": 0,
          "description": "18:00-18:30",
          "from": "18:00",
          "to": "18:30",
          "periodLimitValue": 18.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "18:30-19:00",
          "from": "18:30",
          "to": "19:00",
          "periodLimitValue": 19
        },
        {
          "hour": "19",
          "electricity": 0,
          "description": "19:00-19:30",
          "from": "19:00",
          "to": "19:30",
          "periodLimitValue": 19.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "19:30-20:00",
          "from": "19:30",
          "to": "20:00",
          "periodLimitValue": 20
        },
        {
          "hour": "20",
          "electricity": 0,
          "description": "20:00-20:30",
          "from": "20:00",
          "to": "20:30",
          "periodLimitValue": 20.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "20:30-21:00",
          "from": "20:30",
          "to": "21:00",
          "periodLimitValue": 21
        },
        {
          "hour": "21",
          "electricity": 0,
          "description": "21:00-21:30",
          "from": "21:00",
          "to": "21:30",
          "periodLimitValue": 21.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "21:30-22:00",
          "from": "21:30",
          "to": "22:00",
          "periodLimitValue": 22
        },
        {
          "hour": "22",
          "electricity": 0,
          "description": "22:00-22:30",
          "from": "22:00",
          "to": "22:30",
          "periodLimitValue": 22.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "22:30-23:00",
          "from": "22:30",
          "to": "23:00",
          "periodLimitValue": 23
        },
        {
          "hour": "23",
          "electricity": 0,
          "description": "23:00-23:30",
          "from": "23:00",
          "to": "23:30",
          "periodLimitValue": 23.5
        },
        {
          "hour": "",
          "electricity": 0,
          "description": "23:30-00:00",
          "from": "23:30",
          "to": "00:00",
          "periodLimitValue": 24
        }
      ],
      "eventDate": "2024-12-16"
    }
  },
  "showFutureDateUntil": "01.05.2023"
}
```

---

## Вимоги
- Вебхостинг із підтримкою PHP (для локального використання `energy.php`).
- Telegram-бот (для інтеграції з Telegram).

---

## Ліцензія
Цей проєкт є неофіційним і не пов'язаний із Прикарпаттяобленерго. Використовуйте на свій страх і ризик.
