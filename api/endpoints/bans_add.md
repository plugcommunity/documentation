# bans/add Endpoint

The bans/add endpoint enables you to ban a user.

**Note**: You need to have sufficient permissions in the room to access this resource.


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

More ban information [here](/api/bans.md#variables).



### Endpoint

**bans/add**

### Method

_POST_

### Parameters

**userID**: ID of the user you want to move

**reason**: The reason why the user got banned

**duration**: The duration of the ban

```json
{
    "userID": -1,
    "reason": 1,
    "duration": "x"
}
```

### Possible error messages

Insufficient permissions
```json
{
    "data": [
        "You are not authorized to access this resource."
    ],
    "status": "notAuthorized",
}
```

Wrong userID
```json
{
    "data": [],
    "status": "requestError",
}
```

Wrong duration time
```json
{
    "data": [
        "Not a valid ban duration"
    ],
    "status": "requestError",
}
```

reason or userID is missing
```json
{
    "data": [
        "xxxxxxxx is required"
    ],
    "status": "requestError",
}
```

### Data returned

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```