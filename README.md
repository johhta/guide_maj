# Фармим маджи с помощью твича мцл

1. Качаем архив через кнопку по [ссылке]([url](https://github.com/Gunthersuper/Twitch-Channel-Points-Miner-Render))
 ![image](images\451945623-3ee9ece7-9e57-44af-9f64-63733032c598.png)
2. Распаковываем в любую папку этот архив и настраиваем mainsetup.py
3. Вставляем логин от твича и если хотим, пароль (если оставить только логин, то надо будет авторизовать приложение в твиче, это легко)
![image](images\451945623-3ee9ece7-9e57-44af-9f64-63733032c598.png)
4. Скачиваем последнюю версию питона с оф.сайта https://python.org
![image](images\451946617-b2f50001-af47-4419-b5a6-88484c95159e.png)
5. Устанавливаем не забыв нажать галку на "Add python to PATH" при установке
6. Заходим в папку с майнером и вводим в поисковую строку cmd
![image](images\451947964-7537ca47-6cb9-4f5f-8761-f93424a07d63.png)
7. Вводим туда `pip install -r requirements.txt` и ждём окончания установки
8. Если вылезает ошибка с командой в конце, то просто копируем команду из ошибки и вставляем в кмд, далее пробуем ещё раз ввести прошлую команду
9. Далее запускаем сам скрипт для получения куки файлов `python mainsetup.py`
10. Переходим по ссылке из скрипта и вводим туда код от туда
![image](images\451950306-89776e98-2be1-4eb3-89c3-6516772fbc00.png)
11. Можно закрывать скрипт и переходить к настройке main.py
12. Если нужны уведомления в телеграм или дс канал, то следуя комментам вводим нужные значения
![image](images\451951085-4e1b5b3e-0516-45ac-929c-2a9e1ff363cf.png)
13. Удаляем всех лишних стримеров из списка и добавляем строку с твичом мцла 
`Streamer("majesticmcl", settings=StreamerSettings(make_predictions=False  , follow_raid=True , claim_drops=True  , watch_streak=True , bet=BetSettings(strategy=Strategy.SMART      , percentage=5 , stealth_mode=True,  percentage_gap=20 , max_points=234   , filter_condition=FilterCondition(by=OutcomeKeys.TOTAL_USERS,      where=Condition.LTE, value=800 ) ) )),`
![image](images\451951679-663948e5-9bfe-4030-ba5f-e6adc705e163.png)
14. Если хотите чтоб скрипт сам ставил на самые вероятные исходы ставок баллами, то включаете в строке выше ставки изменив `make_predictions=False` на `make_predictions=True`
15. Если найдёте стримеров которые дают нужные вам бонусы за баллы канал, например маджи, деньги на сервере или сабки на любых стримеров, то добавляйте их ник следующей строкой в файле main.py по шаблону ниже и включайте ставки если надо редактируя make_predictions
`Streamer("ЗДЕСЬ НИК СТРИМЕРА", settings=StreamerSettings(make_predictions=False  , follow_raid=True , claim_drops=True  , watch_streak=True , bet=BetSettings(strategy=Strategy.SMART      , percentage=5 , stealth_mode=True,  percentage_gap=20 , max_points=234   , filter_condition=FilterCondition(by=OutcomeKeys.TOTAL_USERS,      where=Condition.LTE, value=800 ) ) )),`
16. Настроив это всё, заходим на https://github.com , регистрируемся и создаём приватный репозиторий
![image](images\451954017-f42b81f1-cb91-49c1-aff2-95204edc836d.png)
![image](images\451954248-0d8d9be6-f578-407c-afa2-588eeb072968.png)
17. Заливаем всё содержимое папки майнера на гх
![image](images\451954564-01e3a257-b77b-4fe4-832a-8ba372e310af.png)
![image](images\451955050-d637539c-d543-48b8-a49d-8487439f6166.png)
18. Регаемся на сайте https://render.com (можно сразу через гитхаб)
19. Добавляем Web Service в дэшборде
![image](images\451956239-d3fda88b-ddb6-4ee1-87b5-871ee1745ced.png)
20. Выбираем нужный репозиторий и ставим Python 3 вместо Docker
![image](images\451956880-24ee7833-1d23-4fb0-acba-7c104a16b118.png)
22. Вставляем команду для запуска майнера `python main.py` и ставим бесплатный тарифный план
![image](images\451957535-c6ddf8bf-60c6-4694-ae64-20834db46cb0.png)
23. Вставляем username и password в поля, вводим в value свои логин и пароль от твича (хз зачем, но на всякий, можно трайнуть ввести рандомные данные, а потом если не запустит, то поставить как надо)
![image](images\451958568-7631abab-89a0-4081-9f29-0113e0c3c301.png)
24. Тыкаем на Deploy Web Service и ждём пока это всё запустит
![image](images\451959052-b3a447fc-db5e-4060-9bc4-81abb8bae17b.png)
25.После запуска берём ссылку и идём на сайт https://cron-job.org
![image](images\451959761-a29e813a-ed91-4b64-892e-d487ddb56b8d.png)
26. Регаемся на сайте, заходим в Cron задания и создаём новое
![image](images\451960297-dcf264b9-059b-4912-baaf-dcb66420704f.png)
27. Вставляем url с рендера и ставим таймаут 2 минуты
![image](images\451960816-83c5a538-30a5-4551-b857-58f75f261e2b.png)
28. Поздравляю, всё работает.
29. Накопив нужное кол-во баллов 15к и/или более покупаем на твиче нужные награды, 2200 маджей самое выгодное из маджей, остальное по потребности, пишете свой сервер и статик при покупке
![image](images\451963151-625610a7-330c-4287-9678-0c566f107ddf.png)


если хотите мониторить ход работы софта, заходим в https://dashboard.render.com/ и переходим в ваш веб сервис, далее заходим в лог и чекаем ход получения наград
![image](images\452009094-7d9ff03c-4a36-4bfe-ba57-060d388348fd.png)
