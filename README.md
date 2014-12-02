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

Array-based lists must rearrange the list whenever add and remove is used, so add/remove are both 0(n) while with a linked list, you only need to adjust pointers, which results in 0(1), or constant time add and remove.
Get, set, and size are all constant time in an array-based list as variables keep track of, and alter data members using the following methods. In a linked list, get and set are 0(n) due to the need for searching through the entire list, while size is 0(1) due to a variable that keeps track of the size. 

Add table comparing methods of both. Then in essay write why for easier readability. Iterators very important, talk about them, instead of add in the table, could be add at an iterator, get would would be get an iterator for an index then talk about them in terms of iterators. Iterator is like an index, keeps track of where you are on a list.

ArrayList add 0(n) get/set 0(1) get at an iterator 0(1) remove 0(n) get iterator at front/back 0(1) add/rem f/b 0(1)
LinkedList add 0(1) get 0(n) set 0(1) get at an iterator 0(1) remove 0(1) get iterator at front/back 0(1) add/rem f/b 0(1)

* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!) 

The call stack in C++ is the portion of the RAM used for statically allocated variables. Variables in the stack only live as long as that particular variable stays in scope, or in other words while the funtion that created that variable is still running. The stack is a LIFO data structure and can grow too large, resulting in the popular saying "stack overflow".

* The heap (not to be confused with the heap data structure!)

The heap is a pool of memory used for dynamic memory allocation. When the new keyword is used, the object uses memory from the heap. Variables in the heap must be deleted with delete to prevent memory problems.

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

Objects cleaning up after themselves. Java checks heap to see if object still in use, if not object is deleted, c++ does not do this.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?

The main benefit of using templates for creating collection classes is that a template allows for typesafe collection classes. Typesafe collection classes work with any type of data, bypassing the need to create many specialized classes for each type of data.

* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

The compiler must know both the template definition and the type of data to fill in the template. When the compiler gets down to the .cpp code it must already know both or else the compiler won't know what to do with the .cpp code.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

A grocery list keeps a list of items to buy at a store. A good grocery list should sort the items into sections based on where each particular item would be found. My grocery list would be designed as an app for a cellphone, and even the weakest cellphones have enough memory for a grocery list app.
A grocery list will never get bigger than a few hundred items,
thus efficiency is not important, as even the slowest data structure will be very fast at operating on such a small number of items. The operations supported by the data structure is the most important point to consider, as the user should be able to manipulate their grocery list 
as he/she thinks of new items to buy or wants to cross of items already purchased.

With all of that said, a doubly linked list would be a great option for a grocery list. A doubly linked list uses pointers to point to the next and previous item, and thus would allow the user to easily update the grocery list as it is used by manipulating pointers. By using a doubly linked list, items could be easily inserted anywhere in the list or removed without having to recreate the list every time.
The doubly linked list would store strings for the name of each item to be bought at the store. An option that could be considered would be to use a 


What is a grocery list?
How should I decide which data structure to use?
Efficiency not imp, list not very long. Operations supported is most important thing.
Platform list would be on.
Iterators for aisles, 

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

BST
