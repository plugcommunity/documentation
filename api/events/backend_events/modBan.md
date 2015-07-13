# modBan message

Event passed when a moderator bans a user.

**Note**: the ban duration offers you the following three options

* **h**: Banned for an hour
* **d**: Banned for a day
* **f**: Banned for ever

### Example

```js
{
    "a": "modBan",              // Event name
    "p": {
        "t": "Arne",            // User name
        "d": "h",               // Reason of ban 
        "m": "Houdhakker2",     // Moderator name
        "mi": 5113863           // ID moderator 
    }, 
    "s": "thenightcoreclub"
}
```
