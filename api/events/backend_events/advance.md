# advance message

Event passed when the booth advances.

### Example

```js
{
    'a': 'advance',             // Event name
    'p': {
        'd': [-1, -1],          // WaitList
        'c': -1,                // ID of the new DJ
        'h': 'xxxx',            // GUID v4 of the last playback object, also known as historyID
        'm': {
            'cid': 'xxx',       // Media ID used on the originating website
            'title': 'xxx',     // Media title
            'author': 'xxx',    // Media author
            'image': 'xxx',     // Thumbnail (youtube) or Artwork (soundcloud)
            'duration': 0,      // Duration in seconds
            'format': 1,        // Media format (1 = youtube; 2 = soundcloud)
            'id': -1            // Internal media ID
        },
        'p': -1,                // Playlist ID
        't': 'xxx'              // Timestamp of when the playback was
    },

    's': 'xxx'
}
```
### Real life example
```js
{
    'a': 'advance',
    'p': {
        'c': 3364259,
        'd': [5026821, 3709741],
        'h': '7ae868ed-798f-48df-8bff-d9c74a739d5a',
        'm': {
            'cid': '213829851',
            'title': 'Dusk To Dawn (Frameworks Remix)',
            'author': 'Emancipator',
            'image': 'https://i1.sndcdn.com/artworks-000122623555-8gn05d-large.jpg',
            'duration': 357,
            'format': 2,
            'id': 296906716
        },
        'p': 7636199,
        't': '2015-07-09 21:59:01.809993'
    },

    's': 'exampleRoom'
}
```

