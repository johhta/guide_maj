# 🎮 Фармим маджи с помощью Twitch MCL

## 🔧 Установка и настройка

1. **Скачиваем архив скрипта**  
🔗 [Gunthersuper/Twitch-Channel-Points-Miner-Render](https://github.com/Gunthersuper/Twitch-Channel-Points-Miner-Render)  
![Скачивание архива](https://drive.google.com/uc?export=view&id=15DmKrSUYUgNZHNs4FpDvF6jg8wJ0OfHT)

2. 📁 Распаковываем архив в удобную папку и редактируем `mainsetup.py`

3. **Вводим данные Twitch**  
🔑 Логин и пароль (при необходимости)  
![Ввод данных Twitch](https://drive.google.com/uc?export=view&id=1w1-8qXz7hBh3CYtoXDVf-sr5uk--6Z6f)

4. **Устанавливаем Python**  
🐍 [Python.org](https://www.python.org/downloads/)  
![Установка Python](https://drive.google.com/uc?export=view&id=1KqDScUUPZJw925WVPFOssvZ6ajiUj7JH)

5. ✅ При установке обязательно отмечаем "Add Python to PATH"

## ⚙️ Настройка майнера

6. **Открываем папку с майнером** через командную строку  
![Открытие командной строки](https://drive.google.com/uc?export=view&id=1W9pi1V5OrU1TcI0Z2woMk8kTVQ7ixxZj)

7. Устанавливаем зависимости:
```
pip install -r requirements.txt
```

8. Получаем cookies для авторизации:
```
python mainsetup.py
```

9. **Авторизуемся в Twitch** через полученную ссылку  
![Авторизация Twitch](https://drive.google.com/uc?export=view&id=1j7Y937FohYK7QCH0ql1Wb-0tPPikPqDu)

## 🛠 Конфигурация скрипта

10. Настраиваем уведомления (если нужны):  
![Настройка уведомлений](https://drive.google.com/uc?export=view&id=1lTTP_NMT3b4tfwKr9nVTGmUzWTRsob_d)

11. Добавляем конфигурацию для MajesticMCL:
```
Streamer("majesticmcl", 
  settings=StreamerSettings(
    make_predictions=False,
    follow_raid=True,
    claim_drops=True,
    watch_streak=True,
    bet=BetSettings(
      strategy=Strategy.SMART,
      percentage=5,
      stealth_mode=True,
      percentage_gap=20,
      max_points=234,
      filter_condition=FilterCondition(
        by=OutcomeKeys.TOTAL_USERS,
        where=Condition.LTE,
        value=800
      )
    )
  )
)
```
![Настройка стримера](https://drive.google.com/uc?export=view&id=14M99pesUSnC8oHVLV0vrPHWeEOL_mO8H)

12. Для автоматических ставок меняем `make_predictions=False` на `True`

## ☁️ Развертывание на Render.com

13. Создаем приватный репозиторий на GitHub:  
![Создание репозитория](https://drive.google.com/uc?export=view&id=1V8yNpA_clw9OHfv_LJNDHwowel_o_CqU)  
![Настройки репозитория](https://drive.google.com/uc?export=view&id=1hFYONMax9t5d-qlSTRE53xBuQug3YohI)

14. Загружаем файлы майнера:  
![Загрузка файлов](https://drive.google.com/uc?export=view&id=1GQvJsp0xysuOHTC-QVueeemhHL2oz2VN)  
![Подтверждение загрузки](https://drive.google.com/uc?export=view&id=1Pc8CK8o1fnJUm1yNythLjfnqveVIIdv2)

15. Регистрируемся на [Render.com](https://render.com)

16. Создаем Web Service:  
![Создание сервиса](https://drive.google.com/uc?export=view&id=18efAROz9rOEP4peKejWCH1He40RXIDhx)

17. Выбираем Python 3:  
![Выбор окружения](https://drive.google.com/uc?export=view&id=1T7aw15EYEPWdjo26HLsYT8aUMNQRytqA)

18. Указываем команду для запуска:
```
python main.py
```
![Настройка сервиса](https://drive.google.com/uc?export=view&id=1F_F_AOikOhDNgWE9Os0pYcx7yKzJ7vRo)

19. Вводим данные для авторизации:  
![Учетные данные](https://drive.google.com/uc?export=view&id=1aNm2Otc5cNiQ0xwHVdy7V1LaACmVhjqB)

20. Запускаем деплой:  
![Запуск деплоя](https://drive.google.com/uc?export=view&id=1Si-kk4bjNb2XgpLSdtfasjswcOEJmh7D)

## ⏰ Настройка Cron Job

21. Переходим на [cron-job.org](https://cron-job.org)

22. Создаем новое задание:  
![Создание задания](https://drive.google.com/uc?export=view&id=1QG4dkEhlFD_6hNeSmfwWiTpOqF9Sv7XR)

23. Настраиваем расписание (таймаут 2 минуты):  
![Настройка расписания](https://drive.google.com/uc?export=view&id=1y_3qUVKnJ2Eo7NQORCYTnHQyDJQX33p3)

## 🎁 Получение наград

24. После накопления 15к+ баллов покупаем награды в Twitch:  
💰 2200 маджей (самая выгодная награда)  
![Покупка наград](https://drive.google.com/uc?export=view&id=1_rd09JIG5uEKVa37fw0vaCMfPUlAe_hu)

## 🔍 Мониторинг

Для проверки работы:  
📊 Открываем [Render Dashboard](https://dashboard.render.com)  
![Мониторинг логов](https://drive.google.com/uc?export=view&id=1aYDyJAtv9BHXL-KnIR3uP8CTqutQYadY)
