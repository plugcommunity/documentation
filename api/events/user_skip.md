# User Skipped Own Song

Event passed when the current DJ skips their song.

# Frontend

Event name: API.USER_SKIP

### Example Listener

```js
API.on(API.USER_SKIP, function(data){
    //This will log the packet of the event
    console.log(data);
});
```

### Packet Example

(Please add)

# Backend

Event Name: "skip"

### Packet Example

```js
[{
    "a": "skip",            // Event name
    "p": -1,                // ID of the user
    "s": "xxxx"             // Room name
}]
```
### Real life example
```js
[{
    "a": "skip",
    "p": 2348789,
    "s": "loves-kpop"
}]
```
