# playlists/:id/media/delete Endpoint

The playlists/:id/media/delete lets you delete media objects.

### Endpoint

**playlists/:id/media/delete**

### available verbs

_POST_

### Parameters

**ids**: IDs of the media objects you want to delete

```json
{
    "ids": [
        -1
    ]
}
```

### Data returned

```js
{
    'data': [{
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