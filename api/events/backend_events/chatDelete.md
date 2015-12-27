# ChatDelete message

Event passed containing information about a message that was deleted by staff.


### Packet Example

```js
[{
    "a": "chatDelete",                  // Event name
    "p": {
        "c": "xxxxxxx-xxxxxxxxxxxxx",   // Message ID
        "mi": -1                        // ID of user who removed the message
    },
    "s": "xxxx"                         // Room name
}]
```
### Real life example
```js
[{
    "a": "chatDelete",
    "p": {
        "c": "8009977-1436517063257",
        "mi": 5113863
    },
    "s": "thenightcoreclub"
}]
```
