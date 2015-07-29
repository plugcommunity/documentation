# booth/cycle Endpoint

The booth/cycle endpoint enables you to decide whether the waitlist should cycle or not.

**Note**: You need to have sufficient permissions in the room to access this resource.

### Endpoint

**booth/cycle**

### Method

_PUT_

### Parameters

**shouldCycle**: Should the booth cycle?

```json
{
    "shouldCycle": false
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

shouldCycle is missing
```json
{
    "data": [
        "shouldCycle is required"
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