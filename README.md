# api_yamdb
## Описание
Backend приложения YamDB. 
Проект объединяет в себе функционал работы API-сервисов проекта для публикации произведений,
отзывов и комментариев к ним. 
View- функции реализованы с помощью вьюсетов, аутентификация пользователей через JWT-токены.

## Установка
Запустить контейнер:
```
docker image infra-sp2 run 
```

Выполнить миграции:
```
docker-compose exec web python manage.py migrate
```

Выполнить сборку статики:
```
docker-compose exec web python manage.py collectstatic --no-input 
```

Выполнить импорт данных в базу данных (при необходимости):
```
docker-compose exec web python manage.py load_data_from_csv
```

# Запуск проекта
# [http://localhost](http://localhost)

# Переменные окружения (по умолчанию):
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
[http://localhost/redoc/](http://localhost/redoc/)