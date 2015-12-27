# Song Score Update

Event Fired when the value of `woots`, `mehs` or `grabs` changes.

This is a **frontend only** event, where the value of the 'vote' and 'grabs' event is aggregated.

Event name: API.SCORE_UPDATE

### Example Listener

```js
API.on(API.SCORE_UPDATE, function(data){
    //This will log the packet of the event
    console.log(data);
});
```

### Packet Example

```js
[{
    "positive": 17, 
    "negative": 0, 
    "grabs": 0
}]
```