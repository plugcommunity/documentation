# Socket API

Realtime communication with plug.dj happens through the WebSocket server. In particular, every communication that is
initiated by plug.dj happens through the socket server, as well as sending chat messages.

Plug.dj sends information like users joining, chat messages coming in, and song advances over the socket API. As a
client, you can send authentication messages and chat messages.

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

The `h` message is literally just that&em;a packet containing one byte: `h`. Plug.dj occasionally sends these to make
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
   is all about. In the example, someone just `"vote"`d for a song.
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
