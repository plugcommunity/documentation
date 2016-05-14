# rooms/join Endpoint

The rooms/join endpoint enables you to join a room.

### Endpoint

**rooms/join**

### Method

_POST_

### Parameters

**slug**: The URL of the room you want to join

```json
{
    "slug": "xxxxx"
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

slug is missing
```json
{
    "data": [
        "slug is required"
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
