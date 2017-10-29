### Introduction

The plug API is separated into two systems, [WebSocket](https://github.com/plugcommunity/documentation/tree/master/api/events) and [REST](#).

While the WebSocket part is used to communicate at real time (such as chat, booth advancement etc.), the REST API is used to do everything that does not require a real-time connection. While this certainly induces a bit of latency for each action, it is something that can be easily handled with.


### Tips and tricks

The API endpoints are rate limited. If you send too many requests in a given period of time, you will be temporarily
[IP banned](/api/bans.md). This can happen when you spam the booth join, or any other endpoint.

Some methods however, are white listed such as chat deleting, this is in order to prevent spam and other attacks.

### List of endpoints

| Endpoint Name             | Link                                                                        |
|---------------------------|-----------------------------------------------------------------------------|
| Auth Facebook             | "[auth/facebook](/api/endpoints/auth_facebook.md)"                          |
| Auth Login                | "[auth/login](/api/endpoints/auth_login.md)"                                |
| Auth Reset                | "[auth/reset/me](/api/endpoints/auth_reset_me.md)"                          |
| Auth Session              | "[auth/session](/api/endpoints/auth_session.md)"                            |
| Auth Token                | "[auth/token](/api/endpoints/auth_token.md)"                                |
| Bans                      | "[bans](/api/endpoints/bans.md)"                                            |
| Bans Add                  | "[bans/add](/api/endpoints/bans_add.md)"                                    |
| Booth                     | "[booth](/api/endpoints/booth.md)"                                          |
| Booth Add                 | "[booth/add](/api/endpoints/booth_add.md)"                                  |
| Booth Cycle               | "[booth/cycle](/api/endpoints/booth_cycle.md)"                              |
| Booth Lock                | "[booth/lock](/api/endpoints/booth_lock.md)"                                |
| Booth Move                | "[booth/move](/api/endpoints/booth_move.md)"                                |
| Booth Remove              | "[booth/remove/:id](/api/endpoints/booth_remove_id.md)"                     |
| Booth Skip                | "[booth/skip](/api/endpoints/booth_skip.md)"                                |
| Booth Skip Me             | "[booth/skip/me](/api/endpoints/booth_skip_me.md)"                          |
| Booth Waitlist Ban        | "[booth/waitlistban](/api/endpoints/booth_waitlistban.md)"                  |
| Chat Delete               | "[chat/:cid](/api/endpoints/chat_cid.md)"                                   |
| Friends                   | "[friends](/api/endpoints/friends.md)"                                      |
| Friends Ignore            | "[friends/ignore](/api/endpoints/friends_ignore.md)"                        |
| Friends Invites           | "[friends/invites](/api/endpoints/friends_invites.md)"                      |
| Grabs                     | "[grabs](/api/endpoints/grabs.md)"                                          |
| Ignores                   | "[ignores](/api/endpoints/ignores.md)"                                      |
| Mutes                     | "[mutes](/api/endpoints/mutes.md)"                                          |
| News                      | "[news](/api/endpoints/news.md)"                                            |
| Notifications             | "[notifications](/api/endpoints/notifications.md)"                          |
| Playlists                 | "[playlists](/api/endpoints/playlists.md)"                                  |
| Playlists Activate        | "[playlists/:id/activate](/api/endpoints/playlists_id_activate.md)"         |
| Playlists Media Delete    | "[playlists/:id/media/delete](/api/endpoints/playlists_id_media_delete.md)" |
| Playlists Media Insert    | "[playlists/:id/media/insert](/api/endpoints/playlists_id_media_insert.md)" |
| Playlists Media Move      | "[playlists/:id/media/move](/api/endpoints/playlists_id_media_move.md)"     |
| Playlists Media Update    | "[playlists/:id/media/update](/api/endpoints/playlists_id_media_update.md)" |
| Playlists Rename          | "[playlists/:id/rename](/api/endpoints/playlists_id_rename.md)"             |
| Playlists Shuffle         | "[playlists/:id/shuffle](/api/endpoints/playlists_id_shuffle.md)"           |
| Playlists Media           | "[playlists/:id/media](/api/endpoints/playlists_media.md)"                  |
| Profile Blurb             | "[profile/blurb](/api/endpoints/profile_blurb.md)"                          |
| Rooms                     | "[rooms](/api/endpoints/rooms.md)"                                          |
| Rooms Favorites           | "[rooms/favorites](/api/endpoints/rooms_favorites.md)"                      |
| Rooms History             | "[rooms/history](/api/endpoints/rooms_history.md)"                          |
| Rooms Join                | "[rooms/join](/api/endpoints/rooms_join.md)"                                |
| Rooms Me                  | "[rooms/me](/api/endpoints/rooms_me.md)"                                    |
| Rooms SOS                 | "[rooms/sos](/api/endpoints/rooms_sos.md)"                                  |
| Rooms State               | "[rooms/state](/api/endpoints/rooms_state.md)"                              |
| Rooms Update              | "[rooms/update](/api/endpoints/rooms_update.md)"                            |
| Rooms Validate            | "[rooms/validate](/api/endpoints/rooms_validate.md)"                        |
| Staff                     | "[staff](/api/endpoints/staff.md)"                                          |
| Staff Update              | "[staff/update](/api/endpoints/staff_update.md)"                            |
| Store Inventory           | "[store/inventory](/api/endpoints/store_inventory.md)"                      |
| Store Products            | "[store/products](/api/endpoints/store_products.md)"                        |
| Store Purchase            | "[store/purchase](/api/endpoints/store_purchase.md)"                        |
| Store Purchase Username   | "[store/purchase/username](/api/endpoints/store_purchase_username.md)"      |
| Users                     | "[users](/api/endpoints/users.md)"                                          |
| Users Avatar              | "[users/avatar](/api/endpoints/users_avatar.md)"                            |
| Users Badge               | "[users/badge](/api/endpoints/users_badge.md)"                              |
| Users Bulk                | "[users/bulk](/api/endpoints/users_bulk.md)"                                |
| Users Language            | "[users/language](/api/endpoints/users_language.md)"                        |
| Users Me                  | "[users/me](/api/endpoints/users_me.md)"                                    |
| Users Me History          | "[users/me/history](/api/endpoints/users_me_history.md)"                    |
| Users Me Transactions     | "[users/me/transactions](/api/endpoints/users_me_transactions.md)"          |
| Users Settings            | "[users/settings](/api/endpoints/users_settings.md)"                        |
| Users Signup            | "[users/signup](/api/endpoints/users_signup.md)"                        |
| Users Validate            | "[users/validate](/api/endpoints/users_validate.md)"                        |
| Votes                     | "[votes](/api/endpoints/votes.md)"                                          |

*Ordered by Endpoint Name^
