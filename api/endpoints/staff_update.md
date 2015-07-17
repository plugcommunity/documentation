# staff/update Endpoint

The staff/update endpoint enables you to update the role of a user in your room.

**Note**: There's five roles for the user

* **0**: None, just a regular user
* **1**: ResidentDJ, can lock the waitlist
* **2**: Bouncer, can delete chat messages, remove DJs, force skip and ban people
* **3**: Manager, can everything except removing co hosts and managers as well as editing the room meta
* **4**: Co-Host, can everything except removing co hosts
* **5**: Host, owner status 

### Endpoint

**staff/update**

### available verbs

_POST_

### Parameters

**userID**: ID of the user you want to add to the staff
**roleID**: ID of the role you want to apply

```json
{
    "userID": -1,
    "roleID": 1
}
```

### Data returned

```js
{
    'data': [],
    'meta': {},
    'status': 'ok',
    'time': 'xx.xxxxxxxxxxx'
}
```