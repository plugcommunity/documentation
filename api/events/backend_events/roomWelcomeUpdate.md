# roomWelcomeUpdate message

Event passed when a co-host or host updates the room's welcome message.

### Packet Example

```js
[{
    "a": "roomWelcomeUpdate",       // Event name
    "p": {
        "w": "xxxxx",               // Welcome message
        "u": -1                     // ID of moderator
    }, 
    "s": "xxxx"                     // Room name
}]
```
### Real life example
```js
[{
    "a": "roomWelcomeUpdate",
    "p": {
        "w": "Test Welcome",
        "u": 3865819
    }, 
    "s": "loves-kpop"
}]
```