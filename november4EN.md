# November 1-6 Engineering Notebook

We began testing out application using lint and crashlytics. Lint gave us a series of erros that we will detail in a later post in a summary of our testing. One of the interesting issues we ran into was with how to store the crashlytics api key, because we are using a public github repository and wanted to keep that information secure. We handled this problem by creaing an android string resource file and putting the file in out gitignore file. This way we can use the following code in the AndroidManifest.xml file to pull the api key in from the string resource file:

```xml
      <meta-data
            android:name="io.fabric.ApiKey"
            android:value="@string/crashlyticskey"
            tools:replace="android:value"/>
```

Using this approach we keep our api key off github but needed to define instructions for other people cloning our github repository. To handle this issue we give instructions in the projects readme for configuring crashlytics with a cloned version of the repository. Note that this approach only works for collaborating when users are using Android Studio with the Fabric plugin installed. The apporach also only work when using an emulator. In order to build an APK file, the API key must be displayed in the Android Manifest.
