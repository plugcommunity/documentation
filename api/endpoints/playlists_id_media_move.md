# playlists/:id/media/move Endpoint

The playlists/:id/media/move endpoint lets you move media objects to another index in a playlist.

### Endpoint

**playlists/:id/media/move**

### Method

_PUT_

### Parameters

**ids**: Array of media IDs which represent the media you want to move

**beforeID**: ID of the media where the media should be inserted

```json
{
    "ids": [
        -1
    ],
    "beforeID": -1
}
```

### Possible error messages

Insufficient permissions
```json
{
    "data": [
        "You are not authorized to access this resource."
    ],
    "status": "notAuthorized",
}
```

ids or beforeID is missing
```json
{
    "data": [
        "xxxxxxxx is required"
    ],
    "status": "requestError",
}
```

### Data returned

```js
{
    'data': [{              // Contains the requested data
        'cid': 'xxx',       // Media ID used on the originating website
        'title': 'xxx',     // Media title
        'author': 'xxx',    // Media author
        'image': 'xxx',     // Thumbnail (youtube) or Artwork (soundcloud)
        'duration': 0,      // Duration in seconds
        'format': 1,        // Media format (1 = youtube; 2 = soundcloud)
        'id': -1            // Internal media ID
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```