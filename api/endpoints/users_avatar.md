# users/avatar Endpoint

The users/avatar endpoint enables you to change your avatar.

### Endpoint

**users/avatar**

### Method

_PUT_

### Parameters

**id**: The avatarID of the avatar you want to use 

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