# killSession message

<<<<<<< HEAD
Event passed when the socket kills the connection to the room.


### Packet Example

```js
{
    'a': 'killSession', // Event name
    'p': {},            // Is empty
    's': 'xxxx'         // Room name
}
```
### Real life example
```js
{
    'a': 'killSession',
    'p': {},
    's': 'loves-kpop'
}
```
=======
Event passed when you need to relogin. This happens when you are banned, open another client on the same account, ...


### Example

```js
{
	"a":"killSession", // Event name
	"s":"dashboard"    // Source event
}
```

>>>>>>> ff85781228228136d48a3ea13c9fd95eb5dcbd11
