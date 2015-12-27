# roomDescriptionUpdate message

Event passed when a co-host or host updates the room description.

### Packet Example

```js
[{
    "a": "roomDescriptionUpdate",   // Event name
    "p": {
        "d": "xxxxx",               // Room description
        "u": -1                     // ID of moderator
    }, 
    "s": "xxxx"                     // Room name
}]
```
### Real life example
```js
[{
    "a": "roomDescriptionUpdate",
    "p": {
        "d": "Test Description",
        "u": 3865819
    }, 
    "s": "loves-kpop"
}]
```