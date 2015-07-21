# ChatDelete message

Event passed containing information about a received chat message.


### Packet Example

```js
{
    'a': 'chat',                        // Event name
    'p': {
        'message': 'xxxxxxxxxxxxx',     // Actual message
        'un': 'xxxxxxxx',               // Name of the user
        'cid': 'xxxxxxx-xxxxxxxxxxxxx', // Message ID
        'uid': -1,                      // ID of user
        'sub': 0                        // Is the user a subscriber?
    },
    's': 'xxxx'                         // Room name
}
```
### Real life example
```js
{
    'a': 'chat',
    'p': {
        'message': 'example message',
        'un': 'example user',
        'cid': '8009977-1436517063257',
        'uid': 5113863,
        'sub': 0
    },
    's': 'thenightcoreclub'
}
```
