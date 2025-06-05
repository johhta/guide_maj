# Фармим маджи с помощью твича мцл

1. Качаем архив через кнопку по [ссылке](https://github.com/Gunthersuper/Twitch-Channel-Points-Miner-Render)
![image](https://drive.google.com/uc?export=view&id=15DmKrSUYUgNZHNs4FpDvF6jg8wJ0OfHT)

2. Распаковываем в любую папку этот архив и настраиваем mainsetup.py

3. Вставляем логин от твича и если хотим, пароль
![image](https://drive.google.com/uc?export=view&id=1w1-8qXz7hBh3CYtoXDVf-sr5uk--6Z6f)

4. Скачиваем последнюю версию питона с оф.сайта python.org
![image](https://drive.google.com/uc?export=view&id=1KqDScUUPZJw925WVPFOssvZ6ajiUj7JH)

5. Устанавливаем не забыв нажать галку на "Add python to PATH" при установке

6. Заходим в папку с майнером и вводим в поисковую строку cmd
![image](https://drive.google.com/uc?export=view&id=1W9pi1V5OrU1TcI0Z2woMk8kTVQ7ixxZj)

7. Вводим туда `pip install -r requirements.txt` и ждём окончания установки

8. Если вылезает ошибка с командой в конце, то просто копируем команду из ошибки и вставляем в кмд, далее пробуем ещё раз ввести прошлую команду

9. Далее запускаем сам скрипт для получения куки файлов `python mainsetup.py`

10. Переходим по ссылке из скрипта и вводим туда код от туда
![image](https://drive.google.com/uc?export=view&id=1j7Y937FohYK7QCH0ql1Wb-0tPPikPqDu)

11. Можно закрывать скрипт и переходить к настройке main.py

12. Если нужны уведомления в телеграм или дс канал, то следуя комментам вводим нужные значения
![image](https://drive.google.com/uc?export=view&id=1lTTP_NMT3b4tfwKr9nVTGmUzWTRsob_d)

13. Удаляем всех лишних стримеров из списка и добавляем строку с твичом мцла 
`Streamer("majesticmcl", settings=StreamerSettings(make_predictions=False, follow_raid=True, claim_drops=True, watch_streak=True, bet=BetSettings(strategy=Strategy.SMART, percentage=5, stealth_mode=True, percentage_gap=20, max_points=234, filter_condition=FilterCondition(by=OutcomeKeys.TOTAL_USERS, where=Condition.LTE, value=800))))`
![image](https://drive.google.com/uc?export=view&id=14M99pesUSnC8oHVLV0vrPHWeEOL_mO8H)

14. Если хотите чтоб скрипт сам ставил на самые вероятные исходы ставок баллами, то включаете в строке выше ставки изменив `make_predictions=False` на `make_predictions=True`

15. Если найдёте стримеров которые дают нужные вам бонусы за баллы канал, например маджи, деньги на сервере или сабки на любых стримеров, то добавляйте их ник следующей строкой в файле main.py по шаблону ниже и включайте ставки если надо редактируя make_predictions
`Streamer("ЗДЕСЬ НИК СТРИМЕРА", settings=StreamerSettings(make_predictions=False, follow_raid=True, claim_drops=True, watch_streak=True, bet=BetSettings(strategy=Strategy.SMART, percentage=5, stealth_mode=True, percentage_gap=20, max_points=234, filter_condition=FilterCondition(by=OutcomeKeys.TOTAL_USERS, where=Condition.LTE, value=800))))`

16. Настроив это всё, заходим на github.com, регистрируемся и создаём приватный репозиторий
![image](https://drive.google.com/uc?export=view&id=1V8yNpA_clw9OHfv_LJNDHwowel_o_CqU)
![image](https://drive.google.com/uc?export=view&id=1hFYONMax9t5d-qlSTRE53xBuQug3YohI)

17. Заливаем всё содержимое папки майнера на гх
![image](https://drive.google.com/uc?export=view&id=1GQvJsp0xysuOHTC-QVueeemhHL2oz2VN)
![image](https://drive.google.com/uc?export=view&id=1Pc8CK8o1fnJUm1yNythLjfnqveVIIdv2)

18. Регаемся на сайте render.com (можно сразу через гитхаб)

19. Добавляем Web Service в дэшборде
![image](https://drive.google.com/uc?export=view&id=18efAROz9rOEP4peKejWCH1He40RXIDhx)

20. Выбираем нужный репозиторий и ставим Python 3 вместо Docker
![image](https://drive.google.com/uc?export=view&id=1T7aw15EYEPWdjo26HLsYT8aUMNQRytqA)

22. Вставляем команду для запуска майнера `python main.py` и ставим бесплатный тарифный план
![image](https://drive.google.com/uc?export=view&id=1F_F_AOikOhDNgWE9Os0pYcx7yKzJ7vRo)

23. Вставляем username и password в поля, вводим в value свои логин и пароль от твича
![image](https://drive.google.com/uc?export=view&id=1aNm2Otc5cNiQ0xwHVdy7V1LaACmVhjqB)

24. Тыкаем на Deploy Web Service и ждём пока это всё запустит
![image](https://drive.google.com/uc?export=view&id=1Si-kk4bjNb2XgpLSdtfasjswcOEJmh7D)

25. После запуска берём ссылку и идём на сайт cron-job.org
![image](https://drive.google.com/uc?export=view&id=1QG4dkEhlFD_6hNeSmfwWiTpOqF9Sv7XR)

26. Регаемся на сайте, заходим в Cron задания и создаём новое
![image](https://drive.google.com/uc?export=view&id=1y_3qUVKnJ2Eo7NQORCYTnHQyDJQX33p3)

27. Вставляем url с рендера и ставим таймаут 2 минуты
![image](https://drive.google.com/uc?export=view&id=1_rd09JIG5uEKVa37fw0vaCMfPUlAe_hu)

28. Поздравляю, всё работает.

29. Накопив нужное кол-во баллов 15к и/или более покупаем на твиче нужные награды, 2200 маджей самое выгодное из маджей, остальное по потребности, пишете свой сервер и статик при покупке
![image](https://drive.google.com/uc?export=view&id=1BE4QMY83ZXEuuFVYdnpN_3e0NZeQpUEB)

Если хотите мониторить ход работы софта, заходим в https://dashboard.render.com/ и переходим в ваш веб сервис, далее заходим в лог и чекаем ход получения наград
![image](https://drive.google.com/uc?export=view&id=1aYDyJAtv9BHXL-KnIR3uP8CTqutQYadY)
