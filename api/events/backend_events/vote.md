# vote message

Event passed when a user votes for a song.


### Packet Example

```js
[{
    "a": "vote",            // Event name
    "p": {
        "i": -1,            // ID of the user
        "v": 1,             // Direction of the vote (1 = woot; -1 = meh)
    },
    "s": "xxxx"             // Room name
}]
```
### Real life example
```js
[{
    "a": "vote",
    "p": {
        "i": 234098,
        "v": 1
    },
    "s": "loves-kpop"
}]
```
