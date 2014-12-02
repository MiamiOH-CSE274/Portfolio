SEARCH FOR "//" and "TODO" BEFORE TURN IN

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
	In the third lab I created an implementation of a queue and here is the proof: https://github.com/SiegerJman/03_Queue_Lab/blob/master/ArrayQueue.h
//update this
7 - Create an implementation of a List
----
	In the fourth lab I created an implementation of a list and here is the proof: https://github.com/SiegerJman/04_Linked_List_Lab/blob/master/LinkedList.h
//update this
7 - Create an implementation of a Binary Search Tree
----
TODO: Provide a link to your completed 06_BST_Lab OR ClosestStarbucks project (only if you used a search tree)

7 - Create an implementation of a Hash Table
----
TODO: Provide a link to your completed 05_Hashing_Lab
//THIS WILL TAKE A WHILE
7 - Create an implementation of a Heap
----
TODO: Provide a link to your completed 07_Heap_Lab OR Vise project (only if you implemented a heap for it)

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
TODO: Provide a link to your completed 08_Graph_Lab OR Vise project (only if you implemented a graph for it)

7 - Implement graph algorithms
----
TODO: Provide a link to your completed Vise project (only if you used graph traversal), or add a graph traversal to 08_Graph_Lab and provide a link
//add a BFS or DFS to the graph
21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List 
	Both Array and Linked lists have constant running times on their size methods. For get and set methods, they have different run times. For Array list it is constant time while
	Linked list runs in 0(N) time. For the add and remove methods Linked List runs in constant time while Array list runs in 0(N) time.
//insert stuff about iterators here NOTES 10/16
* Binary Search Tree vs. Hash Table
//NOTES 10/28
* Adjacency List vs. Adjacency Matrix
//NOTES 11/6

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!)
	The call stack is the data structure that stores the data tree of active methods in the program.
//add stuff about the difference between the heap and the stack. explain its role in storing variables and parameters.
* The heap (not to be confused with the heap data structure!)
	The heap is the allocation of memory where new dynamic data values are stored.
//be more specific
* Address
	An address gives the location to an object.
* Pointer
	A pointer contains the Address for an object.

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?
	A memory leak is where data is unused but still allocated so that eventually all memory is taken but not used.
* What is a dangling pointer (or dangling reference), and why is it dangerous?
	A dangling pointer is a pointer that points to unallocated data. It is dangerous because it gives whatever value was left in the address and can lead to un expected and unwanted results.
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
	A destructor uninitializes an object and frees up the memory of its location. It isnt necessary in Java because Java has a built in garbage collector that deconstructs objects automatically.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++
//NOTES 9/18
What is the main benefit of using templates when creating collection classes?
In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each) 
//these are substantial essays and should probably have run time tables.

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
//im feeling some hash
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	Array List would be the best option for a grocery list. It would be the best option because the most commonly used method used would be get() which operates in 0(1) time irreguardless of many groceries need to be picked up.
//explain more, include run time tables see email
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
//im feeling heap
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
//none of them cause thats wrong (priority queue)