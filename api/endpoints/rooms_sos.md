# rooms/sos Endpoint

The rooms/sos endpoint enables you to send an emergency ticket to the plug staff.

**Note**: You need to have sufficient permissions in a room to do this

### Endpoint

**rooms/sos**

### Method

_POST_

### Parameters

**message**: Your emergency message 

```json
{
    "message": "xxxxx"
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

message is missing
```json
{
    "data": [
        "message is required"
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