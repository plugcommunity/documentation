# news Endpoint

The news endpoint retrieves a sorted feed from blog.plug.dj

### Endpoint

**news**

### available verbs

_GET_

### Data returned

```js
{
    'data': [{              // Contains the requested data
        'desc': 'xxxxxx',   // Short preview of the article
        'title': 'xxxx',    // Title of the article
        'href': 'xxxx'      // Link to the article (normally blog.plug.dj)
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```