### Introduction

The plug API is seperated into two systems, 
[WebSocket](https://github.com/plugcommunity/documentation/tree/master/api/events) and 
[REST](#).
While the WebSocket part is used to communicate at real time (such as chat, booth advancement etc.), the REST API is 
used to do everything that does not require a real time connection. While this certainly induces a bit of latency
for each action, it is something that can be easily handled with.


### Tips and tricks

One thing to mention is that you can only send a limited amount of request in a certain timespan, if you do overdo it 
for a longer amount of time you'll be banned. This can certainly happen when you decide to go for deleting
a bunch of chat messages without artifically slowing the amount of requests down.

### List of endpoints

| Endpoint Name             | Link                                                                                     |
|-----------------------    | -------------                                                                            |
| Auth Facebook             | "[auth/facebook]                 (/auth_facebook.md)"                                    |
| Auth Login                | "[auth/login]                    (/auth_login.md)"                                       |
| Auth Reset                | "[auth/reset/me]                 (/auth_reset_me.md)"                                    |
| Auth Session              | "[auth/session]                  (/auth_session.md)"                                     |
| Bans                      | "[bans]                          (/bans.md)"                                             |
| Bans Add                  | "[bans/add]                      (/bans_add.md)"                                         |
| Booth                     | "[booth]                         (/booth_md)"                                            |
| Booth Add                 | "[booth/add]                     (/booth_add.md)"                                        |
| Booth Cycle               | "[booth/cycle]                   (/booth_cycle.md)"                                      |
| Booth Lock                | "[booth/lock]                    (/booth_lock.md)"                                       |
| Booth Move                | "[booth/move]                    (/booth_move.md)"                                       |
| Booth Remove              | "[booth/remove/:id]              (/booth_remove.md)"                                     |
| Booth Skip                | "[booth/skip]                    (/booth_skip.md)"                                       |
| Booth Skip Me             | "[booth/skip/me]                 (/booth_skip_me.md)"                                    |
| Chat Delete               | "[chat/:cid]                     (/chat_cid.md)"                                         |
| Friends                   | "[friends]                       (/friends.md)"                                          |
| Friends Ignore            | "[friends/ignore]                (/friends_ignore.md)"                                   |
| Friends Invites           | "[friends/invites]               (/friends_invites.md)"                                  |
| Grabs                     | "[grabs]                         (/grabs.md)"                                            |
| Ignores                   | "[ignores]                       (/ignores.md)"                                          |
| Mutes                     | "[mutes]                         (/mutes.md)"                                            |
| News                      | "[news]                          (/news.md)"                                             |
| Playlists                 | "[playlists]                     (/playlists.md)"                                        |
| Playlists Activate        | "[playlists/:id/activate]        (/playlists_id_activate.md)"                            |
| Playlists Media Delete    | "[playlists/:id/media/delete]    (/playlists_id_media_delete.md)"                        |
| Playlists Media Insert    | "[playlists/:id/media/insert]    (/playlists_id_media_insert.md)"                        |
| Playlists Media Move      | "[playlists/:id/media/move]      (/playlists_id_media_move.md)"                          |
| Playlists Media Update    | "[playlists/:id/media/update]    (/playlists_id_media_update.md)"                        |
| Playlists Rename          | "[playlists/:id/rename]          (/playlists_id_rename.md)"                              |
| Playlists Shuffle         | "[playlists/:id/shuffle]         (/playlists_id_shuffle.md)"                             |
| Playlists Media           | "[playlists/:id/media]           (/playlists_id_media.md)"                               |
| Profile Blurb             | "[profile/blurb]                 (/profile_blurb.md)"                                    |
| Rooms                     | "[rooms]                         (/rooms.md)"                                            |
| Rooms Favorites           | "[rooms/favorites]               (/rooms_favorites.md)"                                  |
| Rooms History             | "[rooms/history]                 (/rooms_history.md)"                                    |
| Rooms Join                | "[rooms/join]                    (/rooms_join.md)"                                       |
| Rooms Me                  | "[rooms/me]                      (/rooms_me.md)"                                         |
| Rooms State               | "[rooms/state]                   (/rooms_state.md)"                                      |
| Rooms Update              | "[rooms/update]                  (/rooms_update.md)"                                     |
| Rooms Validate            | "[rooms/validate]                (/rooms_validate.md)"                                   |
| Staff                     | "[staff]                         (/staff.md)"                                            |
| Staff Update              | "[staff/update]                  (/staff_update.md)"                                     |
| Store Inventory           | "[store/inventory]               (/store_inventory.md)"                                  |
| Store Products            | "[store/products]                (/store_products.md)"                                   |
| Store Purchase            | "[store/purchase]                (/store_purchase.md)"                                   |
| Store Purchase Username   | "[store/purchase/username]       (/store_purchase_username.md)"                          |
| Users                     | "[users]                         (/users.md)"                                            |
| Users Avatar              | "[users/avatar]                  (/users_avatar.md)"                                     |
| Users Bulk                | "[users/bulk]                    (/users_bulk.md)"                                       |
| Users Language            | "[users/language]                (/users_language.md)"                                   |
| Users Me                  | "[users/me]                      (/users_me.md)"                                         |
| Users Me History          | "[users/me/history]              (/users_me_history.md)"                                 |
| Users Me Transactions     | "[users/me/transactions]         (/users_me_transactions.md)"                            |
| Votes                     | "[votes]                         (/votes.md)"                                            |

*Ordered by Endpoint Name^