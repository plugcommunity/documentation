# users/bulk Endpoint

The users/bulk endpoint retrieves the data about several users.

### Endpoint

**users/bulk**

### Method

_POST_

### Parameters

**ids**: The IDs of the users you want to retrieve data of as an array

```json
{
    "ids": [
        -1,
        -1,
        -1
    ]
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

ids is missing
```json
{
    "data": [
        "ids is required"
    ],
    "status": "requestError",
}
```

### Data returned

```js
{
    'data': [{                          // Contains the requested data
        'avatarID': 'xxx',              // Their AvatarID (e.g.: 'base01')
        'badge': 'xxx',                 // Their badge (e.g.: '80sb01')
        'gRole': 0,                     // Their service wide role (0 = None; 3 = Brand Ambassador (BA); 5 = Admin)
        'guest': false,                 // Is the user a guest?
        'id': -1,                       // Their ID
        'joined': 'xxx',                // String representation of the time they joined plug (e.g.: '2014-07-23 22:47:00.573000')
        'language': 'xx',               // ISO 639-1 representation of their used language
        'level': 1,                     // Their level
        'slug': 'xxx',                  // URL conform representation of their name (also used for the profile page)
        'sub': 0,                       // Is the user a subscriber? (0 = false; 1 = true)
        'username': 'xxx',              // Their username
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```