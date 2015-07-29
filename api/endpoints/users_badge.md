# users/badge Endpoint

The users/badge endpoint lets you change your current badge.

### Endpoint

**users/badge**

### Method

_PUT_

### Parameters

**id**: ID of the badge you want to use

```json
{
    "id": "xxx"
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