# votes Endpoint

The votes endpoint enables you to woot or meh the current media.

### Endpoint

**votes**

### Method

_POST_

### Parameters

**direction**: Literally the direction of your vote and as such 1 is interpreted as woot and -1 as meh

**historyID**: Internal GUID v4 history ID of the current playback

```json
{
    "direction": 1,
    "historyID": "xxxxxxxx-xxxx-4xxx-xxxxx-xxxxxxxxxxxx"
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

### Data returned

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```