# modSkip message

Event passed when a moderator skips the current song.

### Packet Example

```js
{
    'a': 'modSkip',     // Event name
    'p': {
        'm': 'xxxxxx',	// Name of the moderator
        'mi': -1        // ID of the moderator
    },
    's': 'xxxx'         // Room name
}
```
### Real life example
```js
{
    'a': 'modSkip',
    'p': {
        'm': 'SooYou',
        'mi': 3865819
    },
    's': 'loves-kpop'
}
```