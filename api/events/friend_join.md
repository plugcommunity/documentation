# Friend join Event

Friend Join events are fired when a friend joins your current room.

# Frontend

Event name: API.FRIEND_JOIN

### Example Listener

```js
API.on(API.FRIEND_JOIN, function(data) {
    //This will log the packet of the chat event
    console.log(data);
});
```

### Packet Example

(Please add)

# Backend

Event name: "friendJoin"

### Example
```js

[{
    "a":"chat",                                     // Event name
    "p":{                                   
        "avatarID": "base01",                       // Their AvatarID (e.g.: "base01")
        "badge": "base01b",                         // Their badge (e.g.: "80sb01")
        "gRole": 0,                                 // Their service wide role (0 = None; 3 = Brand Ambassador (BA); 5 = Admin)
        "guest": false,                             // Is the user a guest?
        "id": 3865819,                              // Their ID
        "joined": "2014-07-23 22:47:00.573000",     // String representation of the time they joined plug (e.g.: "2014-07-23 22:47:00.573000")
        "language": "en",                           // ISO 639-1 representation of their used language
        "level": 12,                                // Their level
        "slug": "sooyou",                           // URL conform representation of their name (also used for the profile page)
        "sub": 0,                                   // Is the user a subscriber? (0 = false; 1 = true)
        "username": "SooYou",                       // Their username
    },
    "s":"loves-kpop"                                // Room name
}]
```