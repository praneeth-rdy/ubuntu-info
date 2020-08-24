

1) You can create a file "studio.desktop" in /usr/share/applications with the following contents:

***************************************


[Desktop Entry]
Name=Android Studio
Comment=Android Studio
Exec=/home/username/.../android-studio/bin/studio.sh
Icon=/home/username/.../android-studio/bin/studio.png
Terminal=false
Type=Application
Categories=Development


***************************************
(don't include *s)


or you can directly run studio.sh from /home/PC/android-studio/bin



2) Event log says:  
                Android Studio is using the following JDK location when running Gradle:
                /home/praneeth/PC/android-studio/jre
                Using different JDK locations on different processes might cause Gradle to
                spawn multiple daemons, for example, by executing Gradle tasks from a terminal
                while using Android Studio.

3) Android sdk location: ' /home/praneeth/Android/Sdk '

4) Android ndk location: ' /home/praneeth/Android/Sdk/ndk-bundle ' (installed on july 15 2020)

