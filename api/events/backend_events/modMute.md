# modMute message

Event passed when a moderator mutes a user.

**Note**: The mute duration offers you 4 different options:

* **o**: None, the user is unmuted

* **s**: Short, the user is muted for 15 minutes

* **m**: Medium, the user is muted for 30 minutes

* **l**: Long, the user is muted for 45 minutes

### Packet Example

```js
[{
    "a": "modMute",     // Event name
    "p": {
        "m": "xxxxxx",	// Name of the moderator
        "i": -1,        // ID of the user
        "t": "xxxxxx",  // Name of the user that got muted
        "r": -1,        // Reason of the mute
        "d": "x",       // Mute duration
    },
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "modMute",
    "p": {
        "m": "SooYou",
        "i": 3865820,
        "t": "kool_panda",
        "r": 31,
        "d": "m"
    },
    "s": "loves-kpop"
}]
```