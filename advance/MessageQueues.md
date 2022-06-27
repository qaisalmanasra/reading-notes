# Message Queues
## Introduction
#### Writing a chat application with popular web applications stacks like LAMP (PHP) has normally been very hard. It involves polling the server for changes, keeping track of timestamps, and it’s a lot slower than it should be.

#### Sockets have traditionally been the solution around which most real-time chat systems are architected, providing a bi-directional communication channel between a client and a server.

#### This means that the server can push messages to clients. Whenever you write a chat message, the idea is that the server will get it and push it to all other connected clients.

## Rooms
#### The "room" feature is implemented by what we call an Adapter. This Adapter is a server-side component which is responsible for:

* #### storing the relationships between the Socket instances and the rooms
* #### broadcasting events to all (or a subset of) clients
#### You can find the code of the default in-memory adapter here.

#### Basically, it consists in two ES6 Maps:

* #### sids: Map<SocketId, Set<Room>>
* #### rooms: Map<Room, Set<SocketId>>
#### Calling socket.join("the-room") will result in:

* #### in the ̀sids Map, adding "the-room" to the Set identified by the socket ID
* #### in the rooms Map, adding the socket ID in the Set identified by the string "the-room"
#### Those two maps are then used when broadcasting:

* #### a broadcast to all sockets (io.emit()) loops through the sids Map, and send the packet to all sockets
* #### a broadcast to a given room (io.to("room21").emit()) loops through the Set in the rooms Map, and sends the packet to all matching sockets
#### You can access those objects with:

#### **// main namespace**
#### const rooms = io.of("/").adapter.rooms;
#### const sids = io.of("/").adapter.sids;

#### **// custom namespace**
#### const rooms = io.of("/my-namespace").adapter.rooms;
#### const sids = io.of("/my-namespace").adapter.sids;
### Notes:

* #### those objects are not meant to be directly modified, you should always use socket.join(...) and socket.leave(...) instead.
* #### in a multi-server setup, the rooms and sids objects are not shared between the Socket.IO servers (a room may only "exist" on one server and not on another).

### **[Reference](https://socket.io/get-started/chat/)**
### **[Reference](https://socket.io/docs/v4/rooms)**
### **[Reference](https://socket.io/docs/v4/namespaces/)**
### **[Bookmark](https://socket.io/docs/v4/emit-cheatsheet/)**