#Testing and Basic Security of You In? 

We tested You In? using Lint, Usability testing with a small set of 5 users, 
Crashlytics and Firebase Robo tests. 

Lint initially provided us with 2 errors and 126 warnings regarding the app.
While Lint provided helpful feedback on syntax and warnings regarding 
android formatting rules, the only 2 errors the first time we used Lint were 
2 instances of OnClick errors where the method did not exist for two buttons.
The functionality of our application was not affected in anyway due to these
errors because the timePickerDialog and datePickerDialog did not exist in the
most recent version of You In?. Despite this, it was good to go through
and fix those errors in order to have an application with no errors. 
After fixing warnings and errors, the second time we ran Lint there was 
1 error and 43 warnings, which was significantly less than our original 
test. A majority of our errors came from obsolete gradle dependencies 
with Firebase, unused resources such as colors, and hardcoded test instead
of text being stored in the strings.xml file. 

We also tested You In with a small set of 5 users. They gave us concrete 
feedback on the color scheme and user experience. Every user noted that a 
back button was needed on every page in order to navigate back to the 
home screen. Users also commented on the importance of having the buttons on
the top outlined in a different color to make it clear those were menu 
options. We had our users test the functionality of every aspect of the 
application, creating an account, adding friends, viewing their own profile, 
creating an event and inviting their friends, and then viewing the event in
the home screen. The users enjoyed the flow and simplicity of the application, and none of the users required guidance for how to navigate
through the application, which was a positive sign that the app is easy 
and enjoyable to use. 

Neither Lint nor Usability tests found major problems in our app except
for the need to add a back button to the pages. 