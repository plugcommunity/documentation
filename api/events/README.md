# API Events list


| Event Name            | Variable^                                                 | Backend Name |
| ----------            | ---------                                                 | ------------ |
| DJ Advance            | [API.ADVANCE](/api/events/advance.md)                     | "[advance](/api/events/advance.md)" |
| Chat Messages         | [API.CHAT](/api/events/chat.md)                           | "[chat](/api/events/chat.md)" |
| Chat (/) Commands     | [API.CHAT_COMMAND](/api/events/chat_commands.md)          | ~Frontend Only~ |
| Friend Join           | [API.FRIEND_JOIN](/api/events/friend_join.md)             | ~Frontend Only~ |
| Grab Updates          | [API.GRAB_UPDATE](/api/events/grab_update.md)             | "[grab](/api/events/grab_update.md)"  |
| History Update        | [API.HISTORY_UPDATE](/api/events/history_update.md)       | ~Frontend Only~ |
| Mod Skip              | [API.MOD_SKIP](/api/events/modSkip.md)                    | "[modSkip](/api/events/modSkip.md)" |
| Score Updates         | [API.SCORE_UPDATE](/api/events/score_update.md)           | ~Frontend Only~ |
| User Joined           | [API.USER_JOIN](/api/events/user_join.md)                 | "[userJoin](/api/events/user_join.md)" |
| User Left             | [API.USER_LEAVE](/api/events/user_leave.md)               | "[userLeave](/api/events/user_leave.md)" |
| User Skip             | [API.USER_SKIP](/api/events/user_skip.md)                 | "[skip](/api/events/backend_events/skip.md)" |
| Vote Updates          | [API.VOTE_UPDATE](/api/events/vote_update.md)             | "[vote](/api/events/vote_update.md)" |
| Wait List Update      | [API.WAIT_LIST_UPDATE](/api/events/wait_list_update.md)   | "[djListUpdate](/api/events/wait_list_update.md)"  |

*Ordered by Variable^

# Backend Socket Events List

| Event Description/Name    | Backend Name^                                                                            |
|-----------------------    | -------------                                                                            |
| User Banned               | "[ban]                           (/api/events/backend_events/ban.md)"                    |
| chatDelete                | "[chatDelete]                    (/api/events/backend_events/chatDelete.md)"             |
| djListCycle               | "[djListCycle]                   (/api/events/backend_events/djListCycle.md)"            |
| djListLocked              | "[djListLocked]                  (/api/events/backend_events/djListLocked.md)"           |
| Earned Plug Points        | "[earn]                          (/api/events/backend_events/earn.md)"                   |
| friendAccept              | "[friendAccept]                  (/api/events/backend_events/friendAccept.md)"           |
| friendRequest             | "[friendRequest]                 (/api/events/backend_events/friendRequest.md)"          |
| gifted                    | "[gifted]                        (/api/events/backend_events/gifted.md)"                 |
| killSession               | "[killSession]                   (/api/events/backend_events/killSession.md)"            |
| Moderator Used Ban        | "[modBan]                        (/api/events/backend_events/modBan.md)"                 |
| Moderator Added DJ        | "[modAddDJ]                      (/api/events/backend_events/modAddDJ.md)"               |
| Moderator Removed DJ      | "[modRemoveDJ]                   (/api/events/backend_events/modRemoveDJ.md)"            |
| Moderator Moved DJ        | "[modMoveDJ ]                    (/api/events/backend_events/modMoveDJ.md)"              |
| Moderator Used Mute       | "[modMute]                       (/api/events/backend_events/modMute.md)"                |
| Moderator Rank Change     | "[modStaff]                      (/api/events/backend_events/modStaff.md)"               |
| playlistCycle             | "[playlistCycle]                 (/api/events/backend_events/playlistCycle.md)"          |
| plugMaintenance           | "[plugMaintenance ]              (/api/events/backend_events/plugMaintenance.md)"        |
| plugMaintenanceAlert      | "[plugMaintenanceAlert]          (/api/events/backend_events/plugMaintenanceAlert.md)"   |
| roomNameUpdate            | "[roomNameUpdate]                (/api/events/backend_events/roomNameUpdate.md)"         |
| roomDescriptionUpdate     | "[roomDescriptionUpdate]         (/api/events/backend_events/roomDescriptionUpdate.md)"  |
| roomWelcomeUpdate         | "[roomWelcomeUpdate]             (/api/events/backend_events/roomWelcomeUpdate.md)"      |
| roomMinChatLevelUpdate    | "[roomMinChatLevelUpdate]        (/api/events/backend_events/roomMinChatLevelUpdate.md)" |
| User Updates              | "[userUpdate]                    (/api/events/backend_events/userUpdate.md)"             |

*Ordered by Backend Name^