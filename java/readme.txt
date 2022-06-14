

JAVA_HOME is added to .bashrc and also to the PATH.
It's the Java version 14 and it is present in /usr/lib/jvm/jdk-14


**** Installation *****
1) Download the .deb package from oracle official website
2) Enter 'sudo apt install <path-to-deb>' or 'sudo dpkg -i <path-to-deb>'
3) This new jdk version will be installed inside /usr/lib/jvm/ by default
4) Enter the command 'sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/<path-to-newly-installed-jdk>/bin/java <priority-number>' to add this newly installed jdk to alternatives
5) Enter the command 'sudo update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/<path-to-newly-installed-jdk>/bin/javac <priority-number>' to add the javac of newly installed jdk to alternatives


To switch between installed versions:
1) Update alternatives using 'sudo update-alternatives --config java'
2) Add/modify JAVA_HOME environment variable







** The reference for the following is taken from: https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-on-ubuntu-20-04

1) You can have multiple Java installations on one system. You can configure which version is the default for use on the command line by using the update-alternatives command: 'sudo update-alternatives --config java'

You can do this for other Java commands, such as the compiler: 'sudo update-alternatives --config javac'



**** Adding env variable *******
Many programs written using Java use the JAVA_HOME environment variable to determine the Java installation location.
To set this environment variable, first determine where Java is installed. Use the update-alternatives command: 'sudo update-alternatives --config java'

- Then open `/etc/environment`
- At the end of this file, add the following line, making sure to replace the highlighted path with your own copied path, but do not include the bin/ portion of the path:
JAVA_HOME="/usr/lib/jvm/java-11-openjdk-amd64"

- Now reload this file to apply the changes to your current session: 'source /etc/environment'
- You can check it by running: 'echo $JAVA_HOME'
