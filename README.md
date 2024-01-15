# Taski - планировщик задач.

### Описание
Приложение для планирования задач. Есть фронтенд (React)
и бэкенд (Django). Задачи можно добавлять, изменять, удалять
и переводить из группы "незавершённые" в "завершённые".

## Технологии

- Фронтенд: React
- Бэкенд: Django Rest Framework
- База данных: PostgreSQL
- Nginx
- Docker
- Gunicorn
- Github actions

## Запуск проекта

Выполняем запуск:

```bash
sudo docker compose -f docker-compose.yml up
```

## После запуска: миграции, сбор статики



```bash
sudo docker compose -f docker-compose.yml exec backend python manage.py migrate

sudo docker compose -f docker-compose.yml exec backend python manage.py collectstatic

sudo docker compose -f docker-compose.yml exec backend cp -r /app/collected_static/. /backend_static/static/
```
