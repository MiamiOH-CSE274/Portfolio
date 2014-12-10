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
7 - Create an implementation of a List
----
	In the fourth lab I created an implementation of a list and here is the proof: https://github.com/SiegerJman/04_Linked_List_Lab/blob/master/LinkedList.h
7 - Create an implementation of a Binary Search Tree
----
	In lab 6 I created an implementation of a BST and here is the proof: https://github.com/SiegerJman/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
	In lab 5 I created an implementation of a hash table and here is the proof: https://github.com/SiegerJman/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
	In lab 7 I created an implementation of a heap and here is the proof: https://github.com/SiegerJman/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----	
	In lab 8 I created an implementation of an adjacency list and here is the proof: https://github.com/SiegerJman/08_Graph_Lab/blob/master/Graph.h

7 - Implement graph algorithms
----
	In lab 8 I added a depth first search and here is the proof: https://github.com/SiegerJman/08_Graph_Lab/blob/master/Graph.h

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List 
	Both Array and Linked lists have constant running times on their size methods. For get and set methods, they have different run times. For Array list it is constant time while
	Linked list runs in 0(N) time. For the add and remove methods Linked List runs in constant time because it runs based on iterators. Array list runs in 0(N) time for these methods
	because it runs on indexes.
* Binary Search Tree vs. Hash Table
	Hash tables run add remove get and set in O(1)time if created correctly. Hash tables run min max next and previous in O(N) time because they are unsorted and need to check each 
	value to determine the correct answer for these methods. BST runs all methods in O(lgN) time if it is a balanced tree or O(h) where h is the height of the BST.
* Adjacency List vs. Adjacency Matrix
	An adjacency matrix has a value for all possible combinations of edges and thus uses more memory than an adjacency list.
	Matrix		List
add	O(1)		O(n)
remove	O(1)		O(n)
get	O(1)		O(n)
set	O(1)		O(n)
more accurately the run times of the list are O(m) where m is the maximum number of edges involing ther same point.

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

* The call stack (not to be confused with the stack data structure!)
	The call stack is the data structure that stores the data tree of active methods in the program and then gives variables with the same name priority if they are higher in 
	the stack.The call stack contains pointers to the heap where the values of the variables are stored.
* The heap (not to be confused with the heap data structure!)
	The heap is the allocation of memory where new dynamic data values are stored to be refrenced from the call stack. These values are removed as they become become irrelevant in the stack.
* Address
	An address gives the location to an object.
* Pointer
	A pointer contains the Address for an object.

* What is a memory leak, and why is it bad?
	A memory leak is where data is unused but still allocated so that eventually all memory is taken but not used.
* What is a dangling pointer (or dangling reference), and why is it dangerous?
	A dangling pointer is a pointer that points to unallocated data. It is dangerous because it gives whatever value was left in the address and can lead to un expected and unwanted results.
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
	A destructor uninitializes an object and frees up the memory of its location. It isnt necessary in Java because Java has a built in garbage collector that deconstructs objects automatically.

5 - Create collection classes using templates in C++
----

What is the main benefit of using templates when creating collection classes?
	A template allows the collection for different data types without rewriting the code for the new data type.
In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.
	This isnt the case in template based collection classes because the declarations will be different based on how the template is defined at run time.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each) 
//these are substantial essays and should probably have run time tables.

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
	The best answer would be a hash table. This way order is irrelevant so the long run times for min, max, next and previous are irrelevant. 
	Add remove and set all run at constant time. Add can be written in such a way that it wont add duplicate values into the hash table if they are already there. 
	The only potential downside to this would memory management. Adding large amounts of strings could lead to longer run times from grow as compared to something like a vector 
	that can change its size very efficiently. A vector would have a lot longer running time when it comes to adding new values O(n) due to the need to make sure it isnt already
	in the vector.
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	The important methods for this data structure are add, remove, and priority (for aisle number). One solution for this could be using a hash table sorted by priority. add and remove are constant time
	which is good. The hash table is sorted by priority so when the list is displayed it just needs to be printed in the order it is in the hash table. One of the drawbacks of a
	hash table could be how much data it uses. Since the grocery list in all normal circumstances wont be longer than 20 items the memory required for the hash table cant be
	that large of an amount.
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	A heap would probably be the best data structure for banner numbers. This way, all memory is efficiently used (assuming banner numbers are numerical starting from 0). Add, remove, get, and set all run in O(1) time. This is
	vital in this usage because they are the methods that are going to be used the most.Inside the heap any data that could need to be applied to a particular banner number.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	A priority queue with priority associated with how much money was paid. This would allow the priority to be set based on the customers payment and from there the packets would
	be processed based on whatever was next in the queue.