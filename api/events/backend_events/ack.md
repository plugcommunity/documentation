# ack message

Event passed when your connection gets acknowledged by the websocket.


### Packet Example

```js
[{
    "a": "ack",            // Event name
    "p": 1,                // Is your connection working?
    "s": "xxxx"            // Room name
}]
```
### Real life example
```js
[{
    "a": "ack",
    "p": 1,
    "s": "loves-kpop"
}]
```
