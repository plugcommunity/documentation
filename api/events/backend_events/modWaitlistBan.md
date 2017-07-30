# modWaitlistBan message

Event passed when a moderator waitlist bans a user.

**Note**: the waitlist ban duration offers you the following four options

* **s**: Banned for 15 minutes

* **m**: Banned for an hour

* **l**: Banned for a day

* **f**: Banned for ever

### Packet Example

```js
[{
    "a": "modWaitlistBan", // Event name
    "p": {
        "m": "xxxxxx",	   // Name of the moderator
        "mi": -1,          // ID of the moderator
        "t": "xxxxxx",     // Name of the user that got banned
        "ti": -1,          // ID of the user that got banned
        "d": "x"           // Duration of the ban
    },
    "s": "xxxx"            // Room name
}]
```
### Real life example
```js
[{
    "a": "modWaitlistBan",
    "p": {
        "m": "SooYou",
        "mi": 3865819,
        "t": "xBytez",
        "ti": 3602201,
        "d": "h"
    },
    "s": "loves-kpop"
}]
```
