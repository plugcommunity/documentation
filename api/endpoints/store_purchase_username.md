# store/purchase/username Endpoint

The store/purchase/username endpoint enables you to change your username.

### Endpoint

**store/purchase/username**

### Method

_POST_

### Parameters

**username**: ID of the item you want to buy

```json
{
    "id": "454",
    "username": "xxx"
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

id or username is missing
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
      'count': 1,
      'name': 'username',
      'pp': 0
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```