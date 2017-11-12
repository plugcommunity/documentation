### Introduction

The websocket introduces a 2 way communication with the service in real time.
This is especially needed for messaging and other events that should be executed with as little time difference as
possible.

### List of emitted events

| Event Name                | Link                                                                             |
|---------------------------|----------------------------------------------------------------------------------|
| Ack                       | "[ack](/api/events/backend_events/ack.md)"                                       |
| Advance                   | "[advance](/api/events/advance.md#backend)"                                      |
| Ban                       | "[ban](/api/events/backend_events/ban.md)"                                       |
| Chat                      | "[chat](/api/events/chat.md#backend)"                                            |
| ChatDelete                | "[chatDelete](/api/events/backend_events/chatDelete.md)"                         |
| DJ List Cycle             | "[djListCycle](/api/events/backend_events/djListCycle.md)"                       |
| DJ List Locked            | "[djListLocked](/api/events/backend_events/djListLocked.md)"                     |
| DJ List Update            | "[djListUpdate](/api/events/wait_list_update.md#backend)"                        |
| Earn                      | "[earn](/api/events/backend_events/earn.md)"                                     |
| Flood API                 | "[floodAPI](/api/events/backend_events/floodAPI.md)"                             |
| Flood Chat                | "[floodChat](/api/events/backend_events/floodChat.md)"                           |
| Friend Accept             | "[friendAccept](/api/events/backend_events/friendAccept.md)"                     |
| Friend Request            | "[friendRequest](/api/events/backend_events/friendRequest.md)"                   |
| Gifted                    | "[gifted](/api/events/backend_events/gifted.md)"                                 |
| Grab                      | "[grab](/api/events/grab_update.md#backend)"                                     |
| Kill Session              | "[killSession](/api/events/backend_events/killSession.md)"                       |
| Level Up                  | "[levelUp](/api/events/backend_events/levelUp.md)"                               |
| Mod Add DJ                | "[modAddDJ](/api/events/backend_events/modAddDJ.md)"                             |
| Mod Ban                   | "[modBan](/api/events/backend_events/modBan.md)"                                 |
| Mod WaitlistBan           | "[modwaitlistBan](/api/events/backend_events/modWaitlistBan.md)"                 |
| Mod Move DJ               | "[modMoveDJ](/api/events/backend_events/modMoveDJ.md)"                           |
| Mod Mute                  | "[modMute](/api/events/backend_events/modMute.md)"                               |
| Mod Remove DJ             | "[modRemoveDJ](/api/events/backend_events/modRemoveDJ.md)"                       |
| Mod Skip                  | "[modSkip](/api/events/mod_skip.md#backend)"                                     |
| Mod Staff                 | "[modStaff](/api/events/backend_events/modStaff.md)"                             |
| Name Changed              | "[nameChanged](/api/events/backend_events/nameChanged.md)"                       |
| Name Changed Room         | "[nameChangedRoom](/api/events/backend_events/nameChangedRoom.md)"               |
| Notify                    | "[notify](/api/events/backend_events/notify.md)"                                 |
| Playlist Cycle            | "[playlistCycle](/api/events/backend_events/playlistCycle.md)"                   |
| Plug Maintenance          | "[plugMaintenance](/api/events/backend_events/plugMaintenance.md)"               |
| Plug Maintenance Alert    | "[plugMaintenanceAlert](/api/events/backend_events/plugMaintenanceAlert.md)"     |
| Plug Message              | "[plugMessage](/api/events/backend_events/plugMessage.md)"                       |
| Rate Limit                | "[rateLimit](/api/events/backend_events/rateLimit.md)"                           |
| Room Description Update   | "[roomDescription](/api/events/backend_events/roomDescription.md)"               |
| Room Min Chat Level Update| "[roomMinChatLevelUpdate](/api/events/backend_events/roomMinChatLevelUpdate.md)" |
| Room Name Update          | "[roomNameUpdate](/api/events/backend_events/roomNameUpdate.md)"                 |
| Room Welcome Update       | "[roomWelcomeUpdate](/api/events/backend_events/roomWelcomeUpdate.md)"           |
| Skip                      | "[skip](/api/events/user_skip.md#backend)"                                       |
| User Join                 | "[userJoin](/api/events/user_join.md#backend)"                                   |
| User Leave                | "[userLeave](/api/events/user_leave.md#backend)"                                 |
| User Update               | "[userUpdate](/api/events/backend_events/userUpdate.md)"                         |
| Vote                      | "[vote](/api/events/vote_update.md#backend)"                                     |

*Ordered by Event Name^
