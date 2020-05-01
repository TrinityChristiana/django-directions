# Run Server

Unless already done so, ```cd``` into project directory then run this command:

```shell
$ python manage.py runserver
```
or this command to have it on a different port 

```shell
$ python manage.py runserver 8080
```

You'll then see something like this in the command line:

```shell
Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).

You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.
May 01, 2020 - 16:49:56
Django version 3.1, using settings 'poll_site.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
```

> *Ignore the Migration warning for now*

Visit the server url [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your web browser to see a "The install worked successfully! Congratulations!" message

***
*These Directions are based on [Writing your first Django app](https://docs.djangoproject.com/en/3.0/intro/tutorial01/) from the [Official Django Website](https://www.djangoproject.com/)*

__Created By: [Trinity Terry](https://github.com/TrinityTerry)__