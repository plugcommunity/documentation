# playlists/:id/rename Endpoint

The playlists/:id/rename endpoint enables you to rename a playlist.

### Endpoint

**playlists/:id/rename**

### Method

_PUT_

### Parameters

**name**: The new name of the playlist

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

name is missing
```json
{
    "data": [
        "name is required"
    ],
    "status": "requestError",
}
```

### Data returned

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```