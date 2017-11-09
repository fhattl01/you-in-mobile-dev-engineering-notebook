# Testing and Basic Security Audit
We tested You In? using  4 methods:
        - Lint
        - Usability testing with 5 users
        - Crashlytic
        - Firebase Robo tests.

## Lint
Lint initially provided us with 2 errors and 126 warnings regarding the app. While Lint provided helpful feedback on syntax and warnings regarding android formatting rules, the only 2 errors the first time we used Lint were 2 instances of OnClick errors where the method did not exist for two buttons. The functionality of our application was not affected in anyway due to these errors because the timePickerDialog and datePickerDialog did not exist in the most recent version of You In?. Despite this, it was good to go through and fix those errors in order to have an application with no errors. After fixing warnings and errors, the second time we ran Lint there were 0 errors and 44 warnings, which was significantly less than our original test. A majority of our warnings came from obsolete gradle dependencies with Firebase, unused resources such as colors, and hardcoded text instead of text being stored in the strings.xml file. Links to an html summary of each test are provided below:

[Initial Lint Test](http://htmlpreview.github.com/?https://github.com/fhattl01/you-in-mobile-dev-engineering-notebook/blob/master/resources/initial-lint-results.html)
[Final Lint Test](http://htmlpreview.github.com/?https://github.com/fhattl01/you-in-mobile-dev-engineering-notebook/blob/master/resources/final-lint-results.html)

## Usability Testing
We also tested You In with a small set of 5 users. They gave us concrete feedback on the color scheme and user experience. Every user noted that a back button was needed on every page in order to navigate back to the home screen. Users also commented on the importance of having the buttons on the top outlined in a different color to make it clear those were menu options. We had our users test the functionality of every aspect of the application, creating an account, adding friends, viewing their own profile, creating an event and inviting their friends, and then viewing the event in the home screen. The users enjoyed the flow and simplicity of the application, and none of the users required guidance for how to navigate through the application, which was a positive sign that the app is easy and enjoyable to use.  One key element that we did add based on usability testing was a back button on the view profile page, and on the search for friends page. This was an easy addition to the UI. Other user feedback we got included: the need to order events so that events at the top are events closest to the present, provide an edit profile feature, provide an edit existing event feature, make it easier to search for new users, and make event cards look better. We hope to implement some of these changes in a future iteration of the application. The UI is still a work and progress and has lots of room to be refined.

## Crashlytics
We installed crashlytics on our app so that we can monitor crashes using the fabric service. This will be incredibly useful in the future when our app is running on Android devices because we will be able to see the exceptions that are causing the application to crash on users devices. We did encounter issues here with where to put the Crashlytics key and ultimately decided to store it in the Github Repo, because the work arounds that we tried cause the app to fail when building.

## Firebase Robo Tests
Our final method of testing You In? was using Firebase's robo testing suite. This suite does a dynamic analysis of your application using a UI crawler to move the through each of the views in the app. The tests ensure that basic usage of the app will not cause a crash, and even tries certain corner cases such as entering empty text boxes etc. The implementation of this test was somewhat challenging because we had to provied a way for the UI crawler to move past the login page. We ultimately decided to give the crawler an APK that logged in using a fixed set of credentials automatically. This allowed us to test the main components of the UI other than the login flow. Another great feature of Robo Tests is that the application can be tested on multiple devices. We ran tests on 5 devices, all of which passed, which gives us further confidence that our app is functional. Results from one of these tests are provided below.

### Robo Test on Google Pixel Phone with API 26:
[Video of the Robo Test](https://youtu.be/TK-MfSBH-40)
[Activity Map](resources/activity-map.png)


