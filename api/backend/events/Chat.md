# Chat message

Event passed containing the message that a user has send


### Packet Example

```js
{
    "a": "chat", // Event name
    "p": {
        "cid":"xxxxxxx-xxxxxxxxxxxxxx", // The chat ID

        "message":"a", // the message with a max of 120 char

        "sub":0, // If the user is subed yes = 1 , no = 2

        "uid":xxxxxxx, // The user ID

        "un":"xxxxxxxx" // The name o the user
    },
    "s":"xxxxxxx" // Room name
}
```
### Real life example
```js

{
    "a":"chat", 
    "p":{
        "cid":"4769627-1429306171276",
        "message":"a",
        "sub":0,
        "uid":4769627,
        "un":"Houdhakker2"
    },
    "s":"thenightcoreclub"
}
```


