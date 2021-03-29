<You should install django everytime you create a newProject/a virtualenv>

STEP-1)Create a project folder(ex:folder1)

STEP-2)Create a virtual environment in that project folder by: 'python3 -m virtualenv <foldername in which virtual environment is to be created ---> ex: env>'

STEP-3)Activate that virtual environment by: 'source env<folder name>/bin/activate' (use this in the folder containing env)

STEP-4)Install django in the project folder containing 'env'(virtual environment directory) by: 'python3 -m pip install django' (not required if already installed in PC, you can directly use django-admin)

****To view the django-admin commands press: 'django-admin'****

STEP-5)To start a project in that folder: 'django-admin startproject <project name> .'(Project and app are different here.)

****Now the project files are created in the project folder(i.e. folder1) with the project name given in step-5****

STEP-6)In the directory containing manage.py create a local server by: 'python3 manage.py runserver'



****The development server starts at " http://127.0.0.1:8000/ "****
****If you want to use a different port than the default 8000, specify the port number on the command line, such as 'python3 manage.py runserver 5000'****
-------------------------------------------------------------------------
****When you run the server the first time, it creates a default SQLite database in the file db.sqlite3, which is intended for development purposes but can be used in production for low-volume web apps.****


****When you deploy to a web host, however, Django uses the host's web server instead. The wsgi.py module in the Django project takes care of hooking into the production servers.****
-------------------------------------------------------------------------
CREATE A DJANGO APP:

-->Read this and other tutorials from 'https://code.visualstudio.com/docs/python/tutorial-django#_create-a-django-app'



Uprading django: '  pip install --upgrade django  '(For latest version) or '  pip install --upgrade django==1.6.5  '(For specific version)

----------------------------------------------------------------------------------

Virtual environment:

1)When the virtual environment is active, PC creates an isolated environment for that particular environment. So when it is activated using 'source env<folder name>/bin/activate', We cannot access the packages of the PC and we should install all the packages-required again in that virtual environment(i.e. packages should be installed when virtualenv is activated.). 

2)Creating virtual env installs python,pip and some necessary tools in virtualenv but if we want any other third party libraries we should install them again in venv.

3) Try using which python,which pip, pip freeze, pip list,etc -- you will find that all these are working from your created(activated) virtual env folder.

4)If you do not activate virtualenv, then everything will be normal and PC uses all packages as usual.

5) If you exit the Terminal and create new terminal instance then virtualenv will be deactivated and everything works as normal.

6)Try using ' which django-admin ', If you find that django-admin is from outside of virtualenv, then install it again in virtualenv and try using ' which django-admin ' then it should probably show ' /<Activated virtualenv folder>/bin/django-admin '

7)Doing something in virtualenv means doing something when virtualenv is activated.

8)Just type ' deactivate ' on terminal to exit from virtual enivronment created and sourced.



****************************************************************
Use this to upgrade django: ' python -m pip install -U Django '
****************************************************************



