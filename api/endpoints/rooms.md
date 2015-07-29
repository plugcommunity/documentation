# rooms Endpoint

The rooms endpoint retrieves all rooms in a sorted list ordered by the amount of people that are connected or creates a room via _POST_.

### Endpoint

**rooms**

**rooms?q=:query&page=:page&limit=:limit**

### Methods

_GET_, _POST_

### Parameters

**q**: Search query used to filter the rooms

**page**: Pagination, starts at page 1

**limit**: The amount of rooms that should be shown per page

### Data returned for _GET_

```js
{
    'data': [{                  // Contains the requested data
        'capacity': null,       // Maximum capacity of the room (it's null for most rooms but the most populated ones)
        'cid': 'xxx',           // ID of the room
        'dj': 'xxx',            // Name of the DJ
        'favorite': false,      // Is this room favorited by you?
        'format': 1,            // Site the media originates from (1 = youtube; 2 = soundcloud)
        'guests': 0,            // Amount of guests connected to the room
        'host': 'xxx'           // Name of the host
        'id': 'xxx'             // ID of the room
        'image': 'xxx.jpg',     // Thumbnail
        'media': 'xxx',         // Author and Title of the media being played
        'name': 'xxx',          // Name of the room
        'nsfw': false,          // Is the room flagged as inappropiate? (can not be set manually)
        'population': 0,        // Current population of the room
        'slug': 'xxx'           // URL conform representation of the room's name
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```

### Parameters for _POST_

**name**: Name of your new community

**private**: Should this community be private? (this means that the room won't be listed in the public listing)  

```json
{
    "name": "xxx",
    "private": false
}
```

### Possible error messages

Insufficient permissions (not being logged in)
```json
{
    "data": [
        "You are not authorized to access this resource."
    ],
    "status": "notAuthorized",
}
```

name or private is missing
```json
{
    "data": [
        "xxxxxxxx is required"
    ],
    "status": "requestError",
}
```

### Data returned for _POST_

```js
{
    'data': [{                  // Contains the requested data
      "id": -1,                 // Internal room ID
      "name": "xxx",            // Name of the room (same as the name you sent via post)
      "slug": "xxx"             // URL conform representation of the room's name
    }],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```