# DJ/Song Advance

Event emitted containing the new playing song, when it starts

# Frontend

Event name: API.ADVANCE

### Example Listener

```js
API.on(API.ADVANCE, function(data){
    //This will log the packet of the event
    console.log(data);
});
```

### Packet Example

```js
{
    dj: {
        id: 0,
        username: '',
        avatarID: '',
        language: 'en',
        joined: undefined,
        level: 1,
        role: 0,
        gRole: 0,
        badge: undefined
    },
    media: {                                    // Media object
        'cid': 'xxx',                           // Media ID used on the originating website
        'title': 'xxx',                         // Media title
        'author': 'xxx',                        // Media author
        'image': 'xxx',                         // Thumbnail (youtube) or Artwork (soundcloud)
        'duration': 0,                          // Duration in seconds
        'format': 1,                            // Media format (1 = youtube; 2 = soundcloud)
        'id': -1                                // Internal media ID
    },
    lastPlay: {
        dj: {UserObject},
        media: {MediaObject},
        score: {ScoreObject}
    }
}
```

# Backend

Event Name: "advance"

### Packet Example

```js
[{
    "a": "advance",                                 // Event Name
    "p": {
        "c": -1,                                    // Current DJ
        "d": [                                      // Other DJs in Wait List
            -1,
            -1, 
            -1
        ],                                          
        "h": "xxxxxxx-xxxx-4xxx-xxxx-xxxxxxx",      // GUID v4 History ID
        "m": {                                      // Media object
            "cid": "xxx",                           // Media ID used on the originating website
            "title": "xxx",                         // Media title
            "author": "xxx",                        // Media author
            "image": "xxx",                         // Thumbnail (youtube) or Artwork (soundcloud)
            "duration": 0,                          // Duration in seconds
            "format": 1,                            // Media format (1 = youtube; 2 = soundcloud)
            "id": -1                                // Internal media ID
        },
        "p": -1,                                    // Playlist ID
        "t": "2015-04-18 00:25:14.899831"           // Starting Timestamp
    }, 
    "s": "xxxxxx"                                   // Room Name
}]
```
### Real Example

```js
[{
    "a": "advance",                                 // Event Name
    "p": {
        "c": 3364259,                               // Current DJ
        "d": [ 
            5026821,
            3709741,
            6202663,
            7699695,
            7815917,
            4521658,
            3756094,
            4017378,
            5825568,
            3681464,
            4797515,
            4609304,
            4366591,
            4014293,
            3842247,
            4175640 
        ],
        "h": "7ae868ed-798f-48df-8bff-d9c74a739d5a",
        "m": { 
            "author": "Emancipator",
            "format": 2,
            "image": "https://i1.sndcdn.com/artworks-000122623555-8gn05d-large.jpg",
            "cid": "213829851",
            "duration": 357,
            "title": "Dusk To Dawn (Frameworks Remix)",
            "id": 296906716 
        },
        "p": 7636199,
        "t": "2015-07-09 21:59:01.809993" 
    }, 
    "s": "xxxxxx"
}]
```

Format is an integer, using 1 for YouTube and 2 for SoundCloud.

