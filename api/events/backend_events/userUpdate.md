# userUpdate message

Event passed when a user changes their username, badge, avatar or reach the next level.

**Note**: Only the member that is relevant to the change is set, so it can only be i and level or i and avatarID, etc.

### Packet Example

```js
{
    'a': 'userUpdate',      // Event name
    'p': {
        'i': 'xxxxx',       // ID of user
        'level': -1,        // Level
        'avatarID': 'xxx',  // ID of the avatar used
        'username': 'xxx',  // Display name of the user
        'badge': 'xxx'      // Badge of the user
    }, 
    's': 'xxxx'             // Room name
}
```
### Real life example
```js
{
    'a': 'userUpdate',
    'p': {
        'i': 3865819,
        'level': 12,
        'avatarID': 'base01',
        'username': 'SooYou',
        'badge': '80sb01'
    }, 
    's': 'dashboard'
}
```