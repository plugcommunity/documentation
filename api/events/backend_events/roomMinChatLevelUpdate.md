# roomMinChatLevel message

Event passed when a staff member changes the minimum chat level.

### Packet Example

```js
[{
    "a": "roomMinChatLevel",    // Event name
    "p": {
        "m": -1,                // Min chat level
        "u": -1                 // ID of moderator
    }, 
    "s": "xxxx"                 // Room name
}]
```
### Real life example
```js
[{
    "a": "roomMinChatLevel",
    "p": {
        "m": 2,
        "u": 3865819
    }, 
    "s": "loves-kpop"
}]
```