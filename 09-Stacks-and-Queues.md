# Stacks and Queues

## Stacks

### Definition

A collection of items in which only the most recently added item may be removed. The latest added item is at the top. Basic operations are push and pop.

### Why we use Stack in data structure ?

A stack is an abstract data type that consists of a predefined capacity. It allows adding and removing elements in a particular order. When every time an element is added, it goes to the top of the stack. Stack enables all data to operations at one end only. So the only element that can be removed is the element at the top of the stack, and only one item can be read or removed at a given time.

### Run-time complexity of Stack Operations

For all the standard stack operations (push, pop, isEmpty, size), the worst-case run-time complexity can be O(1). Because these operations take constant time. It’s obvious that size and isEmpty constant-time operations. push and pop are also O(1) because they only work with one end of the data structure — the top of the stack.

### Stack Operations

- `push()` : Pushing (storing) an element on the stack.

- `pop()` : Removing (accessing) an element from the stack.

- `peek()` : get the top data element of the stack, without removing it.

- `isFull()` : check if stack is full.

- `isEmpty()` : check if stack is empty.


### Push Operation
Step 1 − Checks if the stack is full.

Step 2 − If the stack is full, produces an error and exit.

Step 3 − If the stack is not full, increments top to point next empty space.

Step 4 − Adds data element to the stack location, where top is pointing.

Step 5 − Returns success.

### Pop Operation
Step 1 − Checks if the stack is empty.

Step 2 − If the stack is empty, produces an error and exit.

Step 3 − If the stack is not empty, accesses the data element at which top is pointing.

Step 4 − Decreases the value of top by 1.

Step 5 − Returns success.
___

## Queues

### Definition

A collection of items in which only the earliest added item may be accessed. Basic operations are add (to the tail) or enqueue and delete (from the head) or dequeue. Delete returns the item removed.

### Why we use Queue in data structure ?

Queue is used when things don’t have to be processed immediately, but have to be processed in First In First Out order like Breadth First Search. This property of Queue makes it also useful in following kind of scenarios.

### Queue Operations

- `isEmpty()` : Check if queue is empty or not.

- `enqueue()` : Elements are added form one end (rear/back).

- `dequeue()` : Elements are removed from one end.

- `peek()`    : Get the value of the front of the queue without removing it.

- `count()`   : Gets count of total items in queue.

- `show()` : To show the content of the queue.


___

## Difference between Stack and Queue Data Structures

Stacks | Queues
------------ | ------------
Stacks are based on the LIFO principle, i.e., the element inserted at the last, is the first element to come out of the list.   |  Queues are based on the FIFO principle. The element inserted at the first, is the first element to come out of the list.
Insertion and deletion in stacks takes place only from one end of the list called the top.   |   Insertion and deletion in queues takes place from the opposite ends of the list. The insertion takes place at the rear of the list and the deletion takes place from the front of the list.
Insert operation is called push operation.   |   Insert operation is called enqueue operation.
Delete operation is called pop operation.   | Delete operation is called dequeue operation.

### [Back to the HOME](./README.md)
