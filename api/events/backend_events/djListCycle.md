# djListCycle message

Event passed containing the message that and administrator put off/on the djCycle

### Packet Example

```js
    "a": "djListCycle", // Event name
    "p": {
        "f": False,     // Should the wait list cycle?
        "mi": xxxxxxx,  // User ID
        "m": "xxxxxxx"  // User name
    },  
    "s": "xxxxxxx"      // Room name
}
```
### Real example
```js
{
    "a": "djListCycle",
    "p": {
        "f": False, 
        "mi": 1235782, 
        "m": "Nanzan"
    },  
    "s": "thenightcoreclub"
}
```
