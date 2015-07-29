# User Leave Event

Event passed when a user leaves the room you are in.

# Frontend

Event name: API.USER_LEAVE

### Packet Example

(Please add)

### Example Listener

```js
API.on(API.USER_LEAVE, function(data){
    //This will log the packet of the event
    console.log(data);
});
```

# Backend

Event Name: "userLeave"

### Packet Example

```js
{
    'a': 'userLeave',       // Event name
    'p': -1,                // ID of the user
    's': 'xxxx'             // Room name
}
```
### Real life example
```js
{
    'a': 'userLeave',
    'p': 2348789,
    's': 'loves-kpop'
}
```
