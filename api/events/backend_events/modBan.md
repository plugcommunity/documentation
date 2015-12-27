# modBan message

Event passed when a moderator bans a user.

**Note**: the ban duration offers you the following three options

* **h**: Banned for an hour

* **d**: Banned for a day

* **f**: Banned for ever

### Packet Example

```js
[{
    "a": "modBan",      // Event name
    "p": {
        "m": "xxxxxx",	// Name of the moderator
        "mi": -1,       // ID of the moderator
        "t": "xxxxxx",  // Name of the user that got banned
        "d": "x"        // Duration of the ban
    },
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "modBan",
    "p": {
        "m": "SooYou",
        "mi": 3865819,
        "t": "kool_panda",
        "d": "h"
    },
    "s": "loves-kpop"
}]
```