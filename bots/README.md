#Bots
This contains everythin you should need to make/need to create a bot on plug.dj
##Wats needed:
* username
* password
* roomname (this is the code name you can find here `https://plug.dj/{roomname})`

##The way to login
1. get the csrf of the website and keep the cookies.  
It stands right after `_csrf="` 
2. post this to the endpoint `auth/login`
```js
    {
        "csrf": {csrf},
        "email": {username},
        "password": {password}
    }
```
3. retreve the authkey from `plug.dj/{roomname}`.   
It stands right after `_jm="`.  
Make shure you store this somewere youl need it later.

##The Websocket
###Websocket
Plug uses this way to let the front end api kno that things have happend. These things are calles events. In a later part tay are explained in more detail.
###Login to the websocket
1. Connect to the websocket `wss://godj.plug.dj:443/socket`
2. When the connection opens send this:
```js
    {
        "a": "auth",
        "p": {the authkey},
        "t": {the time now}
    }
```
###Chattig
This is become by sending to the websocket.
```js
{
    "a": "chat",
    "p": {the chat message},
    "t": {the time now}
}
```
## Objects
There are a copple objects that plug sends that always will contain the same information.
###Media
This object defines an video or song 
```js
{
    "author": "Nightcore", // the author of the song/video
    "title": "Break The World", // the title of the song/video
    "image": "http://i.ytimg.com/vi/EqIYqoXt-Go/default.jpg", // an image representing the song/video
    "format": 1, // the format of the song/video (1 = youtube, 2 = soundcloud)
    "cid": "EqIYqoXt-Go", // the song/video id on youtube or soundcloud
    "duration": 162, // the duration of the song/video
    "id": 278833958 // the id within plug of the song/video
}
```
###Person
this object defines a person 
```js
{
    "username": "Eldevin", // the username
    "gRole": 0, // the global rank of people 
    "language": "en", // the language of the person
    "level": 4, // the level
    "avatarID": "base12",// the avatar ID of the person
    "joined": "2015-04-16 02:31:47.846923", // the first time he joined
    "slug": 
    "eldevin", 
    "role": 0, 
    "badge": None, 
    "id": 6322241, 
    "sub": 0
}
```
##Video related events
###Advance message
This event happens when a new song is played
```js
{
    "a": "advance", 
    "p": {
        "c": 6327320, // current playing person
        "d": [5388249,..., 6059187], // people in waitlist
        "h": "143e121c-88bc-47ee-8995-ab47dd98fccd", // history ID
        "m": {Media object}, // media object
        "p": 7097502, // playlist ID
        "t": "2015-04-18 00:25:14.899831" // begin playtime
    }, 
    "s": "thenightcoreclub"
}

```
###PlaylistCycle
When you finished playing your song. To update your playlists
```js
{
    "a": "playlistCycle", 
    "p": 7992168, // playlist ID
    "s": "dashboard"
}
```
##User related events
###User
##Mod related events
