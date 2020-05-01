# How To Create Django Application

> __Projects vs. apps__
> > What’s the difference between a project and an app? An app is a Web application that does something – e.g., a Weblog system, a database of public records or a small poll app. A project is a collection of configuration and apps for a particular website. A project can contain multiple apps. An app can be in multiple projects.
> - *[Official Django Website](https://docs.djangoproject.com/en/3.0/intro/tutorial01/#creating-the-polls-app)*

To create an application in the django project run the following command

```shell
$ python manage.py startapp {APP_NAME}
```

***
## ~/.zshrc Commands
*The following commands will only work if the local django file is in the home directory*

Add this to .zshrc file. THis will start create a django application
```zsh
mkdj() {
source ~/.virtualenvs/djangodev/bin/activate;
   python -m pip install -e ~/django;
   django-admin startproject "$@";
   cd $_;
   code .;
   

}
```

Add this to .zshrc help function to remeber function name
```zsh
echo " - mkdj()                    start virtual env"
```

***
*These Directions are based on [Writing your first Django app](https://docs.djangoproject.com/en/3.0/intro/tutorial01/) from the [Official Django Website](https://www.djangoproject.com/)*

__Created By: [Trinity Terry](https://github.com/TrinityTerry)__