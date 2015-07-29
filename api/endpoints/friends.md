# friends Endpoint

The friends endpoint will retrieve all of your friends or adds a user as a friend.

### Endpoint

**friends**

### Methods

_GET_, _POST_

### Data returned for _GET_

```js
{
    'data': [{              // Contains the requested data
        'avatarID': 'xxx',  // AvatarID (e.g.: 'base01')
        'badge': 'xxx',     // Badge of the user (e.g.: '80sb01')
        'gRole': 0,         // Global role of the user (0 = None; 3 = Brand Ambassador (BA); 5 = Admin)
        'guest': false,     // Is the user a guest? (this is not possible as of now)
        'id': -1,           // ID of the user
        'joined': 'xxx',    // String representation of the time the user joined plug (e.g.: '2014-07-23 22:47:00.573000')
        'language': 'xx',   // ISO 639-1 representation of the language used by the user
        'level': 1,         // Level of the user
        'status': 0,        // (deprecated) Status of the user
        'room': {
            'slug': 'xxx',  // URL conform representaiton of the room's name
            'name': 'xxx',  // Name of the room
            'id': 'xxx'     // ID of the room
        },
        'slug': 'xxx',      // URL conform representation of the user's name (also used for the profile page)
        'sub': 0,           // Is the user a subscriber? (0 = false; 1 = true)
        'username': 'xxx'   // Name of the user
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```

### Parameters for _POST_

**id**: ID of the user you want to add as a friend

```json
{
    "id": -1
}
```

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

id is missing
```json
{
    "data": [
        "id is required"
    ],
    "status": "requestError",
}
```

### Data returned for _POST_

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```