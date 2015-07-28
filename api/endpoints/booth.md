# booth Endpoint

The booth endpoint enables you to join (_POST_) or leave (_DELETE_) the waitlist.

### Endpoint

**booth**

### available verbs

_POST_, _DELETE_

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

Not in a room
```json
{
    "data": [
        "not in a room."
    ],
    "status": "requestError",
}
```

### Data returned for both verbs

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```