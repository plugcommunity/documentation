# Get History

Returns the history list of previously played songs.

### Code

```js
API.getHistory();
```

### Response

```js
[
    {
        media: {
            author: "Sleep Party People",
            cid: "aFUzvbkEvRk",
            duration: 441,
            format: 1,
            id: "0",
            image: "//i.ytimg.com/vi/aFUzvbkEvRk/default.jpg",
            title: "I'm Not Human At All",
        },
        score: {
            grabs: 0,
            listeners: 47,
            negative: 0,
            positive: 11
        },
        user: {
            id: 80,
            username: '',
            avatarID: '',
            language: 'en',
            joined: undefined,
            level: 1,
            role: 0,
            gRole: 0,
            badge: undefined,
        }
    }
]
```

### Endpoint

[https://plug.dj/_/](/api/endpoints/.md)