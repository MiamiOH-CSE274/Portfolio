Portfolio
=========
Document completion of the course's learning outcomes.

Instructions
====
The goal of this is to make it very easy for me (or an employer, or a teaching assistant) to see whether or not you have mastered the material
of the class. The hope is that I would be able to grade your work without downloading and compiling your code. For labs, I can grade them by 
inspecting the code. For projects you must provide a video demonstrations of your programs. Some questions require essay responses.

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
https://github.com/XCCOOP/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
https://github.com/XCCOOP/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
https://github.com/XCCOOP/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/XCCOOP/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
Graph traversal in graph.cpp above ^^^

21 - Determine space and time requirements of common data structure methods
-----
For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times 
for different operations. (7 points each)

* Array-based list vs. Linked List
	
	In an Array-based list, get() and set() are faster and add() and remove() are slower.  In order to get or set something all you need is 
	which element it is in the array and you can read or write its data.  On the other hand in order to add or remove something from the 
	middle of the list, you need to create a whole separate array and copy everything from the old one over to the new one.  In Linked lists
	get and set take longer because in order to find where they are you need to start at the dummyNode and use its next and previous variables.
	Add and remove take less time because in order to cut or add something to the list all you need to do is change some next and previous 
	variables to point to the new object and it's in the list.
	
	All of this is true if you do not have any iterators.  Iterators tell you exactly where something is, for instance the spot in memory where 
	the third element of an array is.  They allow access to specific elements without having to take time to find them.  With an iterator, get 
	and set will both be the same speed but finding the address for the iterator (if you don't already have the address) in a linked list will still
	be slow.
	
	| Operations            | Array-based List | Linked List |
	|:---------------------:|:----------------:|:-----------:|
	| Get/Set               | O(1)             | O(n)        |
	| Get/Set w/Iterator    | O(1)             | O(1)        |
	| Add/Remove            | O(n)             | O(n)        |
	| Add/Remove w/Iterator | O(n)             | O(1)        |

* Binary Search Tree vs. Hash Table

	BST's and hash tables have the same worst case runtime for their main functions, searching, adding, and removing.  However on average a hash 
	table will have faster speeds than a BST.  The main difference between the two is in their layout and size.  A BST only needs as much space as 
	you have entries.  Each entry gets added to the tree and is either a parent leading to more entries or a leaf at the bottom of the tree.  All 
	of the children to the left of a parent are smaller than the parent and all to the right are larger.  When perfectly balanced this leads to very 
	fast search speeds.  In the worst case, every entry could be to one side or the other leading to slow speeds.  Hash tables however take up much
	more space than BST's do.  In a hash table you want to always have at least twice the space allocated then you have entries.  This allows for 
	minimal collisions (when two different keys map to the same spot in the table) and keeps the speed up.

	| Operations | BST                             | Hash Table                  |
	|:----------:|:-------------------------------:|:---------------------------:|
	| Get/Set    | Average - O(log n) Worst - O(n) | Average - O(1) Worst - O(n) |
	| Add/Remove | Average - O(log n) Worst - O(n) | Average - O(1) Worst - O(n) |
	
* Adjacency List vs. Adjacency Matrix

	One of the main differences between adjacency lists and adjacency matrices is the size they take.  A matrix is basically a 2d array with a spot 
	for every possible cost from one vertex to another.  Unless there are a lot of edges, most of the space is wasted.  A matrix does have very fast 
	speeds for most operations.  Because it has a specific spot for each cost, you can quickly add, remove, and get the cost for a particular edge.  
	One downside other than the size is that if you need to add vertex, creating a new 2d array takes a long time.  A list takes up much less space,
	only requiring as much space as vertices and edges.  If you know exactly how many vertices you will have and space is not an issue, a matrix will 
	give you faster results.  If you have limited space or it is unknown how many vertices you will have, a list will be slightly slower for most operations
	but will save time if adding a lot of vertices. 

    | Operations  | Adjacency List | Adjacency Matrix |
	|:-----------:|:--------------:|:----------------:|
    | Add Vertex  | O(1)           | O(V^2)           |
    | Add Edge    | O(E)           | O(1)             |
    | Remove Edge | O(E)           | O(1)             |
    | Get Cost    | O(V + E)       | O(1)             |

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!)

	The call stack is a portion of memory where local variables are stored.  It can be thought of as similar to the stack data structure 
	in that it is last in first out.  That is, when a function is called, it stores the return address and then proceeds to carry out
	the function, returning any data to the return address, and so on until the entire program has run its course.


* The heap (not to be confused with the heap data structure!)

	The heap is a section of memory where dynamically allocated variables are stored.  Whenever an object is created with the new operator
	it is stored in memory here.  Anything created here must be deleted when no longer needed or a memory leak will occur, where the heap
	runs out of memory and the program crashes.

