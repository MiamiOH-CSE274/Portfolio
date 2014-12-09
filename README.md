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
Link: https://github.com/MabeCr/03_Queue_Lab

7 - Create an implementation of a List
----
Link: https://github.com/MabeCr/04_Linked_List_Lab

7 - Create an implementation of a Binary Search Tree
----
Link: https://github.com/MabeCr/06_BST_Lab

7 - Create an implementation of a Hash Table
----
Link: https://github.com/MabeCr/05_Hashing_Lab

7 - Create an implementation of a Heap
----
Link: https://github.com/MabeCr/07_Heap_Lab

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
Link: https://github.com/MabeCr/08_Graph_Lab

7 - Implement graph algorithms
----
Link: https://github.com/MabeCr/08_Graph_Lab

21 - Determine space and time requirements of common data structure methods
-----
For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

Array-based list vs. Linked List
	In an array-based list, the run time of get() and set() is O(1). However, add() and remove() are O(n).
	In a linked list, the run time of add() and remove is O(1) because you can use an iterator. This allows you to skip the iteration step, eliminating the O(n) 		once the iterator has been found. Get() and set() are both O(n). If you are keeping track of the size using an external variable, size() will always be O(1) no 	matter which option you chose to use.

* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Define/describe each of the following terms, as they apply to memory management in C++

The call stack - The call stack is a "buffer" that everything that needs to be handled gets placed in. As things are introduced, they are added onto the stack. As they 	get completed, they are removed.
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
1. What is the main benefit of using templates when creating collection classes?
	Using template collection classes allows someone to write abstract functions and variables in a way that makes them accessible to more than one 		variable type. If someone instantiates the template class somewhere else within the proje creates a separate version based on what the user has 	specified for that class.

2. In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes. 
	When you are instantiating a template, a new class is created by the compiler with the given template as th argument. This means that if a template 		class ReadMe uses the template <typename T>, and in a .cpp file ReadMe<int> is instantiated, a new class will be created. Every time the T parameter 	is used inside of this class, it ends up being compiled as an integer in that new class. Because of this fact, the compiler has to receive all the 		function definitions to be able to create the new class. If the functions are not defined anywhere in the header, the compiler will never be able to 	use them.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
	I am certain that using a hash table would be the best fit for this problem, since hash tables don't have to have an order and don't store 	duplicates. Hash tables also have add, remove, and a find function, which checks to see if the item is already the set. If you took the string and 		ran it through a hash function, the add, remove, find, and key exists functions would run in in O(1), making your program very fast at computing. 		Using an array or a linked-list wouldn't make that much sense, since the running time of the add, remove, and find functions would end up being O(n), since they have to check every slot in order to find what they are looking for. Hash table allows instant access, and generally seems like the 	best way to sort the strings.

If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	I would personally go with a linked list for a grocery list strictly based on the fact that the required functions that you would use the most would 	be O(1). Add() and remove() are both O(1), so as you pull things off the shelf, you can remove them from your list quickly and efficiently. I 			doubt you would need to use the find() function too often, so it just makes sense to use a linked list based on the fact that it does what you want 		to do in the fasted time. An array would end up having a ton of empty spaces on it, which is not very practical.

If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	I believe a hash table would be the idea way to do this. You could take a student's banner number, run it through a hash function, and the add, 		remove, and find functions would all be completed in O(1). Something to keep in mind is that a hash table cannot keep duplicate entries in it. This 		is not a problem though, as there should never be two students with the same banner number. The reason an array, which would be the fastest data 		structure in this situation, would not work (assuming the banner numbers are like they are at Miami University) is that they do not start at 0, and 		are not in any particular order. The index could just be the banner number, and finding the student's information would be as simple as calling the 		array at the index of their number. The array, in this situation, would be very inefficient at finding information. 

Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	If I was going to implement this network router, I would most likely go with an implicit binary tree. More specifically, I would set it up as a 	heap. I would choose this because it would allow multiple keys that have the same value to be a descendent or parent of each other. The higher the 	company pays to send their packets, the lower their key number would be. (For example, if X pays $20, they would get a key of 1. If Y pays $10, they 	would get a key of 2, and so on.) BubbleUp would end up with all the keys of 1 at the top of the tree, and then the keys would follow in descending 	order down the tree. This data structure is the best because there are no others that are as efficient at arranging the data from least to greatest, 	or greatest to least.
