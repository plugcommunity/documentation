# earn message

Event passed when the user earns some **xp** (experience points) and **pp** (plug points).

The XP system is used to level up in plug; plug points can be used to buy avatars, badges, etc.

Note: on plug.dj, only the XP since the last level-up are shown, not the internally used total XP.

The room slug will always be "dashboard", because this event is not room-specific.


### Packet Example

```js
[{
    "a": "earn",        // Event name
    "p": {
        "xp": 0,	    // new xp amount
        "pp": 0,	    // new pp amount
        "level": -1     // current level (or new level, on level-up)
    },
    "s": "dashboard"    // Room slug
}]
```
### Real life example
```js
[{
    "a": "earn",
    "p": {
        "pp":177858,
        "xp":130870,
        "level":16
    },
    "s": "dashboard"
}]
```
