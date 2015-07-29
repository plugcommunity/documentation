# users/me/transactions Endpoint

The users/me/transactions endpoint retrieves the full list of your transactions with plug.

### Endpoint

**users/me/transactions**

### Method

_GET_

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
    'data': [{              // Contains the requested data
        'id': 'xxx',        // Internal ID of the transaction
        'item': 'xxxx',     // Name of the item you bought
        'pp': 0,            // The price you paid in plug points
        'cash': 0,          // The price you paid in cash
        'timestamp': 'xxx', // Date of the transaction
        'type': 'xxxx'      // The type of item you bought
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```