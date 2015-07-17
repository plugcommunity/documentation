# booth/add Endpoint

The booth/add endpoint enables you to add a user to the waitlist.

**Note**: You need to have sufficient permissions in the room to access this resource.

### Endpoint

**booth/add**

### available verbs

_POST_

### Parameters

**id**: ID of the user you want to add

```json
{
    "id": -1
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