# nameChanged message

Event passed when your username is forcefully changed by plug.

**Note**: This only happens when you violate the terms of service.

### Packet Example

```js
[{
    "a": "nameChanged", // Event name
    "p": {},
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "nameChanged",
    "p": {},
    "s": "loves-kpop"
}]
```