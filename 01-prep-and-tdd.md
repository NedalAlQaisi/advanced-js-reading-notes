# 01-prep-and-tdd

- Event Loop:

A queue is a data structure that works on the First in First out principle, so as tasks get pushed into the queue, they get out in that same order. Tasks that have been executed by the Web API’s, which are being pushed to the Task Queue, then go back to the Call Stack to get their result printed out.

- JS callback functions:

A stack is a data structure in which the last element added is always the first to be removed from the stack, you could think of it as a stack of a plate in which only the first plate which was the last added can be removed first. A Call Stack is simply nothing but a stack data structure where tasks or code is being executed accordingly.


- JS Promises:

A Promise is a proxy for a value not necessarily known when the promise is created. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason. This lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value, the asynchronous method returns a promise to supply the value at some point in the future.

A Promise is in one of these states:

pending: initial state, neither fulfilled nor rejected.
fulfilled: meaning that the operation was completed successfully.
rejected: meaning that the operation failed.
A pending promise can either be fulfilled with a value or rejected with a reason (error). When either of these options happens, the associated handlers queued up by a promise's then method are called. If the promise has already been fulfilled or rejected when a corresponding handler is attached, the handler will be called, so there is no race condition between an asynchronous operation completing and its handlers being attached.

- JS Async/Await:

Asynchronous programming means that the code runs in an event loop. When there is a blocking operation, the event is started. The blocking code keeps running without blocking the main execution thread. When the blocking code finishes running, it queue’s the result of the blocking operations and pushes them back to the stack.

JavaScript is single-threaded
JavaScript is non-blocking, i.e. slow processes don’t block its execution
JavaScript is concurrent, i.e. it executes its code in more than one thread at the same time
JavaScript is asynchronous, i.e., it runs blocking code somewhere else.

- Test-Driven Development:

Test-driven development is a style of programming that closely intertwines coding, testing, and designing. So, when designing the functionality of your application, you first write unit tests and then implement the code afterwards.