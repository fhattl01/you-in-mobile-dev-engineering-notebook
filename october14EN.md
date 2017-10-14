#October 8th - 14th Engineering Notebook 

Added Profile and Event List Activities and connected them to the backend. 
The UI needs a fair amount of work, but a majority of the backend is linked. 
Set up Google Firebase Auth for users to log in. 

The largest challenge in setting up Auth was getting the gradle dependencies 
to link correctly. This took a fair amount of manipulation. 

Our next step is to set up the app so everytime we get an event, we go into 
the event database and add that event to the event list activity. We also need
to figure out how to get a unique event id for every event. 
