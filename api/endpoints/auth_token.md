# auth/token Endpoint

The auth/token endpoint retrieves your ID token.

**Note**: This is used to connect the websocket.

### Endpoint

**auth/token**

### Method

_GET_

### Data returned

```js
{
    'data': [
        'xxxx'                  // Your token here.
    ],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```