## Данные

Информация о действиях пользователей приложения по продаже продуктов питания: 
- название события,
- уникальный идентификатор пользователя,
- время события,
- номер эксперимента (две контрольные группы и одна экспериментальная).

## Задача

Необходимо изучить воронку продаж. Узнать, как пользователи доходят до покупки. Сколько пользователей доходят до покупки, а сколько — «застревают» на предыдущих шагах. На каких именно.

Необходимо исследовать результаты A/A/B-теста. Дизайнеры захотели поменять шрифты в приложении. Решение должно быть принято по результатам A/A/B-теста. Пользователей разбили на 3 группы: 2 контрольные со старыми шрифтами и одну экспериментальную — с новыми. Необхоидмо выяснить, какой шрифт лучше.

Причины создания двух А-групп вместо одной: если две контрольные группы окажутся равны, можно быть уверенными в точности проведенного тестирования. Если же между значениями A и A есть существенные различия, это поможет обнаружить факторы, которые привели к искажению результатов. Сравнение контрольных групп также поможет понять, сколько времени и данных потребуется для дальнейших тестов.

## Технологии

Python, Pandas, SciPy, Matplotlib, NumPy

## Выводы

Ни на одном этапе не получилось отвергнуть нулевую гипотезу, между долями пользователей нет значимой разницы. Это касается и проверки между группами А1, А2. И проверки каждой из групп А с группой В, и сравнения объединенной группы А с группой В. Получается изменение шрифта не повлияло на поведение пользователей. Они не стали чаще переходить на следующий этап воронки.

Для проверки результатов эксперимента был выбран уровень значимости 0.05. Также была применена поправка Бонферрони - использовался уровень статистической значимости 0.003.

В процессе анализа и тестирования, была сформирована следующая воронка:

- Посещение главного экрана
- Посещение экрана с предложением
- Экран корзины
- Экран успешной оплаты
- 
Основная потеря пользователей происходит после посещения главного экрана. Пользователи решают продолжать ли взаимодействие дальше или покинуть приложение. В этот момент теряется 38%. От оставшихся 4593 пользователей 19% не переходят в корзину. На этапе корзины люди уже более-менее определились надо ли им совершать покупку и из них отказываются от оплаты заказа 14%

Доля пользователей, которые доходят от главного экрана до оплаты, составляет 48%
