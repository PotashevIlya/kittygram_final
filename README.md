# Проект Kittygram
## Описание проекта
Kittygram - это проект, который позволяет вам делиться с миром информацией о своих котиках. Вы можете загрузить фотографию вашего любимца, указать его имя, год рождения и, конечно же, самые разнообразные "достижения". 
## Как запустить проект
1. Клонировать репозиторий и перейти в него в командной строке:
```
https://github.com/PotashevIlya/kittygram_final
```
```
cd kittygram_final
```
2. Создать .env файл в корневой директории по образцу .env.example
3. Запустить docker-compose
```
docker compose -f docker-compose.production.yml up
```
4. Применить миграции в контейнере бекэнда
```
docker compose -f docker-compose.production.yml exec backend python manage.py migrate
```
5. Собрать статику бекэнда
```
docker compose -f docker-compose.production.yml exec backend python manage.py collectstatic
```
6. Скопировать статику в директорию, связанную с volume
```
docker compose -f docker-compose.production.yml exec backend cp -r /app/collected_static/. /backend_static/static/
```
___
### Стек :bulb:
Django, Gunicorn, nginx, Rest API (DRF), PostgreSQL, Docker, CI/CD (GitHub Actions), React, Yandex Cloud.
___
### Workflow
[![Main Kittygram workflow](https://github.com/PotashevIlya/kittygram_final/actions/workflows/main.yml/badge.svg)](https://github.com/PotashevIlya/kittygram_final/actions/workflows/main.yml)

___  
#### Автор проекта:    
:small_orange_diamond: [Поташев Илья](https://github.com/PotashevIlya)  

