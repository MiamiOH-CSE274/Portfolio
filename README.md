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
Link to my 03_Queue_Lab: https://github.com/mccarts3/03_Queue_Lab/blob/master/ArrayQueue.ipp

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
	- A memory leak is when memory that you have used in your program continues to remain even after your use for it has ended.  If you created an object or something in which you have not properly deleted or allocated it as usable memory, it will remain and not be reused by your program's limited memory, leading to the possibility of memory overflow.  This could crash your program if too much memory is leaked and not able to be reused, or lead to memory being accessible when it is not meant to be.
* What is a dangling pointer (or dangling reference), and why is it dangerous?
	- A dangling pointer is a pointer variable that no longer points to memory that is allocated in memory by the program.  If you delete the object or data the pointer references, but not the pointer variable, you can still use the pointer variable.  If the deallocated memory it points to is replaced by something else by the computer, the pointer variable will have extremely unpredictable results, most likely leading to a crash or misinterpretation of your program.
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
	- In C++, efficiency comes at a cost.  Lots of stuff under the hood in Java that takes extra time because it's just extra memory/security precautions is left out of c++ so the programmer only includes it when needed, making the code sleeker and faster.  Java includes the destructor, even when c++ programmers might not deem it necessary.  In c++, we must include the destructor when it IS necessary.  When we won't use things again, we call the destructor so that memory can be allocated again.  If we don't use the destructor, c++ won't automatically do it like java, and a memory leak (as described in the question above) will occur, as variables we aren't using anymore remain allocated in memory until eventually there is no available memory left. 

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
