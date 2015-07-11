# Vote

This event happens when a user votes using the woot or meh buttons (Or via the API)

# Frontend

Event name: API.VOTE_UPDATE

### Example

```js
{
    vote: 1,
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

Where vote is the value of the user vote:

| Vote Value | Name |
| ---------- | ---- |
| 1          | Woot |
| -1         | Meh  |

User is the user object of the person that voted.

### Code Example

```js
API.on(API.VOTE_UPDATE, function(data){
    console.log(data);
});
```

# Backend

Event Name: "vote"

### Example

```js
{
    "a": "vote", 
    "p": {
        "i": 5113863,           // User ID
        "v": 1                  // Value: (1 for woot -1 for meh)
    }, 
    s": "thenightcoreclub"
}
```