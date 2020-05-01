# How To Create Django Project

> __Projects vs. apps__
> > What’s the difference between a project and an app? An app is a Web application that does something – e.g., a Weblog system, a database of public records or a small poll app. A project is a collection of configuration and apps for a particular website. A project can contain multiple apps. An app can be in multiple projects.
> - *[Official Django Website](https://docs.djangoproject.com/en/3.0/intro/tutorial01/#creating-the-polls-app)*

- Run command  

    ```shell
    django-admin startproject {PROJECT_NAME}
    ```
- Created FIles information

    > These files are:
    > 1. The outer mysite/ root directory is a container for your project. Its name doesn’t matter to Django; you can rename it to anything you like.
    > 1. `manage.py`: A command-line utility that lets you interact with this Django project in various ways. You can read all the details about `manage.py` in django-admin and `manage.py`.
    > 1. The inner mysite/ directory is the actual Python package for your project. Its name is the Python package name you’ll need to use to import anything inside it (e.g. mysite.urls).
    > 1. `mysite/__init__.p`y: An empty file that tells Python that this directory should be considered a Python package. If you’re a Python beginner, read more about packages in the official Python docs.
    >  1. `mysite/settings.py`: Settings/configuration for this Django project. Django settings will tell you all about how settings work.
    >  1. `mysite/urls.py`: The URL declarations for this Django project; a “table of contents” of your Django-powered site. You can read more about URLs in URL dispatcher.
    >  1. `mysite/asgi.py`: An entry-point for ASGI-compatible web servers to serve your project. See How to deploy with ASGI for more details.
    > 1. `mysite/wsgi.py`: An entry-point for WSGI-compatible web servers to serve your project. See How to deploy with WSGI for more details.

    *- [Official Django website](https://docs.djangoproject.com/en/3.0/intro/tutorial01/#creating-a-project)*

***
*These Directions are based on [Writing your first Django app](https://docs.djangoproject.com/en/3.0/intro/tutorial01/) from the [Official Django Website](https://www.djangoproject.com/)*

__Created By: [Trinity Terry](https://github.com/TrinityTerry)__