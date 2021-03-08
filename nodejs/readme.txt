nvm: nodejs version manager
npm: nodejs package manager
nodejs: JavaScript RUNTIME ENVIRONMENT(NOT FRAMEWORK, NOT LIBRARY) which uses V8 Javascript engine


***************Installing nvm*********

1) Download nvm installation script using curl and note that version number given in the command may differ
$ curl -sL https://raw.githubusercontent.com/creationix/nvm/v0.35.3/install.sh -o install_nvm.sh

2) (Optional) To inspect Installation Script: $ nano install_nvm.sh

3) Run the Installation Script: $ bash install_nvm.sh

Now reopen the Terminal and use $ nvm ls-remote to list all the available versions.


*********** Installing nodejs ****************

1) You can directly install nodejs using nvm.
$ nvm install 12.18.3

2) You can tell nvm to use the version you just downloaded by typing:
$ nvm use 12.18.3

*********** Uninstalling nodejs ****************

1) use: "sudo apt purge nodejs" or "sudo apt remove nodejs" to uninstall nodejs. First command to remove it completely

2) And then: "sudo apt autoremove"

3) Or use: "nvm uninstall node_version"

*****************Additional info***************
1) Now, to check the node version: either type "node -v" or "nodejs --version"

2) To list the installed nodejs versions: "nvm ls"

3) To default one of the versions: "nvm alias default 12.18.3"



****************npm*************************
1) to install packages using npm: "npm install <package-name>" or "npm install -g <package-name>" to install globally
2) to install any package only for the development purposes: "npm install <package-name> --save-dev"

** To use an existing js project use: 'npm install' to install dependencies from package.json and then 'npm run dev'
In case of next applications add this to scripts of package.json
"dev": "next dev",
"build": "next build",
"start": "next start"

** use 'npx <package-name> <cmd-arguments>' to run node packages without installing them
ex: 'npx next dev', 'npx create-react-app myapp'

***********Local*******************
node version: 14.15.1
nodejs version: 10.19.0