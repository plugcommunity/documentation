# Advance message

Event passed containing the new playing song, when it starts


### Packet Example

```js
{
    "a": "advance", //Event Name
    "p": {
        "c": xxxxxxx, // Current DJ
        
        "d": [
            xxxxxxx,
            xxxxxxx, 
            xxxxxxx
        ], // Other DJs in Waitlist
        
        "h": "xxxxxxx-xxxxxxx-xxxxxxx-xxxxxxx", // History ID
        
        "m": {
            //Media Object
        },
        
        "p": xxxxxxx, // Playlist ID
        
        "t": "2015-04-18 00:25:14.899831" // Starting Timestamp
    }, 
    "s": "xxxxxx" //Room Name
}
```

##### Media Object

```js
{ 
    author: 'xxxxxxxx',
    format: 1,
    image: 'https://xxxxxxx.com/xxxxxxxxxxxxxxxx.jpg',
    cid: 'xxxxxxxx',
    duration: 000,
    title: 'xxxxxxxxxxxxxxxxxx',
    id: xxxxxxxx 
}
```

Format is variable using the value 1 for YouTube, and 2 for SoundCloud.

