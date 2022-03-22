# Message Queues

## Discussion

### 1. What does it mean that web sockets are bidirectional? Why is this useful?
This enables the server to send real-time updates asynchronously, without requiring the client to submit a request each time.

### 2. Does socket.io use HTTP? Why?
Require an http server for the initial upgrade handshake.

### 3. What happens when a client emits an event?
It fires events in the server and it listen to events

### 4. What happens when a server emits an event?
This events fires for all the clients that connected to this server. 

### 5. What happens if a client “misses” an event?
When mistakes happen it’s important to be honest and identify where errors have occurred.

### 6. How can we mitigate this?


___

## Term

Term | Definition
------------ | ------------
Socket |   Is one endpoint of a two-way communication link between two programs running on the network.
Web Socket   |    Is a communications protocol for a persistent, bi-directional, full duplex TCP connection from a user's web browser to a server. 
Socket.io   |   Is a library that enables low-latency, bidirectional and event-based communication between a client and a server.
Client   |   A client is a computer or a program that, as part of its operation, relies on sending a request to another program or a computer hardware or software that accesses a service made available by a server (which may or may not be located on another computer).
Server   |    Is a computer program or device that provides a service to another computer program and its user, also known as the client. 
OSI Model   |   describes seven layers that computer systems use to communicate over a network.
TCP Model   |    The model represents how data is exchanged and organized over networks.
TCP   |   TCP stands for Transmission Control Protocol a communications standard that enables application programs and computing devices to exchange messages over a network. It is designed to send packets across the internet and ensure the successful delivery of data and messages over networks.
UDP   |   Is a communications protocol that is primarily used to establish low-latency and loss-tolerating connections between applications on the internet.
Packets   |   Is a small amount of data sent over a network, such as a LAN or the Internet. Similar to a real-life package, each packet includes a source and destination as well as the content (or data) being transferred.

___








### [Back to the HOME](./README.md)