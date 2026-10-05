# Linked List Lab Notes

This lab focuses on understanding how linked-list structures behave in C++.

## Singly linked list goals

Students should be able to:

- add nodes to the front and back;
- remove from the front and back;
- maintain a correct size counter;
- traverse the list safely;
- search for an element.

SLinkedList has head_ pointer and a size_. Operations at the end ends special cases for an empty or a case where there is only one node in the linked list, because head_ can change. pop_back goes to the second to last node because a node can't point backward. 

## Doubly linked list goals

Students should be able to:

- use sentinel header and trailer nodes;
- maintain correct previous and next links;
- add and remove from both ends;
- avoid breaking the list while deleting nodes.

DLinkedList uses header_ and trailer_, that is why every node has prev and next, so inserting and removing use the necessary pointer.

## Important design points

- The singly linked list stores only a head pointer and a size counter.
- The doubly linked list uses a header and trailer sentinel to simplify edge-case logic.
- Both implementations must avoid memory leaks and must keep the list consistent after every update.

All the nodes are created with 'new' and deleted afterwards. clear() deletes all the created nodes and avoids memory leaks. clear() is called by descructor. The copy contructor creates new nodes so lists never share memory.