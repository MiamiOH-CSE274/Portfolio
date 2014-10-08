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
https://github.com/aryelle-player/03_Queue_Lab

7 - Create an implementation of a List
----
https://github.com/aryelle-player/04_Linked_List_Lab

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
	Array-based lists tend to run in constant time for all operations except add() and remove(). Add() and remove() for an array-based list run in linear time. tHe reason for this is because array-based lists offer constant time access to any value in an array but array-based lists aren't terribly dynamic therefore adding and removing elemetns require the array to be shifted. Linked lists that are singly-linked are the complete opposite of array-based lists in terms of running time for operations. For doubly-linked lists, instead of linear time, these lists take O(1+min{i,n-1}) time fr add(), remove(), get(), and set().

* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!)
	The call stack is the space in memory that has been allotted for use.
* The heap (not to be confused with the heap data structure!)
	The heap is the end of the call stack.
* Address
	An address is basically just where an object lives in memory.
* Pointer
	A pointer is an object that points to another object.

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?
	Memory leak is allowing memory to still be used once a programs runtime is through. This is bad because it can allow someone to access something in memory even after the program has stopped running. (the reasons hackers can obtain things they shouldn't have)
* What is a dangling pointer (or dangling reference), and why is it dangerous?
	A dangling pointer is a pointer that points to a space in memory that no longer has anything in it.
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
	A destructor deletes everything in memory after runtime. This prevents memory leak because there is now no way to access something in memory after runtime because the memory is no longer accessible. This is not needed in Java because Jave does this autmactically.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)

* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	The best data structure for a grocery list would be an arry-based list because this data struture allows adding and removing anywhere in the list.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	The best data structure for this task would be a hashtable because hashtables allow you to store key & data pairs. This is necessary for this particualar task because every student is associated with a banner number, a key and data pair.

* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
