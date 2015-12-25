# auth/login Endpoint

The auth/login endpoint logs you into the plug.dj service.

### Endpoint

**auth/login**

### Method

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

CSRF token has expired
```json
{
    "data": [
        "This CSRF token has expired."
    ],
    "status": "csrfTokenExpired",
}
```

CSRF token is invalid
```json
{
    "data": [
        "This CSRF token is invalid."
    ],
    "status": "csrfTokenInvalid",
}
```

Email or password isn't correct
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
