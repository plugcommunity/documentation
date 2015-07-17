# booth/move Endpoint

The booth/move endpoint enables you to move a user in a waitlist.

**Note**: you need to have sufficient permissions in the room to access this resource.

### Endpoint

**booth/move**

### available verbs

_POST_

### Parameters

**userID**: ID of the user you want to move
**position**: The new position of the user

**Note**: the waitlist has a zero based index, so to move the user to the desired position you have to think 
n-1 where n equals the desired position

```json
{
    "userID": -1,
    "position": 0
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