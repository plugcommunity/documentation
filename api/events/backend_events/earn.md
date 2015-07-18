# earn message

Event passed when the user earns some xp.

The XP system is used to level up in plug.

### Packet Example
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

