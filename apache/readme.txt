1) sudo service apache2 restart, to restart the apache server
2) pm2 restart <app-name>, to restart the app
3) pm2 start filename.js, to start the node app
4) pm2 delete <app-name>, to stop and delete the app from memory
5) pm2 ps to list the running servers
6) pm2 logs <app-name> to see the app logs


1) normal npm run start or npm run dev will only run the application until the terminal closes
2) But the server to run even after closing the terminal, we use pm2
