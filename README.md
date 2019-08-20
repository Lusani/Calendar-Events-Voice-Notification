# Calendar-Events-Voice-Notification
The idea is to create a program that will continuously poll my google calendar, and play an audio notification when a given calendar event’s start time is reached. Several steps are involved:

Retrieving calendar events: this requires authenticating and interfacing with Google Calendar API.


The authentication process require two things:

-A client Id for the OAuth2 authentication protocol, and the associated client secret code
-An API key 

First time authentication is achieved by executing the credentials.py script. The template for this script was obtained from the google developer website.


Generating an audio notification corresponding to the event: Microsoft’s Bing Text To Speech API is used for this. This decision was made after I failed to create a billing account for the google translate service due to card issues. Moreover, the free use of the google translate API is largely undocumented and google translate is mostly a paid service. 

Execute the TaskVoiceNotify.py script. 

I did not have enough time to work on the front-end. Please see the log file for results. The scripts runs in Daemon mode.


Sample output: 

 INFO     Event #15, Name: bake scones, Start: 2019-09-05T15:40, Reminder at 5 minutes
2019-08-20 16:04:03,142 INFO     Event #16, Name: bake scones, Start: 2019-09-06T15:40, Reminder at 5 minutes
2019-08-20 16:04:03,142 INFO     Event #17, Name: bake scones, Start: 2019-09-07T15:40, Reminder at 5 minutes
2019-08-20 16:04:03,142 INFO     Event #18, Name: bake scones, Start: 2019-09-08T15:40, Reminder at 5 minutes
2019-08-20 16:04:03,142 INFO     Event #19, Name: bake scones, Start: 2019-09-09T15:40, Reminder at 5 minutes
2019-08-20 16:04:03,142 INFO     Event #20, Name: bake scones, Start: 2019-09-10T15:40, Reminder at 5 minutes
2019-08-20 16:04:03,142 INFO     Event #21, Name: bake scones, Start: 2019-09-11T15:40, Reminder at 5 minutes
2019-08-20 16:04:03,142 INFO     Event #22, Name: bake scones, Start: 2019-09-12T15:40, Reminder at 5 minutes
2019-08-20 16:04:03,142 INFO     Event #23, Name: bake scones, Start: 2019-09-13T15:40, Reminder at 5 minutes
2019-08-20 16:04:03,142 INFO     Event #24, Name: bake scones, Start: 2019-09-14T15:40, Reminder at 5 minutes
2019-08-20 16:04:03,142 INFO     Event #25, Name: bake scones, Start: 2019-09-15T15:40, Reminder at 5 minutes
2019-08-20 16:04:03,142 INFO     Event #26, Name: bake scones, Start: 2019-09-16T15:40, Reminder at 5 minutes
2019-08-20 16:04:03,143 INFO     Event #27, Name: bake scones, Start: 2019-09-17T15:40, Reminder at 5 minutes
2019-08-20 16:04:03,143 INFO     Event #28, Name: bake scones, Start: 2019-09-18T15:40, Reminder at 5 minutes
2019-08-20 16:04:03,143 INFO     Event #29, Name: bake scones, Start: 2019-09-19T15:40, Reminder at 5 minutes
