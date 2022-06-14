Go to official website of mongodb and select softwares from the navbar

Download .deb packages of MongoDB Community Edition and MongoDB Compass Tool
cd Downloads
Then Install them using ' sudo apt install ./<deb-name>.deb '

OR
1) sudo apt install mongodb
2) sudo service mongodb start // This will work
3) mongo // To open the shell
4) // Now install the mongodb compass to use UI tool


On mongodb shell:
1) Use 'show dbs' to list info
2) enter 'use <db-name>' to use an existing database or to create a new one
3) enter 'db;' to get the name of the current database
4) Mongodb is no sql db. It is based on collections. To insert values
'db.<collection-name>.insert({name: value})'
5) 'show collections;' to get the list of collections
system.indexes is by default
6) db.<collection-name>.find();
You will get the data from that collection.



Imagine collections as tables and documents as rows in the tables.


**** Other Commands To Manage MongoDB ****
1) Start MongoDB: 'sudo systemctl start mongod'
run 'sudo systemctl daemon-reload' first, if you get Unit mongod.service not found.

2) Verifying the mongoDB status: sudo systemctl status mongod

* You can optionally ensure that MongoDB will start following a system reboot by issuing the following command: 'sudo systemctl enable mongod'

3) To stop MongoDB: 'sudo systemctl stop mongod'

4) To restart mongoDB: 'sudo systemctl restart mongod'

5) To use mongoDB: 'mongosh'


Uninstalling:

1) sudo service mongod stop
2) sudo apt-get purge mongodb-org*
3) sudo rm -r /var/log/mongodb
4) sudo rm -r /var/lib/mongodb


By default, mongodb can only be accessed via localhost.
If you want to make it remotely accessible, you should bind the IP using '--bind_ip'.
* Read more here: https://docs.mongodb.com/manual/reference/program/mongod/#std-option-mongod.--bind_ip


To populate data into the db from a dump folder (Command to run on system shell):
mongorestore -d db_name dump_folder_path
