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
Here is the link to the Queue I implemented: https://github.com/eaglesonA/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
An example of a List is in our Linked List Lab, in the header file, located here: 
https://github.com/eaglesonA/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
TODO: Provide a link to your completed 06_BST_Lab OR ClosestStarbucks project (only if you used a search tree)

7 - Create an implementation of a Hash Table
----
TODO: Provide a link to your completed 05_Hashing_Lab

7 - Create an implementation of a Heap
----
TODO: Provide a link to your completed 07_Heap_Lab

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
TODO: Provide a link to your completed 08_Graph_Lab

7 - Implement graph algorithms
----
TODO: Add a graph traversal (DFS or BFS) to 08_Graph_Lab and provide a link

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List
There are pros and cons to using Array Lists or Linked Lists. LinkedList is wonderful if you have a lot of items you need to add, and need to put those in a particular
order. The add and remove methods in a Linked List are constant time, much better than ArrayList's linear time. ArrayList, however, has the advantage in the get and set
methods, running with constant time, instead of Linked list's linear time. 

* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

* The call stack is the order in which operations get done. All commands (and local variables, objects, and operations) are stored in 
the computer's RAM. The stack is the reason we can perform recursive methods. It keeps track of everything we need, and puts it off to the
side, until it either runs out of space, or a command is performed. Once the function is completed all data is deleted from the stack.
* The heap is also stored in the computer's RAM. The heap is a giant space used for dynamic memory allocation. You can access any sort of 
information at any time from it, unlike the stack where there is an order of execution. It is the programmer's responsibility to delete
unused variables in the heap, because C++ will not do it for you (like Java does with the garbage collector). 
* An Address is the address of a variable stored in memory. It can be found using '&', and to access the value stored within that address of RAM 
you need to use a pointer. 
* As stated above, a pointer can be used to store the value of an address. Declaring a pointer involves a star; ClassType* foo (foo being the pointer).
Changing the value of the pointer would only require *foo="new value". 


* What is a memory leak, and why is it bad?
A memory leak is caused by programmers/developers not deleting variables they create in a function- so it is still accessible. It is important
to delete any objects not in use, so RAM isn't taken up by useless things. Also, since the data is still accessible it becomes a major
security issues, potentially allowing a breach, or random people getting into your information.

* What is a dangling pointer (or dangling reference), and why is it dangerous?
A dangling pointer is one that continues to point to an address after you delete the data that was there. To fix this, you would either delete
the pointer, or reassign it to point to data in use. 

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
This is called automatically (like how the constructor is called automatically). But instead of creating objects, the destructor
deletes them. This is where everything created and used in the function is erased, so there are no memory leaks (no one can access
items after the function ends). Java has something called a garbage collector, which deletes unused or data without pointers, for you.
C++ does not have this luxury, so it is done by hand. 


5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?
* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
My grocery list is the Notes app on my phone. In the app I am able to add, remove, and edit whatever I want. I can place certain things at various points in the list, and the “paper” is endless (the app doesn’t set a max of how many items I can have). Because of all these reasons, I would use a Linked List, since it will allow me to add items at any point in the list (I’m forgetful, and being in the bread section might remind me to get donuts). Also, if I start in a different part of the store (say I want to go clockwise), I can arrange my list easily to reflect my decision. If I find an item isn’t on sale, or is too expensive, I can delete it and there won’t be any blank spaces in my list. 

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
