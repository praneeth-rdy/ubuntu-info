
Don't messup the server usernames, passwords and databases without knowing the consequence.

1)Master password for pgadmin: praneeth19

2)Password for the username 'postgres': praneeth19

3)Password for the username 'praneeth': praneeth19

4)'PostgreSQL 11' server in group Servers is created using username postgres.

5)Learn about tablespaces.

***commands on normal terminal***

1)Use the command('psql -d <db name> -U <owner/username of db>') to open the psql shell of that db; You can directly enter 'psql' if the current user is the owner and db has same name as that of user.

2)Use : 'sudo -i' to become root.

3)Use(on 'root@PC') : 'su - <username>' to switch users.


******commands on database shell******

(Don't forget the semicolon at the end of command here, if you don't put ; then the shell assumes that the command is conitinued.)
(ex: 'postgres=#', 'postgres-#')

1)To list role names,roles attributes,member use the command : '\du;'

2)To exit from the shell use the command: '\q;' or 'Cntrl+D'

2)Only superusers and users with the CREATEROLE privilege can remove Postgresql users. A user cannot be if any objects(example: a database) depend on it. 
command is: 'DROP ROLE <role name>;', 'DROP USER <username>;'

3)A user cannot remove a database, if the database is accessed by some other users or if clients are connected to it.
command is : 'DROP DATABASE <database name>;' or 

4)For alter role commands follow the screenshot.
command is : 'ALTER ROLE <username> WITH <options>;'

5)Giving password to db user using db shell
command is: "ALTER USER <username> PASSWORD '<password as string>';".

6)A database is created using the following commands:
commands: 'CREATE DATABASE <dbname>;'(This will create a DB with owner as current user)
to mention a different user: 'CREATE DATABASE <dbname> OWNER <rolename>;'






