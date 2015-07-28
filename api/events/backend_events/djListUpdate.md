# djListUpdate message

Event passed when the waitlist changes.


### Packet Example

```js
{
    'a': 'djListUpdate',    // Event name
    'p': [-1, -1],          // WaitList as an array of user IDs
    's': 'xxxx'             // Room name
}
```
### Real life example
```js
{
    'a': 'djListUpdate',
    'p': [2348789, 4930583],
    's': 'loves-kpop'
}
```
