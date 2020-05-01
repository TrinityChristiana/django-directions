# Models

## Contents
1. ### [Create Model](https://github.com/TrinityTerry/django-directions/blob/master/contents/models.md#create-model-1)
1. ### [Activating Models](https://github.com/TrinityTerry/django-directions/blob/master/contents/models.md#activating-models-1)

## Create Model

*Database Layout*

- In the app's `models.py` here is an example of creating a couple models
    ``` python
    from django.db import models


    class Question(models.Model):
        question_text = models.CharField(max_length=200)
        pub_date = models.DateTimeField('date published')


    class Choice(models.Model):
        question = models.ForeignKey(Question, on_delete=models.CASCADE)
        choice_text = models.CharField(max_length=200)
        votes = models.IntegerField(default=0)
    ```
- The _models_ are creaded by defining a class that inherits the [django.db.models.Model](https://docs.djangoproject.com/en/3.0/ref/models/instances/#django.db.models.Model) class

- Each variable in each class represents a _database field_ within the models

- _Fields_ are created by instantiating a [Field](https://docs.djangoproject.com/en/3.0/ref/models/fields/#django.db.models.Field) instance ([CharField](https://docs.djangoproject.com/en/3.0/ref/models/fields/#django.db.models.CharField), [DateTileField](https://docs.djangoproject.com/en/3.0/ref/models/fields/#django.db.models.DateTimeField), etc.)

- Name of variable that holds instance will be the _field name_ (__question_text__ or __pub_date__) Database will use this as the column name

- In the field function you can pass in a first argument to give the field a name. Ex. `DateTimeField('date published')`

- Relationship defined by using [`ForeignKey`](https://docs.djangoproject.com/en/3.0/ref/models/fields/#django.db.models.ForeignKey). Here tells Django that each `Choice` is related to a single `Question`. 

    ```python
    question = models.ForeignKey(Question, on_delete=models.CASCADE)
    ```
## Activating Models
*Connecting Application with Project*

- Get AppConfig class's path from app's `apps.py` file. In the below example, the path name would be `polls.apps.PollsConfig` 
    ```python
    # PATH: polls/apps.py
    class PollsConfig(AppConfig):
    name = 'polls'
    ```
- Go to Projects `settings.py` file
- Use path name to create a refrence of the application in the [INSTALLED_APPS](https://docs.djangoproject.com/en/3.0/ref/settings/#std:setting-INSTALLED_APPS) setting like this:

    ```python
    INSTALLED_APPS = [
        'polls.apps.PollsConfig', # <-- This line
        'django.contrib.admin',
        'django.contrib.auth',
        'django.contrib.contenttypes',
        'django.contrib.sessions',
        'django.contrib.messages',
        'django.contrib.staticfiles',
    ]
    ```
- Tell Django that some models were updated by running this command

    ```shell
    python manage.py makemigrations {APP_NAME}
    ```
- Migrate again to apply changes to the database

    ```shell
    python manage.py migrate
    ```
***
*These Directions are based on [Writing your first Django app](https://docs.djangoproject.com/en/3.0/intro/tutorial01/) from the [Official Django Website](https://www.djangoproject.com/)*

__Created By: [Trinity Terry](https://github.com/TrinityTerry)__