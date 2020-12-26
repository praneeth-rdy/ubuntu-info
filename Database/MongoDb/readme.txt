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