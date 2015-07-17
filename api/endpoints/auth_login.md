# auth/login Endpoint

The auth/login endpoint logs you into the plug.dj service

### Endpoint

**auth/login**

### available verbs

_POST_

### Parameters

```js
{
    'csrf': 'xxxxx',        // Cross Site Request Forgery token
    'email': 'xxx@xxx.com', // E-Mail address
    'password': 'xxx'       // Password in plaintext
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