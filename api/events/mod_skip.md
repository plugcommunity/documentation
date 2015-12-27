# Moderator Skip

Event passed when a moderator skips the current song.

# Frontend

Event name: API.MOD_SKIP

### Example Listener

```js
API.on(API.MOD_SKIP, function(data){
    //This will log the packet of the event
    console.log(data);
});
```

### Packet Example

(Please add)

# Backend

Event Name: "modSkip"

### Packet Example

```js
[{
    "a": "modSkip",     // Event name
    "p": {
        "m": "xxxxxx",  // Name of the moderator
        "mi": -1        // ID of the moderator
    },
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "modSkip",
    "p": {
        "m": "SooYou",
        "mi": 3865819
    },
    "s": "loves-kpop"
}]
```

