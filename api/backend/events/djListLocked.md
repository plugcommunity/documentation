# djListLocked message

Event passed containing the message that and administrator locked or unlocked the waitlist


### Packet Example

```js
{
    'a': 'djListLocked', // Event name
    'p': {
        'c': True, // Clear the wait or not
        'mi': xxxxxxxx, // User ID
        'f': True, // Ennables/ dissables the waitlist
        'm': 'xxxxxxxx' // User name
    }, 
    's': 'xxxxxxxx' // Room name
}
```
### Real example
```js
{
    'a': 'djListLocked', 
    'p': {
        'c': True, 
        'mi': 5113863, 
        'f': True, 
        'm': 'Houdhakker2'
    }, 
    's': 'houdhakker2-dj'
}
```

