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
https://github.com/ernstcc/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
https://github.com/ernstcc/04_Linked_List_Lab/blob/master/LinkedList.h

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
While there are numerous different variations of a List interface, Array-based and Linked Lists are two of the most common and useful.  The basis of an Array-based list is storing data in a single array that is organized in a manner such as a queue or stack.  As a result of being a single array, there is constant time access to any member data through the get and set functions.  Another result of all data being stored in a single array is that adding or removing an element is run, at worst case, in linear time because the array may need to relocate every piece of data.  Finally, the only way to resize the array is to completely allocate a larger array and move the current array into it which is a relatively expensive process.  Linked Lists work by using pointers to hold all data in successive order.  Each piece of data is given a spot in the list also known as a node and has a link to both the next and previous nodes.  Contrasting array-based lists, all linked list functions (add, remove, get, set) run in constant time once the relevant node has been determined, however, finding the relevant node can take up to linear time.  This results in the add and remove being faster in Linkedlists, but the get and set theoretically being faster in an array-based list.
	

* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!) - The call stack is the order in which the source code is executed after being compiled.  The callstack directly modifies the memory of system in order to execute whatever was written in the source code.  
* The heap (not to be confused with the heap data structure!) - The heap is the total amount of memory available to the system.  Most often this memory comes in the form of RAM, or random access memory.  When any variable or classes are allocated in a program, memory is reserved from the heap to store the data.  
* Address - An address is the location in the heap where a specified variable is present.    
* Pointer - A pointer represents the data present at a given address.  

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?
A memory leak is when a program uses excessive memory because inaccessible data is still stored on the heap.  Often times memory leaks are caused by forgetting to delete variables or arrays after use.  The result of memory leaks is slower code and potentially heavily taxing the computer by using all the RAM.
* What is a dangling pointer (or dangling reference), and why is it dangerous?
A dangling pointer is a pointer that references data that has already been deleted by the program.  The danger in dangling pointers comes from the memory manipulation potential of C++.  By using a reference into the memory, one could access any part of the program or system. 
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
A destructor flags the information to be deleted that is stored on the heap for deletion so that it can be overwritten when necessary.  This functionality is not needed in Java because Java automatically deleted all references after variables have gone out of scope.  

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
In order to store a grocery list, a linked list would be the most effective data structure.  The reasoning behind this decision is that the add and remove functions run in almost constant time, so crossing items off the list would be very efficient.  Additionally, adding items to the list would be at least as efficient as an array-based list and very likely much more efficient.  Furthermore, traversing through the list would be simple and effective by simply moving from one node to the next.  

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
