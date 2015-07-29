# booth/move Endpoint

The booth/move endpoint enables you to move a user in the waitlist.

**Note**: You need to have sufficient permissions in the room to access this resource.

### Endpoint

**booth/move**

### Method

_POST_

### Parameters

**userID**: ID of the user you want to move

**position**: The new position of the user

**Note**: The waitlist has a zero based index, so to move the user to the desired position you have to think 
about it as **n-1** where **n** equals the **desired position**

```json
{
    "userID": -1,
    "position": 0
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

User is not in the waitlist
```json
{
    "data": [],
    "status": "userNotInBooth",
}
```

userID or position is missing
```json
{
    "data": [
        "xxxxx is required"
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