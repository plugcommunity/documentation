# earn message

<<<<<<< HEAD
Event passed when the user earns some xp.

The XP system is used to level up in plug.


### Packet Example

```js
{
    'a': 'earn',        // Event name
    'p': {
        'xp': 0,	    // xp generated
        'level': -1     // current level
    },
    's': 'xxxx'         // Room name
}
```
### Real life example
```js
{
    'a': 'earn',
    'p': {
        'xp': 386,
        'level': 2
    },
    's': 'loves-kpop'
}
```
=======
Event passed when you earn experiance or plug points.


### Example

```js
{
	"s": "dashboard", 	// Source
	"a": "earn",  		// Evnet name
	"p": {				
		"level": 12, 	// Level of user
		"xp": 45365, 	// Experience of user
		"pp": 73676		// Plug points of user
	}
}
```

>>>>>>> ff85781228228136d48a3ea13c9fd95eb5dcbd11
