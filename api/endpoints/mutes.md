# mutes Endpoint

The mutes endpoint modifies the current mutes.

**Note**: You need to have sufficient permissions in the room to access this resource, otherwise you'll just be greeted
with a requestError message.

**Reason**: The reason member is set as a single number which represent the following reasons:

**1**: (VIOLATING_COMMUNITY_RULES) User violated the community rules

**2**: (VERBAL_ABUSE) User was harsh to other community members

**3**: (SPAMMING) User spammed the chat

**4**: (OFFENSIVE_LANGUAGE) User was using offensive language

**5**: (NEGATIVE_ATTITUDE) User was having a negative attitude towards others

**MuteDuration**: The duration member can have the following values:

**s**: User is muted for 15 minutes

**m**: User is muted for 30 minutes

**l**: User is muted for 45 minutes

### Endpoint

**mutes**

**mutes/:userID**

### Methods

_GET_, _POST_, _DELETE_

### Possible error messages for _GET_

Insufficient permissions

```json
{
    "data": [
        "You are not authorized to access this resource."
    ],
    "status": "notAuthorized",
}
```

### Data returned for _GET_

```js
{
    'data': [{                  // Contains the requested data
        'expires': 0,           // Duration in seconds
        'moderator': 'xxxx',    // Name of the moderator
        'reason': 1,            // Reason why they got muted
        'id': -1,               // ID of the user
        'username': 'xxxx'      // Name of the user
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```

### Parameters for _POST_

**userID**: ID of the user you want to mute

**reason**: The reason of the mute

**duration**: The duration of the mute

```json
{
    "userID": -1,
    "reason": 1,
    "duration": "x"
}
```

### Possible error messages for _POST_

Insufficient permissions
```json
{
    "data": [
        "You are not authorized to access this resource."
    ],
    "status": "notAuthorized",
}
```

userID or reason is missing
```json
{
    "data": [
        "xxxxxxxx is required"
    ],
    "status": "requestError",
}
```

### Data returned for _POST_

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```

### Parameters for _DELETE_

**userID**: ID of the user you want to unmute

### Possible error messages for _DELETE_

Insufficient permissions
```json
{
    "data": [
        "You are not authorized to access this resource."
    ],
    "status": "notAuthorized",
}
```

### Data returned for _DELETE_

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```