# friends/ignore Endpoint

The friends/ignore endpoint enables you to ignore a friend request.

### Endpoint

**friends/ignore**

### available verbs

_PUT_

### Parameters

**id**: The ID of the user whose friend request you want to reject

```json
{
    "id": "xxxxx"
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