# bans Endpoint

The bans endpoint retrieves a list of active bans.

**Note**: You need to have sufficient permissions in the room to access this resource, otherwise you'll just be greeted
with a requestError status.

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

**bans**

### available verbs

_GET_

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

### Data returned

```js
{
    'data': [{                  // Contains the requested data
        'duration': 'x',        // See BanDuration above
        'moderator': 'xxxx',    // Name of the moderator
        'reason': 1,            // Reason why they got banned. See BanReason above
        'id': -1,               // ID of the user
        'timestamp': 'xxx',     // Date when the ban became active
        'username': 'xxxx'      // Name of the user
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```