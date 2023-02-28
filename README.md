# Docker - compose
REST API для сервиса YaMDb — базы отзывов о фильмах, книгах и музыке.

![Django-app workflow](https://github.com/NomernayaRadiostancia/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

## Описание
Учебный проект 13 спринта. CI и CD проекта api_yamdb

## Стек технологий
- Python
- Django
- Docker
- Nginx

### Запуск проекта в dev-режиме
Склонируйте репозиторий. Находясь в папке с кодом создайте виртуальное окружение `python -m venv venv`, активируйте его (Windows: `source venv\scripts\activate`; Linux/Mac: `sorce venv/bin/activate`), установите зависимости `python -m pip install -r requirements.txt`.

### Запустить приложение в контейнерах:
Из директории infra/
`docker-compose up -d --build`

### Выполнить миграции:
Из директории infra/
`docker-compose exec web python manage.py migrate`

### Создать суперпользователя:
Из директории infra/
`docker-compose exec web python manage.py createsuperuser`

## Примеры запросов к API

## Собрать статику:
Из директории infra/
`docker-compose exec web python manage.py collectstatic --no-input`
## Запуск pytest:
Из корневой папки:
`pytest`

## Описание команды для заполнения базы данными:
`docker-compose exec web python manage.py dumpdata > fixtures.json`

## Развернутый проект:
`http:/158.160.58.80/admin/`
## Документация API с примерами:
`http://158.160.58.80/redoc/`

## шаблон наполнения env-файла:
/infra/.env.template
### итоговый проект курса выполнила:
- Елизавета Огай