* Address

	All variable are stored somewhere in memory. The location that an object is stored is its address.  An address can manually be given data 
	and we can manually read data at a specific address.

* Pointer

	Pointers are a data type that hold address for objects that can't be interacted with in other ways.  When something like an array is created 
	we also create a pointer to gain access to where it is stored in order to change and read the data stored there.

Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?

	A memory leak us when a dynamically allocated variable is created and then not deleted when it is no longer in use.  The variable just 
	sits in the heap taking up memory until the program closes or more likely, the program freezes or crashes from running out of memory.

* What is a dangling pointer (or dangling reference), and why is it dangerous?

	A dangling pointer is when you have a pointer pointing to something, say an array, and then delete the array.  You then have a pointer that
	just points to a random spot in memory that anyone could use and access data that might get stored in that spot in the future.

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?

	A destructor generally cleans up anything created with the constructor.  It deletes and dynamically allocated variables and removes any 
	dangling pointers.  This is necessary because without it no dynamic variables in the heap would get deleted and then you have a memory leak.  
	In Java this is done for you.  When something you have created goes out of scope, that is there are no longer any references to it, the
	object is automatically deleted and memory is freed up for use again.


5 - Create collection classes using templates in C++
----
Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?

	Templates allow you to create collection classes that do not depend on specific data types.  You write the collection class with a sort of 
	place holder data type that could be anything.  When the code is used, the user then specifies what data type the place holder is.
 	
* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why 
  this isn't the case with template-based collection classes.
  
	When the compiler looks at a template it creates a different version of the code for each data type that is trying to use the template code.
	In order to do this it needs to have access to every part of the code including implementations.  This is the reason some code has what would be 
	in the .cpp in a .ipp that is #included at the bottom of the .h file.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be 
  most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove
  items, and check to see if an item is already in the set.)
  
	With this application in mind I would probably choose a hash table for the data structure.  There is no order to a hash table, it does not store
	duplicates, we can search for a specific item fairly quickly and because so can add or remove an item just a quick.  In this hash table the key 
	and value would both just be the string we are storing.  When adding to the table, we would hash the string to find where in the array it goes 
	and see if it's already in that spot.  If it is already there then we don't need to do anything.  If something else is there we continue looking in
	other spots according to our collision strategy.  If we don't find the string we are trying to add, we go and add it in the first available location
	according to the hash and collision strategy.  Removing goes through the same process as adding instead we just mark the string to be removed as 
	"removed" to save time from actually deleting it.  If we have a good hash function and leave enough memory for our table, we should be able to achieve 
	a runtime of O(1) for every operation.  
  
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most
  appropriate? Carefully explain why.
  
	For this question I am going to assume that a grocery list is ordered by location of item in store, and that it will be written down on paper 
	and not coded on computer.  Lets say the average grocery list is about one page long.  Because the list is reasonably short, efficiency will not
	factor into deciding a data structure because the speed difference will be unnoticeable for all of them.  The main operation for the list would
	be adding items to it, but we might also need remove if we discover (after we've added it) we don't need something.  With all of this in mind I 
	would use something like a linked list data structure(Maybe a little too complex for just paper but the idea still works).  Adding and removing 
	would be fast because all that is needed is to write down or scratch out an entry.  Adding into the middle of a list (to keep ordering by location 
	in store) would also be fast because all you would need are arrows pointing from one entry to another and then back.  

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures)
  that we learned this semester would be most appropriate? Carefully explain why.
  
	Because of the speed needed for searching and the potential for a large number of students I would suggest a binary search tree for this problem.
	Assuming the tree is balanced properly, that is it's short and fat as opposed to long and skinny, it will have search speeds of O(log n) and will 
	only take up as much space as the number of students.  Each students Banner number would be stored in the tree as the key and any data that needs
	to be stored will be associated as the data for that key.  The speed comes in when searching because of the way a BST is ordered.  All Banner numbers 
	smaller than the one you're looking at are to the left and all larger are to the right.  This means you would only have to search though a handful of 
	possible entries before you find the one you're looking for.
  
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a
  special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent
  out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if
  X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

	For this instance the only data structure I see being appropriate is a priority queue.  You need to keep a list of all the packets waiting to be
	sent out over the network as well as which ones to send first (priority).  A packet would get added to the end of the queue(FIFO), and then its
	priority would get considered.  If it has a high priority it would get bumped up to the end of whichever priority it is.  This structure would ensure 
	that no packets from a company paying less would get sent out before any from a higher paying company got sent.  As long as a higher paying company's 
	packet is received before a lesser is sent, the higher will get sent.