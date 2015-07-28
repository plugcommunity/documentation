# skip message

Event passed when the current DJ skips their song.


### Packet Example

```js
{
    'a': 'skip',            // Event name
    'p': -1,                // ID of the user
    's': 'xxxx'             // Room name
}
```
### Real life example
```js
{
    'a': 'skip',
    'p': 2348789,
    's': 'loves-kpop'
}
```
