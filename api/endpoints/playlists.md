# playlists Endpoint

The playlists endpoint retrieves or modifies your playlists.

### Endpoint

**playlists**
**playlists/:id**

### available verbs

_GET_, _POST_, _DELETE_

### Data returned for _GET_

```js
{
    'data': [{              // Contains the requested data
        'active': false,    // Is the playlist currently selected for playback?
        'count': 0,         // Amount of songs in this playlist
        'id': -1,           // ID of the playlist
        'name': 'xxx'       // Name of the playlist
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```

### Parameters for _POST_

**name**: Name of the new playlist
**media**: Array of media objects used to fill the playlist

```json
{
    "name": "xxx",
    "media": [{
        "cid": "",
        "title": "xxx",
        "author": "xxx",
        "image": "xxx",
        "duration": 0,
        "format": 1,
        "id": -1
    }]
}
```

### Data returned for _POST_

```js
{
    'data': [{              // Contains the requested data
        'active': false,    // Is the playlist currently selected for playback?
        'count': 0,         // Amount of songs in this playlist
        'id': -1,           // ID of the playlist
        'name': 'xxx'       // Name of the playlist
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```

### URL Parameters

**id**: ID of the playlist you want to delete

>https://plug.dj/_/playlists/-1

### Data returned for _DELETE_

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```