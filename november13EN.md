# Engineering Notebook November 13: Firebase Robo Test

One of the cool features we found on firebase is the robo testing feature. This feature uses a UI crawler to test your application's APK to ensure that basic usage of the UI does not cause a crash. Robo tests do not require any coding. In this post we provide a guide to two of the in depth features provided through this testing service.

The first feature we found is the test account credentials feature. This allows the tester to provide login credentials so that the crawler can move past the login UI. The tester must provide the unique identifier for the "username" and "password" fields and the login credentails. In addition to providing login credentials a tester can specify values for certain fields that the crawler will enter if it encounters the field.

![Test Credentials Image](/resources/robotest-credentials.png)

The second feature we used was Robo test scrips. This feature allows the tester to specify a certain series of actions that the crawler will perform when it enters the application. The scripts are easy to create using the Firebase plugin for Android Studio. The tester must open their applicaiton using the plugin and then move through the series of actions that should be included in the script. The firebase plugin records the series of actions and creates a script that can be uploaded for a test.
