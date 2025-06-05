# Фармим маджи с помощью твича мцл

1. Качаем архив через кнопку по [ссылке]([url](https://github.com/Gunthersuper/Twitch-Channel-Points-Miner-Render))
 ![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_1.png)
2. Распаковываем в любую папку этот архив и настраиваем mainsetup.py
3. Вставляем логин от твича и если хотим, пароль (если оставить только логин, то надо будет авторизовать приложение в твиче, это легко)
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_2.png)
4. Скачиваем последнюю версию питона с оф.сайта https://python.org
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_3.png)
5. Устанавливаем не забыв нажать галку на "Add python to PATH" при установке
6. Заходим в папку с майнером и вводим в поисковую строку cmd
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_4.png)
7. Вводим туда `pip install -r requirements.txt` и ждём окончания установки
8. Если вылезает ошибка с командой в конце, то просто копируем команду из ошибки и вставляем в кмд, далее пробуем ещё раз ввести прошлую команду
9. Далее запускаем сам скрипт для получения куки файлов `python mainsetup.py`
10. Переходим по ссылке из скрипта и вводим туда код от туда
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_5.png)
11. Можно закрывать скрипт и переходить к настройке main.py
12. Если нужны уведомления в телеграм или дс канал, то следуя комментам вводим нужные значения
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_6.png)
13. Удаляем всех лишних стримеров из списка и добавляем строку с твичом мцла 
`Streamer("majesticmcl", settings=StreamerSettings(make_predictions=False  , follow_raid=True , claim_drops=True  , watch_streak=True , bet=BetSettings(strategy=Strategy.SMART      , percentage=5 , stealth_mode=True,  percentage_gap=20 , max_points=234   , filter_condition=FilterCondition(by=OutcomeKeys.TOTAL_USERS,      where=Condition.LTE, value=800 ) ) )),`
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_7.png)
14. Если хотите чтоб скрипт сам ставил на самые вероятные исходы ставок баллами, то включаете в строке выше ставки изменив `make_predictions=False` на `make_predictions=True`
15. Если найдёте стримеров которые дают нужные вам бонусы за баллы канал, например маджи, деньги на сервере или сабки на любых стримеров, то добавляйте их ник следующей строкой в файле main.py по шаблону ниже и включайте ставки если надо редактируя make_predictions
`Streamer("ЗДЕСЬ НИК СТРИМЕРА", settings=StreamerSettings(make_predictions=False  , follow_raid=True , claim_drops=True  , watch_streak=True , bet=BetSettings(strategy=Strategy.SMART      , percentage=5 , stealth_mode=True,  percentage_gap=20 , max_points=234   , filter_condition=FilterCondition(by=OutcomeKeys.TOTAL_USERS,      where=Condition.LTE, value=800 ) ) )),`
16. Настроив это всё, заходим на https://github.com , регистрируемся и создаём приватный репозиторий
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_8.png)
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_9.png)
17. Заливаем всё содержимое папки майнера на гх
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_10.png)
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_11.png)
18. Регаемся на сайте https://render.com (можно сразу через гитхаб)
19. Добавляем Web Service в дэшборде
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_12.png)
20. Выбираем нужный репозиторий и ставим Python 3 вместо Docker
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_13.png)
22. Вставляем команду для запуска майнера `python main.py` и ставим бесплатный тарифный план
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_14.png)
23. Вставляем username и password в поля, вводим в value свои логин и пароль от твича (хз зачем, но на всякий, можно трайнуть ввести рандомные данные, а потом если не запустит, то поставить как надо)
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_15.png)
24. Тыкаем на Deploy Web Service и ждём пока это всё запустит
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_16.png)
25.После запуска берём ссылку и идём на сайт https://cron-job.org
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_17.png)
26. Регаемся на сайте, заходим в Cron задания и создаём новое
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_18.png)
27. Вставляем url с рендера и ставим таймаут 2 минуты
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_19.png)
28. Поздравляю, всё работает.
29. Накопив нужное кол-во баллов 15к и/или более покупаем на твиче нужные награды, 2200 маджей самое выгодное из маджей, остальное по потребности, пишете свой сервер и статик при покупке
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_20.png)


если хотите мониторить ход работы софта, заходим в https://dashboard.render.com/ и переходим в ваш веб сервис, далее заходим в лог и чекаем ход получения наград
![image](https://raw.githubusercontent.com/johhta/guide_maj/main/images/\step_21.png)
