# "My ToDo List"

My ToDo List - сервис, который помогает не забыть выполнить свои задания.

## Возможности
1. Создание задачи.
2. Редактирование задачи.
3. Изменение статуса задаси (выполнена/не выполнена).
4. Просмотр невыполненных задач.
5. Вспомнить выполненные задачи.

# Инструкция по развёртыванию (Windows)
* Склонировать проект в свою рабочую папку
    - ```git clone git@github.com:AndreyHlim/my_todo_list.git```
    - ```cd my_todo_list/```
* Развернуть и активировать виртуальное окружение
    - ```python -m venv venv```
    - ```source venv/Scripts/activate```
* Установить зависимости
    - ```pip install -r backend/requirements.txt```
* Создать файл .env на примере файла .env.example в директории my_todo_list
* Запустить проект
    - ```docker compose up --build -d```
* Применить миграции и собрать статику
    - ```docker compose exec backend python manage.py migrate```
    - ```docker compose exec backend python manage.py collectstatic```
    - ```docker compose exec backend cp -r /app/collected_static/. /backend_static/static/```
* Перейти по адресу http://localhost:8000/

## Инструменты, стек, технологии
1. Python,
2. Docker,
3. API,
4. Workflows,
5. Django,
6. Django REST framework,
7. Nginx.
