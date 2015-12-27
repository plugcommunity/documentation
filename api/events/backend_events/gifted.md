# gifted message

Event passed when a user sends another one a gift.

### Packet Example

```js
[{
    "a": "gifted",   // Event name
    "p": {
        "s": "xxx",     // Sender
        "r": "xxx"      // Recipient
    },
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "gifted",
    "p": {
        "s": "kool_panda",
        "r": "SooYou"
    },
    "s": "loves-kpop"
}]
```