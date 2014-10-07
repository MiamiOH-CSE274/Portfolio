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
TODO: Provide a link to your completed 03_Queue_Lab

7 - Create an implementation of a List
----
Link to my 04_Linked_List_Lab: https://github.com/mccarts3/04_Linked_List_Lab/blob/master/LinkedList.h

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
* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!)
* The heap (not to be confused with the heap data structure!)
* Address
* Pointer

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?
* What is a dangling pointer (or dangling reference), and why is it dangerous?
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	- For grocery lists, where we add and remove elements as we acquire them throughout the store, the two most suitable data structures would be an Array List or a Linked List. I keep my grocery list on my phone, adding items I need throughout the week with no real concern for order.  As I walk through the store and get an item, I read through, find the item, and delete it from the list, leaving no "null" spots between two items.  The most important methods we would need for this grocery list are add() at the end of the list as I think of new methods, and remove().  I would choose Linked List for this grocery list task because adding a new element at the end runs in O(1) constant time.  All we do is create a new node, and make sure it points to the dummyNode and the previous one, and vice versa, which takes a constant, small number of steps, no matter how big the list gets.  If we used an ArrayList, we would run at constant time until our list gets too big for our array to hold, meaning we would have to call a separate grow() method, increasing our method to O(n) linear time, much less efficient for our task than a Linked List.  Remove() for a Linked List requires going from node to node through the list to find the item you just got, which takes O(n) constant time.  The main benefit of an Array List is a fast remove() method, but that only works if you have your list in order of the store's layout, otherwise you'll be running from one end of the store to the other to remove the first item off your list, making it significantly less efficient than a Linked List.  A Linked List also gives me the ability to have no gaps between items, because remove has the previous node to the item you want to remove point to the following item, therefore creating a nice, structured grocery list that is easily accessible and able to efficiently add items to the list and keep track of which items you already have.
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
