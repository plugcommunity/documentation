# users/validate/:name Endpoint

The users/validate/:name endpoint escapes a user's name into an URL conform string.

**Note**: While this is also used to remove special characters, not all are removed, i.e. some like '**<**' or '**>**' will
just be converted to '**lt**' and '**gt**'

### Endpoint

**users/validate/:name**

### Method

_GET_

### Parameters

**name**: Name of the user

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
    'data': [{                  // Contains the requested data
        'slug': 'xxx'           // URL conform representation of the user's name
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```