# ignores Endpoint

The ignores endpoint retrieves or modifies your ignores.

### Endpoint

**ignores**

### Methods

_GET_, _POST_

### Data returned for _GET_

```js
{
    'data': [{                  // Contains the requested data
        'id': -1,               // ID of the user
        'username': 'xxxx'      // Name of the user
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```

### Parameters for _POST_

**id**: ID of the user you want to mute

```json
{
    "id": -1
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

### Data returned for _POST_

```js
{
    'data': [{                  // Contains the requested data
        'id': -1,               // ID of the user
        'username': 'xxxx'      // Name of the user
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```