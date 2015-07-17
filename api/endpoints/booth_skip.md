# booth/skip Endpoint

The booth/skip endpoint enables you to skip the current DJ.

**Note**: You need to have sufficient permission in the room to acces this resource.

### Endpoint

**booth/skip**

### available verbs

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

### Data returned

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```