Special files of GitHub repos: CONTRIBUTING.md, LICENSE.md, README.md, CODE_OF_CONDUCT.md, CHANGELOG.md, SUPPORT.md, CONTRIBUTERS.md, AUTHORS.md, ACKNOWLEDGEMENTS.md, ISSUE_TEMPLATE.md, PULL_REQUEST_TEMPLATE.md, CODEOWNERS.md, etc.
Configuring a remote for fork: https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/configuring-a-remote-for-a-fork


To update your fork on local repo(Assuming that you have cloned your forked repo):
1) Add remote upstream of original repo which you have forked:
'git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git'

2) fetch from upstream: 'git fetch upstream'
3) Checkout to the master branch 'git checkout master'
4) merge the fetched data with current local repo master: 'git merge upstream/master'
** or you can use 'git pull upstream master' instead of fetch and merge
5) To update the central forked repo: 'git push'

** To list current configured remote repositories: 'git remote -v'

-----------Contributing to OpenSource using GitHub-----------

1) Fork the repo that you want to contribute to.

2) Clone the forked repo which is on your GitHub account and create a Local repo to work with.

3) Create a new branch with any name and remeber that you need to work on this branch.

4) Switch to the newly created branch.

5) Make changes that you want and remember to follow the contribution guidelines while making changes.

6) Update your local repo using git pull.

7) Set up your 'newly created branch' to track remote branch 'master' from 'origin'.

8) Add the files to index.

9) Commit the changes_made/files_added.

10) Push the commits to the github origin.

11) Now open the github repo using browser and click on 'compare and create a pull request'.

12) Finally, proceed to create a pull request.

*Use the base branch dropdown menu to select the branch you'd like to merge your changes into,
then use the compare branch drop-down menu to choose the topic branch you made your changes in.*



Example:(The following is a simple example of commands on terminal using git):

* Consider the name of the new working branch as 'my_Contribution' *

2) ' git clone https://github.com/Praneeth-rdy/Best-websites-a-programmer-should-visit.git '

3) ' git branch my_Contribution '

4) ' git checkout my_Contribution '

6) ' git pull  (Run this both on master and my_Contribution) '

7) ' git branch --set-upstream-to=origin/master my_Contribution '   (Run this on my_Contribution i.e. after you checkout to my_Contribution)

8) ' git add . '

9) ' git commit -m "Added a new website in computer books section. This website is a good source to download ebooks." '

10) ' git push origin my_Contribution '

11) Create a pull request on GitHub.