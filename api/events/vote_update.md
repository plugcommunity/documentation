# Vote Updates

Event passed when a user votes for a song.

This is usually done via the frontend, where the user clicks the `woot` or `meh` buttons.

If you grab a song, it will automatically `woot` a track if you have not done so already. (Frontend)

If you grab via the Song History window, you will not show up as grabbing the track.

# Frontend

Event name: API.VOTE_UPDATE

### Example Listener

```js
API.on(API.VOTE_UPDATE, function(data){
    console.log(data);
});
```

### Packet Example

```js
{
    'vote': 1,
    'user': {
        'id': 0,
        'username': '',
        'avatarID': '',
        'language': 'en',
        'joined': undefined,
        'level': 1,
        'role': 0,
        'gRole': 0,
        'badge': undefined,
    }
}
```

Where vote is the value of the user vote:

| Vote Value | Name |
| ---------- | ---- |
| 1          | Woot |
| -1         | Meh  |

User is the user object of the person that voted.

# Backend

Event Name: "vote"

### Packet Example

```js
[{
    "a": "vote",            // Event name
    "p": {
        "i": -1,            // ID of the user
        "v": 1,             // Direction of the vote (1 = woot; -1 = meh)
    },
    "s": "xxxx"             // Room name
}]
```
### Real life example
```js
[{
    "a": "vote",
    "p": {
        "i": 234098,
        "v": 1
    },
    "s": "loves-kpop"
}]
```