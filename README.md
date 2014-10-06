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

7 - Create an implementation of a Queue
----
Queue Lab code can be accessed at https://github.com/clarkdb/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
Linked List code can be accessed at https://github.com/clarkdb/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
TODO: Provide a link to your completed 06_BST_Lab OR ClosestStarbucks project (only if you used a search tree)

7 - Create an implementation of a Hash Table
----
TODO: Provide a link to your completed 05_Hashing_Lab

7 - Create an implementation of a Heap
----
TODO: Provide a link to your completed 07_Heap_Lab OR Vise project (only if you implemented a heap for it)

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
TODO: Provide a link to your completed 08_Graph_Lab OR Vise project (only if you implemented a graph for it)

7 - Implement graph algorithms
----
TODO: Provide a link to your completed Vise project (only if you used graph traversal), or add a graph traversal to 08_Graph_Lab and provide a link

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List



* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!)

The call stack is the list of operations that the debugger console shows to allow you to see where in the code an error occurs. The call stack is important because it will tell you which operations are working and where the problem with your code occurs by showing each operation and what other places in the libraries or elsewhere in the code is being accessed, or "called".

* The heap (not to be confused with the heap data structure!)

The heap and the stack are the two separate areas of a computer's RAM that are used when allocating space for variables within a program. The stack is where statically allocated memory gets mapped to(when not using "new"), and the heap is where dynamically allocated memory gets mapped to. The stack and heap are kept separate for the ease of access to variables that are created differently and any memory allocated on the heap needs to use the delete function in order to avoid poor memory management. 

* Address

An address is the physical interpretation of where some data is being stored in the computer's RAM. An address is a hexadecimal representing the location but not contents of a spot in the computer's memory that can be accessed through the use of variables and pointers.

* Pointer

A pointer is a variable that contains an address of a certain type of variable data. A pointer must be the same type as the data stored at its address with an asterisk next to the type name to indicate that it is a pointer rather than a variable. A pointer only holds the address if a variable and does not store the data, but can be dereferenced in order to retrieve the data; moreover, when a pointer is deleted, the data remains in memory but the variable that stored the access of the data is lost, creating memory leak.


TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?
* What is a dangling pointer (or dangling reference), and why is it dangerous?
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.


* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
