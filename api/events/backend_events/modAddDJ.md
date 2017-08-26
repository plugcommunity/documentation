# modAddDJ message

Event passed when a moderator adds a user to the wait list.


### Packet Example

```js
[{
    "a": "modAddDJ",    // Event name
    "p": {
        "m": "xxxxxx",	// Username of the moderator
        "mi": -1,       // ID of the moderator
        "t": "xxxxxx"   // Name of the user that got added
    },
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "modAddDJ",
    "p": {
        "m": "SooYou",
        "mi": 3865819,
        "t": "kool_panda"
    },
    "s": "loves-kpop"
}]
```
