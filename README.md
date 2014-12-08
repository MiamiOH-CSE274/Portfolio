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
https://github.com/richarkc/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
https://github.com/richarkc/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
TODO: Provide a link to your completed 06_BST_Lab OR ClosestStarbucks project (only if you used a search tree)

7 - Create an implementation of a Hash Table
----
https://github.com/richarkc/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
TODO: Provide a link to your completed 07_Heap_Lab

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

An array based list is faster in finding a specific element in an array and/or modifying a certain element due to its ability to
instantly access any element in the list, and so it can be done in constant time, compared to linear time in a linked list
due to having to actually loop through the list however a linked list will be faster in adding and removing elements and can do it
in constant time due to only having to edit the two elements around it to no longer point to that element, while an array based list must change almost the entire array to add or remove from the middle of the array. 

* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

* The call stack (not to be confused with the stack data structure!)

The call stack stores all statically allocated variables and any imformation relating to function calls (return address, parameters). Allows for fast and convenient access of memory.
* The heap (not to be confused with the heap data structure!)

The heap stores all dynamically allocated memory, i.e. any variables allocated with the new keyword, and requires manual memory management
* Address

An address is the physical location of a variable in virtual memory.
* Pointer

A pointer is a variable that stores an address and type of another variable in memory, so that you can pass that specific item around in code.


* What is a memory leak, and why is it bad?

A memory leak is an item in memory that no longer has any pointers to it. It is bad because it is occupying memory space that could be freed, and eventually could overflow your allocated memory and cause a crash.
* What is a dangling pointer (or dangling reference), and why is it dangerous?

A dangling pointer is a pointer to a point in memory that has already been deallocated. It is dangerous because you could still access that memory and cause errors, segfaults, and program crashes.
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why aren't they necessary in Java?

A destructor is a method that is called when an item goes out of scope, and is used to deallocate dynamic memory in that object, due to the fact the c++ does not have its own garbage collector. It is not necessary in java because java automatically collects that garbage when it goes out of scope.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?
* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

A doubly linked list with iterators would be the best data structure to store a grocery list. The reason being is that while shopping, one would have to frequently delete or add specific items within the list, and linkedlist provides the greatest efficiency for it, being O(1) for both those operations. By far, adding and removing will be the two most used operations and as such efficiency for those are the most important. An array, which also provides the same efficiency for those operations, has weaknesses in the case that people wish to change the order of the list, which could be potentially important for some people, as an array you must move all the other elements behind where you move the object, and you would also have to size the array fairly large so as to not overflow the bounds of the array or force you to resize it, where as a linked list only has space for all elements and the pointer to the next and last elements. With an iterator, it also allows for searching for certain items, but that operation will not be called very often, so it's not nearly as important. A grocery list also likely won't be very large, so storing extra space for something like a hash table, which also provides O(1) for adding, removing, and lookup, would be very inefficient in terms of space, so it wouldn't be a good choice, leaving a doubly linked list as the best available data structure.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

A hash table would likely be the best data structure for this problem, with the Banner number being the key and the record being the value. For this problem, we know that banner numbers are unique, so we are guarenteed a unique key, so a Hash table should provide O(1) performance when looking up, adding, or deleting. Assuming that looking up, adding, and removing will be the most common operations, we want the most efficiency with those operations. Since our keys are unique, with a good hash function and a properly sized backing array for our hash table, bucket collisions should be fairly low keeping our running times low. For collisions doing linear probing would probably be the best solution since collisions will likely be fairly low for given reasons. The only tradeoff for the speed of using a hash table would be space, however considering that space is fairly cheap and the person using this data structure would likely have a large amount of space to store all the student records to begin with, space is not a huge concern. This makes the Hash table the best data structure for this problem. If space is a concern, a binary search tree would also be a good option, providing O(log n) for the same operations, however only allocates the space that it needs for the items. The speed tradeoff, however, would likely not be worth it as O(1) is considerably faster than O(log n).

* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* 

