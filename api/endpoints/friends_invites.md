# friends/invites Endpoint

The friends/invites endpoint will retrieve all of the friend invites you received.

### Endpoint

**friends/invites**

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
    'data': [{              // Contains the requested data
        'avatarID': 'xxx',  // AvatarID (e.g.: 'base01')
        'gRole': 0,         // Global role of the user (0 = None; 3 = Brand Ambassador (BA); 5 = Admin)
        'id': -1,           // ID of the user
        'joined': 'xxx',    // String representation of the time the user joined plug (e.g.: '2014-07-23 22:47:00.573000')
        'level': 1,         // Level of the user
        'status': 0,        // (deprecated) Status of the user
        'timestamp': 'xxx', // When the friend invite was sent
        'username': 'xxx'   // Name of the user
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```