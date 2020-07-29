1)Upgrading pip- '  /usr/bin/python3 -m pip install --upgrade pip  '

2)Upgrading python packages- ' pip install <package-name> --upgrade '

****************Installing packages************
1) pip install <module-name>

2) Installing from a text file:
    * create a text file requirements.txt as shown below-
        Kivy-Garden==0.1.4
        macholib==1.5.1
        idna==2.6
        geoip2nation==0.1.2
        docutils>=0.14
        Cython
    * Run this command - ' pip install -r requirements.txt '