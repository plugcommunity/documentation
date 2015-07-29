# grabs Endpoint

The grabs endpoint enables you to grabs a song and add it to a playlist.

### Endpoint

**grabs**

### Method

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

playlistID or historyID is missing
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