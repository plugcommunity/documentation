# users/me/history Endpoint

The users/me/history endpoint retrieves a sorted list of songs you have played in the past.

### Endpoint

**users/me/history**

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
    'data': [{                                          // Contains the requested data in an array of objects
        'id': 'xxxxxxxx-xxxx-4xxx-xxxx-xxxxxxxxxxxx',   // Internal GUID v4 history ID
        'media': {
            'cid': 'xxx',                               // Media ID used on the originating website
            'title': 'xxx',                             // Media title
            'author': 'xxx',                            // Media author
            'image': 'xxx',                             // Thumbnail (youtube) or Artwork (soundcloud)
            'duration': 0,                              // Duration in seconds
            'format': 1,                                // Media format (1 = youtube; 2 = soundcloud)
            'id': -1                                    // Internal media ID
        },
        'room': {
            'name': 'xxx',                              // Name of the room the media was played in
            'private': false,                           // Is the room private?
            'slug': 'xxx'                               // URL conform representation of the room's name
        },
        'score': {
            'grabs': 0,                                 // Amount of grabs
            'listeners': 0,                             // Amount of listeners
            'negative': 0,                              // Amount of mehs
            'positive': 0,                              // Amount of woots
            'skipped': 0                                // Indicated whether the DJ was skipped or not
        },
        'timestamp': 'xx-xx-xx',                        // Indicates when this media was played
        'user': {
            'id': -1,                                   // ID of the DJ
            'username': 'xxx'                           // Name of the user
        }
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```