# Waitlist Update

This event happens when someone joins the waitlist

# Frontend

Event Constant: API.WAITLST_UPDATE

```js
[
    {      id: 0,
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

# Backend

Event name: "djListUpdate"

``` js
{
	"a": "djListUpdate", 
	"p": [6124312, ... 6163797], // the new dj list
	"s": "thenightcoreclub"
}
```