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
I have created a queue in lab 3: https://github.com/busdiekc/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
I have created a linked list in lab 4: https://github.com/busdiekc/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
I have created an implementation of a binary search tree in lab 6: https://github.com/busdiekc/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
(grow currently not working)
I have created a hash table in lab 5: https://github.com/busdiekc/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
I have created an implementation of a heap in lab 7: https://github.com/busdiekc/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
I have created an implementation of an adjacency list graph in lab 8: https://github.com/busdiekc/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
TODO: Add a graph traversal (DFS or BFS) to 08_Graph_Lab and provide a link

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List
-----
In general array based lists are easier to work with but are less flexible than linked lists. In an array based list the get() and set() methods can be completed
	in constant time, O(1). However, the drawback to having constant time get() and set() methods is that the add() and remove() methods take linear time, O(n). When an
	element is added or removed from the array all other elements in the array must be moved backward one spot or forward one spot to accommodate the added/removed 
	element. This can be a time consuming process when the array that you are working with has thousands of elements in it. Linked lists are the opposite of array based lists
	in a sense. Linked lists require a bit more complexity to build but allow greater flexibility than array lists. In a linked list the get() and set() methods are completed in
	linear time O(n) unless iterators are used. Unlike the array lists, linked lists must iterate through each element in order to find the correct element being accessed. The time these two operations
	take depends on the number of elements in the list. The add() and remove() methods will take constant time, O(1), however. Because you need only change
	where a couple of the other node structures point to, the linked list does not need to move around the elements when a new element is added or an existing element
	is removed. Array based lists and linked lists will both be able to have the size() method run in constant time O(1) by keeping track of the number of elements using a
	variable that is returned by the size() method. In my opinion, array based lists are more suited for static lists. That is, lists that will not need to add and remove many
	elements but will require heavy use of the get() and set() methods. Linked lists would be better suited for more dynamic lists where the elements inside of the list
	will be frequently added or removed.
	
* Binary Search Tree vs. Hash Table
-----
On average hash tables have O(1) running time for searching, inserting and deleting. The worst case scenario for searching, inserting and deleting are O(n). Binary search trees on the other hand have an average running time of O(log n) for searching, inserting and deleting. The worst case running times for a binary search tree are the same as the worst case running times of a hash table, which is O(n). The big differences between hash tables and binary search trees are the space that each takes up and how the elements are stored. In order for a hash table to achieve its average running times of O(1) it must have a large amount of space allocated. Usually the space allocated for a hash table is twice as big as the amount of entries that will go into the hash table. The extra space is needed because there needs to be empty space for keys to be mapped to in order to distribute the entries throughout the hash table. Hash tables also suffer from collisions, which is when two different keys are mapped to the same place. When this happens the hash table's running time is negatively impacted because the solutions for dealing with a collision (such as linear probing) end up taking much more time than O(1). Collisions are unavoidable when using a hash table because there is not a perfect hashing function that we know of. Hash tables do not store the entries in any order either. This makes searching through the hash table for a specific entry slow if you do not have the key for the entry you are looking for. Binary search trees do not require extra space like hash tables. A binary search tree can be kept in a memory allocation that is only as big as the data in the binary search tree. The running time for inserting into a binary search tree will not suffer from collisions like a hash table. This will give a much more consistent running time. However, a binary search tree may need to bubble up a newly inserted element which will negatively impact the running time but bubbling up is generally not as slow as linear probing. Binary search trees store their entries in an ordered fashion. The left child will always be smaller than the parent and the right child will always be larger than the parent. Because of this searching through a binary search tree is much faster than searching through a hash table.

* Adjacency List vs. Adjacency Matrix
-----
An adjacency matrix provides O(1) running time when looking for a specific edge but suffers from large memory usage. The space that an adjacency matrix takes up is (n*n) which can be a considerable amount depending on the size of n. The adjacency matrix stores an entry, either true or false, for every node in the graph. This is the reason an adjacency matrix takes up so much space. However, because of this a specific edge between two nodes can be found in constant time. Getting a list of neighbours for a particular node is slow because the computer will have to look at all n nodes to get a complete list of neighbours. An adjacency list uses less memory but does not have the constant time look up for a specific edge. It does have a shorter running time for getting a list of neighbours to a particular node though because adjacency lists only store the nodes that a particular node is connected to rather than having an entry for every single node. 

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

