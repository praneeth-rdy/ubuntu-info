*****Git commands*****


1)Create a github repo(Empty or initialized) and copy the link by clicking on clone.

2)Create an empty folder on local machine and open it in Terminal.

*3)Then use ' git init ' to initialize it as a git repo.

*4)Add the repo's origin using ' git remote add origin "<Paste the copied link here>" '

*5) Then pull the files from the central repo using ' git pull origin master '.

6)Then start working on your project. After making some changes, to commit the changes, add the files to index and then commit them.

8)only Indexed files will be committed.(You can commit all the files using a single command)

9)The files once indexed will be directly commited, if you don't index any file before commiting.

10)Don't forget to give a message while commiting.

10)Push the files to central repo to see the changes on github. Type the username and password while you push.

*11)Adding all files to index: ' git add -A ' or ' git add --all '.

*12)Commiting files:
 1) ' git commit -m "<Your commit message>" ' (only commits your prsesent indexed files)
 2) ' git commit -a -m "<message>" ' (commits all files which once indexed)

*13)Push the commits: ' git push origin master '

ORDER: 
1)Create empty folder>git init>add origin>pull the files from origin(sync)

2)After making changes: Adding to index(once per newfile)>Commit changes>Push to central repo

***Cache your credentials***:
(if git prompts you to enter your GitHub credentials every time you pull or push a repository, try caching the credentials.)

command: ' git config --global credential.helper cache '

