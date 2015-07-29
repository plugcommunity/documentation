# profile/blurb Endpoint

The profile/blurb endpoint enables you to change your profile message.

### Endpoint

**profile/blurb**

### Method

_PUT_

### Parameters

**blurb**: Your new profile message 

```json
{
    "blurb": "xxxxx"
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

blurb is missing
```json
{
    "data": [
        "blurb is required"
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