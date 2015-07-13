# Get Banned Users

Returns an array containing the of banned users.

Must be manager or above, must have clicked the banned user list tab at least once since loading the page.

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
        "reason": 0, 
        "duration": "d"
    }
]
```

### Endpoint

[https://plug.dj/_/](/api/endpoints/.md)