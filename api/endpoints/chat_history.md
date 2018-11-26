# chat/history Endpoint

The chat/history endpoint retrieves the last 30 messages that were sent in the room and the users object from the different authors.
If a message gets deleted, the list is updated accordingly.

### Endpoint

**chat/history**

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
    'data': [{                              // Contains the requested data
        'history': [{
            'cid': 'xxx',                   // Internal ID of the message
            'message': 'xxx',               // The content of the message
            'sub': 0,                       // Is the user a subscriber? (0 = false; 1 = true)
            'timestamp': 'xxx',             // String representation of the time the message was sent (e.g.: '2018-01-23 06:45:23.000000')
            'uid': -1,                      // Author's ID
            'un': 'xxx'                     // Author's username
        }],
        'users': [{                         // Contains the requested data
            'avatarID': 'xxx',              // Their AvatarID (e.g.: 'base01')
            'badge': 'xxx',                 // Their badge (e.g.: '80sb01')
            'gRole': 0,                     // Their service wide role (0 = None; 3000 = Brand Ambassador (BA); 5000 = Admin)
            'guest': false,                 // Is the user a guest?
            'id': -1,                       // Their ID
            'joined': 'xxx',                // String representation of the time they joined plug (e.g.: '2014-07-23 22:47:00.573000')
            'language': 'xx',               // ISO 639-1 representation of their used language
            'level': 1,                     // Their level
            'silver': false                 // Is the user a silver subscriber?
            'slug': 'xxx',                  // URL conform representation of their name (also used for the profile page)
            'sub': 0,                       // Is the user a subscriber? (0 = false; 1 = true)
            'username': 'xxx',              // Their username
        }]
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```
