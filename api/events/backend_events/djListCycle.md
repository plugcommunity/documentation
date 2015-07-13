# djListCycle message

<<<<<<< HEAD
Event passed when a moderator decides whether the wait list should cycle or not
=======
Event passed containing the message that and administrator put off/on the djCycle
>>>>>>> ff85781228228136d48a3ea13c9fd95eb5dcbd11


### Packet Example

```js
{
<<<<<<< HEAD
    'a': 'djListCycle', // Event name
    'p': {
        'f': false,	    // Should the wait list cycle?
        'm': '',		// Name of the moderator that triggered this event
        'mi': -1        // ID of the moderator
    },
    's': 'xxxx'         // Room name
}
```
### Real life example
```js
{
    'a': 'djListCycle',
    'p': {
        'c': false,
        'm': 'SooYou',
        'mi': 3865819
    },
    's': 'loves-kpop'
}
```
=======
    "a": "djListCycle", // Event name
    "p": {
        "f": False, // DJCycle is on or not
        "mi": xxxxxxx, // User ID
        "m": "xxxxxxx" // User name
    },  
    "s": "xxxxxxx" // Room name
}
```
### Real example
```js
{
    "a": "djListCycle",
    "p": {
        "f": False, 
        "mi": 1235782, 
        "m": "Nanzan"
    },  
    "s": "thenightcoreclub"
}
```

>>>>>>> ff85781228228136d48a3ea13c9fd95eb5dcbd11
