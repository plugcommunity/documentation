# rooms/users Endpoint

The rooms/users endpoint lets you retrieve a list of up to 250 users currently in the room (this includes guests).
Anyone with a role superior than 0 will be excluded, this also applies on gRole.

### Endpoint

**rooms/users**

### Method

_GET_

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

### Data returned

```js
{
    'data': [{              // Contains the requested data
        'id': -1,           // Their ID
        'username': 'xxx',  // Their username
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```
