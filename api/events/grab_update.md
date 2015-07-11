# Grab Update

Event emitted when a user grabs a track (Previously known as curated)

# Frontend

Event name: API.GRAB_UPDATE

### Example

```js
{
    user: {
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
}
```

Returns `Object.user` containing the user object of the person who 

### Example Listener

```js
API.on(API.GRAB_UPDATE, function(data){
    //This will log the packet of the event
    console.log(data);
});
```

# Backend

Event Name: "grab"

### Example
```js
{
    "s": "thenightcoreclub", // Source of event
    "a": "grab",             // Event name
    "p": 5113863             // User who grabed
}
```

