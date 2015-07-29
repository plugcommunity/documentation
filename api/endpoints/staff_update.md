# staff/update Endpoint

The staff/update endpoint enables you to update the role of a user in your room.

You can view information on staff roles, [here](/api/roles.md).

### Endpoint

**staff/update**

### Method

_POST_

### Parameters

**userID**: ID of the user you want to add to the staff

**roleID**: ID of the role you want to apply

```json
{
    "userID": -1,
    "roleID": 1
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

userID or roleID is missing
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
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```