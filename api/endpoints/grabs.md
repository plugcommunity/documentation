# grabs Endpoint

The grabs endpoint enables you to grabs a song and add it to a playlist.

### Endpoint

**grabs**

### available verbs

_POST_

### Parameters

**playlistID**: ID of the playlist you want to add the song to
**historyID**: ID of the playback

```json
{
    "playlistID": -1,
    "historyID": "xxxxxxxx-xxxx-4xxx-xxxxx-xxxxxxxxxxxx"
}
```

### Data returned

```js
{
    'data': [{
      "active": false,              // Is the playlist active?
      "count": 0,                   // Amount of Media in this playlist
      "id": -1,                     // ID of the playlist
      "name": "xxx"                 // Name of the playlist
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```