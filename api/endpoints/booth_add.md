# booth/add Endpoint

The booth/add endpoint enables you to add a user to the waitlist.

**Note**: You need to have sufficient permissions in the room to access this resource.

### Endpoint

**booth/add**

### Method

_POST_

### Parameters

**id**: ID of the user you want to add

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

User isn't in the room
```json
{
    "data": [],
    "status": "roomMismatch",
}
```

Waitlist is full
```json
{
    "data": [],
    "status": "boothFull",
}
```


User doesn't have a playlist
```json
{
    "data": [],
    "status": "noValidPlaylist",
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
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```
