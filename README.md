# API_Yatube
Version: 1.01
Release Date: 04/08/2021
## The API for Yatube service
[![YaMDB_final workflow](https://github.com/andrew-dj/yamdb_final/actions/workflows/main.yml/badge.svg)](https://github.com/andrew-dj/yamdb_final/actions/workflows/main.yml)
This is an application providing API functionality for movie reviews database.
- JWT token auth
- CRUD on reviews
- Reviews rating
- ✨Magic ✨

## Authors
* Andrey Bulynin
## Technologies
* Python
* Django
* PostgreSQL

## Installation
####Variables in .env:
- DB_ENGINE=# database infrastructure service
- DB_NAME= # database name
- POSTGRES_USER=# database user login
- POSTGRES_PASSWORD=# database user password
- DB_HOST= # database container  
- DB_PORT= # database port

#### 1 - Building the container up
```bash
docker-compose build
```
#### 2 - Mounting the container
```bash
docker-compose up
```
#### 3 - Necessary database operations
```bash
docker-compose run web python manage.py makemigrations --no-input
docker-compose run web python manage.py migrate --no-input
```
## Usage
### Making a Django superuser
```bash
docker-compose run web python manage.py createsuperuser
```
### Import dumpdata from .json
```bash
docker-compose run web python manage.py loaddata path/to/your/json
```
### Unmount a container
```bash
docker-compose down
```
