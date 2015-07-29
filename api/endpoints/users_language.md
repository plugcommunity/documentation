# users/language Endpoint

The users/language endpoint enables you to change your language settings.

### Endpoint

**users/language**

### Method

_PUT_

### Parameters

**language**: ISO 639-1 representation of the language you want to use

```json
{
    "language": "xx"
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

language is missing
```json
{
    "data": [
        "language is required"
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