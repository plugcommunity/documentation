# auth/facebook Endpoint

The auth/facebook endpoint logs you into the plug.dj service.

**Note**: This sets the **pw** member in your state data to false

### Endpoint

**auth/facebook**

### available verbs

_POST_

### Parameters

**csrf**: Cross Site Request Forgery token

**accessToken**: Access token given by facebook.com

**userID**: userID given by facebook.com

```json
{
    "csrf": "xxxxx",
    "accessToken": "xxx", 
    "userID": "xxx"
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