# users/settings Endpoint

The users/settings endpoint enables you to save your settings.

### Endpoint

**users/settings**

### Method

_PUT_

### Parameters

**videoOnly**: Should only the video be shown?

**chatTimestamps**: Format of the timestamp (**12** or **24**)

**emoji**: Should emojis be shown?

**tooltips**: Should tooltips be shown?

**chatImages**: Should chat images be shown?

**notifyDJ**: Should DJ notifications be shown?

**notifyScore**: Should score notifications be shown?

**notifyFriendJoin**: Should friend join notifications be shown?

**nsfw**: Should rooms that are flagged as not safe for work be listed?

**friendAvatarsOnly**: Should only the avatars of your friends be shown?

```json
{
    "videoOnly": false,
    "chatTimestamps": 12,
    "emoji": true,
    "tooltips": true,
    "chatImages": true,
    "notifyDJ": true,
    "notifyScore": true,
    "notifyFriendJoin": true,
    "nsfw": false,
    "friendAvatarsOnly": false,
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

Missing fields
```json
{
    "data": [
        "At least 1 of these fields is required: videoOnly, chatTimestamps, emoji, tooltips, chatImages, notifyDJ, notifyScore, notifyFriendJoin, nsfw, friendAvatarsOnly"
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