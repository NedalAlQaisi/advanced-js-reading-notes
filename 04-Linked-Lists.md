# What’s a Linked List ?

## The Big(O) :
### What is Big(O) and why do we need it in programming??
- We use this metric to measure how long it takes to perform an operation and what are the consequences of delaying results.
- In large projects, the issues and processes that are implemented in it usually require the analysis of a large amount of software... It is necessary to find a way to write the code so that it can show an effective output in the shortest possible time
- Big(O) analysis statistics ranking.
![](./assets/mypic.png)

### The criteria that you use in choosing the appropriate Big(O)...

- Running Time: The amount of time required for an algorithm to complete.
- Input Size: Represented by the variable n, the total size of values used as parameters in an algorithm.
- Memory Space: The amount of memory resources required for an algorithm to complete.

## Linked List

### Definition :
A linked list is a linear data structure that represents a collection of elements, where each element points to the next one. The first element in the linked list is the head and the last element is the tail.

### Each element of a linked list data structure must have the following properties:

- `value`: The value of the element
- `next`: A pointer to the next element in the linked list (null if there is none)

#### The main properties of a linked list data structure are:

- `size`: The number of elements in the linked list
- `head`: The first element in the linked list
- `tail`: The last element in the linked list


#### The main operations of a linked list data structure are:

- `insertAt`: Inserts an element at the specific index
- `removeAt`: Removes the element at the specific index
- `getAt`: Retrieves the element at the specific index
- `clear`: Empties the linked list
- `reverse`: Reverses the order of elements in the linked list


### How many types of Linked List exist?

#### There are multiple types of Linked Lists available:

- Singly Linked List

The singly linked list includes nodes which contain a data field and next field. The next field further points to the next node in the line of nodes.

In other words, the nodes in singly linked lists contain a pointer to the next node in the list. We can perform operations like insertion, deletion, and traversal in singly linked lists.

A singly linked list is shown below whose nodes contain two fields: an integer value and a pointer value (a link to the next node).

- Doubly Linked List

The doubly linked list includes a pointer (link) to the next node as well as to the previous node in the list. The two links between the nodes may be called "forward" and "backward, "or "next" and "prev (previous)." A doubly linked list is shown below whose nodes consist of three fields: an integer value, a link that points to the next node, and a link that points to the previous node.
- Multiply Linked List

n a multiply linked list, each node consists of two or more link fields. Each field is used to join the same set of records in a different order of the same set.


- Circular Linked List

### [Back to the HOME](./README.md)