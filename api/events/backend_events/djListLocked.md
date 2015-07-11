# djListLocked message

Event passed when a moderator decides whether the waitlist should be locked or not


### Packet Example

```js
{
    'a': 'djListLocked',    // Event name
    'p': {
        'c': false,	        // Should the waitlist be cleared?
        'f': false,         // Should the waitlist be locked?
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