Portfolio
=========
Document completion of the course's learning outcomes.

Instructions
====
The goal of this is to make it very easy for me (or an employer, or a teaching assistant) to see whether or not you have mastered the material of the class. The hope is that I would be able to grade your work without downloading and compiling your code. For labs, I can grade them by inspecting the code. For projects you must provide a video demonstrations of your programs. Some questions require essay responses.

Important
=========
If you prefer, you may turn this in to me via email, instead of hosting it on GitHub. Please talk to me about it during office hours or before or after class.

Body of portfolio
====

7 - Create an implementation of a Queue using a circular array-based list
----
https://github.com/samsab/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
https://github.com/samsab/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
https://github.com/samsab/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
https://github.com/samsab/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
https://github.com/samsab/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/samsab/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
https://github.com/samsab/08_Graph_Lab/blob/master/Graph.cpp

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List
An array-based list is a good choice to make for lists when the list needs to be accessed many times. Accessing an array list is quicker than accessing a linked list. The 'get' method is O(1) for array lists and O(n) for linked lists. However, an iterator is very advantageous when using a linked list. The iterator can add or remove elements at O(1). Any method in a linked list which requires stepping through the list ('get', 'add(index, element)', 'remove') is O(n), while any method not requiring the index ('add(element)', iterator methods) is O(1). All methods but get and add in an array list are O(n-index), which could be advantageous if the list is shorter.

* Binary Search Tree vs. Hash Table


* Adjacency List vs. Adjacency Matrix


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!) - 
The call stack holds variables like an array, but stores in a LIFO structure.

* The heap (not to be confused with the heap data structure!) - 
The heap is a pool of memory used for dynamic allocation.

* Address - 
The location of a variable's memory stored in the computer.

* Pointer - 
A variable which stores the address to a variable and can reference the address at any time.

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?

Memory which is allocated but not released is said to have 'leaked'. This leaked memory takes up space on the computer and will slow applications on the computer unless handled correctly.

* What is a dangling pointer (or dangling reference), and why is it dangerous?

Dangling pointers are those which point to invalid data or data which is no longer valid as it has been removed. These references are bugs which typically crash the program, and do so in a way which makes them difficult to find, as they usually do not crash right away.

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
Destructors delete unneeded memory to prevent memory leakage. In Java, developers need not worry about this, as the built-in garbage collector cleans up the program for the user.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)


* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
I believe an ArrayList would be most advantageous to storing a grocery list. It's easy to add in items which we need, and just as easy to pop them out as we get the items on the list. It's the simplest way to make a basic list, such as one for groceries.


* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.


* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
