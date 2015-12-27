# notify message

Event passed when you receive a notification.

### Packet Example

```js
[{
    "a": "notify",          // Event name
    "p": {
        "action": "xxx",    // Type of the notification
        "id": -1,           // Internal ID
        "timestamp": "xxx", // Date when the notification triggered
        "value": "x"        // Value carried with the notification
    },
    "s": "xxxx"             // Room name
}]
```
### Real life example
```js
[{
    "a": "notify",
    "p": {
        "action": "levelUp",
        "id": 34798283,
        "timestamp": "2014-07-23 22:47:00.573000",
        "value": "12"
    },
    "s": "loves-kpop"
}]
```