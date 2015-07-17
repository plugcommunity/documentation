# rooms/favorites Endpoint

The rooms/favorites endpoint requests metadata or modifies your favorite rooms list.

### Endpoints

**rooms/favorites**
**rooms/favorites?page=:page&limit=:limit**
**rooms/favorites/:slug**

### available verbs

_GET_, _POST_, _DELETE_

### Parameters for _GET_

**page**: Pagination, starts at page 1
**limit**: The amount of rooms that should be shown per page

### Data returned for _GET_

```js
{
    'data': [{                  // Contains the requested data
        'capacity': null,       // Maximum capacity of the room (it's null for most rooms but the most populated ones)
        'cid': 'xxx',           // ID of the room
        'dj': '',               // Username of the DJ
        'favorite': true,       // Is this room favorited by you?
        'format': 1,            // Site the media originates from (1 = youtube; 2 = soundcloud)
        'guests': 0,            // Amount of guests that are connected 
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

**id**: ID of the room you want to add to your favorites  

```json
{
    "id": -1
}
```

### Data returned for _POST_

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```

### URL Parameters

**id**: ID of the playlist you want to delete

>https://plug.dj/_/rooms/favorites/xxx

### Data returned for _DELETE_

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```