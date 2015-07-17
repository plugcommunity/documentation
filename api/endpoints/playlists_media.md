# playlists/:id/media Endpoint

The playlists/:id/media endpoint retrieves all of your playlists.

### Endpoint

**playlists/:id/media**

### available verbs

_GET_

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