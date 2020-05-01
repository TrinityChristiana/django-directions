# Django Admin
## Content

1. ### [Creating Admin]()
1. ### [Open Admin Page]()
1. ### [Enter Admin Site]()
1. ### [Make App Editable in Admin]()
1. ### [Explore the admin functionality]()

## Create Admin User
- Run this command
    ```shell
    python manage.py createsuperuser
    ```
- Enter your desired username and press enter.
    ```shell
    Username: admin
    ```
- You will then be prompted for your desired email address:
    ```shell
    Email address: admin@example.com
    ```
- The final step is to enter your password. You will be asked to enter your password twice, the second time as a confirmation of the first.
    ```shell
    Password: **********
    Password (again): *********
    Superuser created successfully.
    ```
## Open Admin Page
- Make sure [server is running](https://github.com/TrinityTerry/django-directions/blob/master/contents/run_server.md#run-server)
- Go to development server url `http://localhost:8000/admin/`
- You should see admin's login screen

    ![Admin Login Screen](images/admin_login_screen.png)

## Enter Admin Site
- Login with the new login information you created with `createsuperuser`
- You should see this Admin Index Page
    ![Admin Index Page](images/admin_index.png)
- On the page, you should see a few types of editable content: groups and users. They are provided by [`django.contrib.auth`](https://docs.djangoproject.com/en/3.0/topics/auth/#module-django.contrib.auth), the authentication framework shipped by Django.

## Make App Editable in Admin
- Open App's `admin.py` file
- Import Object they you want availible in the admin.
    ```python
    from .models import Question
    ```
- Make it availible to admin
    ```python
    admin.site.register(Question)
    ```
- In all it will look like this:
    ```python
    from django.contrib import admin

    from .models import Question

    admin.site.register(Question)
    ```

## Explore the admin functionality
- If you go back to the Admin Index page, it Question should be displayed as an editable item.

    ![Updated Admin Question](images/updated_admin_question.png)
- If you click questions, a page that displays all the questions in the database lets you choose one to change it.

    ![question_admin_page](images/question_admin_page.png)

- If you select an question to change it, a page with a form will pop-up:

    ![Editing form for question object](images/admin_edit_question.png)

    - Things to note here:

        - The form on the page is automatically created from the Question model.

        - The different model field types ([`DateTimeField`](https://docs.djangoproject.com/en/3.0/ref/models/fields/#django.db.models.DateTimeField), [`CharField`](https://docs.djangoproject.com/en/3.0/ref/models/fields/#django.db.models.CharField)) correspond to the appropriate HTML input widget. Each type of field knows how to display itself in the Django admin.

        - Each [`DateTimeField`](https://docs.djangoproject.com/en/3.0/ref/models/fields/#django.db.models.DateTimeField) gets free JavaScript shortcuts. Dates get a “Today” shortcut and calendar popup, and times get a “Now” shortcut and a convenient popup that lists commonly entered times.

    - At the bottom part of the page, there are a few options:

        - Save: Saves changes and returns to the page with list of questions 

        - Save and continue editing – Saves changes but stays on current page

        - Save and add another – Saves changes and loads a new, blank form to create a new question

        - Delete – Displays a delete confirmation page.

    - In the top right hand corner, there's a History option. If you click it, you'll see a page that lists all changes made to this object from the Django admin side, with the date of log and username of the person who made the update:

        ![History page for question object](images/admin_history_page.png)
***
*These Directions are based on [Writing your first Django app](https://docs.djangoproject.com/en/3.0/intro/tutorial01/) from the [Official Django Website](https://www.djangoproject.com/)*

__Created By: [Trinity Terry](https://github.com/TrinityTerry)__