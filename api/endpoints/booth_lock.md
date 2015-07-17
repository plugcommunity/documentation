# booth/lock Endpoint

The booth/lock endpoint enables you to decide whether the waitlist should be locked or not.

**Note**: You need to have sufficient permissions in the room to access this resource.

### Endpoint

**booth/lock**

### available verbs

_PUT_

### Parameters

**isLocked**: Should the waitlist be locked?
**removeAllDJs**: Should all DJs be removed from the waitlist?

```json
{
    "isLocked": false,
    "removeAllDJs": false
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