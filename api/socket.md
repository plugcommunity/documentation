# Socket API

Realtime communication with plug.dj happens through the WebSocket server. In particular, every communication that is
initiated by plug.dj happens through the socket server, as well as sending chat messages.

Plug.dj sends information like users joining, chat messages coming in, and song advances over the socket API. As a
client, you can send authentication messages and chat messages.

## Connecting To The Socket Server

The socket server is a WebSocket server that lives at `wss://godj.plug.dj:443/socket`. The socket server is separated
from plug.dj's other servers, so you have to do a little bit of work to authenticate yourself to it.

(Domain trivia: `godj` stands for Go DJ, because the socket server is written in Go!)

These examples will assume JavaScript and Node.js, but the principles apply to every language/platform/library.

 1. First, you need to connect to the server. This is the easiest part&em;just use your favourite WebSocket library:
    ```js
    var WebSocket = require('ws');
    var socket = new WebSocket('wss://godj.plug.dj:443/socket', {
        origin: 'https://plug.dj'
    });
    ```
    As you may notice, though, there is a small caveat here: the socket server only accepts connections that originate
    from https://plug.dj. Browsers set the `Origin:` header automatically, but your websocket library may not! If you're
    having trouble connecting, check the documentation of your library on how to set the `Origin` header properly.

 1. Second, once the connection is complete, you need to send an authentication token to prove that you're you. You can
    obtain a token from the [`auth/token`](./endpoints/auth_token.md) endpoint. Sending this token to the server is
    described in [Sending Messages: `auth`](#auth).

Once you are connected and authenticated, you can start sending and receiving messages.

## Messages From Plug.dj

There are two types of messages that you might receive. One is the `h` message, the other is the Event message.
Everything is passed as strings, because that's what WebSockets do!

To listen for messages, you can use something akin to: (Node.js)

```js
var socket = getWebSocketConnectionSomehow();
socket.on('message', function (message) {
    // handle messages
});
```

### The `h` Message

The `h` message is simply that, a packet containing a one character string: `h`. Plug.dj occasionally sends these to make
sure that you're still alive. You don't have to respond to these packets at all, but you may want to keep track of them
anyway. If you don't get an `h` message for a very long time, you're probably no longer connected properly to the socket
server.

### Event Messages

Event Messages are JSON-encoded arrays containing one or more event objects. These events can be anything from a user
chatting or the DJ cycle setting changing to a plug.dj maintenance announcement (the latter being the most common!
:smile: ). For a list of socket events, see [events](./events) and [backend_events](./events/backend_events).

Because WebSockets only pass strings, you have to decode the messages yourself, probably using your favourite JSON
library.

An example message could look like:

```json
[
    {
        "a": "vote",
        "p": {
            "i": 8222444,
            "v": -1
        },
        "s": "tastycat"
    }
]
```

We can see that an event message has three cryptically named properties: `a`, `p` and `s`.

 * The `a` property is short for "action", but is also referred to as "event" or "type". This tells you what the event
   is all about. In the example, someone just `"vote"`'d for a song.
 * The `p` property is short for "parameter". The contents of this property depend on the "action". In the example, it's
   an object with a user ID and a vote value, but it can also be a number for some messages, or even `undefined`. Refer
   to the [events](./events) and [backend_events](./events/backend_events) pages for detailed documentation on every
   action/event, including their parameter.
 * The `s` property is short for "slug". This tells you which community the event happened in. It contains the room slug
   (the community URL without `https://plug.dj/`), or "dashboard" for events that don't have a community. Of course, you
   generally know which community you're in, so this property might seem superfluous. However, if you switch
   communities, sometimes it takes a few milliseconds for the socket server to catch up. In those cases, you might still
   receive some messages from the previous community you were in. For example, if you switch from a chillout room to a
   classical room right when the next song is about to start in the chillout room, you can still receive an "advance"
   message from the chillout room, even though you've joined the classical room. You can ignore that message by checking
   the `s` property.
   
   That might be a lot to swallow, so TL;DR: verify that the `s` property is "dashboard" or the current community slug
   before processing messages.

## Sending Messages

You can only send two types of messages to plug.dj: The "auth" and "chat" messages. They follow a format that's somewhat
similar to the Event Messages format, but in a plain JSON Object instead of a JSON array.

```json
{
    "a": "chat",
    "p": "My Chat Message",
    "t": 1437829673
}
```

The `a` and `p` properties again are short for "action" and "parameter". In both the "auth" and "chat" messages, the
parameter is just a string (an auth token or chat message contents). You don't need to send the room slug in chat
messages, because you can only be in a single room at a time--so plug.dj already knows where your message should go.

The `t` property is new: It's the UNIX time at which you sent your message. (In seconds, so if you're using JavaScript
you should divide by 1000 first: `Math.floor(Date.now() / 1000)`.) Theoretically, the plug.dj web app offsets this to be
close to the plug.dj server time using the `window._st` JavaScript variable, but it doesn't appear to affect much. For
now, you're safe just using your local UNIX time--or even completely bogus values like your birthday.

### "auth"

The "auth" message is the first message you should send to the socket, and you should send it _immediately_ when the
connection is set up. Plug.dj won't wait for you for long, so you can't open the socket and send your message ten
seconds later.

The parameter to this message is the auth token you got from the [`auth/token`](./endpoints/auth_token.md) endpoint.

An example auth message could look like:

```json
{
    "a": "auth",
    "p": "feod3wEqG4YxXJ+Y0xedVsuMdubvXnkbDXP27v8F2XNu8X4T8yzA2dJIXWxxzGKyLZSBpK0xVydaIh71cZ9TaUTtS6SzK89ZqU9UbuxY0TkPnFEyg9gReOISup4xBDvPDLjE+qJt2rV9qSK+TLvw8wsBqn1j6pDggE5arOZzUzRK",
    "t": 1437829673
}
```

Example in Node.js:

```js
socket.on('open', function () {
    var message = {
        a: 'auth',
        p: authTokenFromServer,
        t: Math.floor(Date.now() / 1000) // #CloseEnough
    };
    socket.send(JSON.stringify(message));
});
```

If your authentication was successful, you'll get an [`ack`](./events/backend_events/ack.md) message back from the
server.

### "chat"

Chat messages are a little more exciting, but also have a few more caveats to be aware of.

```json
{
    "a": "chat",
    "p": "Hello from the WebSocket! O/",
    "t": 1437829673
}
```

Note that chat is rate limited, and plug.dj will silently drop messages if you send too many too quickly. If you add a
1-second interval between messages on your end, you should be safe. (This is what the PlugAPI library does.) Plug.dj's
rate limiting actually isn't constant, so you can send messages a little more quickly if you use some sort of backoff
algorithm. (The Plugged library uses a linear backoff that allows it to semi-reliably send over 5 messages per second.)

You cannot send newline characters (`\n`) in your messages, and plug.dj will again silently drop your messages if you
attempt to. Instead, split them up into multiple consecutive messages.
