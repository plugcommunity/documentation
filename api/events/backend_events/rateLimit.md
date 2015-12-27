# rateLimit message

Event passed when chat enters slow mode.

### Packet Example

```js
[{
    "a": "rateLimit",   // Event name
    "p": {},
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "rateLimit",
    "p": {},
    "s": "loves-kpop"
}]
```