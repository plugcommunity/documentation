# auth/facebook Endpoint

The auth/facebook endpoint logs you into the plug.dj service

**Note**: This sets the **pw** member in your state data to false

### Endpoint

**auth/facebook**

### available verbs

_POST_

### Parameters

```js
{
    'csrf': 'xxxxx',        // Cross Site Request Forgery token
    'accessToken': 'xxx',   // Access token given by facebook.com
    'userID': 'xxx'         // userID given by facebook.com
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