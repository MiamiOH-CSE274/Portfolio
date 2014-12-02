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
https://github.com/XCCOOP/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
https://github.com/XCCOOP/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
TODO: Provide a link to your completed 06_BST_Lab OR ClosestStarbucks project (only if you used a search tree)

7 - Create an implementation of a Hash Table
----
TODO: Provide a link to your completed 05_Hashing_Lab

7 - Create an implementation of a Heap
----
TODO: Provide a link to your completed 07_Heap_Lab OR

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

	//TODO Talk about iterators (add at an iterator, add at an index)
		Tables

	Iterators are bookmarks keeping track of where you are in a data structure.  

	get an iterator for an index in array list O(1) in linked list O(n)

	Array list add remove O(n)

	get/set iterator

	get iterator front/back

	add/remove front/back
	
	In an Array-based list, get() and set() are faster and add() and remove() are slower.  In order to get or set something all you need is which element it is in the array and 
	you can read or write its data.  On the other hand in order to add or remove something from the middle of the list, you need to create a whole separate array and copy everything 
	from the old one over to the new one.  In Linked lists get and set take longer because in order to find where they are you need to start at the dummyNode and use its next and previous 
	variables.  Add and remove take less time because in order to cut or add something to the list all you need to do is change some next and previous variables to point to the new object
	and it's in the list.

* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!)

	//TODO Not the window!!!

	The call stack is a list of calls to different functions in your program starting from the operating system going all the way to wherever you currently are in your program.  

* The heap (not to be confused with the heap data structure!)

	The heap is a section of memory where dynamically allocated variable are stored.  Whenever an object is created with the new operator it is stored in memory here.  Anything created here must be deleted when no longer needed
	 or a memory leak will occur, where the heap runs out of memory and the program crashes.

* Address

	All variable are stored somewhere in memory. The location that an object is stored is its address.  An address can manually be given data and we can manually read data at a specific address.

* Pointer

	Pointers are a data type that hold address for objects that can't be interacted with in other ways.  When something like an array is created we also create a pointer to gain access to where it is stored in order to change and read the data stored there.

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?

	A memory leak us when a dynamically allocated variable is created and then not deleted when it is no longer in use.  The variable just sits in the heap taking up memory until the program closes or more likely, the program freezes or crashes from running out of memory.

* What is a dangling pointer (or dangling reference), and why is it dangerous?

	A dangling pointer is when you have a pointer pointing to something, say an array, and then delete the array.  You then have a pointer that just points to a random spot in memory that anyone could use and access data that might get stored in that spot in the future.

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?

	A destructor generally cleans up anything created with the constructor.  It deletes and dynamically allocated variables and removes any dangling pointers.  This is necessary 
	because without it no dynamic variables in the heap would get deleted and then you have a memory leak.  In Java this is done for you.  When something you have created goes 
	out of scope, that is there are no longer any references to it, the object is automatically deleted and memory is freed up for use again.


5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?
* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why 
  this isn't the case with template-based collection classes.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

	//TODO 
		---What is a grocery list
		---How to decide which data structure?
			---Efficiency? ---Lists aren't going to be that long that so runtime will not matter depending on datastructure.
			---What opperations they support?
			---Easiest acceptable solution!
			---Platform(computer(new/old), smartphone, paper)

	First lets assume that when you're writing your grocery list that you write it in order that the items are found in the store.  With this in mind I would use a linked list data structure when implementing the shopping list because the add and remove methods in linked lists are faster than those found in array-based lists.  With shopping lists the main functions you would 
	need are adding and removing to and from the list.  Another reason for a linked list is the ability to add a forgotten item directly into the middle of the list without creating a completely new list and copying everything over. 

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
