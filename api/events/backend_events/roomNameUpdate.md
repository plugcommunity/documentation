# roomNameUpdate message

Event passed when a co-host or host updates the room's name.

### Packet Example

```js
[{
    "a": "roomNameUpdate",          // Event name
    "p": {
        "n": "xxxxx",               // Room name
        "u": -1                     // ID of moderator
    }, 
    "s": "xxxx"                     // Room name
}]
```
### Real life example
```js
[{
    "a": "roomNameUpdate",
    "p": {
        "n": "Test room please ignore",
        "u": 3865819
    }, 
    "s": "test-room"
}]
```