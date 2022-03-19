# Socket.io

## Discussion

### 1. What is the benefit of transforming data into packets?
TDM-based networks must transform into packet-based networks to meet the demands of pervasive data-centric applications and services.

Packet-based networks not only enable new innovations, services, and business opportunities, they are also the most cost-effective, efficient, and scalable networks for content delivery.

### 2. UDP is often referred to as a connectionless protocol. Why is this?
It is known as a datagram protocol because it is analogous to sending a letter where you don't acknowledge receipt.

### 3. Can a socket server application have multiple socket connections?
Multiple connections on the same server can share the same server-side IP/Port pair as long as they are associated with different client-side IP/Port pairs

### 4. Can a socket connection application be connected to multiple socket servers?
Cannot use a single socket to connect to multiple servers.

### 5. Can an application be both a socket server and a socket connection?
You can not combine server and client sockets into one, because a TCP/IP connection goes from a source port to a destination port, with each having unique port numbers.


___

## Term

Term | Definition
------------ | ------------
Observer Pattern |  Observer is a behavioral design pattern that lets you define a subscription mechanism to notify multiple objects about any events that happen to the object they’re observing.
Listener   |   An event listener is a procedure in JavaScript that waits for an event to occur.
Event Handler   |   Event handlers are the JavaScript code that invokes a specific piece of code when a particular action happens on an HTML element.
Event Driven Programming   |   Website load, user click, window resize, etc. As a developer, you have to make sure that your applications have a flow. That flow is determined by all the possible events that can occur as the user interacts with your app.
Event Loop   |   Is a constantly running process that monitors both the callback queue and the call stack.
Event Queue   |   Is responsible for sending new functions to the stack for processing.
Call Stack   |    Is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function.
Emit/Raise/Trigger   |   Emit: on() function that allows one or more functions to be attached to named events emitted by the object. Raise: Errors are thrown by the engine, and exceptions are thrown by the developer. Trigger: The specified event and the default behavior of an event (like form submission) for the selected elements.
Subscribe   |   Is an object that represents a disposable resource, usually the execution of an Observable. 
database   |   a structured set of data held in a computer, especially one that is accessible in various ways.

___



### [Back to the HOME](./README.md)