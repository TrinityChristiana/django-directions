# Installations

## Contents
1. ### [Install Python](https://github.com/TrinityTerry/django-directions/blob/master/installations.md#install-python)
1. ### [Install Django](https://github.com/TrinityTerry/django-directions/blob/master/installations.md#install-django)
1. ## [Test Installations](https://github.com/TrinityTerry/django-directions/blob/master/installations.md#test-that-you-have-django-installed-correctly)
***

## Install Python

Check to make sure Python is Installed by running this command

```shell
$ python
```

If python is installed you should see something like this:

```shell
Python X.X.X 
[Clang 10.0.1 (clang-1001.0.46.4)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
```

If you do not see this, you can go to [Python's Official download page](https://www.python.org/downloads/) to download the latest version of Python.
***

## Install Django
- [Install pip](https://pip.pypa.io/en/stable/installing/)
- Get copy of Django's development version
    1. [Fork Django on Github](https://github.com/django/django/fork)
    1. ```cd``` to home directory 

        *This is where the local copy of Django will live. If you choose to place it somewhere else, the zshrc commands at the end of this document will not work*
    1. Download Django source code by uwing the following command:
        ``` shell
        $ git clone https://github.com/{YOUR_GITHUB_NAME}/django.git
        ```
- Virtual Environment
    1. Create Virtual Environemnt
        ```shell
        $ python3 -m venv ~/.virtualenvs/djangodev
        ```
    1. Activate Virtual Environemt
        ```shell
        $ source ~/.virtualenvs/djangodev/bin/activate
        ```

        *If the above command does not work due to the __source__ keyword, try using this dot notation command to activate the Virtual Environment*

        ```shell
        $ . ~/.virtualenvs/djangodev/bin/activate
        ```
- Install Django

    1. Run command
        ```shell
        $ python -m pip install Django
        ```
***

## Test That you have Django installed correctly

- Run command

    ```shell
    python -m django --version
    ```
- This should return a version number for Django (X.X)

***
*These Directions are based on [Writing your first Django app](https://docs.djangoproject.com/en/3.0/intro/tutorial01/) from the [Official Django Website](https://www.djangoproject.com/)*