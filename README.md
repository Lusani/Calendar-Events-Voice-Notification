# Calendar-Events-Voice-Notification
The idea is to create a program that will continuously poll my google calendar, and play an audio notification when a given calendar event’s start time is reached. Several steps are involved:

Retrieving calendar events: this requires authenticating and interfacing with Google Calendar API.


The authentication process require two things:

-A client Id for the OAuth2 authentication protocol, and the associated client secret code

-An API key 

First time authentication is achieved by executing the credentials.py script. The template for this script was obtained from the google developer website.

Generating an audio notification corresponding to the event: 

Microsoft’s Bing Text To Speech API is used for this. This decision was made after I failed to create a billing account for the google translate service due to card issues. Moreover, the free use of the google translate API is largely undocumented and google translate is mostly a paid service. 

Execute the TaskVoiceNotify.py script. 

I did not have enough time to work on the front-end. Please see the log file for results. The scripts runs in Daemon mode.


Sample output: 

