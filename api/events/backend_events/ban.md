# Ban message

Event passed when you are banned from a room.

**Note**: the ban duration offers you the following three options:

* **h**: Banned for an hour

* **d**: Banned for a day

* **f**: Banned forever

### Example

```js
[{
    "a": "ban",         // Event name
    "p": {
        "t": "ban",
        "d": "x",       // Duration
        "r": -1         // Reason
    },

    "s": "dashboard"
}]
```
### Real life example
```js
[{
    "a": "ban",
    "p": {
        "t": "ban",
        "d": "h",
        "r": 1
    },

    "s": "dashboard"
}]
```

