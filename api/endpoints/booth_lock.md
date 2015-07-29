# booth/lock Endpoint

The booth/lock endpoint enables you to decide whether the waitlist should be locked or not.

**Note**: You need to have sufficient permissions in the room to access this resource.

### Endpoint

**booth/lock**

### Method

_PUT_

### Parameters

**isLocked**: Should the waitlist be locked?

**removeAllDJs**: Should all DJs be removed from the waitlist?

```json
{
    "isLocked": false,
    "removeAllDJs": false
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

isLocked or removeAllDJs is missing
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