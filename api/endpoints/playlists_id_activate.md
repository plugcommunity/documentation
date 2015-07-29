# playlists/:id/activate Endpoint

The playlists/:id/activate endpoint enables you to activate a playlist as the one you want to play media of.

### Endpoint

**playlists/:id/activate**

### Method

_PUT_

### Parameters

**id**: ID of the playlist you want to activate

```json
{
    "id": -1
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

id is missing
```json
{
    "data": [
        "id is required"
    ],
    "status": "requestError",
}
```

### Data returned

```js
{
    'data': [{                  // Contains the requested data
        'activated': -1         // ID of the playlist you just activated
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```