* The call stack (not to be confused with the stack data structure!)
------
The stack is a section of your computer's memory that stores statically allocated variables. Memory allocation and deallocation in the call stack is done for you by the computer. When these variables leave the scope of the executing code all statically allocated variables are erased and that memory is available to be used again.
	
* The heap (not to be confused with the heap data structure!)
-----
The heap is a section of your computer's memory that is not managed for you automatically. The heap forces you to dynamically allocate the memory needed for your variables and allows you to allocate memory without any restrictions on the size of the memory allocated as long as your computer has that much memory available. Using the heap also means that you must deallocate any memory that was allocated otherwise a memory leak will result. This means that memory is being used to store a variable that cannot be accessed because it has gone out of scope.

* Address
------
An address is the location in the computer's memory that the data of a variable is stored at. 
	
* Pointer
------
A pointer is a special variable that stores the address of another variable. The pointer can then be used to access that section of memory throughout a program. This allows you to directly change the stored data of a variable without explicitly accessing that variable.

* What is a memory leak, and why is it bad?
------
A memory leak results when memory in the heap is allocated to a variable but then is never deallocated after the executing codes leaves the scope of that variable. The allocated memory remains unusable and is referred to as a memory leak. If this happens too much a computer can run out of memory and crash. A less serious problem would be slower performance of the running program.
	
* What is a dangling pointer (or dangling reference), and why is it dangerous?
-------
A dangling pointer points to a non-existant variable's address in memory. The variable has been deleted and does not exist anymore but the pointer that used to point to that variable's address has not been updated to reflected this change. If you use a dangling pointer without realizing it the returned data will not be what is expected. Operations on the data returned by a dangling pointer could change important information and cause problems in other areas of your program.
	
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
-----
A destructor is used to manually deallocate memory that was previously allocated. It is essentially the opposite of a constructor. Destructors are needed to prevent memory leaks in C++ because they give programmers the ability to free up memory that had previously been allocated. C++ lacks garbage collection and therefore it is the responsibility of the programmer to deallocate memory that is dynamically allocated. Destructors are not needed in Java because Java manages your memory allocation and deallocation for you through garbage collection. In Java the compiler is able to detect when allocated memory is no longer reachable and will then deallocated that memory for you. This is not the case with C++ and hence the need for destructors so that programmers have a way to deallocate memory. 

5 - Create collection classes using templates in C++
----

* What is the main benefit of using templates when creating collection classes?
-----
The main benefit of using templates when creating collection classes is that you can design your class without using a specific data type in the code. With templates you create a place holder data type that stands in for a real data type. This allows the collection class that you write to be used for different data types and the only thing that needs to change when using the same class for two different data types is the line of code used to construct your object.

* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.
------
The normal separation of declarations and implementation of methods cannot be maintained when using template classes because in order to instantiate a template class with a particular template argument the compiler needs to have access to the implementation of the methods. If these implementations are not in the header file then the compiler won't be able to instantiate the template. In order to circumvent this problem .ipp files are used to keep the declarations and implementations separate. The declarations of a template class's methods will remain in the .h file and the implementations of those methods will go into the .ipp file which is #included at the end of the .h file.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
-----
For this problem I am assuming that we will want to keep track of the number of times a string appears without adding duplicate entries to our data structure. Adding duplicates of a string would use more space than just storing the count along with the string. I am also assuming that we don't need these strings in any kind of specific order. With these conditions in mind, I believe that the best way to store our set of strings would be to implement a set using a hash table. In our hash table the key will be the string that is being stored and the associated data will just be the count of that string's frequency. By using the set abstract data type we are ensuring that no duplicate entries are going to be added. With the hash table, checking for duplicate entries is rather easy. If a string to be added maps to the same spot as an existing string and their keys are equal then we forgo the addition and instead update the count of the existing string entry. The operation of adding new strings will most likely be the most frequent action performed and the running time on average for adding in a hash table is O(1). As long as we have a good hash function and plenty of extra memory allocated we should be able to achieve a running time close to O(1). The main drawback to this setup is the large space requirements. Hash tables need a large amount of extra memory in order to perform their best but storage is relatively cheap in our economy so I believe the trade-off is worth it for the better performance. Searching for a specific string will also be quick because our searches will be based on the keys of our entries. Unfortunately trying to find a particular entry based on the data within an entry will take O(n) time because we will have to iterate through each entry in order to find what we are looking for. In summary I believe that the hash table will work best for this problem because we will have an easy and fast way to check for duplicates, search for a specific string, and the main disadvantage, which is taking up more space than other data structures, is not a big concern with storage prices as cheap as they are.

* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
-----
Grocery lists can be written in a variety of ways and the data structure that stores the items should be as equally as flexible. Some people write their grocery lists in a specific order while others just write items down as they think of them. The most frequent operations that will be done on this grocery list data structure in my opinion will be adding and removing items. These operations should therefore have a short running time. With these conditions in mind I believe that a list implemented as a doubly linked list will be the most appropriate data structure to store the grocery lists. A linked list lends itself to no particular ordering of its elements and it is easy to change the order of its elements. The flexibility of the ordering in a linked list will allow this data structure to meet the demands of different people. To change the order of the list the pointers of an element that point to the previous and next elements in the list will be changed instead of having to move the actual location that the element is stored at. This will make it easy to adapt the data structure if somebody wants to order their grocery list by location in the store, by price, or by food group, etc.. The linked list data structure will also provided a running time of O(1) for inserting new items to the list which will most likely be the most used operation. The second most used operation would be remove and this too has a running time of O(1). Unlike in a simple array where elements must be moved to accomodate the addition or removal of a new element a doubly linked list does not have to move an elements around. The pointers that point to the previous and next elements are all that need to be changed which makes this data structure ideal for inserting and removing items in an arbitrary order. In summary I believe that a doubly linked list is the best choice of data structure as it will provide a flexible framework for the differing preferences of grocery list creation while having constant time running times for the two most frequent operations. 
	
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
------
Since searching will be the most used operation in this application the data structure that is implemented will need to be able to search quickly. In my opinion the best data structure for this task would be a set implemented as a binary search tree. The binary search tree will use a student's banner number as the key for their entry and the rest of the information associated with that student will be the data that goes with the key. The structure of the binary search tree will make searching for a specific banner number run on average in O(log n) time. If the binary search tree is not properly maintained (that is we want a short and fat tree versus a tall and skinny tree), the running time for searching will be negatively impacted. A binary search tree orders its entries as a series of nodes with a parent node generally having two children nodes, a left and a right node. The key for each node is used to determine where the node will be placed in the tree. A left child's key is always smaller than its parent's key and a right child's key is always larger than its parent's key. Another advantage of the binary search tree is that it will not need extra memory allocation to make it run efficiently. This could be helpful when we're storing the information for thousands of students. 

* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue needs a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
-----
The main feature that this data structure will need to incorporate is a way to quickly differentiate between the packets so as to ensure that the next packet sent is the one who's sender has paid the most money. The data structure best suited for this task is a priority queue implemented as a heap. The heap is tree structure that orders the nodes so that the node with the highest priority is on top and will be the next one removed. In this case we will be using the amount of money a customer has paid as the priority ranking of the packets. This heap will prioritize the packets with the largest amount of money and will make sure that nodes with the largest payments are floated to the top of the tree so that they will be sent through the router before packets who's senders haven't paid as much money. The heap data structure is able to find the max, that is the node with the highest priority, in O(1) running time. The constant time for this operation will be invaluable for sending out packets on the router with minimal delay. 

* Zeitgeist Youtube Video
------
link here
