# auth/login Endpoint

The auth/login endpoint logs you into the plug.dj service.

### Endpoint

**auth/login**

### available verbs

_POST_

### Parameters

**csrf**: Cross Site Request Forgery token
**email**: Your email
**password**: Your password

```json
{
    "csrf": "xxxxx",
    "email": "xxx@xxx.com",
    "password": "xxx"
}
```

### Possible error messages

CSRF token is invalid
```json
{
    "data": [
        "This CSRF token has expired."
    ],
    "status": "csrfTokenExpired",
}
```

Email or password aren't correct
```json
{
    "data": [],
    "status": "badLogin",
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