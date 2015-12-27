# floodChat message

Event passed when you send too many chat messages at once.

### Packet Example

```js
[{
    "a": "floodChat",   // Event name
    "p": {},
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "floodChat",
    "p": {},
    "s": "loves-kpop"
}]
```