# plugUpdate message

Event passed when plug gets an update.

**Note**: This forces a refresh on the web app.

### Packet Example

```js
[{
    "a": "plugUpdate",  // Event name
    "p": {},
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "plugUpdate",
    "p": {},
    "s": "loves-kpop"
}]
```