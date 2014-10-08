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
Link: https://github.com/MabeCr/03_Queue_Lab

7 - Create an implementation of a List
----
Link: https://github.com/MabeCr/04_Linked_List_Lab

7 - Create an implementation of a Binary Search Tree
----
TODO: Provide a link to your completed 06_BST_Lab OR ClosestStarbucks project (only if you used a search tree)

7 - Create an implementation of a Hash Table
----
Link: https://github.com/MabeCr/05_Hashing_Lab

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
For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

Array-based list vs. Linked List
	In an array-based list, the run time of get() and set() is O(1). However, add() and remove() are O(n).
	In a linked list, the run time of add() and remove is O(1). Get() and set() are both O(n).
	If you are keeping track of the size using an external variable, size() will always be O(1) no matter which option you chose to use.

* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Define/describe each of the following terms, as they apply to memory management in C++

The call stack - The call stack is a "buffer" that everything that needs to be handled gets placed in. 
The heap - The heap is a place in the RAM that stores all the dynamic variables that the program will use. It is "freed" after the program finishes.
Address - An address is the place that an object is stored in the computer's memory that can be accessed and computed.
Pointer - A pointer is a variable that has a value equal to the address of another variable. It is used to reference the area in memory quickly.

Answer the following questions about memory management and dynamic variables

What is a memory leak, and why is it bad?
	A memory leak is when an entity is not deleted in C++. It is bad because it will slow down the program since the object is stored in memory, but it 		cannot be accessed by the code.

What is a dangling pointer (or dangling reference), and why is it dangerous?
	A dangling pointer is a pointer that does not point toward a valid object of the right type. It is kind of like a memory leak, in that it is still 		pointing to something that is not there anymore, and is wasting memory and RAM.

What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
	A destructor is the opposite of a destructor; it deletes the entity in question. In Java, this is something that automatically happens. However, we 		need this in C++ because we cannot allow the entity to remain if it is not being used anymore because it takes up space that could be filled by 		something else. It keeps the program running in an efficient and quick way.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)

If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	I would personally go with a linked list for a grocery list strictly based on the fact that the required functions that you would use the most would 	be O(1). Add() and remove() are both O(1), so as you pull things off the shelf, you can remove them from your list quickly and efficiently. I 	doubt you would need to use the find() function too often, so it just makes sense to use a linked list based on the fact that it does what you want 	to do in the fasted time.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
