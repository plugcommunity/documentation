# Frontend API Documentation

The Frontend API is the name given to the API that was written by steven, powered by backbone.js on the website. It is 
the API that the UI is built using, and how the majority of extensions, and browser side plugins and bots operate.

Frontend APIs are essentially a wrapper for the (Formerly accessed by ajax) API endpoints that are available via the 
REST server, the Backend API.

* [Events](/api/events/README.md)
* [Methods](/api/methods/README.md)
* [API Constants](/api/constants.md)
* [Roles & Permissions](/api/roles.md)

# Backend API Documentation

The Backend API is the label given to the RESTful API, it's endpoints and the socket events that power plug.dj.
You can grab information on demand, perform actions etc. with the POST, GET and DELETE methods, using the API.
Using the socket, you will be able to listen to the stream of information emitted by plug, such as chat and song info.

It's the combination of these two systems, that power the frontend API that normal users see. By using these, you can 
emulate the frontend environment, and build native applications/clients and bots.


The Socket Server
* [Server Information](/api/socket.md)

The RESTful API
* [API Endpoints](/api/endpoints/README.md)
