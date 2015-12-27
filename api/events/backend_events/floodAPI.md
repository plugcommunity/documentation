# floodAPI message

Event passed when you send too many API requests at once.

### Packet Example

```js
[{
    "a": "floodAPI",    // Event name
    "p": {},
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "floodAPI",
    "p": {},
    "s": "loves-kpop"
}]
```