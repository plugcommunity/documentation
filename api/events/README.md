# API Events list


| Event Name            | Variable                                                  | Backend Name |
| ----------            | --------                                                  | ------------ |
| Chat Messages         | [API.CHAT](/api/events/chat.md)                           | "[chat](/api/events/chat.md)" |
| User Skip             | [API.USER_SKIP](/api/events/user_skip.md)                 | "[userSkip](/api/events/user_skip.md)" |
| User Joined           | [API.USER_JOIN](/api/events/user_join.md)                 | "[userJoin](/api/events/user_join.md)" |
| User Left             | [API.USER_LEAVE](/api/events/user_leave.md)               | "[userLeave](/api/events/user_leave.md)" |
| Vote Updates          | [API.VOTE_UPDATE](/api/events/vote_update.md)             | "[vote](/api/events/vote_update.md)" |
| Grab Updates          | [API.GRAB_UPDATE](/api/events/grab_update.md)             | "[grab](/api/events/grab_update.md)"  |
| Score Updates         | [API.ROOM_SCORE_UPDATE](/api/events/score_update.md)      | ~Frontend Only~ |
| DJ Advance            | [API.DJ_ADVANCE](/api/events/advance.md)                  | "[advance](/api/events/advance.md)" |
| Mod Skip              | [API.MOD_SKIP](/api/events/modSkip.md)                    | "[modSkip](/api/events/modSkip.md)" |
| Wait list Update      | [API.WAIT_LIST_UPDATE](/api/events/waitlist_update.md)    | "[djListUpdate](/api/events/waitlist_update.md)"  |
| Chat (/) Commands     | [API.CHAT_COMMAND](/api/events/commands.md)               | ~Frontend Only~ |
| History Update        | [API.HISTORY_UPDATE](/api/events/history_update.md)       | ~Frontend Only~ |

# Backend Socket Events List

| Event                     | Name |
|------                     | ---- |
| User Banned               | "[ban]                           (/api/events/ban.md)"                        |
| chatDelete                | "[chatDelete]                    (/api/events/chatDelete.md)"                 |
| djListCycle               | "[djListCycle]                   (/api/events/djListCycle.md)"                |
| djListLocked              | "[djListLocked]                  (/api/events/djListLocked.md)"               |
| Earned Plug Points        | "[earn]                          (/api/events/earn.md)"                       |
| friendRequest             | "[friendRequest]                 (/api/events/friendRequest.md)"              |
| friendAccept              | "[friendAccept]                  (/api/events/friendAccept.md)"               |
| gifted                    | "[gifted]                        (/api/events/gifted.md)"                     |
| killSession               | "[killSession]                   (/api/events/killSession.md)"                |
| Moderator Used Ban        | "[modBan]                        (/api/events/modBan.md)"                     |
| Moderator Added DJ        | "[modAddDJ]                      (/api/events/modAddDJ.md)"                   |
| Moderator Removed DJ      | "[modRemoveDJ]                   (/api/events/modRemoveDJ.md)"                |
| Moderator Moved DJ        | "[modMoveDJ ]                    (/api/events/modMoveDJ.md)"                  |
| Moderator Used Mute       | "[modMute]                       (/api/events/modMute.md)"                    |
| Moderator Rank Change     | "[modStaff]                      (/api/events/modStaff.md)"                   |
| playlistCycle             | "[playlistCycle]                 (/api/events/playlistCycle.md)"              |
| plugMaintenance           | "[plugMaintenance ]              (/api/events/plugMaintenance.md)"            |
| plugMaintenanceAlert      | "[plugMaintenanceAlert]          (/api/events/plugMaintenanceAlert.md)"       |
| roomNameUpdate            | "[roomNameUpdate]                (/api/events/roomNameUpdate.md)"             |
| roomDescriptionUpdate     | "[roomDescriptionUpdate]         (/api/events/roomDescriptionUpdate.md)"      |
| roomWelcomeUpdate         | "[roomWelcomeUpdate]             (/api/events/roomWelcomeUpdate.md)"          |
| roomMinChatLevelUpdate    | "[roomMinChatLevelUpdate]        (/api/events/roomMinChatLevelUpdate.md)"     |
| Skip                      | "[skip]                          (/api/events/skip.md)"                       |
| User Updates              | "[userUpdate]                    (/api/events/userUpdate.md)"                 |