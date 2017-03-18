# nameChangedRoom message

Event passed when an username is forcefully changed by plug.

**Note**: This only happens when you violate the terms of service.

### Packet Example

```js
[{
    "a": "nameChangedRoom", // Event name
    "p": {
      "i": 1234567890,
      "o": "xxx",   // previous username
      "n": "xxx"    // new username
    },
    "s": "xxxx"         // Room name
}]
```
### Real life example
```js
[{
    "a": "nameChangedRoom",
    "p": {
      "i": 25527728,
      "o": "Kill Yourself F****t",   // previous username
      "n": "Love Yourself Greatly"    // new username
    },
    "s": "bass-line"
}]
```
