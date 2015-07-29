# rooms/update Endpoint

The rooms/update endpoint enables you to partially change the metadata of your room.

### Endpoint

**rooms/update**

### Method

_POST_

### Parameters

**name**: Name of your room

**description**: Description of your room

**welcome**: Welcome message of your room

```json
{
    "name": "xxx",
    "description": "xxx",
    "welcome": "xxx",
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

name, description or welcome is missing
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