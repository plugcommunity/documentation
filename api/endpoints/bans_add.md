# bans/add Endpoint

The bans/add endpoint enables you to ban a user.

**Note**: You need to have sufficient permissions in the room to access this resource.

**Reason**: The reason member is set as a single number which represent the following reasons:
**1**: (VIOLATING_COMMUNITY_RULES) User violated the community rules
**2**: (VERBAL_ABUSE) User was harsh to other community members
**3**: (SPAMMING) User spammed the chat
**4**: (OFFENSIVE_LANGUAGE) User was using offensive language
**5**: (NEGATIVE_ATTITUDE) User was having a negative attitude towards others

**BanDuration**: The duration member can have the following values:
**f**: User is banned permanently
**d**: User is banned for a day
**h**: User is banned for an hour

### Endpoint

**bans/add**

### available verbs

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

### Data returned

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```