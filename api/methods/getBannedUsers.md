# Get Banned Users

Returns an array containing the of banned users.

Must be manager or above, must have clicked the banned user list tab at least once since loading the page.

**Reason**: The reason member is set as a single number which represent the following reasons:

**1**: (SPAMMING) User spammed the chat

**2**: (VERBAL_ABUSE) User was harsh to other community members

**3**: (OFFENSIVE_VIDEOS) User was playing offensive media

**4**: (PLAYING_INAPPROPIATE_GENRES) User was playing inappropiate media repeatedly

**5**: (NEGATIVE_ATTITUDE) User was having a negative attitude towards others

**BanDuration**: The duration member can have the following values:

**f**: User is banned permanently

**d**: User is banned for a day

**h**: User is banned for an hour

### Code

```js
API.getBannedUsers();
```

### Response

```json
[
    {
        "timestamp": TIMESTAMP, 
        "id": 7120546, 
        "username": "ce3e1d30", 
        "moderator": "CakeBot", 
        "reason": 1, 
        "duration": "d"
    }
]
```

### Endpoint

[https://plug.dj/_/](/api/endpoints/.md)