# djListLocked message

<<<<<<< HEAD
Event passed when a moderator decides whether the wait list should be locked or not
=======
Event passed containing the message that and administrator locked or unlocked the waitlist
>>>>>>> ff85781228228136d48a3ea13c9fd95eb5dcbd11


### Packet Example

```js
{
<<<<<<< HEAD
    'a': 'djListLocked',    // Event name
    'p': {
        'c': false,	        // Should the wait list be cleared?
        'f': false,         // Should the wait list be locked?
        'm': '',		    // Name of the moderator that triggered this event
        'mi': -1            // ID of the moderator
    },
    's': 'xxxx'             // Room name
}
```
### Real life example
```js
{
    'a': 'djListLocked',
    'p': {
        'c': false,
        'f': false,
        'm': 'SooYou',
        'mi': 3865819
    },
    's': 'loves-kpop'
}
```
=======
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

>>>>>>> ff85781228228136d48a3ea13c9fd95eb5dcbd11
