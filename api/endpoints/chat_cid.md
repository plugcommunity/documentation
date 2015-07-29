# chat/:cid Endpoint

The chat/:cid endpoint enables you to delete a chat message via the Chat ID (cid).

**Note**: You need to have sufficient permissions in the room to access this resource.

### Endpoint

**chat/:cid**

### Method

_DELETE_

### URL Parameters

**cid**: ID of the chat message you want to delete

>https://plug.dj/_/chat/xxxxxx-xxxxxxxxxxx

### Data returned

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```