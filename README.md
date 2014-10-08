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
https://github.com/laufengd/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
https://github.com/laufengd/04_Linked_List_Lab/blob/master/LinkedList.h

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
* In an Array-Based list, add() and remove() take O(n) operational time because the items in the list need to be shifted in order for more items to be added.
Array-Based size(1), get(1) and set(1) run in 0(1) time. For Linked lists, getNode(i) takes O(1+ min{i, n-i}) time, other than that all the other
functions run in O(1) time.
* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* Call Stack: A Stack data structure on the computer's RAM that is used to store parameters and local variables for the subroutines of an active program.
* heap: A data structure on the RAM used for storing dynamically allocated variables
* Address: A location on the RAM where data is stored denoted by a number and can be referenced or pointed to.
* Pointer: An object that points to an Address on the RAM

TODO: Answer the following questions about memory management and dynamic variables

* A memory leak is when data stored on the RAM can no longer be accessed and therefore takes up unnesesary space
* A dangling pointer is a pointer that references an address of an invalid data type and often times is the result of when data in a address is deleted or deallocated without deleting the pointer.
These are dangerous because often times other data can fill into the address being pointed to and cause the code to break.
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java? Destructors deallocate memory and delete dangling pointers.
Java does not need destructors as much because the java compiler is very good and figuring out when something is no longer in use and getting rid of it automatically.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* If I were to implement a data structure for a grocery list I would probably used a Linked list. Linked lists allow for more convenient adding and removing of items in between one another which is optimal
for when I think of things I want to add or remove at different times. In addition, if I were to use an Array-Based list, I would have to grow() the list if I added too many items, which would usually mean doubling
the size of my list. I would not want to carry an abnormally large list around the supermarket if I wasn't going to use all of the space on it.
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
