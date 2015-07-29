# Permission Levels

Within plug there are two types of roles: staff roles, and global roles.

You can see the staff roles API constants [here](/api/constants.md), in the staff roles column.

**Note**: There's five roles for the user

* **0**: None, just a regular user

* **1**: ResidentDJ, can lock the waitlist

* **2**: Bouncer, can delete chat messages, remove DJs, force skip and ban people

* **3**: Manager, can everything except removing co hosts and managers as well as editing the room meta

* **4**: Co-Host, can everything except removing co hosts

* **5**: Host, owner status 

The gRoles are reserved for Admins and Brand Ambassadors.

|                                   | User  | Resident DJ   | Bouncer   | Manager   | Co-Host   | Host  |
| --------------------------------- | ----  | -----------   | -------   | -------   | -------   | ----  |
| Add/Remove Co-Hosts               |       |               |           |           |           | √     |
| Add/Remove Managers               |       |               |           |           | √         | √     |
| Add/Remove Bouncers               |       |               |           | √         | √         | √     |
| Add/Remove Resident DJs           |       |               |           | √         | √         | √     |
| Delete Chat                       |       |               | √         | √         | √         | √     |
| Edit Community Name               |       |               |           |           | √         | √     |
| Edit Community Description        |       |               |           |           | √         | √     |
| Edit Community Welcome Message    |       |               |           |           | √         | √     |
| Add/Remove DJs to the Wait List   |       |               | √         | √         | √         | √     |
| Lock/Unlock DJ Wait List          |       |               |           | √         | √         | √     |
| Toggle DJ Cycle On/Off            |       |               |           | √         | √         | √     |
| Join Locked Wait List             |       | √             |           | √         | √         | √     |
| Force Skip a Song                 |       |               | √         | √         | √         | √     |
| Ban People                        |       |               | √         | √         | √         | √     |
| Unban People                      |       |               |           | √         | √         | √     |
| Mute Users                        |       |               | √         | √         | √         | √     |


Admins have all permissions, as well as being un-ban-able, able to delete rooms, privatise rooms, and change hosts.

BAs inherit from managers, and are global managers. They are able to do anything a manager can do, but in any room. They
are also un-ban-able by anyone except Admins, although there have been exploits around this.

