# plugMaintenanceAlert message

Event passed when plug is about to go into maintenance mode.

### Packet Example

```js
[{
    "a": "plugMaintenanceAlert",    // Event name
    "p": -1,                        // Time remaining in minutes
    "s": "xxxx"                     // Room name
}]
```
### Real life example
```js
[{
    "a": "plugMaintenanceAlert",
    "p": 15,
    "s": "loves-kpop"
}]
```