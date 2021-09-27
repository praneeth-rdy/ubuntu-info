An SSH key consists of the following files:
- A public SSH key file that is applied to instance-level metadata or project-wide metadata.
- A private SSH key file that the user stores on their local devices.

If a user presents their private SSH key, they can use a third-party tool to connect to any instance that is configured with the matching public SSH key file, even if they aren't a member of your Google Cloud project.
Therefore, you can control which instances a user can access by changing the public SSH key metadata for one or more instances.



** To generate rsa key: 'ssh-keygen -t rsa -f ~/.ssh/[KEY_FILENAME] -C [USERNAME]'


** This command generates a private SSH key file and a matching public SSH key (at ~/.ssh/[KEY_FILENAME].pub) with the following structure: 
ssh-rsa [KEY_VALUE] [USERNAME]

** Restrict access to your private key so that only you can read it and nobody can write to it.
chmod 400 ~/.ssh/[KEY_FILENAME]

** Locating the keys
Public key file: ~/.ssh/[KEY_FILENAME].pub
Private key file: ~/.ssh/[KEY_FILENAME]


For more info: https://cloud.google.com/compute/docs/instances/adding-removing-ssh-keys



Connecting to server:
1) Add your public ssh key to the server
2) Access server through command line using ssh as: ssh [username]@[serverIP]
3) use 'sudo poweroff' to shutdown remote server.
4) Adding ssh key to remote server from terminal: 'ssh-copy-id -i ~/.ssh/[key-name] [username]@[server-ip]'


Creating ssh server:
1) Install openssh-server
2) General commands: 'sudo service ssh start', 'sudo service ssh restart', 'sudo service ssh stop'
3) 'sudo lsof -i -n -P | grep LISTEN' to check if your server is listening at port 22 (by default used by ssh)
4) Now locate sshd_config file and set Port option (at grep Port /etc/ssh/sshd_config)
5) 