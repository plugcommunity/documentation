# playlists/:id/media/insert Endpoint

The playlists/:id/media/insert endpoint lets you insert media objects into a playlist.

### Endpoint

**playlists/:id/media/insert**

### Method

_POST_

### Parameters

**media**: Media objects you want to insert

**append**: Should the array be concatenated at the end of the playlist?

```json
{
    "media": [{
        "cid": "xxx",
        "title": "xxx",
        "author": "xxx",
        "image": "xxx",
        "duration": 0,
        "format": 1,
        "id": -1
    }],
    "append": false
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

media or append is missing
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
