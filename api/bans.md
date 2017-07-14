# Banning Users


Banning users is to remove them forcefully from the room.

### Variables


**Reason**: The reason member is set as a single number which represent the following reasons:

**1**: (SPAMMING) User spammed the chat

**2**: (VERBAL_ABUSE) User was harsh to other community members

**3**: (OFFENSIVE_VIDEOS) User was playing offensive media

**4**: (PLAYING_INAPPROPIATE_GENRES) User was playing inappropiate media repeatedly

**5**: (NEGATIVE_ATTITUDE) User was having a negative attitude towards others



**BanDuration**: The duration member can have the following values:

**f**: User is banned permanently

**d**: User is banned for a day

**h**: User is banned for an hour

You can view the frontend constants [here](/api/constants.md)

**WaitlistBanDuration**: The duration member can have the following values:

**f**: User is banned permanently

**l**: User is banned for a day

**m**: User is banned for an hour

**s**: User is banned for 15 minutes

### Known Bugs

*Users continue talking after being banned due to socket delay

### IP Bans

plug.dj uses IP bans for spamming or otherwise malicious intent.

These come in the form of short (15 minute) bans, and permanent bans.