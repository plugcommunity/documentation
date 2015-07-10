# Waitlist Update

This event happens when someone joins the waitlist

# Frontend

Event Constant: API.WAITLST_UPDATE

```js
[
    {
        id: 0,
        username: '',
        avatarID: '',
        language: 'en',
        joined: undefined,
        level: 1,
        role: 0,
        gRole: 0,
        status: 1,
        badge: undefined,
        vote: 0,
        grab: false,
        priority: 0,
        uIndex: undefined,
    },
]
```

Ordered array of users in the wait list.

# Backend

Event name: "djListUpdate"

``` js
{
	"a": "djListUpdate", 
	"p": [6124312, ... 6163797],
	"s": "thenightcoreclub"
}
```

'p' is an ordered list of the users in the wait list.

Index 0 is position 1 when relayed back to the user, as there is no position "0" when you translate to a user 
understandable language.