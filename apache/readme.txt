gyws: apache configuration can be found in /etc/apache2/

1) sudo service apache2 restart, to restart the apache server
2) pm2 restart <app-name>, to restart the app
3) pm2 start filename.js, to start the node app
4) pm2 delete <app-name>, to stop and delete the app from memory
5) pm2 ps to list the running servers
6) pm2 logs <app-name> to see the app logs


1) normal npm run start or npm run dev will only run the application until the terminal closes
2) But the server to run even after closing the terminal, we use pm2


Refer to: https://www.youtube.com/watch?v=rvwYzs6IMog
******** Installing apache server on ubuntu: *********
1) 'sudo apt update && sudo apt -y install apache2'
2) To check whether the apache server: sudo systemctl status apache2
3) Create directories where the website files will be stored ex: 'sudo mkdir -p /var/www/music'
4) change the permissions 'sudo chmod -R 755 /var/www' and to check the permissions sudo chmod -R 755 /var/www

* Configure Apache:
5) Go to /etc/apache2/sites-available and copy the 000-default.conf to a new .conf file in the same dir.
6) This is the virtual host file. Edit this according to your needs including the port number.
7) Now enable your site using 'sudo a2ensite <sitename-basedon-conf-file>'
8) Now activate the configuration by reloading the server using: 'service apache2 reload' or 'systemctl reload apache2' (Now you can find the config file in sites enabled too)
9) To disable the default configuration: 'sudo a2dissite <sitename-basedon-conf-file>'

* Allowing ports
10) You need to add 'Listen [portnumber]' to ports.config
11) Check the status by 'sudo ufw status'
12) Enable if inactive: 'sudo ufw enable'
13) To allow ssh: 'sudo ufw allow ssh'
14) 'sudo ufw allow 8080' to allow the port and 'sudo ufw deny 8080' to deny the port


My public IP of omen: 192.168.29.124

***** Commands ****
Service and Systemctl
1) run 'sudo service apache2 restart' or 'systemctl start apache2.service' to start the apache server
2) 'sudo service apache2 restart' or 'systemctl restart apache2.service' to restart the apache server
3) 'sudo service apache2 stop' or 'systemctl stop apache2.service' to stop the apache server
4) To view status 'sudo systemctl status apache2.service' or 'sudo systemctl status apache2'


********* Difference between service and systemctl commands ***********
Service operates on the files in /etc/init.d and was used in conjunction with the old init system. 
Systemctl operates on the files in /lib/systemd. 
If there is a file for your service in /lib/systemd it will use that first and if not it will fall back to the file in /etc/init.d. 
Also If you are using OS like ubuntu-14.04 only service command will be available.

So if systemctl is available, it will be better to use it.
**************************