# store/purchase Endpoint

The store/purchase endpoint enables you to buy items from the store.

### Endpoint

**store/purchase**

### Method

_POST_

### Parameters

**id**: ID of the item you want to buy

```json
{
    "id": "xxx"
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

id is missing
```json
{
    "data": [
        "id is required"
    ],
    "status": "requestError",
}
```

Not enough plug points
```json
{
    "data": [
        "fundsPP"
    ],
    "status": "requestError",
}
```

Not a store item
```json
{
    "data": [
        "listing"
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