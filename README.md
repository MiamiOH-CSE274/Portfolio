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
I have created a working queue program and my evidence is my ArrayQueue.ipp file.
https://github.com/dieterc2/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
I have created a working linked list data structure and my evidence is my LinkedList.h file.
https://github.com/dieterc2/04_Linked_List_Lab/blob/master/LinkedList.h

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
	The biggest differences that array-based lists and linked lists have between each other is that the linked list does not use an array to store data while the array-based list does. In terms of running time, they 
	experience different runtimes for most operations because of their structures and how the program can access each data set. In the array-based list, for example, the add and remove funtions take O(n) time because 
	it has to iterate through the array to find which element to take out. The worst case run time would be dependant on every element in the array. In contrast, the add and remove functions of the linked list take 0(1)
	time because adding and removing do not depend on the number of elements in the data structure. Instead, node surgery is done on the list at a single point so that all of the other data sets do not have to be moved. 
	The get and set methods of a linked list do take 0(n) time to complete though because the program needs to iterate through the arrays in order to find the correct node to operate on. This is different than in the 
	array-based list because the program can access array elements with the preset array functions. This allows for 0(1) runtime for get and set functions in array-based lists. Finally, both the array-based list and the
	linked list have a size function with 0(1) time because all this function does is return a counter variable that is updated elsewhere in the program. 
* Binary Search Tree vs. Hash Table
	Like the main difference between array-based lists and linked lists, one of the major differences between the binary search tree and the hash table is that the hash table uses a backing array while the binary search 
	tree uses nodes. Moreover, additions into the hash table require a hash function, and are not sorted upon entry (instead, the hash function computes an index in the array). This creates 0(1) run time because adding at 
	an index in an array takes constant time. For the binary search tree, additions are made with regards to keeping the tree sorted. A node is first compared to the root node to see if it is larger or smaller, and then goes 
	down the directed path, effectively eliminating one half of the root’s sub-tree that it is currently being compared with. This takes 0(lg(n)) time. For remove, the hash table also takes 0(1) time if given a key, because 
	the hash can be performed on the key, finding the exact index at which the key is stored. The binary search tree still takes 0(lg(n)) time because  	of the time it takes to find the key of which to delete. This is done 
	by progressively going down a branch of the tree, comparing the key with a root and then proceeding down one of the roots’ sub-tree’s branches. This process of finding the key on which to operate is also why get and set, min 
	and max, and next and previous are 0(lg(n)) time, because at most half of the nodes must be touched upon to find the key. Hash tables run get and set in constant time because of their ability to compute the exact index of the 
	key in the array, but run min and max and next and previous in 0(n) time because of the unsorted nature of the hash table. Every value must be compared with the picked key in order to ensure that the right next or previous key 
	has been chosen. Finally, the min and max of an unsorted array can only be found by touching on every node, which is why hash tables have bad run times for these operations. 
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!) - The call stack is a special portion of memory that the program uses during runtime. As the instructions from the program execute, local variables, parameters,
	and functions all get stored within this part of memory. It is a last in first out stucture, so as variables get stored and executed, they are popped off the list as soon as they are not needed anymore. This allows for their
	memory locations to be overwritten. A stack overflow can occur if the program puts more information into the stack than what it was originally allocated. 
* The heap (not to be confused with the heap data structure!) - The heap is a portion of free memory for the program that is used to store dynamically allocated variables. Anytime the program delcares a new object, memory
	is allocated from the heap because that is where the free memory is stored. Once an object has been properly deleted, the memory is returned to the heap.
* Address - This is the actual location of where the data is stored in memory. For example, the address of a string variable 'c' could be 6626. 
* Pointer - A pointer is a type of variable assignment that stores the address of a variable. Any type can be a pointer, though a star must be added at the end to show it as a pointer. 

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad? A memory leak is when parts of the program have not be deallocated after they are used. So even if the program is finished running, the part in memory where the objects were stored would still
	be in use, not allowing that reserved memory to be overwritten. Memory leaks are bad because they cause the computer to use more memory than it has to, eventually causing the the RAM to run out entirely and rely on the hard disk to 
	store information.
* What is a dangling pointer (or dangling reference), and why is it dangerous? - A dangling pointer is a pointer that does not point to a valid object or data, in that what was stored in memory has been deleted (leaving the pointer behind). These are
	dangerous because they take up space in memory and can lead to unpredictable behavior in the program. Specifically, if the pointer is called to perform functions, many bugs will arise because the pointer is pointing to nothing. 
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java? - A deconstructor is a function that deallocates the memory that was used to store new objects and other parts of the program.4
	They are necessary in C++ because the language does not automatically deallocate memory when the program is done with it. We do not need these in Java because the JVM is smart enough to know when dynmically allocated variables have reached
	their lifespan and deletes it at this point. 

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++
* What is the main benefit of using templates when creating collection classes? - One of the main benefits of using templates for collection classes over using classes is that a template can be created to accept any data type unlike classes which
	have to be specialized to handle different types of data. Also, templates are typesafe because the compiler knows the data types before compile time, so it can check for errors before they occur.
* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes. - This is because whenever a template class is instantiated within a .cpp file, 
	a class is created with the argument of the template. When this class becomes instantiated, the compiler will have to find out where the private functions and variables are to create the class with the template arguments. Thus, it will look in the	
	.h file that is included with the program. Without the inclusion of the template within the .h file, the compiler will not be able to find the private functions and variables of the newly instantiated class. 


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	I will first define a grocery list as the model I have been using all of my life. I start out writing each individual product on its own seperate line, starting at the top. Then, at the grocery store, I start at the top of the list and work my way down. This resembles a first in first out queue. If I remember
	a product that I had previously forgot, I add it to the bottom of the list, though this is a rare scenario. Because I place more importance on removing items from the top of the list than anything else, I would choose to use a linked list because it offers the fastest runtimes for the add and remove functions. This
	also works well if I have to add something on at the end, because I can do that in real time as opposed to an array-based list where I would have to iterate through all n items. Although the runtime of get and set in the linked list are slower, the cases where I modify the details of any product in my list are extremely rare
	so those functions would probably never be called. Thus, the linked list offers the best solution to the grocery list because of its fast add and remove functions. 
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
