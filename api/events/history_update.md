# History Update

This is a **frontend only** event. It is a result of the getHistory method, which is obtained when DJ_ADVANCE is fired.

Event name: API.HISTORY_UPDATE

### Example Listener

```js
API.on(API.HISTORY_UPDATE, function(data){
    //This will log the packet of the event
    console.log(data);
});
```

### Packet Example

```js
[
	0: {
		media: {
			author: '',     // Author of the track
			cid: 'x',       // Internal ID
			duration: 0,    // Song duration (seconds)
			format: 1,      // 1: Youtube 2: Soundcloud
			id: '0',        // Please add description (will always be '0')
			image: '',      // Image URL of the track cover for soundcloud, video thumbnail for youtube
			title: ''       // Title of the track
		},
		score: {
			grabs: 0,
			listeners: 0,
			negative: 0,
			positive: 0
		},
		user: {
			id: 0,
			username: ''
		}
	},
	// ...
]
```
