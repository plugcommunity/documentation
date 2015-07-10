# Ban message

Event passed containing the ban that happened


### Packet Example
```js
{
    "a": "ban", 
    "p": {
        "t": "xxx", // the type of ban 

        "d": "x", // the lenght of the ban
        
        "r": x // the reason of the ban
    }, 
    "s": "dashboard"
}
```

### Real life example
```js

{
    "a": "ban", 
    "p": {
        "t": "ban", 
        "d": "h", 
        "r": 1
    }, 
    "s": "dashboard"
}
```

