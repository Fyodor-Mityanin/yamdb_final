# API YAmdb
[Workflow badge](https://github.com/Fyodor-Mityanin/yamdb_final/workflows/YaMDB_final%20workflow/badge.svg)

This is a training project from the Yandex Prakticum

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them

```
Docker v20.10.2 or newer
```

### Installing

Clone repository to your pc and run Docker-Compose

```
docker-compose up
```
You need to create .env file and fill it with your data. Watch .env.example file in root directory, it's example.

Then you need to be sure that container is running

```
docker container ls
```

Take CONTAINER ID and run

```
docker exec -it <CONTAINER ID> bash
```

Now you need to make migrations

```
python manage.py migrate
```

and create superuser

```
python manage.py createsuperuser
```

You can also fill DB from fixtures.json file

```
python manage.py loaddata fixtures.json

```

## Project avalible at

[Redoc](http://130.193.52.84/redoc/) - This is redoc page, you can read about YaMDB_API
[Admin](http://130.193.52.84/admin/) - This is admin login page
[API](http://130.193.52.84/api/v1/titles/) - You can check how API works


## Built With

* [Django 3.1](https://docs.djangoproject.com/en/3.1/) - The web framework used
* [Django REST framework 3.11](https://www.django-rest-framework.org/) - The REST framework used
* [PostgreSQL 12.4](https://www.postgresql.org/docs/12/plperl-builtins.html) - Object-relational database system used
* [Docker 20.10.2](https://www.docker.com/) - Package software used
* [JWT 1.7.1](https://jwt.io//) - JSON Web Token


## Authors

* **Fedor Mityanin** - [Fyodor-Mityanin](https://github.com/Fyodor-Mityanin)
