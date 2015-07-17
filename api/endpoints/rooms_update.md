# rooms/update Endpoint

The rooms/update endpoint enables you to partially change the metadata of your room.

### Endpoint

**rooms/update**

### available verbs

_POST_

### Parameters

**name**: Name of your room
**description**: Description of your room
**welcome**: Welcome message of your room

```json
{
    "name": "xxx",
    "description": "xxx",
    "welcome": "xxx",
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