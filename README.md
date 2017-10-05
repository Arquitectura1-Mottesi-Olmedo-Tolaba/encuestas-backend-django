#encuestas-backend-django
[![Build Status](https://travis-ci.org/Arquitectura1-Mottesi-Olmedo-Tolaba/encuestas-backend-django.svg?branch=master)](https://travis-ci.org/Arquitectura1-Mottesi-Olmedo-Tolaba/encuestas-backend-django)

Preinscripcion UNQ backend en Django. Check out the project's [documentation](http://Arquitectura1-Mottesi-Olmedo-Tolaba.github.io/encuestas-backend-django/).

# Prerequisites
- [virtualenv](https://virtualenv.pypa.io/en/latest/)
- [postgresql](http://www.postgresql.org/)
- [redis](http://redis.io/)
- [travis cli](http://blog.travis-ci.com/2013-01-14-new-client/)
- [heroku toolbelt](https://toolbelt.heroku.com/)

# Initialize the project
Create and activate a virtualenv:

```bash
virtualenv env
source env/bin/activate
```
Install dependencies:

```bash
pip install -r requirements/local.txt
```
Create the database:

```bash
createdb encuestas-backend-django
```
Initialize the git repository

```
git init
git remote add origin git@github.com:Arquitectura1-Mottesi-Olmedo-Tolaba/encuestas-backend-django.git
```

Migrate the database and create a superuser:
```bash
python encuestas-backend-django/manage.py migrate
python encuestas-backend-django/manage.py createsuperuser
```

Run the development server:
```bash
python encuestas-backend-django/manage.py runserver
```

# Create Servers
By default the included fabfile will setup three environments:

- dev -- The bleeding edge of development
- qa -- For quality assurance testing
- prod -- For the live application

Create these servers on Heroku with:

```bash
fab init
```

# Automated Deployment
Deployment is handled via Travis. When builds pass Travis will automatically deploy that branch to Heroku. Enable this with:
```bash
travis encrypt $(heroku auth:token) --add deploy.api_key
```
