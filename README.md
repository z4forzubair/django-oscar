# Django Oscar[3.1] Setup

## Stack Details

Python = 3.8

Django = 4.0

Postgres = 12

## Apps Description

The project is an implementation of `django-oscar` package.

## Setup Project

### Create Database

This project uses Postgres database. Database configurations are stored in `frobshop/local_settings.py` which are being
imported in main
`frobshop/settings.py` file.

`local_settings.py` should have this object as per local configurations.

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': 'database-name',
        'USER': 'user',
        'PASSWORD': 'password',
        'HOST': 'localhost',
        'PORT': '5432',
        'ATOMIC_REQUESTS': True,
    }
}
```

### Run Project

Once database is set up, run the following commands.

**Install Requirements**

`pip install -r requirements.txt`

**Set Environment variables**

**Apply Migrations**

`python manage.py migrate`

**Run Server**

`python manage.py runserver`

**Create Super User**

`python manage.py createsuperuser`
