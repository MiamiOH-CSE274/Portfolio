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
https://github.com/adammast/03_Queue_Lab

7 - Create an implementation of a List
----
https://github.com/adammast/04_Linked_List_Lab

7 - Create an implementation of a Binary Search Tree
----
https://github.com/adammast/06_BST_Lab

7 - Create an implementation of a Hash Table
----
https://github.com/adammast/05_Hashing_Lab

7 - Create an implementation of a Heap
----
https://github.com/adammast/07_Heap_Lab

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/adammast/08_Graph_Lab

7 - Implement graph algorithms
----
https://github.com/adammast/08_Graph_Lab
-Added a DFT method as well as a DFT helper method

21 - Determine space and time requirements of common data structure methods
-----

* Array-based list vs. Linked List
	Array-based lists and Linked lists each have their pros and cons. First off, the array-based list has quick set() and get()
	methods, each with a running time of O(1). This is because the array can quickly be told to look something up using the
	number that corresponds with that elements spot in the array. The array, however, takes a lot longer to do the add() and 
	remove() methods if the array is supposed to be ordered in some way. These methods take O(n) time. This is because in order
	for the array to put the element in the proper spot or remove an element from a certain spot, it may have to move quite a 
	few of the other elements in the array. Also, the array may need to be resized as arrays' sizes need to be specified upon
	creation. Linked lists on the other hand are much slower at the get() and set() functions. This is because linked lists
	need to travel from the beginning of the list every time to find a certain element in the list. This gives those methods
	O(n) time. Linked lists also need O(n) time to add and remove elements unless you use an iterator. One of the benefits of
	a linked list is that you don't need to resize it because it is dynamic. This makes it easier when adding a very large number
	of elements to the list. When comparing memory space for both, a linked list will take up more space because it has to keep
	track of the element's data as well as the pointers to the previous element and the next element whereas the array just keeps
	track of where the element is in the list and the data corresponding with that element.


* Binary Search Tree vs. Hash Table
	Hash tables are usually faster than binary search tress. Hash tables can do get() set() and remove() all in O(1) time. Binary
	search trees require O(log n) time for those same functions. The hash table requires more space, however, as it typically needs
	2x as much to avoid two elements hashing to the same spot. This still does not rule out the possibility of a collision to occur,
	in which case the running times for the hash table can increase dramatically. This all depends upon the hash function for the
	table and using a decent size. Binary search trees on the other hand only use enough space needed to hold all of the items in
	the tree. The binary search tree also has the advantage of all of its items being sorted, so it makes it quicker to retrieve
	the items within the tree all in order. This also allows for the next() and prev() operations to be quicker since the tree
	is already sorted.

* Adjacency List vs. Adjacency Matrix
	An adjacency matrix is good for finding whether or not a specific adjacecy exists. To do this, all you have to do is go to
	the element that represents the adjacency in the matrix and get the boolean that tells you whether or not it exists. Theproblem
	with adjacency matrixes is that they take up a lot of space. The matrix has to store all possible adjacencies. The list on the
	other hand only needs to hold all the existing adjacencies. A matrix can get a specific adjacency in O(1) time while a list has
	the worst case ofO(n) time, so a matrix is faster but potentially takes up a lot more space.


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

* The call stack (not to be confused with the stack data structure!)
	The call stack allows for fast access of memory. It stores all statically allocated variables and info related to function calls.
	For example,  parameters and return addresses.

* The heap (not to be confused with the heap data structure!)
	This stores all dynamically allocated memeory and requires manual memory management. For example, any variable allocated with
	the new keyword will be stored here.

* Address
	This is the physical location of a variable in memory.

* Pointer
	A pointer is a variable that holds a memory address. Using the address of an object, you can easily see what is stored there.


* What is a memory leak, and why is it bad?
	A memory leak is an item in memory that no longer has any pointers to it. It is bad because it is occupying memory space that
	could be freed for other resources. This waste of valuable resources in the worst case might cause a crash in your system, or
	simply slow it down.

* What is a dangling pointer (or dangling reference), and why is it dangerous?
	A dangling pointer occurs when you deallocate an object without dereferencing it. The pointer that used to point to that object
	still points to the memory location of that deallocated object. This can lead to unexcpected behaviour in your program or even
	potential crashes.

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
	A destructor is a method that is used in C++ to destroy in object that is no longer needed for whatever reason. This deallocates
	the memory that was being used by that object and prevents a memory leak. This is not needed in Java coding because Java
	automattically destroys all the objects that are no longer in use in your code.	


5 - Create collection classes using templates in C++
----

* What is the main benefit of using templates when creating collection classes?
	The main benefit of using templates when creating collection classes is that you don't have to make a class for every single
	data type. Instead what you do is make it general for all data types and then when you implement it you can specify which
	data type is going to be stored in that collection. This saves time as you don't need to write repeated code over and over
	again for each data type that you want to store within the collection.

* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.
	This is due to the fact that the compiler will compile a new class with the specified data type every time that it is 
	instantiated with that given data type.	So we have to put the code in the .h file in order for the compiler to be able to
	compile it. Another way around this is to put the implementations in a .ipp file and #include that file at the end of the
	header file.


20 - Using time and space analysis, justify the selection of a data structure for a given application
----

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
	I would use a hash table for this problem. I would use that because hash tables are fast at adding and removing items, which
	I'm assuming would be the main functions used in this program. The time for these in a hash table would be O(1). The hash table
	will also be able to check for the existence of a given key whenever another key is added to the set, which can be helpful. The
	problem with using a hash table is that it uses a lot of space because you want to avoid collisions between items in the set.
	In my opinion, the added speed of using a hash table outweighs the space issue though, so I would go with a hash table for this
	problem for sure.

* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	For this problem I'd use a doubly linked list. The reason for this is that I believe the most used functions for a grocery list
	would be the add and remove functions. I believe this because as you pick up something from the store, you'll always have to
	mark it off your list, or delete it. And whenever you think of something new you need form the store, you need to add to the
	list, so being able to add and remove things quickly seems very important for this problem. Luckily, doubly linked list does
	both of these funstions in O(1) time. Also, with a doubly linked list, you won't have to worry about the size of the list, as
	it is dynamic unlike an array where you'd need to resize the list every time the list outgrows the size of the array.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	I would use a hash table for this one as well, with the banner number as the key and the record being the value. Since banner
	numbers are all unique for students, we know we can use that as a unique identifier. Hash tables with unique keys have a time
	of O(1) for the add and remove functions as well as looking up certain elements. Assuming that these would be the most used
	functions, this would be very efficient for the user of this program.Of course, as usual, whenever we use a hash table, we need
	to make sure we avoid collisions. This would require that we have a good hash function and a properly sized backing array. This
	requires a lot of space, but gives you an advantage with speed. If space is an issue however, then I would go with a binary
	search tree as it only uses the neccessary space to store all of the items in the tree. The downside though is that the methods
	discussed earlier would be O(log n) time instead of O(1), so it would be much slower. If space is not important, the ideal data
	structure would be a hash table.

* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	I believe that the best option for this problem would be a heap implemented as a priority queue. Since priority is large factor
	in this problem, the priority queue would be perfect for this if we simply use money as the priority. Also, a heap is very good 
	at implementing a priority queue because of the fact that most of its functions run at O(log n) time except for looking up the 
	highest priority which is O(1) time. Also, it doesn't need to be fully sorted, just sorted so that all the objects of lesser 
	priority are below the node.

