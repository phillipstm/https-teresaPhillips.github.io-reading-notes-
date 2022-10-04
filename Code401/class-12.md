# Socket.io

Socket.IO is a JavaScript library for real-time web applications. It enables real-time, bi-directional communication between web clients and servers. It has two parts − a client-side library that runs in the browser, and a server-side library for node.js. Both components have an identical API.

## Web Sockets

<https://en.wikipedia.org/wiki/WebSocket>

1.What is a Web Socket?

It is a computer communications protocol providing full-duplex communication channels over a single TCP connection. Communication is usually ran on port 443 or 80 if unsecured.

2.Describe the Web Socket request/response handshake and what happens once the connection is established.

WebSocket handshake uses the HTTP Upgrade header[3] to change from the HTTP protocol to the WebSocket protocol.

In the exchange, the client begins by making a cleartext request, which is later upgraded to a newer HTTP protocol version or switched to a different protocol.

A connection upgrade must be requested by the client; if the server wants to enforce an upgrade it may send a 426 Upgrade Required response. 

The client can then send a new request with the appropriate upgrade headers while keeping the connection open.

3.Web Sockets provide a standardized way for the server to send content to a client without first receiving a _**REQUEST**___ from that client.

## Socket.io Tutorial

<https://www.tutorialspoint.com/socket.io/>

1.What does the event handler io.on() do?

It is a function that gets executed whenever someone connects when socket.io is a requirement.

The io.on event handler handles connection, disconnection, etc., events in it, using the socket object.

2.Describe some possible proof of life or proof that the code works as expected

 Now we will be using the message event to
pass message from the server to the client. To do this, modify the io.on
('connection', function(socket)) as shown below –var app =
require('express')();
var http = require('http').Server(app);
var io = require('socket.io')(http);

io.on('connection', function(socket){
   console.log('A user connected');

3.What does socket.emit() do?

You can create and fire custom events using the socket.emit function.

To handle these events, use the on function on the socket object on your server.

io.on('connection', function(socket){
   socket.on('clientEvent', function(data){
      console.log(data);

io.on('connection', function(socket){
   console.log('A user connected');

## Socket.io vs Web Sockets

<https://www.educba.com/websocket-vs-socket-io/>

1.What is the difference between WebSocket and Socket.IO? (think Git and GitHub, or OAuth and Auth0).

**websocket**
Is the protocol that establishes the TCP connection.
It provides duplex communication.
Proxy and load balancer not supported.
It doesn't support broadcasting.
No fallback option

    **VS**

**Socket.io**
A library to work with the websocket.
It provides event based communication between browser and server.
Connection can be established in the presence of proxies and load balancers.
It supports broadcasting
It supports fallback options.

2.When would you use Socket.IO?

When you want to create listening events.

3.When would you use WebSockets?

When you want to persist the connection between client and server. And have real time communication.

## OSI Model Explained

<https://www.youtube.com/watch?v=vv4y_uOneC0>

What are a couple of key takeaways from this video?

That the seven layers that make up the OSI Model are:

Application Layer
Presentation Layer
Session Layer
Transport Layer
Network Layer
Data Link Layer
Physical Layer

Each layer has a specific job to do when as it relates to transfering data between clients.

### TCP Handshakes Explained

<https://www.youtube.com/watch?v=xMtP5ZB3wSk>

Translate the gist of this video to a non-technical friend.

TCP stands for transmission control protocol. TCP is a reliable and connection-oriented transport protocol. With TCP, data can be delivered successfully and accurately. 
Many applications, such as web,  email, and FTP, use TCP. Before TCP transmits data,it will use three-way handshake to establish a connection.


#### Socket.io Documentation

<https://socket.io/docs/>

npm install socket.io

Additional Packages- 2 optional packages that can be installed alongside this package. These packages are binary add-ons which improve certain operations.

npm install --save-optional bufferutil utf-8-validate

Dependency tree-A basic installation of the server includes 23 packages:

└─┬ socket.io@4.5.0
  ├─┬ accepts@1.3.8
  │ ├─┬ mime-types@2.1.35
  │ │ └── mime-db@1.52.0
  │ └── negotiator@0.6.3
  ├── base64id@2.0.0
  ├─┬ debug@4.3.4
  │ └── ms@2.1.2
  ├─┬ engine.io@6.2.0
  │ ├── @types/cookie@0.4.1
  │ ├── @types/cors@2.8.12
  │ ├── @types/node@17.0.26
  │ ├── accepts@1.3.8 deduped
  │ ├── base64id@2.0.0 deduped
  │ ├── cookie@0.4.2
  │ ├─┬ cors@2.8.5
  │ │ ├── object-assign@4.1.1
  │ │ └── vary@1.1.2
  │ ├── debug@4.3.4 deduped
  │ ├─┬ engine.io-parser@5.0.3
  │ │ └── @socket.io/base64-arraybuffer@1.0.2
  │ └─┬ ws@8.2.3
  │   ├── UNMET OPTIONAL DEPENDENCY bufferutil@^4.0.1
  │   └── UNMET OPTIONAL DEPENDENCY utf-8-validate@^5.0.2
  ├── socket.io-adapter@2.4.0
  └─┬ socket.io-parser@4.0.4
    ├── @types/component-emitter@1.2.11
    ├── component-emitter@1.3.0
    └── debug@4.3.4 deduped

<https://socket.io/docs/v4/server-initialization/>
<https://socket.io/docs/v4/middlewares/>
<https://socket.io/docs/v4/handling-cors/>

#### Socket.io Server API

<https://socket.io/docs/server-api>

#### Socket.io Client API

<https://socket.io/docs/client-api>

#### Socket Testing Tool

<https://amritb.github.io/socketio-client-tool/>


### Things I want to know more about

npm install --save express socket.io

I think I will reference this page a lot for all web socket info.
