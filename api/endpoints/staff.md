# staff Endpoint

The staff endpoint requests all staff members of the room you are currently in.

**Note**: There's five roles for the user

* **0**: None, just a regular user
* **1**: ResidentDJ, can lock the waitlist
* **2**: Bouncer, can delete chat messages, remove DJs, force skip and ban people
* **3**: Manager, can everything except removing co hosts and managers as well as editing the room meta
* **4**: Co-Host, can everything except removing co hosts
* **5**: Host, owner status 

### Endpoint

**staff**

### available verbs

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
    'data': [{              // Contains the requested data
        'avatarID': 'xxx',  // AvatarID (e.g.: 'base01')
        'badge': 'xxx',     // Badge of the DJ (e.g.: '80sb01')
        'gRole': 0,         // Global role of the user (0 = None; 3 = Brand Ambassador (BA); 5 = Admin)
        'guest': false,     // Is the DJ a guest? (this is not possible as of now)
        'id': -1,           // ID of the DJ
        'joined': 'xxx',    // String representation of the time the DJ joined plug (e.g.: '2014-07-23 22:47:00.573000')
        'language': 'xx',   // ISO 639-1 representation of the language used by the DJ
        'level': 1,         // Level of the DJ,
        'role': 1,          // Role of the user in this room
        'slug': 'xxx',      // URL conform representation of the DJ's name (also used for the profile page)
        'sub': 0,           // Is the DJ a subscriber? (0 = false; 1 = true)
        'username': 'xxx'   // Name of the DJ
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```