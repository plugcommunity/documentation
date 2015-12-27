# modMoveDJ message

Event passed when a moderator moves a user in the wait list.

### Packet Example

```js
[{
    "a": "modMoveDJ",   // Event name
    "p": {
        "m": "xxxxxx",	// Name of the moderator
        "mi": -1,       // ID of the moderator
        "u": "xxxxxx",  // Name of the user that got moved
        "o": -1,        // Old position in the wait list
        "n": -1,        // New position in the wait list
    },
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "modMoveDJ",
    "p": {
        "m": "SooYou",
        "mi": 3865819,
        "u": "kool_panda",
        "o": 31,
        "n": 0
    },
    "s": "loves-kpop"
}]
```