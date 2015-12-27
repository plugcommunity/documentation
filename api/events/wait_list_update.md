# Wait List Update

This event happens when someone joins the wait list

# Frontend

Event Constant: API.WAIT_LIST_UPDATE

### Example Listener

```js
API.on(API.WAIT_LIST_UPDATE, function(data){
    //This will log the packet of the event
    console.log(data);
});
```

### Packet Example


```js
[
    {
        id: 0,
        username: '',
        avatarID: '',
        language: 'en',
        joined: undefined,
        level: 1,
        role: 0,
        gRole: 0,
        badge: undefined,
    }
]
```

Ordered array of users in the wait list.

# Backend

Event name: "djListUpdate"

### Packet Example

```js
[{
    "a": "djListUpdate",    // Event name
    "p": [-1, -1],          // WaitList as an array of user IDs
    "s": "xxxx"             // Room name
}]
```
### Real life example
```js
[{
    "a": "djListUpdate",
    "p": [2348789, 4930583],
    "s": "loves-kpop"
}]
```

'p' is an ordered list of the users in the wait list.

Index 0 is position 1 when relayed back to the user, as there is no position "0" when you translate to a user 
understandable number, aka the first person in the wait list.