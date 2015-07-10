# Chat message

Event passed containing the message that a user sended


### Packet Example

```js
{
    "a":"chat", // Event name
    "p":{
        "cid":"xxxxxxx-xxxxxxxxxxxxx", // Chat ID

        "message":"xxxxxxx", // Message

        "sub":0, // Subbed or not

        "uid":xxxxxxx, // User ID

        "un":"xxxxxxx" // User name
    },
    "s":"xxxxxxx" // Room name
}

```
### Real example
```js

{
    "a":"chat",
    "p":{
        "cid":"4769627-1429306171276",
        "message":"a",
        "sub":0,
        "uid":4769627,
        "un":"OokamiHolo"
    },
    "s":"thenightcoreclub"
}
```

