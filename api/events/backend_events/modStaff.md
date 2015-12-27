# modStaff message

Event passed when a moderator sets a user as staff member.

**Note**: There"s five roles of which you can choose

* **0**: None, just a regular user

* **1**: ResidentDJ, can lock the wait list

* **2**: Bouncer, can delete chat messages, remove DJs, force skip and ban people

* **3**: Manager, can everything except removing co hosts and managers as well as editing the room meta

* **4**: Co-Host, can everything except removing co hosts

* **5**: Host, owner status 

**Note**: The array giving by the member _u_ does only include 2 users when the host transfers ownership of the room.

### Packet Example

```js
[{
    "a": "modStaff",        // Event name
    "p": {
        "m": "xxxxxx",	    // Name of the moderator
        "mi": -1,           // ID of the moderator
        "u": [{
            "n": "xxxxxx",  // Name of the user
            "i": -1,        // ID of the user
            "p": -1         // Their new role in the room
        }]
    },
    "s": "xxxx"             // Room name
}]
```
### Real life example
```js
[{
    "a": "modStaff",        // Event name
    "p": {
        "m": "kool_panda",  // Name of the moderator
        "mi": 3865820,      // ID of the moderator
        "u": [{
            "n": "SooYou",  // Name of the user
            "i": 3865819,   // ID of the user
            "p": 0          // Their new role in the room
        }]
    },
    "s": "loves-kpop"       // Room name
}]
```