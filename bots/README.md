
<div class="row" id="needed">
  <h3>Wats needed:</h3>
  <ul>
      <li>username</li>
      <li>password</li>
      <li>roomname (this is the code name you can find here <code>https://plug.dj/{roomname})</code></li>
  </ul>
</div>
<div class="row" id="Login">
  <h3>The way to login</h3>
  <ol>
      <li>
          get the csrf of the website and keep the cookies <br>
          It stands right after <code>_csrf="</code> 
      </li>
      <li>
          post this to the endpoint <code>auth/login</code><br>
          <code class="code">
              {<br>
              &nbsp;&nbsp;&nbsp;&nbsp;"csrf": csrf,<br>
              &nbsp;&nbsp;&nbsp;&nbsp;"email": this.username,<br>
              &nbsp;&nbsp;&nbsp;&nbsp;"password": this.password<br>
              }<br>
          </code>
      </li>
      <li>
          retreve the authkey from <code>plug.dj/{roomname}</code>.<br>
          It stands right after <code>_jm="</code>.<br>
          Make shure you store this somewere youl need it later.
      </li>
  </ol>
</div>
<div class="row" id="websocket">
  <h3>The Websocket</h3>
  <h4>Websocket</h4>
  <p>Plug uses this way to let the front end api kno that things have happend. These things are calles events. In a later part tay are explained in more detail.</p>
  <h4>Login to the websocket</h4>
  <ol>
      <li>Connect to the websocket <code>wss://godj.plug.dj:443/socket</code></li>
      <li>When the connection opens send this:<br>
          <code class="code">
              {<br>
              &nbsp;&nbsp;&nbsp;&nbsp;"a": "auth",<br>
              &nbsp;&nbsp;&nbsp;&nbsp;"p": {the authkey},<br>
              &nbsp;&nbsp;&nbsp;&nbsp;"t": {the time now}<br>
              }<br>
          </code>
      </li>
  </ol>
  
  <h4>Chattig</h4>
  <p>This is become by sending to the websocket.</p>
  <code class="code">
      {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"a": "chat",<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"p": {the chat message},<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"t": {the time now}<br>
      }<br>
  </code>
</div>
<div class="row">
  <h3> Objects</h3>
  <p>There are a copple objects that plug sends that always will contain the same information.</p>
  <h4>Media</h4>
  <p>This object defines an video or song </p>
  <code class="code">
      {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"author": "Nightcore", <span>// the author of the song/video</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;"title": "Break The World", <span>// the title of the song/video</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;"image": "http://i.ytimg.com/vi/EqIYqoXt-Go/default.jpg", <span>// an image representing the song/video</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;"format": 1, <span>// the format of the song/video (1 = youtube, 2 = soundcloud)</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;"cid": "EqIYqoXt-Go", <span>// the song/video id on youtube or soundcloud</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;"duration": 162, <span>// the duration of the song/video</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;"id": 278833958 <span>// the id within plug of the song/video</span><br>
      }
  </code>
  <h4>Person</h4>
  <p>this object defines a person </p>
  <code class="code">
      {
      &nbsp;&nbsp;&nbsp;&nbsp;"username": "Eldevin", <span>// the username</span>
      &nbsp;&nbsp;&nbsp;&nbsp;"gRole": 0, <span>// the global rank of people </span>
      &nbsp;&nbsp;&nbsp;&nbsp;"language": "en", <span>// the language of the person</span>
      &nbsp;&nbsp;&nbsp;&nbsp;"level": 4, <span>// the level</span>
      &nbsp;&nbsp;&nbsp;&nbsp;"avatarID": "base12",<span>// the avatar ID of the person</span>
      &nbsp;&nbsp;&nbsp;&nbsp;"joined": "2015-04-16 02:31:47.846923", <span>// the first time he joined</span>
      &nbsp;&nbsp;&nbsp;&nbsp;"slug": 
      &nbsp;&nbsp;&nbsp;&nbsp;"eldevin", 
      &nbsp;&nbsp;&nbsp;&nbsp;"role": 0, 
      &nbsp;&nbsp;&nbsp;&nbsp;"badge": None, 
      &nbsp;&nbsp;&nbsp;&nbsp;"id": 6322241, 
      &nbsp;&nbsp;&nbsp;&nbsp;"sub": 0
      }
  </code>
</div>
<div class="row" id="events">
  <h3>Video related events</h3>
  <h4>Advance message</h4>
  <p>This event happens when a new song is played</p>
  <code class="code">
      {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"a": "advance", <br>
      &nbsp;&nbsp;&nbsp;&nbsp;"p": {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"c": 6327320, <span>// current playing person</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"d": [5388249,..., 6059187], <span>// people in waitlist</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"h": "143e121c-88bc-47ee-8995-ab47dd98fccd", <span>// history ID</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"m": {Media object}, <span>// media object</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"p": 7097502, <span>// playlist ID</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"t": "2015-04-18 00:25:14.899831" <span>// begin playtime</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;}, <br>
      &nbsp;&nbsp;&nbsp;&nbsp;"s": "thenightcoreclub"<br>
      }<br>
      
  </code>
  <h4>PlaylistCycle</h4>
  <p>When you finished playing your song. To update your playlists</p>
  <code class="code">
      {<br>
      &nbsp;&nbsp;&nbsp;&nbsp;"a": "playlistCycle", <br>
      &nbsp;&nbsp;&nbsp;&nbsp;"p": 7992168, <span>// playlist ID</span><br>
      &nbsp;&nbsp;&nbsp;&nbsp;"s": "dashboard"<br>
      }<br>
  </code>
  <h3>User related events</h3>
  <h4>User</h4>
  <h3>Mod related events</h3>
</div>
<div class="row" id="REST">
</div>
