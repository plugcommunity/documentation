# rooms/validate Endpoint

The rooms/validate endpoint escapes a room's name into an URL conform string.

### Endpoint

**rooms/validate/:name**

### available verbs

_GET_

### Parameters

**name**: Name of the room

### Data returned

```js
{
    'data': [{                  // Contains the requested data
        'slug': 'xxx'           // URL conform representation of the room's name
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```