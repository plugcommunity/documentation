# Permission Levels

Within plug there are two types of roles: staff roles, and global roles.

You can see the staff roles API constants [here](/api/constants.md), in the staff roles column.

**Note**: There's five roles for the user

* **0**: None, just a regular user

* **1000**: ResidentDJ, can lock the waitlist

* **2000**: Bouncer, can delete chat messages, remove DJs, force skip and ban people

* **3000**: Manager, can everything except removing co hosts and managers as well as editing the room meta

* **4000**: Co-Host, can everything except removing co hosts

* **5000**: Host, owner status 

The gRoles are reserved for Admins,Brand Ambassadors, Site Moderators, Plot members , and  Promoters.

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

Site Moderators inherit from bouncers, and are global bouncers.They are able to do anything a bouncer can do, but in any room. They
are also un-ban-able by anyone except Admins & BA's, although there have been exploits around this.

Plot and Promoters do not inherit any permissions. Although they have a color and a title in every room.
