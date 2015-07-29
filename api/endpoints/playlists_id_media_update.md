# playlists/:id/media/update Endpoint

The playlists/:id/media/update endpoint lets you update the metadata of a media object.

### Endpoint

**playlists/:id/media/update**

### Method

_PUT_

### Parameters

**id**: ID of the media you want to update

**author**: Author of the media

**title**: Title of the media

```json
{
    "id": -1,
    "author": "xxx",
    "title": "xxx"
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

id, author or title is missing
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
        'author': 'xxx',    // Media author
        'title': 'xxx'      // Media title
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```