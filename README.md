# api_yamdb
api_yamdb

## Установка
Запустите docker-compose командой ```docker-compose up```. 
У вас развернётся проект, запущенный через Gunicorn с базой данных Postgres.

Выполните по очереди команды:
- docker-compose exec web python manage.py migrate
- docker-compose exec web python manage.py createsuperuser
- docker-compose exec web python manage.py collectstatic --no-input 

Проверьте работоспособность приложения:
- зайдите на http://localhost/admin/ и убедитесь, что страница отображается полностью: статика подгрузилась;
- авторизуйтесь под аккаунтом суперпользователя и убедитесь, что миграции прошли успешно;
- протестируйте приложение, например, через Postman.

## Примеры запровов:
```
Когда вы запустите проект, по адресу http://127.0.0.1:8000/redoc/ будет доступна документация для API Yatube. В документации описано, как должен работать ваш API. Документация представлена в формате Redoc
```