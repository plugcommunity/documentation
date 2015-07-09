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
