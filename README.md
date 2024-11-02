# Проект "Foodgram"

## Стек технологий
[![Python](https://img.shields.io/badge/-Python-464646?style=flat&logo=Python&logoColor=56C0C0&color=008080)](https://www.python.org/)
[![Django](https://img.shields.io/badge/-Django-464646?style=flat&logo=Django&logoColor=56C0C0&color=008080)](https://www.djangoproject.com/)
[![Django REST Framework](https://img.shields.io/badge/-Django%20REST%20Framework-464646?style=flat&logo=Django%20REST%20Framework&logoColor=56C0C0&color=008080)](https://www.django-rest-framework.org/)
[![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-464646?style=flat&logo=PostgreSQL&logoColor=56C0C0&color=008080)](https://www.postgresql.org/)
[![Nginx](https://img.shields.io/badge/-NGINX-464646?style=flat&logo=NGINX&logoColor=56C0C0&color=008080)](https://nginx.org/ru/)
[![gunicorn](https://img.shields.io/badge/-gunicorn-464646?style=flat&logo=gunicorn&logoColor=56C0C0&color=008080)](https://gunicorn.org/)
[![Docker](https://img.shields.io/badge/-Docker-464646?style=flat&logo=Docker&logoColor=56C0C0&color=008080)](https://www.docker.com/)
[![Docker-compose](https://img.shields.io/badge/-Docker%20compose-464646?style=flat&logo=Docker&logoColor=56C0C0&color=008080)](https://www.docker.com/)
[![Docker Hub](https://img.shields.io/badge/-Docker%20Hub-464646?style=flat&logo=Docker&logoColor=56C0C0&color=008080)](https://www.docker.com/products/docker-hub)
[![GitHub%20Actions](https://img.shields.io/badge/-GitHub%20Actions-464646?style=flat&logo=GitHub%20actions&logoColor=56C0C0&color=008080)](https://github.com/features/actions)

## Общее описание
Проект Foodgram - онлайн-сервис, пользователи которого могут выкладывать свои рецепты, просматривать рецепты других пользователей, и если чей-то рецепт приглянулся, пользователь может добавить его в "Избранное". Пользователь может подписаться на автора, чьи рецепты нравятся ему. Присутствует фильтрация по тегам, чтобы было удобно выбирать блюда на разные виды приема пищи. Если пользователь решит приготовить блюдо по выбранному рецепту, нужно будет добавить его в "Список покупок". В данном разделе можно скачать получившийся список покупок, в котором будут ингредиенты и их количество.



## Как развернуть проект локально

1. Клонируйте репозиторий [foodgram](https://github.com/SergoBu/foodgram) с помощью следующей команды:

```bash
git clone git@github.com:SergoBu/foodgram.git
```

3. В локальной директории проекта клонированного репозитория создайте файл `.env` и заполнить его по аналогии с файлом `.env.example`.

4. В локальной директории проекта клонированного репозитория запустите `docker compose` с помощью команды:

```bash
docker compose up -d
```

5. Соберите статические данные и примените миграции с помощью команд:

```bash
docker compose exec backend python manage.py collectstatic
```
```bash
docker compose exec backend python manage.py makemigrations
```
```bash
docker compose exec backend python manage.py migrate
```

6. Загрузите в базу данных начальный набор ингредиентов:
```bash
docker compose exec backend python manage.py add_ingredients
```

7. Приложение будет доступно в браузере по адресу [http://localhost](http://localhost).

---

Проект "Foodgram" доступен по ссылке: [foodgram.ddnsking.com](https://foodgram.ddnsking.com)

Автор проекта: [Сергей Будорин](https://github.com/SergoBu)