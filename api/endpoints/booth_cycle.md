# booth/cycle Endpoint

The booth/cycle endpoint enables you to cycle the waitlist.

**Note**: you need to have sufficient permissions in the room to access this resource.

### Endpoint

**booth/cycle**

### available verbs

_PUT_

### Parameters

**shouldCycle**: Should the booth cycle?

```json
{
    "shouldCycle": false
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