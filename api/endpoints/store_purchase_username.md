# store/purchase/username Endpoint

The store/purchase/username endpoint enables you to change your username.

### Endpoint

**store/purchase/username**

### available verbs

_POST_

### Parameters

**username**: ID of the item you want to buy

```json
{
    "id": "454",
    "username": "xxx"
}
```

### Data returned

```js
{
    'data': [{
      'count': 1,
      'name': 'username',
      'pp': 0
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```