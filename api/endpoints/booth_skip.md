# booth/skip Endpoint

The booth/skip endpoint enables you to skip the current DJ.

**Note**: You need to have sufficient permissions in the room to access this resource.

### Endpoint

**booth/skip**

### Method

_POST_

### Parameters

**userID**: ID of the DJ you want to skip

**historyID**: History ID of the playback 

```json
{
    "userID": -1,
    "historyID": "xxxxxxxx-xxxx-4xxx-xxxx-xxxxxxxxxxxx"
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

userID or historyID is missing
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