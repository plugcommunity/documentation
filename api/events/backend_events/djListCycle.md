# djListCycle message

Event passed when a moderator decides whether the wait list should cycle or not.


### Packet Example

```js
[{
    "a": "djListCycle", // Event name
    "p": {
        "f": false,	    // Should the wait list cycle?
        "m": "",		// Name of the moderator that triggered this event
        "mi": -1        // ID of the moderator
    },
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "djListCycle",
    "p": {
        "c": false,
        "m": "SooYou",
        "mi": 3865819
    },
    "s": "loves-kpop"
}]
```