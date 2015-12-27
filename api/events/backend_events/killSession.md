# killSession message

Event passed when the socket kills the connection to the room.


### Packet Example

```js
[{
    "a": "killSession", // Event name
    "p": {},            // Is empty
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "killSession",
    "p": {},
    "s": "loves-kpop"
}]
```