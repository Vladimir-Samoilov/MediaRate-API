# MediaRate API

MediaRate API — это RESTful сервис для сбора отзывов и рейтингов на произведения искусства: книги, фильмы, музыку и другие медиа. Проект реализован на Python с использованием Django REST Framework.

## Возможности

- Регистрация и аутентификация пользователей
- Добавление, редактирование и удаление отзывов
- Система рейтингов для каждого произведения
- Категоризация: жанры, категории, произведения
- Модерация комментариев и отзывов
- Поддержка JWT-аутентификации

## Технологический стек

- Python 3.8+
- Django 3.2+
- Django REST Framework
- Simple JWT
- PostgreSQL
- Docker, docker-compose (для быстрого развертывания)

## Быстрый старт

### Клонирование репозитория

```bash
git clone https://github.com/Vladimir-Samoilov/MediaRate-API.git
cd MediaRate-API
```

### Запуск с помощью Docker

1. Создайте файл `.env` по образцу `.env.example` и заполните переменные окружения.
2. Соберите и запустите контейнеры:

```bash
docker-compose up --build
```

3. Приложение будет доступно по адресу: http://localhost/api/

### Запуск локально (без Docker)

1. Установите зависимости:

```bash
pip install -r requirements.txt
```

2. Настройте переменные окружения (см. `.env.example`).
3. Примените миграции и создайте суперпользователя:

```bash
python manage.py migrate
python manage.py createsuperuser
```

4. Запустите сервер:

```bash
python manage.py runserver
```

## Примеры API-запросов

- Получить список произведений:  
  `GET /api/titles/`
- Оставить отзыв на произведение:  
  `POST /api/titles/{title_id}/reviews/`
- Зарегистрировать пользователя:  
  `POST /api/v1/auth/signup/`
- Получить JWT-токен:  
  `POST /api/v1/auth/token/`

## Документация

После запуска проекта документация доступна по адресу:  
`http://localhost/redoc/`  
или  
`http://localhost/api/docs/`

## Контакты

Автор: Владимир Самойлов  
GitHub: [Vladimir-Samoilov](https://github.com/Vladimir-Samoilov)
