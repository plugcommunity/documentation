# rooms/state Endpoint

The rooms/state endpoint requests meta information about the room you are currently in.

**NOTE**: The guests member is not available in this request, **neither** is the amount of guests included in the 
population count.

### Endpoint

**rooms/state**

### Method

_GET_

### Possible error messages

Insufficient permissions (not being logged in)
```json
{
    "data": [
        "You are not authorized to access this resource."
    ],
    "status": "notAuthorized",
}
```

Still on dashboard
```json
{
    "data": [
        "not in a room."
    ],
    "status": "requestError",
}
```

### Data returned

```js
{
    'data': [{                      // Contains the requested data
        'booth': {
            'currentDJ': -1,        // ID of the current DJ
            'isLocked': false,      // Is the WaitList locked?
            'shouldCycle': false,   // Should the WaitList cycle?
            'waitingDJs': []        // Representation of the WaitList as an ordered array of IDs
        },
        'fx': [],                   // Effects available for this room
        'grabs': {},                // Representation of the grabs as an array of IDs
        'meta': {                   // Meta information about the room
            'description': 'xxx',   // Description of the room
            'favorite': false,      // Is this room favorited by you?
            'guests': 0,            // Amount of guests connected
            'hostID': -1,           // ID of the host
            'hostName': 'xxx',      // Name of the host
            'id': -1,               // ID of the room
            'minChatLevel': 1,      // Minimum level needed to chat
            'name': 'xxx',          // Name of the room
            'population': 0,        // Amount of real users in the room (guests excluded)
            'slug': 'xxx',          // URL conform representation of the room's name
            'welcome': 'xxx'        // Welcome message of the room
        },
        'mutes': {                  // Representation of the muted users as an array
            'xxxx': -1,             // "ID of the user": time remaining in seconds 
        },
        'playback': {
            'historyID': 'xxx',     // HistoryID of the playback
            'playlistID': 'xxx',    // ID of the playlist this media is in
            'startTime': 'xxx',     // Date and time when the media started playing
            'media': {
                'author': 'xxx',    // Author of the media
                'title': 'xxx',     // Title of the media
                'cid': 'xxx',       // Media ID used on the originating website
                'duration': 0,      // Duration in seconds
                'format': 1,        // Site the media originates from (1 = youtube; 2 = soundcloud)
                'id': -1,           // Internal media ID
                'image': 'xxx'      // Thumbnail
            }
        },
        'role': 0,                  // Your role in the room
        'users': [{                 // Array of user objects containing the currently connected users
            'avatarID': 'xxx',      // AvatarID (e.g.: 'base01')
            'badge': 'xxx',         // Badge of the DJ (e.g.: '80sb01')
            'gRole': 0,             // Global role of the user (0 = None; 3 = Brand Ambassador (BA); 5 = Admin)
            'id': -1,               // ID of the DJ
            'joined': 'xxx',        // String representation of the time the DJ joined plug (e.g.: '2014-07-23 22:47:00.573000')
            'level': 1,             // Level of the DJ,
            'role': 0,              // Role of the user in this room
            'sub': 0,               // Is the DJ a subscriber? (0 = false; 1 = true)
            'username': 'xxx'       // Name of the DJ
        }],
        'votes': {                  // Representation of the votes as an array
            'xxx': -1,              // 'ID of the user': vote direction (1 = woot; -1 = meh)
        }
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```