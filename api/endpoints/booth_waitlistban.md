# waitlistban Endpoint

The waitlistban endpoint retrieves a list of active waitlist bans, adds a waitlistban or deletes a waitlistban depending on HTTP method.

**Note**: You need to have sufficient permissions in the room to access this resource, otherwise you'll just be greeted
with a requestError status. The required permission for fetching is Manager (role 3), required permission for banning is Bouncer (role 2) unless you are permanently banning then you need Manager (role 3), required permission for deleting is Manager (role 3)


**Reason**: The reason member is set as a single number which represent the following reasons:

**1**: Spamming or trolling.

**2**: Verbal abuse or offensive languages.

**3**: Playing offensive videos/songs.

**4**: Repeatedly playing inappropiate genres.

**5**: Negative attitude.

**WaitlistBanDuration**: The duration member can have the following values:

**f**: User is banned permanently

**l**: User is banned for a day

**m**: User is banned for an hour

**s**: User is banned for 15 minutes

More ban information [here](/api/bans.md#variables).



### Endpoint

**booth/waitlistban**

**booth/waitlistban/:userID**

### Method

_POST_, _GET_, _DELETE_

### Parameters for _POST_

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


Wrong reason
```json
{
    "data": [
        "Not a valid ban reason"
    ],
    "status": "requestError",
}
```


Not in a room
```json
{
    "data": [
        "Not in a room"
    ],
    "status": "requestError",
}
```

Trying to permaban as bouncer
```json
{
    "data": [
        "Nice try buddy, bouncers can't perm ban"
    ],
    "status": "requestError",
}
```

Trying to ban an admin/BA
```json
{
    "data": [
        "That user is too powerful to ban"
    ],
    "status": "requestError",
}
```


Trying to ban someone higher ranked than you
```json
{
    "data": [
        "Cannot ban a >= ranking user"
    ],
    "status": "requestError",
}
```


Trying to ban as user
```json
{
    "data": [
        "Not a moderator"
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

### Data returned for _POST_

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```

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
        'duration': 'x',        // See WaitlistBanDuration above
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

### Parameters for _DELETE_

**userID**: ID of the user you want to unban

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