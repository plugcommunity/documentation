# earn message

Event passed when the user earns some xp.

The XP system is used to level up in plug.


### Packet Example

```js
{
    "a": "earn",        // Event name
    "p": {
        "xp": 0,	    // xp generated
        "level": -1     // current level
    },
    "s": "xxxx"         // Room name
}
```
### Real life example
```js
{
    "a": "earn",
    "p": {
        "xp": 386,
        "level": 2
    },
    "s": "loves-kpop"
}
```