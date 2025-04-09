# GoFast_rent
Анализ данных сервиса аренды самокатов GoFast и проверка гипотез

Цель исследования
**Анализ данных сервиса аренды самокатов GoFast и проверка гипотез**  
​
Чтобы совершать поездки по городу, пользователи сервиса GoFast пользуются мобильным приложением. Сервисом можно пользоваться:
1. без подписки
 - абонентская плата отсутствует;
 - стоимость одной минуты поездки — 8 рублей;
 - стоимость старта (начала поездки) — 50 рублей;
2. с подпиской Ultra
 - абонентская плата — 199 рублей в месяц;
 - стоимость одной минуты поездки — 6 рублей;
 - стоимость старта — бесплатно.
​
**Входные данные:**
​
Пользователи —  `users_go.csv`
​
| Столбец | Обозначение |
| ------- | ------- |
| `user_id` | уникальный идентификатор пользователя |
| `name` | имя пользователя |
| `age` | возраст |
| `city` | город |
| `subscription_type` | тип подписки (free, ultra) |
​
Поездки — `rides_go.csv`
​
| Столбец | Обозначение |
| ------- | ------- |
| `user_id` | уникальный идентификатор пользователя |
| `distance` | расстояние, которое пользователь проехал в текущей сессии (в метрах) |
| `duration` | продолжительность сессии (в минутах) — время с того момента, как пользователь нажал кнопку «Начать поездку» до момента, как он нажал кнопку «Завершить поездку» |
| `date` | дата совершения поездки |
​
Подписки — `subscriptions_go.csv`
​
| Столбец | Обозначение |
| ------- | ------- |
| `subscription_type` | тип подписки |
| `minute_price` | стоимость одной минуты поездки по данной подписке |
| `start_ride_price` | стоимость начала поездки |
| `subscription_fee` | стоимость ежемесячного платежа |
​
​
Пути к файлам: 
​
- `/datasets/users_go.csv`
- `/datasets/rides_go.csv`
- `/datasets/subscriptions_go.csv`
​
### Ход исследования 
​
1. Обзор данных:
- Импортирование необходимых библиотек.
- Чтение файлов с данными.
- Общий обзор информации.
​
2. Предобработка данных:
​
- Приведение типов данных к корректным
- Проверка и обработка дубликатов
​
3. Исследовательский анализ данных (EDA):
​
- Анализ частоты встречающихся городов
- Анализ соотношение пользователей с подпиской и без
- Анализ распределения пользователей по возрасту
- Анализ расстояния, которое пользователь преодолел за одну поездку
​
4. Объединение данных
- Объеденение данных в один датафрейм
- Создание дополнительных датафреймов
- Анализ распределения расстояний поездок по подпискам
- Анализ распределения времени поездок по подпискам
​
5. Подсчет выручки
​
- Создание аггрегированного датафрейма
- Добавления столбца с помесячной выручкой
​
6. Проверка гипотез:
​
- Тратят ли пользователи с подпиской больше времени на поездки?
- Среднее расстояние, которое проезжают пользователи с подпиской за одну поездку, не превышает 3130 метров?
- Будет ли помесячная выручка от пользователей с подпиской по месяцам выше, чем выручка от пользователей без подписки.
- Количество обращений в техподдержку значимо снизилось
​
7. Распределения
​
- Рассылка промокодов
- Открытие push-уведомлений
​
8. Формирование вывода
