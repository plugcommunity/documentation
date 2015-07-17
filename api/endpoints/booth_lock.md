# booth/lock Endpoint

The booth/lock endpoint enables you to lock the waitlist.

**Note**: you need to have sufficient permissions in the room to access this resource.

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