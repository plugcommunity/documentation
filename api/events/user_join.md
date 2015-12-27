# User Join Event

Event passed when a user joins the room.

# Frontend

Event name: API.USER_JOIN

### Example Listener

```js
API.on(API.USER_JOIN, function(data){
    //This will log the packet of the event
    console.log(data);
});
```

### Packet Example

(Please add)

# Backend

Event Name: "userJoin"

### Packet Example

```js
[{
    "a": "userJoin",                // Event name
    "p": {                          // User object
        "avatarID": "xxx",          // AvatarID (e.g.: "base01")
        "username": "xxx",          // Name of the user  
        "language": "xx",           // ISO 639-1 representation of the language used by the user
        "guest": false,             // Is the user a guest? (this is not possible as of now)
        "level": 1,                 // Level of the user
        "role": 0,                  // Role of the user in this room
        "gRole": 0,                 // Global role of the user (0 = None; 3 = Brand Ambassador (BA); 5 = Admin)
        "joined": "xxxx",           // String representation of the time the user joined plug (e.g.: "2014-07-23 22:47:00.573000")
        "id": -1,                   // ID of the user
        "badge": "xxx",             // Badge of the user (e.g.: "80sb01")
        "slug": "xxx",              // URL conform representation of the user"s name (also used for the profile page)
        "sub": 0                    // Is the user a subscriber? (0 = false; 1 = true)
    },
    "s": "xxxx"                     // Room name
}]
```
### Real life example
```js
[{
    "a": "userJoin",
    "p": {
        "avatarID": "base01"
        "username": "SooYou",
        "language": "en",
        "guest": false,
        "level": 12,
        "role": 0,
        "gRole": 0,
        "joined": "2014-07-23 22:47:00.573000",
        "id": 3865819,
        "badge": "warrior01b",
        "slug": "sooyou",
        "sub": 0
    },
    "s": "loves-kpop"        
}]
```
