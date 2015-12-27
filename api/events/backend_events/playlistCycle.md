# playlistCycle message

Event passed when your playlist cycles (you finish playing a song from your playlist).

### Packet Example

```js
[{
    "a": "playlistCycle",   // Event name
    "p": -1,                // ID of activated playlist
    "s": "xxxx"             // Room name
}]
```
### Real life example
```js
[{
    "a": "playlistCycle",
    "p": 329847,
    "s": "loves-kpop"
}]
```