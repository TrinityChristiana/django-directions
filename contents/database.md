# Database Setup

1. Open project `settings.py` file
1. Find the Database Dctionary to find these key values

   If you're using a database thats not SQLite you will have to change these values.

   - [ENGINE](https://docs.djangoproject.com/en/3.0/ref/settings/#std:setting-DATABASE-ENGINE)
   - [NAME](https://docs.djangoproject.com/en/3.0/ref/settings/#std:setting-NAME)

   > _If you are not using SQLite as your database, additional settings such as [USER](https://docs.djangoproject.com/en/3.0/ref/settings/#std:setting-USER), [PASSWORD](https://docs.djangoproject.com/en/3.0/ref/settings/#std:setting-PASSWORD), and [HOST](https://docs.djangoproject.com/en/3.0/ref/settings/#std:setting-HOST) must be added. For more details, see the reference documentation for [DATABASES](https://docs.djangoproject.com/en/3.0/ref/settings/#std:setting-DATABASES)._

1. Set [TIME_ZONE](https://docs.djangoproject.com/en/3.0/ref/settings/#std:setting-TIME_ZONE) to your timezone
1. Note the [INSTALLED_APPS](https://docs.djangoproject.com/en/3.0/ref/settings/#std:setting-INSTALLED_APPS) setting at the top of the file. That holds the names of all Django applications that are activated in this Django instance. Apps can be used in multiple projects, and you can package and distribute them for use by others in their projects.

   By default, [INSTALLED_APPS](https://docs.djangoproject.com/en/3.0/ref/settings/#std:setting-INSTALLED_APPS) contains the following apps, all of which come with Django:

   [django.contrib.admin](https://docs.djangoproject.com/en/3.0/ref/contrib/admin/#module-django.contrib.admin) – The admin site. You’ll use it shortly.

   [django.contrib.auth](https://docs.djangoproject.com/en/3.0/topics/auth/#module-django.contrib.auth) – An authentication system.

   [django.contrib.contenttypes](https://docs.djangoproject.com/en/3.0/ref/contrib/contenttypes/#module-django.contrib.contenttypes) – A framework for content types.

   [django.contrib.sessions](https://docs.djangoproject.com/en/3.0/topics/http/sessions/#module-django.contrib.sessions) – A session framework.

   [django.contrib.messages](https://docs.djangoproject.com/en/3.0/ref/contrib/messages/#module-django.contrib.messages) – A messaging framework.

   [django.contrib.staticfiles](https://docs.djangoproject.com/en/3.0/ref/contrib/staticfiles/#module-django.contrib.staticfiles) – A framework for managing static files.

1. Create Tables

   - Run the following command:
     ```shell
     $ python manage.py migrate
     ```
   - This command looks at [INSTALLED_APPS](https://docs.djangoproject.com/en/3.0/ref/settings/#std:setting-INSTALLED_APPS) settings and created database tables needed according to the daabase settings.

***
*These Directions are based on [Writing your first Django app](https://docs.djangoproject.com/en/3.0/intro/tutorial01/) from the [Official Django Website](https://www.djangoproject.com/)*

__Created By: [Trinity Terry](https://github.com/TrinityTerry)__