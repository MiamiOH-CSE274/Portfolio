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
The link below proves that I can implement a C++ Queue Data Structure
https://github.com/GrasysER/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
The link below proves that I can implement a C++ List Data Structure
https://github.com/GrasysER/04_Linked_List_Lab/blob/master/LinkedList.h

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

Array-based lists must rearrange the list whenever add and remove is used, so add/remove are both 0(n) while with a linked list, you only need to adjust pointers, which results in 0(1), or constant time add and remove.
Get, set, and size are all constant time in an array-based list as variables keep track of, and alter data members using the following methods. In a linked list, get and set are 0(n) due to the need for searching through the entire list, while size is 0(1) due to a variable that keeps track of the size. 

* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!) 

The call stack in C++ (and most other programming languages) is used to show the execution of local variables, parameters, and function calls.

* The heap (not to be confused with the heap data structure!)

The heap is a pool of memory used for dynamic memory allocation. When the new keyword is used, the object uses memory from the heap.

* Address

A location in memory of the object.

* Pointer

A pointer is a type of variable used for storing addresses.

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?

Memory leaks occur when memory is no longer in use, but still has information allocated to it.
Memory leaks slow down performance, introduce bugs to the program, or in the worst case scenario, result in the program crashing due to insufficient free memory. 

* What is a dangling pointer (or dangling reference), and why is it dangerous?

A dangling pointer is a pointer that points to unallocated memory.

Dangling pointers are dangerous because they introduce bugs to programs without crashing them, and can also create security risks if the dangling pointer is used to access other data or overwrite memory.

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?

Destructor's are used to free up memory that is no longer in use. Destructor's are necessary in C++, but not Java because Java automatically frees up memory while C++ does not.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

For a grocery list, a doubly linked list would be preffered.
A doubly linked list would allow for products to be inserted anywhere in the list, which is preferrable for a grocery list.
Other data types we have used so far only allow data to be added to the front or back, which could make the grocery list hard to read. 

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
