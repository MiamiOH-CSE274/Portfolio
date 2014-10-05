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
I have created a queue in lab 3: https://github.com/busdiekc/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
I have created a linked list in lab 4: https://github.com/busdiekc/04_Linked_List_Lab/blob/master/LinkedList.h

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
	In a general array based lists are easier to work with but are less flexible than linked lists. In an array based list the get() and set() methods can be completed
	in constant time, O(1). However, the drawback to having constant time get() and set() methods is that the add() and remove() methods take linear time, O(n). When an
	element is added or removed from the array all other elements in the array must be moved backward one spot or forward one spot to accommodate the added/removed 
	element. This can be a time consuming process when the array that you are working with has thousands of elements in it. Linked lists are the opposite of array based lists
	in a sense. Linked lists require a bit more complexity to build but allow greater flexibility than array lists. In a linked list the get() and set() methods are completed in
	linear time O(n). Unlike the array lists, linked lists must iterate through each element in order to find the correct element being accessed. The time these two operations
	take depends on the number of elements in the list. The add() and remove() methods will take constant time, O(1), however. Because you need only change
	where a couple of the other node structures point to, the linked list does not need to move around the elements when a new element is added or an existing element
	is removed. Array based lists and linked lists will both be able to have the size() method run in constant time O(1) by keeping track of the number of elements using a
	variable that is returned by the size() method. In my opinion, array based lists are more suited for static lists. That is, lists that will not need to add and remove many
	elements but will require heavy use of the get() and set() methods. Linked lists would be better suited for more dynamic lists where the elements inside of the list
	will be frequently added or removed.
	
* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!)
	The stack is a section of your computer's memory that stores temporary variables. The cpu closely monitors the stack. Memory allocation and deallocation is
	done for you by the computer. When a program exits all of its associated variables are wiped and that memory is available to be used again.
	
* The heap (not to be confused with the heap data structure!)
	The heap is a section of your computer's memory that is not managed for you automatically and is also not as tightly managed by the cpu. The heap allows you to
	allocate memory without any restrictions on the size of the memory allocated as long as your computer has that much memory available. Using the heap also
	means that you must deallocate any memory that was allocated otherwise a memory leak will result. This means that memory is being used to store a variable
	that cannot be accessed by any programs.
* Address
	An address is the location in the computer's memory that the data of a variable is stored. 
	
* Pointer
	A pointer is a special variable that stores the address of another variable. The pointer can then be used to access that section of memory throughout a
	program. This allows you to directly change the stored data of a variable.
	
TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?
	A memory leak results when memory in the heap is allocated to a variable but then is never deallocated. The allocated memory remains unusable and is referred to
	as a memory leak. If this happens too much a computer can run out of memory and crash. 
	
* What is a dangling pointer (or dangling reference), and why is it dangerous?
	A dangling pointer points to memory that has already been deallocated. If you use a dangling pointer without realizing it the returned data will not be
	what is expected.
	
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
	A destructor is used to deallocate memory that was previously allocated. It is essentially the opposite of a constructor. They are needed to prevent
	memory leaks because they give programmers any easy to free up memory that had been allocated for a purpose. Destructors are not needed in
	Java because Java manages your memory allocation and deallocation for you. 

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
