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
https://github.com/schultjw/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
https://github.com/schultjw/04_Linked_List_Lab/blob/master/LinkedList.h

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
	Array-based lists can be accessed randomly, making them very efficient in their set and get methods (O(1)), but their add and remove methods create entirely new arrays,
		into which they copy all their data, making these less efficient at (O(n)). Link lists, on the other hand, are sequential, 
		meaning it is more expensive to use the set and get methods (O(n)), but they don't need to make a whole new data structure in add and remove,
		instead they can just change a few pointers making it very efficient (O(1)).
* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!)
	The order in which functions are run, when the main method calls a function, it stacks that new function on top of itself,
	and the stack is always resolved top-down, so that the last function called resolves then the one that called it resolves and so on.
* The heap (not to be confused with the heap data structure!)
	A pool of memory used for allocation. When the 'new' operator is used, memory is allocated from the heap.
* Address
	The location in memory of any piece of data.
* Pointer
	Stores the address of another variable, making it directly accessible through dereferencing. 

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?
	If 'new' is used, but there is not a 'delete' to balance it, the mheap will run out of memory to allocate eventually. This is bad.
* What is a dangling pointer (or dangling reference), and why is it dangerous?
	A dangling pointer is a pointer that doesn't actaully point to anything (and a dangling reference is something that is no longer pointed to.)
	These are useless to us and waste memory space, slowing everything down.
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
	A destructor deletes all remaining 'new' objects so that the memory can be returned to the stack.
	Java has automatic garbage collection so anything it sees is unused from that point on is automatically returned to the heap.
5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	A LinkedList data structure would suffice for a Grocery List. A LinkedList porceeds sequentially, just as a person would look down the list.
	If something was forgotten and needs to be added, LinkedLists can handle that efficiently. When a item is found and placed in the cart, 
	the LinkedList can remove that item without any trouble as well. The only limitation is being unable to scan the entire list easily, but with a LinkedList with enough open space,
	it is easily possible for all the items to be sorted so that they are near one another in the store.
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
