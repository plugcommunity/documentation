# auth/login Endpoint

The auth/login endpoint logs you into the plug.dj service.

### Endpoint

**auth/login**

### available verbs

_POST_

### Parameters

**csrf**: Cross Site Request Forgery token
**email**: your email
**password**: your password

```json
{
    "csrf": "xxxxx"
    "email": "xxx@xxx.com"
    "password": "xxx"
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