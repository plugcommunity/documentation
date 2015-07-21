### Introduction

The websocket introduces a 2 way communication with the service in real time.
This is especially needed for messaging and other events that should be executed with as little time difference as 
possible.



### Tips and tricks

One thing to mention is that you can only send a limited amount of request in a certain timespan, if you overdo it 
for a longer amount of time you'll be banned. This can certainly happen when you decide to to delete
a bunch of chat messages without artifically slowing the amount of requests down.

### List of endpoints

| Event Name                | Link                                                                                          |
|-----------------------    | -------------                                                                                 |
| Ack                       | "[ack]                           (/api/backend_events/ack.md)"                                |
| Ban                       | "[ban]                           (/api/backend_events/ban.md)"                                |
| Chat                      | "[chat]                          (/api/backend_events/chat.md)"                               |
| ChatDelete                | "[chatDelete]                    (/api/backend_events/chatDelete.md)"                         |
| DJ List Cycle             | "[djListCycle]                   (/api/backend_events/djListCycle.md)"                        |
| DJ List Locked            | "[djListLocked]                  (/api/backend_events/djListLocked.md)"                       |
| DJ List Update            | "[djListUpdate]                  (/api/backend_events/djListUpdate.md)"                       |
| Earn                      | "[earn]                          (/api/backend_events/earn.md)"                               |
| Flood API                 | "[floodAPI]                      (/api/backend_events/floodAPI.md)"                           |
| Flood Chat                | "[floodChat]                     (/api/backend_events/floodChat.md)"                          |
| Friend Accept             | "[friendAccept]                  (/api/backend_events/friendAccept.md)"                       |
| Friend Request            | "[friendRequest]                 (/api/backend_events/friendRequest.md)"                      |
| Grab                      | "[grab]                          (/api/backend_events/grab.md)"                               |
| Kill Session              | "[killSession]                   (/api/backend_events/killSession.md)"                        |
| Mod Add DJ                | "[modAddDJ]                      (/api/backend_events/modAddDJ.md)"                           |
| Mod Ban                   | "[modBan]                        (/api/backend_events/modBan.md)"                             |
| Mod Move DJ               | "[modMoveDJ]                     (/api/backend_events/modMoveDJ.md)"                          |
| Mod Mute                  | "[modMute]                       (/api/backend_events/modMute.md)"                            |
| Mod Remove DJ             | "[modRemoveDJ]                   (/api/backend_events/modRemoveDJ.md)"                        |
| Mod Skip                  | "[modSkip]                       (/api/backend_events/modSkip.md)"                            |
| Mod Staff                 | "[modStaff]                      (/api/backend_events/modStaff.md)"                           |
| Name Changed              | "[nameChanged]                   (/api/backend_events/nameChanged.md)"                        |
| Notify                    | "[notify]                        (/api/backend_events/notify.md)"                             |
| Playlist Cycle            | "[playlistCycle]                 (/api/backend_events/playlistCycle.md)"                      |
| Plug Maintenance          | "[plugMaintenance]               (/api/backend_events/plugMaintenance.md)"                    |
| Plug Maintenance Alert    | "[plugMaintenanceAlert]          (/api/backend_events/plugMaintenanceAlert.md)"               |
| Plug Message              | "[plugMessage]                   (/api/backend_events/plugMessage.md)"                        |
| Rate Limit                | "[rateLimit]                     (/api/backend_events/rateLimit.md)"                          |
| Room Description Update   | "[roomDescription]               (/api/backend_events/roomDescription.md)"                    |
| Room Min Chat Level Update| "[roomMinChatLevelUpdate]        (/api/backend_events/roomMinChatLevelUpdate.md)"             |
| Room Name Update          | "[roomNameUpdate]                (/api/backend_events/roomNameUpdate.md)"                     |
| Room Welcome Update       | "[roomWelcomeUpdate]             (/api/backend_events/roomWelcomeUpdate.md)"                  |
| Skip                      | "[skip]                          (/api/backend_events/skip.md)"                               |
| User Join                 | "[userJoin]                      (/api/backend_events/userJoin.md)"                           |
| User Leave                | "[userLeave]                     (/api/backend_events/userLeave.md)"                          |
| User Update               | "[userUpdate]                    (/api/backend_events/userUpdate.md)"                         |
| Vote                      | "[vote]                          (/api/backend_events/vote.md)"                               |

*Ordered by Event Name^