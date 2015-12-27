# modRemoveDJ message

Event passed when a moderator removes a user from the wait list.

### Packet Example

```js
[{
    "a": "modRemoveDJ",   // Event name
    "p": {
        "m": "xxxxxx",	// Name of the moderator
        "mi": -1,       // ID of the moderator
        "t": "xxxxxx",  // Name of the user that got removed
        "d": false      // Was the user in the booth (DJing)?
    },
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "modRemoveDJ",
    "p": {
        "m": "SooYou",
        "mi": 3865819,
        "t": "kool_panda",
        "d": false
    },
    "s": "loves-kpop"
}]
```