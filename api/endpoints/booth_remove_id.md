# booth/remove/:id Endpoint

The booth/remove/:id endpoint lets you remove a user from the waitlist.

**Note**: You need to have sufficient permissions in the room to access this resource.

### Endpoint

**booth/remove/:id**

### Method

_DELETE_

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
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```