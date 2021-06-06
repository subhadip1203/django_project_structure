# Django project structure 

1. Virtual environment 


## Virtual environment

install virtual environment : `pip install virtualenv`

make a virtual environment in folder named "venv" :<br>
ubuntu : `virtualenv venv` <br>

Activate virtual environment :<br>
ubuntu : `source venv/bin/activate` <br>
windows: `source ./venv/Scripts/activate` (by gitbash ) <br>

## install Django
by pip install :  `pip install django` <br>
by requirements.txt file: `pip install -r requirements.txt`<br>
To list all the installed packages : `pip freeze > requirements.txt`


##  divide project in different moules : like V1 , V2 , etc
create folder V1 and make a file __init__.py: `mkdir V1 && touch V1/__init__.py` 

### create project 

command: `django-admin startproject Project_SetUp .` <br>
( dot at the end of the command will seperate the "Project_SetUp" in a separate folder than other apps)

## create an app ( example : inside V1 folder  )


first create a folder for the app : `mkdir V1/app1` <br>
create the app : `python manage.py startapp app1 V1/app1` <br>

in sort: `mkdir V1/app1 &&  python manage.py startapp app1 V1/app1` <br>

create another folder : `mkdir V1/app2` <br>
create another app : `python manage.py startapp app2 V1/app2` <br>

in sort: `mkdir V1/app2 &&  python manage.py startapp app2 V1/app2` <br>


edit file settings.py => location : Project_SetUp/settings.py

INSTALLED_APPS = (
    ...
+    'V1.app1',
+    'V1.app2',
    ...
)