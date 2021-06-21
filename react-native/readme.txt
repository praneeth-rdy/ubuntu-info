
** Installation and Setup
Reference: https://reactnative.dev/docs/environment-setup

1) Android Studio (+ Install Android SDK and configue ANDROID_HOME env variable)
2) Nodejs for execution environment
3) JDK
4) Watchman (optional) to watch for changes in the filesystem: sudo apt-get install watchman

** Creating project
Creates a new project-
1) npx react-native init AwesomeProject

** Running
Run the following command in your React Native project folder to start Metro bundler-
1) npx react-native start
Let metro bundler run in its own terminal.
Now, open a new terminal and run the following command to run your application in an avd-
2) npx react-native run-android


** Development
1) Multiple styles can be applied to a single component by passing a list of objects to the style attribute
