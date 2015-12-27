# djListLocked message

Event passed when a moderator decides whether the wait list should be locked or not.


### Packet Example

```js
[{
    "a": "djListLocked",    // Event name
    "p": {
        "c": false,	        // Should the wait list be cleared?
        "f": false,         // Should the wait list be locked?
        "m": "",		    // Name of the moderator that triggered this event
        "mi": -1            // ID of the moderator
    },
    "s": "xxxx"             // Room name
}]
```
### Real life example
```js
[{
    "a": "djListLocked",
    "p": {
        "c": false,
        "f": false,
        "m": "SooYou",
        "mi": 3865819
    },
    "s": "loves-kpop"
}]
```