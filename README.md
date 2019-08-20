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

    2019-08-20 16:27:36,991 INFO     Starting Google Calendar Polling and Notification Service

    2019-08-20 16:27:36,991 INFO     Using google developerkey AIzaSyCATEhSbhESLMialMmEA0xLmp_8xAh75AY
    
    2019-08-20 16:27:36,991 INFO     Using microsoft speech key c0b03292d4ac40f09e2b392f21a6ff44
    
    2019-08-20 16:27:36,991 INFO     Using calendar list: ['lravhuanzwo@gmail.com']
    
    2019-08-20 16:27:36,991 INFO     Beginning authentication...
    
    2019-08-20 16:27:36,993 INFO     Authentication completed

    2019-08-20 16:27:37,599 INFO     Starting calendars polling & notification loop...
    
    2019-08-20 16:27:37,599 INFO     Checking calendars...
    
    2019-08-20 16:27:37,976 INFO     Event #0, Name: configure openstack, Start: 2019-08-21T15:00, Reminder at 30 minutes
    
    2019-08-20 16:27:37,976 INFO     Event #1, Name: configure epc, Start: 2019-08-22T15:30, Reminder at 30 minutes
    
    2019-08-20 16:27:37,977 INFO     Event #2, Name: attend market analysis meeting, Start: 2019-08-23T15:30, Reminder at 30 minutes
    
    2019-08-20 16:27:37,977 INFO     Event #3, Name: bake cheesy scones, Start: 2019-08-24T15:30, Reminder at 30 minutes





