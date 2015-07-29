# users/me Endpoint

The users/me endpoint retrieves some data about yourself as well as notifications.

### Endpoint

**users/me**

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
    'data': [{                          // Contains the requested data
        'avatarID': 'xxx',              // Your AvatarID (e.g.: 'base01')
        'badge': 'xxx',                 // Your badge (e.g.: '80sb01')
        'gRole': 0,                     // Your service wide role (0 = None; 3 = Brand Ambassador (BA); 5 = Admin)
        'guest': false,                 // Are you a guest?
        'id': -1,                       // Your ID
        'joined': 'xxx',                // String representation of the time you joined plug (e.g.: '2014-07-23 22:47:00.573000')
        'language': 'xx',               // ISO 639-1 representation of the language used by you
        'level': 1,                     // Your level
        'blurb': 'xxx',                 // Profile message set by you
        'slug': 'xxx',                  // URL conform representation of the your name (also used for the profile page)
        'sub': 0,                       // Are you a subscriber? (0 = false; 1 = true)
        'username': 'xxx',              // Your username
        'xp': 0,                        // Your XP count
        'pp': 0,                        // Amount of plug points you gathered
        'pw': true,                     // Logged in via email?
        'settings': {
            'chatImages': true,         // Are chat images activates?
            'chatTimestamps': 12,       // Chat timestamps as 12 or 24 hour version
            'emoji': true,              // Should emojis be shown?
            'friendAvatarsOnly': true,  // Should only the avatars of my friends be shown?
            'notifyDJ': true,           // Notify me about a switch in DJs
            'notifyFriendJoin': true,   // Should you notify me about friends joining?
            'notifyScore': true,        // Should you notify me about the last played song's score?
            'tooltips': true,           // Should tooltips be shown?
            'videoOnly': true,          // Should only the video be shown?
        },
        'ignores': [{
            'id': -1,                   // ID of the user
            'username': 'xxxx'          // Name of the user
        }],
        'notifications': [{
            'action': 'xxx',            // Type of the notification
            'id': -1,                   // Internal ID
            'timestamp': 'xxx',         // Date when the notification triggered
            'value': 'x'                // Value carried with the notification
        }]
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```