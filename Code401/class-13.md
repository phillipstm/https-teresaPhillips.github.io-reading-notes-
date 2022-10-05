# Message Queues

## Socket.io Chat Example

<https://socket.io/get-started/chat/>

git clone <https://github.com/socketio/chat-example.git>

1.Explain to a non-technical recruiter what the Chat Example (above) does.

It creates a chat application that allows a client and users to interact, by sending and recieving messages in real time.

2.What proof of life are we getting on the backend from the above app?

It is showing up in the terminal and on the local port.

3.Socket.IO gives us the i0.emit() method to send an event to everyone. What flag would you use if you want to send a message to everyone except for a certain emitting socket?

socket.broadcast.emit

## Rooms

<https://socket.io/docs/v4/rooms>

1.What is a room and how might a room be useful?

A room is an arbitrary channel that sockets can join and leave. It can be used to broadcast events to a subset of clients.

2.How do you join a room?

You can call join to subscribe the socket to a given channel:

io.on("connection", (socket) => {
  socket.join("some room");
});

3.how do you leave a room?

Upon disconnection, sockets leave all the channels they were part of automatically, and no special teardown is needed on your part.

You can fetch the rooms the Socket was in by listening to the disconnecting event:

io.on("connection", socket => {
  socket.on("disconnecting", () => {
    console.log(socket.rooms); // the Set contains at least the socket ID
  });

  socket.on("disconnect", () => {
    // socket.rooms.size === 0
  });
});

## Namespaces

<https://socket.io/docs/v4/namespaces/>

1.What is a Namespace and what does it allow you to do?

A Namespace is a communication channel that allows you to split the logic of your application over a single shared connection (also called "multiplexing").

2.Each namespace potentially has its own what? (hint: 3 things)

event handlers
rooms
middleware

3.Discuss a possible use case for separate namespaces

A school website could have multiple rooms for authorized users as teacher's for collaboration, or meeting with parents, and student study rooms, and interest rooms, like music, sports, art, etc.

## Bookmark and Review

### Socket.io Emit Cheatsheet

<https://socket.io/docs/v4/emit-cheatsheet/>

**Server-side**
io.on("connection", (socket) => {

  // basic emit
  socket.emit(/*...*/);

  // to all clients in the current namespace except the sender
  socket.broadcast.emit(/*...*/);

  // to all clients in room1 except the sender
  socket.to("room1").emit(/*...*/);

  // to all clients in room1 and/or room2 except the sender
  socket.to(["room1", "room2"]).emit(/*...*/);

  // to all clients in room1
  io.in("room1").emit(/*...*/);

  // to all clients in room1 and/or room2 except those in room3
  io.to(["room1", "room2"]).except("room3").emit(/*...*/);

  // to all clients in namespace "myNamespace"
  io.of("myNamespace").emit(/*...*/);

  // to all clients in room1 in namespace "myNamespace"
  io.of("myNamespace").to("room1").emit(/*...*/);

  // to individual socketid (private message)
  io.to(socketId).emit(/*...*/);

  // to all clients on this node (when using multiple nodes)
  io.local.emit(/*...*/);

  // to all connected clients
  io.emit(/*...*/);

  // WARNING: `socket.to(socket.id).emit()` will NOT work, as it will send to everyone in the room
  // named `socket.id` but the sender. Please use the classic `socket.emit()` instead.

  // with acknowledgement
  socket.emit("question", (answer) => {
    // ...
  });

  // without compression
  socket.compress(false).emit(/*...*/);

  // a message that might be dropped if the low-level transport is not writable
  socket.volatile.emit(/*...*/);

  // with timeout
  socket.timeout(5000).emit("my-event", (err) => {
    if (err) {
      // the other side did not acknowledge the event in the given delay
    }
  });
});

**Client-side**
// basic emit
socket.emit(/* ... */);

// with acknowledgement
socket.emit("question", (answer) => {
  // ...
});

// without compression
socket.compress(false).emit(/* ... */);

// a message that might be dropped if the low-level transport is not writable
socket.volatile.emit(/* ... */);

// with timeout
socket.timeout(5000).emit("my-event", (err) => {
  if (err) {
    // the other side did not acknowledge the event in the given delay
  }
});

**Reserved events**
On each side, the following events are reserved and should not be used as event names by your application:

connect
connect_error
disconnect
disconnecting
newListener
removeListener

// BAD, will throw an error
socket.emit("disconnecting");

## Things I want to know more about

<ttps://socket.io/docs/v4/adapter/>

Besides the in-memory adapter, there are four official implementations:

the Redis adapter
the MongoDB adapter
the Postgres adapter
the Cluster adapter

sticky sessions ?????<https://socket.io/docs/v4/using-multiple-nodes/#why-is-sticky-session-required>

Emitter cheatsheet
<https://socket.io/docs/v4/adapter/#emitter-cheatsheet>