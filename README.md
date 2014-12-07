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
https://github.com/SamHausfeld/03_Queue_Lab

7 - Create an implementation of a List
----
https://github.com/SamHausfeld/04_Linked_List_Lab

7 - Create an implementation of a Binary Search Tree
----

https://github.com/SamHausfeld/06_BST_Lab

7 - Create an implementation of a Hash Table
----
https://github.com/SamHausfeld/05_Hashing_Lab

7 - Create an implementation of a Heap
----
https://github.com/SamHausfeld/07_Heap_Lab

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/SamHausfeld/08_Graph_Lab

7 - Implement graph algorithms
----
https://github.com/SamHausfeld/08_Graph_Lab

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List

In terms of running times, Array-based Lists and Linked Lists are virtually opposites.  All the things that one does in constant time, the other can do in linear time and vice versa. (With an exception for the size function which is always constant time, due to it's simplicity.)
For example, in an Array-based List; the get, set and size methods all run in constant time, where as add and remove take linear time.
Vice versa, in a LinkedList, the add and remove (and size) methods are constant instead.
The difference here is due to each data structures approach to the particular methods.  A fair rule of them that I've observed, is that a method is slower if ever needs to use a loop to search through the entirity/majority of an array.


* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!)

The call stack is basically the list of actions (or requests) that the computer needs to handle, and the order in which it needs to handle them.  When too many requests are made, we have "stack overflow."

* The heap (not to be confused with the heap data structure!)

An allocated space for a program to do it's processing in, instead of on the stack/disk.

* Address

The "location" of a variable, object or some other element within the disk space.  We can use the & command to access these.

* Pointer

An unique type of element that points to the addresses of other specified elements.

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?

Memory leak is when you allocate disk space that you don't intend to, slowing down your entire computer.

* What is a dangling pointer (or dangling reference), and why is it dangerous?

These dangling pointers are pointers that no longer "point" to anything, and they can be used by hackers to infiltrate complex systems.

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?

Java is intelligent, and basically...knows when to delete the information it no longer needs.  C++, quite simply doesn't.  But the reason C++ is so barebones is so that it can operate at absolute maximum efficiency.  A destructor is exactly like a constructor, except it deletes any data that is no longer needed by the programming.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++


???????????????????????????????????????


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

When I make a grocery list, I use a text app on my phone.  I generally try to order the items on my list based on their location in the store.  Sometimes, I think of something I want to add to my grocery list on my way to the store, and need to place it between two items.  This sort of functionality is only supported by the LinkedList's add() function, seeing as it can slip a new element between two existing elements at the users discretion.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
