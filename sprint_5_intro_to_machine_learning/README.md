# Рекомендательная система тарифов

### Статус проекта
- Завершен ✅

### Задача  
- Построить рекомендательную систему тарифов для оператора связи.

### Описание
- Оператор мобильной связи «Мегалайн» выяснил: многие клиенты пользуются архивными тарифами. Необходимо создать рекомендательную систему тарифов, которая позволит предложить пользователю наиболее подходящий новый тариф. Для этого используется заранее предобработанный набор данных, содержащий в себе информацию о клиентах, уже пользующихся целевыми тарифами. Для выполнения задачи был протестирован набор различных моделей машинного обучения и выбрана наиболее эффективная. 

### Вывод
- Был использован целый зоопарк различных алгоритмов машинного обучения. Наилучшие метрики продемонстрировали алгоритмы на основе решающих деревьев, причем лес случайных деревьев побеждает с ощутимым отрывом. Это может говорить о том, что использованный набор данных имеет нелинейные зависимости, с котороми "деревянные" алгоритмы справляются лучше линейных. Также к таким результатам мог привести размер датасета - он весьма скромен, поэтому алгоритм с применением бэггинга показывает себя наилучшим образом. 

### Сферы интереса
- Онлайн-сервисы, b2b-сервисы, E-commerce, телеком, рекламные платформы

### Применяемые технологии
- Pandas, Numpy, Sklearn

### Ретроспектива
- В данной работе допущено множество ошибок: не учтен дисбаланс классов при разбиении на выборки (каким образом выглядит разбиение в каждой из них - неизвестно) и проверке на вменяемость, также дисбаланс классов никак не учитывается в метрике; при обучении с использованием Grid/RandomizedSearch происходит дополнительная валидация на отдельной валидационной выборке, без чего можно было обойтись; функции для обучения абсолютно неоптимальны и раздуты в размерах, можно было бы сделать через цикл, также стоит избавиться от объявления глобальных переменных в теле функции; ошибки в codestyle - неиспользуемые переменные, закоменченные старые куски кода.  
