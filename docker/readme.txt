** To experiment/play with docker without installation, go to 'https://labs.play-with-docker.com/'

** To uninstall the older versions use the command 'sudo apt-get remove docker docker-engine docker.io containerd runc'

- It’s OK if apt-get reports that none of these packages are installed.
- The contents of /var/lib/docker/, including images, containers, volumes, and networks, are preserved.
- If you do not need to save your existing data, and want to start with a clean installation,
    - Uninstall the Docker Engine, CLI, and Containerd packages: 'sudo apt-get purge docker-ce docker-ce-cli containerd.io'
    - Images, containers, volumes, or customized configuration files on your host are not automatically removed. To delete all images, containers, and volumes:
        'sudo rm -rf /var/lib/docker' and 'sudo rm -rf /var/lib/containerd'
    - You must delete any edited configuration files manually.


** Installing Docker using installation script
1) To download the installation script 'curl -fsSL https://get.docker.com -o get-docker.sh'
2) To run the script 'sudo sh ./get-docker.sh' (DRY_RUN=1 option to learn what steps the script will execute during installation)

** Visit docker hub to install the existing public repositories of many images at 'https://hub.docker.com/'

** Errors
1) If you get an error 'E: Sub-process /usr/bin/dpkg returned an error code (1)' during the installation use command 'sudo dpkg --configure -a'
This reconfigures the unpacked packages that were not installed during the installation process.


