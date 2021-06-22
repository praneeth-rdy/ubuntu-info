
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
2) To move App.js to any other place, modify the path to App.js in both index.js and __tests__/App-test.js
3) Add the line 'prettier/prettier: false,' to module.exports of .eslintrc.js
4) Adding custom fonts (for react-native version > 0.60):
- Create a file named react-native.config.js in the root folder of your project.
- Add the following in that new file
module.exports = {
project: {
    ios: {},
    android: {},
},
assets: ['./assets/fonts']
};

- run 'react-native link' command in the root project path. (Make sure you have right path for the fonts folder)
- Now, you can use them directly in your code styles
ex: fontFamily: 'your-font-name without extension'
if your font is Raleway-Bold.ttf then,
fontFamily: 'Raleway-Bold'
5) To use react native icons
- Install react-native-vector-icons
- Then link them with the project using react-native link
6) Refer to official reactnavigation.org documentation to implement navigation in your react project
- @react-navigation/native
- react-native-reanimated react-native-gesture-handler react-native-screens react-native-safe-area-context @react-native-community/masked-view
