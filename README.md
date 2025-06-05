# Фармим маджи с помощью Twitch MCL

## Установка и настройка

1. Скачиваем архив через кнопку по ссылке:  
   https://github.com/Gunthersuper/Twitch-Channel-Points-Miner-Render

   [Изображение: Шаг 1 - Скачивание архива](https://drive.google.com/uc?export=view&id=15DmKrSUYUgNZHNs4FpDvF6jg8wJ0OfHT)

2. Распаковываем архив в любую папку и настраиваем `mainsetup.py`

3. Вводим логин от Twitch (и пароль при необходимости):

   [Изображение: Шаг 3 - Ввод данных](https://drive.google.com/uc?export=view&id=1w1-8qXz7hBh3CYtoXDVf-sr5uk--6Z6f)

4. Скачиваем Python с официального сайта:  
   https://www.python.org/downloads/

   [Изображение: Шаг 4 - Установка Python](https://drive.google.com/uc?export=view&id=1KqDScUUPZJw925WVPFOssvZ6ajiUj7JH)

5. При установке обязательно отмечаем галочку "Add Python to PATH"

## Настройка майнера

6. Открываем папку с майнером и вводим в адресной строке `cmd`:

   [Изображение: Шаг 6 - Командная строка](https://drive.google.com/uc?export=view&id=1W9pi1V5OrU1TcI0Z2woMk8kTVQ7ixxZj)

7. Устанавливаем зависимости:
  `pip install -r requirements.txt`

9. Получаем cookie-файлы:
   `python mainsetup.py`


9. Авторизуемся через Twitch по полученной ссылке:

[Изображение: Шаг 9 - Авторизация](https://drive.google.com/uc?export=view&id=1j7Y937FohYK7QCH0ql1Wb-0tPPikPqDu)

10. Настраиваем основной файл `main.py`

## Конфигурация стримеров

11. Настройка уведомлений (если нужны):

 [Изображение: Шаг 11 - Настройка уведомлений](https://drive.google.com/uc?export=view&id=1lTTP_NMT3b4tfwKr9nVTGmUzWTRsob_d)

12. Добавляем конфигурацию для MajesticMCL:
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

 [Изображение: Шаг 12 - Настройка стримера](https://drive.google.com/uc?export=view&id=14M99pesUSnC8oHVLV0vrPHWeEOL_mO8H)

13. Для автоматических ставок меняем `make_predictions=False` на `True`

## Развертывание на Render.com

14. Создаем приватный репозиторий на GitHub:

 [Изображение: Шаг 14-1 - Создание репозитория](https://drive.google.com/uc?export=view&id=1V8yNpA_clw9OHfv_LJNDHwowel_o_CqU)
 
 [Изображение: Шаг 14-2 - Настройки репозитория](https://drive.google.com/uc?export=view&id=1hFYONMax9t5d-qlSTRE53xBuQug3YohI)

15. Загружаем файлы майнера:

 [Изображение: Шаг 15-1 - Загрузка файлов](https://drive.google.com/uc?export=view&id=1GQvJsp0xysuOHTC-QVueeemhHL2oz2VN)
 
 [Изображение: Шаг 15-2 - Подтверждение](https://drive.google.com/uc?export=view&id=1Pc8CK8o1fnJUm1yNythLjfnqveVIIdv2)

16. Регистрируемся на https://render.com

17. Создаем Web Service:

 [Изображение: Шаг 17 - Создание сервиса](https://drive.google.com/uc?export=view&id=18efAROz9rOEP4peKejWCH1He40RXIDhx)

18. Выбираем Python 3:

 [Изображение: Шаг 18 - Выбор окружения](https://drive.google.com/uc?export=view&id=1T7aw15EYEPWdjo26HLsYT8aUMNQRytqA)

19. Указываем команду для запуска:
 ```
 python main.py
 ```

 [Изображение: Шаг 19 - Настройка сервиса](https://drive.google.com/uc?export=view&id=1F_F_AOikOhDNgWE9Os0pYcx7yKzJ7vRo)

20. Вводим данные для авторизации:

 [Изображение: Шаг 20 - Учетные данные](https://drive.google.com/uc?export=view&id=1aNm2Otc5cNiQ0xwHVdy7V1LaACmVhjqB)

21. Запускаем деплой:

 [Изображение: Шаг 21 - Запуск](https://drive.google.com/uc?export=view&id=1Si-kk4bjNb2XgpLSdtfasjswcOEJmh7D)

## Настройка Cron Job

22. Переходим на https://cron-job.org и создаем задание:

 [Изображение: Шаг 22 - Создание задания](https://drive.google.com/uc?export=view&id=1QG4dkEhlFD_6hNeSmfwWiTpOqF9Sv7XR)

23. Настраиваем расписание (таймаут 2 минуты):

 [Изображение: Шаг 23 - Настройка расписания](https://drive.google.com/uc?export=view&id=1y_3qUVKnJ2Eo7NQORCYTnHQyDJQX33p3)

## Получение наград

24. После накопления 15к+ баллов покупаем награды в Twitch:
 - 2200 маджей (самая выгодная награда)
 - Указываем сервер и ник при покупке

 [Изображение: Шаг 24 - Покупка наград](https://drive.google.com/uc?export=view&id=1_rd09JIG5uEKVa37fw0vaCMfPUlAe_hu)

## Мониторинг

Для проверки работы:
- Открываем https://dashboard.render.com
- Проверяем логи выполнения

[Изображение: Мониторинг логов](https://drive.google.com/uc?export=view&id=1aYDyJAtv9BHXL-KnIR3uP8CTqutQYadY)
