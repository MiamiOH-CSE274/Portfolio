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
I have created a queue in lab 3: https://github.com/busdiekc/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
I have created a linked list in lab 4: https://github.com/busdiekc/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
I have created an implementation of a binary search tree in lab 6: https://github.com/busdiekc/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
I have created a hash table in lab 5: https://github.com/busdiekc/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
I have created an implementation of a heap in lab 7: https://github.com/busdiekc/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
I have created an implementation of an adjacency list graph in lab 8: https://github.com/busdiekc/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
TODO: Add a graph traversal (DFS or BFS) to 08_Graph_Lab and provide a link

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List
-----
In general array based lists are easier to work with but are less flexible than linked lists. In an array based list the get() and set() methods can be completed
	in constant time, O(1). However, the drawback to having constant time get() and set() methods is that the add() and remove() methods take linear time, O(n). When an
	element is added or removed from the array all other elements in the array must be moved backward one spot or forward one spot to accommodate the added/removed 
	element. This can be a time consuming process when the array that you are working with has thousands of elements in it. Linked lists are the opposite of array based lists
	in a sense. Linked lists require a bit more complexity to build but allow greater flexibility than array lists. In a linked list the get() and set() methods are completed in
	linear time O(n) unless iterators are used. Unlike the array lists, linked lists must iterate through each element in order to find the correct element being accessed. The time these two operations
	take depends on the number of elements in the list. The add() and remove() methods will take constant time, O(1), however. Because you need only change
	where a couple of the other node structures point to, the linked list does not need to move around the elements when a new element is added or an existing element
	is removed. Array based lists and linked lists will both be able to have the size() method run in constant time O(1) by keeping track of the number of elements using a
	variable that is returned by the size() method. In my opinion, array based lists are more suited for static lists. That is, lists that will not need to add and remove many
	elements but will require heavy use of the get() and set() methods. Linked lists would be better suited for more dynamic lists where the elements inside of the list
	will be frequently added or removed.
	
* Binary Search Tree vs. Hash Table
-----
stuff here

* Adjacency List vs. Adjacency Matrix
-----
stuff here

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!)
------
The stack is a section of your computer's memory that stores statically allocated variables. Memory allocation and deallocation in the call stack is done for you by the computer. When a these variables leave the scope of the executing code all the statically allocated variables are erased and that memory is available to be used again.
	
* The heap (not to be confused with the heap data structure!)
-----
The heap is a section of your computer's memory that is not managed for you automatically. The heap forces you to dynamically allocate the memory needed for your variables and allows you to allocate memory without any restrictions on the size of the memory allocated as long as your computer has that much memory available. Using the heap also means that you must deallocate any memory that was allocated otherwise a memory leak will result. This means that memory is being used to store a variable that cannot be accessed because it has gone out of scope.

* Address
------
An address is the location in the computer's memory that the data of a variable is stored. 
	
* Pointer
------
A pointer is a special variable that stores the address of another variable. The pointer can then be used to access that section of memory throughout a program. This allows you to directly change the stored data of a variable.
	
TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?
------
A memory leak results when memory in the heap is allocated to a variable but then is never deallocated. The allocated memory remains unusable and is referred to as a memory leak. If this happens too much a computer can run out of memory and crash. 
	
* What is a dangling pointer (or dangling reference), and why is it dangerous?
-------
A dangling pointer points to memory that has already been deallocated. If you use a dangling pointer without realizing it the returned data will not be what is expected. Operations on the data returned by a dangling pointer could change important information and cause problems in other areas of your program.
	
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
-----
A destructor is used to deallocate memory that was previously allocated. It is essentially the opposite of a constructor. Destructors are needed to prevent memory leaks because they give programmers the ability to free up memory that had previously been allocated. Destructors are not needed in Java because Java manages your memory allocation and deallocation for you through a process called garbage collection. In Java the compiler is able to detect when allocated memory is no longer reachable and will then deallocated that memory for you. This is not the case with C++ and hence the need for destructors so that programmers have a way to deallocate memory. 

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?
-----
stuff here

* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.
------
stuff here

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
-----
stuff here

* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
-----
I would use a linked list to create a grocery list data structure. Using a linked list would give the data structure greater flexibility when adding, removing, or reordering the elements in the list. Some people prefer to have their grocery list written out in a particular order and with a linked list new elements can easily be added into any place in the list. The most common commands that you would use on a grocery list in my opinion would be adding or removing elements from the list and a linked list provides these methods with O(1) time instead of O(n). Constant time would help the thrifty shopper save precious milliseconds off adding or removing forgotten grocery items to/from their list.
	
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
------
stuff here

* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
-----
stuff here

* Zeitgeist Youtube Video
------
link here
