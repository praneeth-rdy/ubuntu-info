1) Create an account on python anywhere.
2) Create a web app through web tab
3) Select manual configuration and python 3.8
4) Then open wsgi.py, copy paste the code from django-wsgi.txt
5) Now open the console and git pull the code.
6) Then cd into base directory and create virtualenv using 'mkvirtualenv <env-name> --python=/usr/bin/python3.8'
This virtualenv will be created at '/home/<username>/.virtualenvs/<env-name>/'
7) virtual env will be activated directly. If not, then use 'workon <env-name>' and 
then install the packages through 'pip install -r requirements.txt'
8) Now open web tab and add '/home/<username>/.virtualenvs/<env-name>' to virtual-env path
9) Add source code and working directory paths in the web tab.
10) Then add the urls in the static files section with pairs as
    a) (/static/, /home/<username>/<base-dir>/static/),
    b) (/media/, /home/<username>/<base-dir>/media/),
    c) (templates/, /home/<username>/<base-dir>/templates/)
