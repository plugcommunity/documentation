# Grab Update

Event emitted when a user grabs a track (Previously known as curated)

# Frontend

Event name: API.GRAB_UPDATE

### Example Listener

```js
API.on(API.GRAB_UPDATE, function(data){
    //This will log the packet of the event
    console.log(data);
});
```

### Packet Example

```js
{
    'user': {
        'id': 0,
        'username': 'xxx',
        'avatarID': 'xxx',
        'language': 'en',
        'joined': undefined,
        'level': 1,
        'role': 0,
        'gRole': 0,
        'badge': undefined
    }
}
```

Returns `Object.user` containing the user object of the person who 

# Backend

Event Name: "grab"

### Packet Example

```js
[{
    "a": "grab",            // Event name
    "p": -1,                // ID of the user
    "s": "xxxx"             // Room name
}]
```
### Real life example
```js
[{
    "a": "grab",
    "p": 2348789,
    "s": "loves-kpop"
}]
```