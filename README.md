# api_yamdb
## Описание
Backend приложения YamDB. 
Проект объединяет в себе функционал работы api сервисов проекта для публикации произведений,
отзывов и комментариев к ним. 
View- функции реализованы с помощью вьюсетов, аутентификация пользователей через JWT-токены.

## Установка
```
https://github.com/Diana187/api_yamdb.git
```
```
cd api_yamdb
```
Cоздать и активировать виртуальное окружение:
```
python3 -m venv env
```
```
source env/bin/activate
```
Установить зависимости из файла requirements.txt:
```
python3 -m pip install --upgrade pip
```
```
pip install -r requirements.txt
```
Выполнить миграции:
```
python3 manage.py migrate
```
Выполнить импорт данных в базу данных (при необходимости):
```
python3 manage.py load_data_from_csv
```
Запустить проект:
```
python3 manage.py runserver
```
Переменные окружения (по умолчанию):
```
====содержание файла .env=====
# указываем, что работаем с postgresql
DB_ENGINE

# имя базы данных
DB_NAME

# логин для подключения к базе данных
POSTGRES_USER

# пароль для подключения к БД (установите свой)
POSTGRES_PASSWORD

# название сервиса (контейнера)
DB_HOST

# порт для подключения к БД
DB_PORT
```


# Примеры
Доступ к документации API представлен по ссылке:
[http://127.0.0.1:8000/redoc/](http://127.0.0.1:8000/redoc/)