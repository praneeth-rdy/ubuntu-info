**************Configuring git lfs****************
Git Large File Storage (LFS) replaces large files such as audio samples, videos, datasets, and graphics with text pointers inside Git,
while storing the file contents on a remote server like GitHub.com or GitHub Enterprise
Install:
1) ' curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | sudo bash '
2) ' sudo apt-get install git-lfs '
Configure large files on lfs:
1) ' git lfs install '
2) ' git lfs track "*.pdf" ' or use any other file extension
3) ' git add .gitattributes '
4) 
' git add file.psd '
' git commit -m "Add design file"'
' git push origin master '
*************************************************
...........Using ssh keys............
Read this to setup an ssh key in local:
https://medium.com/make-school/a-noob-s-guide-f20b3db28011

1) Generate ssh key in the local machine if doesn't exist (this key will generally be in ~/ssh/*.pub file)
use 'ssh-keygen -t rsa -b 4096 -C "your_github_email@example.com"' to generate the public key.
Press enter to use the default location and enter again if you don't want to set the passphrase.
2) Copy the key from the .pub file and add it to the github account/repo of which you want to provide access to.
3) Then whenever the repo or account is accessed with that ssh key, github recognises it and provides the access.


*************************************Creating a local repo********************************


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
*********************************************************************************************

************************Commands************************

1) Create a new branch and checkout to it in a single command: ' git checkout -b <newbranchname> '

**
To resolve any bug or add a new feature, it is recommended to work on a new branch.
Because the master branch is the representation of what's on production and 
we shouldn't mess it up until we complete the project on the new branch.
We should be careful while we commit something to the master branch.
**

2) To create a new branch - ' git branch <newbranchname> '

3) To delete a branch - ' git branch -d <newbranchname> '
If the branch is not fully merged, then it's going to give you a warning then replace '-d' in command with '-D'.

**
1) You cannot delete a branch while you are working on it.
2) When you switch to another branch, any work(or modified but not committed work/files) 
that we might have in the staging area, or the working directory will come over with us to the switched to branch.
3) We can't switch to a new branch, if any of the files in the working directory or the staging would be overwritten.
4) You may see files disappear or reappear when switching between branches. All these files will stay on their respective branches until you merge them.
**

4) 

********************************************************


****************Cache your credentials**********************

(if git prompts you to enter your GitHub credentials every time you pull or push a repository, try caching the credentials.)

command: ' git config --global credential.helper cache '

************************************************************


***************Working on branches**************************

1) No branch(not even master) will be created immediately after using ' git init '.

2) You need to add and commit something to create a master branch.

3) Then try creating a new branch(say b1).

4) Now creating a new file doesn't add it to any of the branches until you add them to index and commit to the newly created branch.
i.e. Just created file will be untracked until you add and commit it. The commited file belongs to that git branch on which you are working when you (added and commited) that file.

5) The files belonging to a particular branch will be visible (in the dir/repo either using UI or terminal) only when you switch to (or present on) that particular branch using git.

************************************************************
* Use 'git reset --soft HEAD~1' to undo the recent commit.


** Renaming master branch to main branch 'git branch -m master main'

** Changing date of the last commit 'GIT_COMMITTER_DATE="Sat Jun 12 21:05:23 2021 +0530" git commit --amend --no-edit --date="Sat Jun 12 21:05:23 2021 +0530"'
