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


** If you would like to use docker as a non-root user, you should now consider adding your user to the 'docker' group with something like 'sudo usermod -aG docker your-user'
Remember that you will have to log out and back in for this to take effect

** My first docker use while creating an OS kernel
1) Create a Dockerfile
2) Run 'docker build' to build the image
3) Run 'docker run' to create a docker container

** Docker Architecture
- Docker file creates Docker Image. Docker Image is a blueprint of the project.
- You can create your own docker images and publish them to docker hub or store in your local registry. Docker hub is also a registry.
- You can also pull the publicly available docker images into your local machine. These are readonly templates used to create containers.
- Docker container is an instance of Docker Image. This can be built from one or more docker images.
- Running docker image creates docker containers.
- Docker containers store the application along with all the dependencies (contains everything needed to run the application).
- You can create as many docker containers as you want using a docker image.

- Docker Engine will have client(docker-cli) and server (docker daemon or docker-d). In our case, both on same machine.
Docker cli interacts with server (docker daemon or docker-d) through a rest api. All the commands like pull, run, rm goes to the server.
- This manages container, images, network and data volumes

** Docker commands
1) To list the running containers: 'docker ps'
2) To list all the containers: 'docker ps -a'
3) To list the images 'docker image ls' or 'docker images'
4) To remove the docker image: 'docker rmi <image-id>'
5) To remove the docker container: 'docker rm <container-id>'
6) To pull the image: 'docker image pull <image-name>' or 'docker image pull <image-name>:latest'
7) To run the image: 'docker run <image-name>'
8) 'docker run -it <image>:tag <command-to-run> <arguments(optional)>'
(ex: docker run -it 4e5021d210f6 /bin/bash)(The -it instructs Docker to allocate a pseudo-TTY connected to the container's stdin; creating an interactive bash shell in the container.)
9) 


** Dockerfile
- Dockerfile consists of comments and commands + arguments
ex:
# Print "Hello World"
RUN echo "Hellp World"

- FROM command is the most important command amongst all and it defines the base image to use to start the build process
ex:
# Usage: FROM [imagename]
FROM ubuntu

- RUN command is the central executing directive for Dockerfiles. It takes commands as its arguments and runs it to form the image. Unlike CMD, it actually is used to build the image.
ex:
# Usage: RUN [command]
RUN apt-get install -y riak

- CMD command is similar to RUN. Unlike RUN it is not executed during build, but when a container is instantiated using the image being built
ex:
# Usage 1: CMD application "argument1" "argument2"
CMD "echo" "Welcome To Edureka"

- ADD command gets two arguments: a source and a destination. It basically copies the files from the source on the host into the container's own filesystem at the set destination
ex:
# Usage: ADD [source directory or URL] [destination directory]
ADD /my_app_folder /my_app_folder

- ENV command is used to set the environment variables (one or more).
These variables consist of "key value" pairs which can be accessed within the container by scripts and applications alike
ex:
# Usage: ENV key value
ENV SERVER_WORKS 4

- WORKDIR directive is used to set where the command defined with CMD is to be executed
ex:
# Usage: WORKDIR [path]
WORKDIR /path WORKDIR ~/

- EXPOSE command is used to associate a specified port to enable networking between the running process inside the container and the outside world i.e. the host
ex:
# Usage: EXPOSE [port]
EXPOSE 8080

- MAINTAINER command is used to set author field of an image
ex:
# Usage: MAINTAINER [name]
MAINTAINER authors_name

- USER directive is used to set the UID (or username) which is to run the container based on the image being built
ex:
# Usage: USER [UID]
USER 751

- VOLUME command is used to enable access from your container to a directory on the host machine (i.e. mounting it)
ex:
# Usage: VOLUME ["/dir_1", "/dir_2", ...]

VOLUME [/"my_files"]
