# store/inventory Endpoint

The store/inventory endpoint lists all of your boughts items.

### Endpoint

**store/inventory**

### Method

_GET_

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

### Data returned

```js
{
    'data': [{              // Contains the requested data in an array of objects
        'category': 'xxx',  // Item category
        'id': 'xxx',        // Item ID (which will then be set in avatarID for avatars and badge for badges)
        'type': 'xxx'       // Item type (e.g.: avatars or badges)
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```