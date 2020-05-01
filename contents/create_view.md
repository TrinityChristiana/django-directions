# Create View

## Contents
1. ### [Update `view.py` file](https://github.com/TrinityTerry/django-directions/blob/master/create_view.md#update-viewpy-file)
2. ### [Call View](https://github.com/TrinityTerry/django-directions/blob/master/create_view.md#call-view)
3. ### [include function](https://github.com/TrinityTerry/django-directions/blob/master/create_view.md#include-)
4. ### [path function](https://github.com/TrinityTerry/django-directions/blob/master/create_view.md#path-)
***

## Update `view.py` file
- Open `view.py` file in application file
- Copy and paste this into the doccument
```python
from django.http import HttpResponse


def index(request):
    return HttpResponse("Hello, world.")
```
***

## Call View
To call this view, we need to map it to a URL

1. Create a URLconf in the app directory by creating a file called ```urls.py```
2. Add the following to the url file

    ```python
    from django.urls import path

    from . import views

    urlpatterns = [
        path('', views.index, name='index'),
    ]
    ```
1. In the root project folder, go to the second project folder and update tge urls.py file in there with

    ```python
    rom django.contrib import admin
    from django.urls import include, path

    urlpatterns = [
        path('{URL_PATH}/', include('{APP_FOLDER}.urls')),
        path('admin/', admin.site.urls),
    ]
    ```

    

1. Check to see that view works

- Make sure [server is running](https://github.com/TrinityTerry/django-directions/blob/master/run_server.md)
- Go to development server url `http://localhost:8000/{URL_PAYH}/`
- You should see `"Hello, world."`
***

## [include( )](https://docs.djangoproject.com/en/3.0/ref/urls/#django.urls.include)

> - The include() function allows referencing other URLconfs. Whenever Django encounters include(), it chops off whatever part of the URL matched up to that point and sends the remaining string to the included URLconf for further processing.
> - The idea behind include() is to make it easy to plug-and-play URLs. Since polls are in their own URLconf (`polls/urls.py`), they can be placed under “/polls/”, or under “/fun_polls/”, or under “/content/polls/”, or any other path root, and the app will still work.
>   - [Official Django Website](https://docs.djangoproject.com/en/3.0/intro/tutorial01/#write-your-first-view)
***

## [path( )](https://docs.djangoproject.com/en/3.0/ref/urls/#django.urls.path)
> The path() function is passed four arguments, two required: route and view, and two optional: kwargs, and name. At this point, it’s worth reviewing what these arguments are for.
- [Official Django Website](https://docs.djangoproject.com/en/3.0/intro/tutorial01/#write-your-first-view)

    ## [path( ) argument: route](https://docs.djangoproject.com/en/3.0/intro/tutorial01/#path-argument-route)

    ## [path( ) argument: view](https://docs.djangoproject.com/en/3.0/intro/tutorial01/#path-argument-view)

    ## [path( ) argument: kwargs](https://docs.djangoproject.com/en/3.0/intro/tutorial01/#path-argument-kwargs)

    ## [path( ) argument: name](https://docs.djangoproject.com/en/3.0/intro/tutorial01/#path-argument-name)
***
*These Directions are based on [Writing your first Django app](https://docs.djangoproject.com/en/3.0/intro/tutorial01/) from the [Official Django Website](https://www.djangoproject.com/)*

__Created By: [Trinity Terry](https://github.com/TrinityTerry)__
