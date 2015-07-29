# rooms/me Endpoint

The rooms/me endpoint requests meta information about the rooms you host.

**NOTE**: The guests member is not available in this request, **neither** is the amount of guests included in the 
population count.

### Endpoint

**rooms/me**

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

### Data returned

```js
{
    'data': [{                  // Contains the requested data
        'capacity': null,       // Maximum capacity of the room (it's null for most rooms but the most populated ones)
        'cid': 'xxx',           // ID of the room
        'dj': {                 // Current DJ (this is null if no DJ is playing)
            'avatarID': 'xxx',  // AvatarID (e.g.: 'base01')
            'badge': 'xxx',     // Badge of the DJ (e.g.: '80sb01')
            'gRole': 0,         // Global role of the user (0 = None; 3 = Brand Ambassador (BA); 5 = Admin)
            'guest': false,     // Is the DJ a guest? (this is not possible as of now)
            'id': -1,           // ID of the DJ
            'joined': 'xxx',    // String representation of the time the DJ joined plug (e.g.: '2014-07-23 22:47:00.573000')
            'language': 'xx',   // ISO 639-1 representation of the language used by the DJ
            'level': 1,         // Level of the DJ,
            'slug': 'xxx',      // URL conform representation of the DJ's name (also used for the profile page)
            'sub': 0,           // Is the DJ a subscriber? (0 = false; 1 = true)
            'username': 'xxx'   // Name of the DJ
        },
        'favorite': false,      // Is this room favorited by you?
        'format': 1,            // Site the media originates from (1 = youtube; 2 = soundcloud)
        'host': 'xxx'           // Name of the host
        'id': 'xxx'             // ID of the room
        'image': 'xxx.jpg',     // Thumbnail
        'media': 'xxx',         // Author and Title of the media being played
        'name': 'xxx',          // Name of the room
        'nsfw': false,          // Is the room flagged as inappropiate? (can not be set manually)
        'population': 0,        // Current population of the room
        'private': false,       // Is the room private?
        'slug': 'xxx'           // URL conform representation of the room's name
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```