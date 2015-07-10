# Advance message

Event emitted containing the new playing song, when it starts

# Frontend

# Backend

### Packet Example

```js
{
    "a": "advance",             //Event Name
    "p": {
        "c": xxxxxxx,           // Current DJ
        "d": [                  // Other DJs in Waitlist
            xxxxxxx,
            xxxxxxx, 
            xxxxxxx
        ],                                          
        "h": "xxxxxxx-xxxxxxx-xxxxxxx-xxxxxxx",     // History ID
        "m": {
           //Media Object
        },
        "p": xxxxxxx,                       // Playlist ID
        "t": "2015-04-18 00:25:14.899831"   // Starting Timestamp
    }, 
    "s": "xxxxxx"                           //Room Name
}
```
### Real Example

```js
{
    "a": "advance", //Event Name
    "p": {
        c: 3364259, //Current DJ
        d: [ 
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
        h: '7ae868ed-798f-48df-8bff-d9c74a739d5a',
        m: { 
            author: 'Emancipator',
            format: 2,
            image: 'https://i1.sndcdn.com/artworks-000122623555-8gn05d-large.jpg',
            cid: '213829851',
            duration: 357,
            title: 'Dusk To Dawn (Frameworks Remix)',
            id: 296906716 
        },
        p: 7636199,
        t: '2015-07-09 21:59:01.809993' 
    }, 
    "s": "xxxxxx"
}    
```

Format is an integer, using 1 for YouTube and 2 for SoundCloud.

