# friends/ignore Endpoint

The friends/ignore endpoint enables you to ignore a friend request.

### Endpoint

**friends/ignore**

### Method

_PUT_

### Parameters

**id**: The ID of the user whose friend request you want to reject

```json
{
    "id": "xxxxx"
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