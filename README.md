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
Here is the link to the Queue I implemented: https://github.com/eaglesonA/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
An example of a List is in our Linked List Lab, in the header file, located here: 
https://github.com/eaglesonA/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
The link to the Binary Search Tree Lab:
https://github.com/eaglesonA/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
https://github.com/eaglesonA/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
A heap was implemented in our 07_Heap_Lab:
https://github.com/eaglesonA/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
An adjacency list is implemented in: https://github.com/eaglesonA/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
TODO: TODO: Add a graph traversal (DFS or BFS) to 08_Graph_Lab and provide a link


21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List
There are pros and cons to using Array Lists or Linked Lists. LinkedList is wonderful if you have a lot of items you need to add, and need to put those in a particular
order. The add and remove methods in a Linked List are constant time, much better than ArrayList's linear time. ArrayList, however, has the advantage in the get and set
methods, running with constant time, instead of Linked list's linear time. Getting and setting at an iterator is constant time for both data structures. An iterator keeps 
track of where you are in a data structure. So, getting, setting, and adding are constant time (except in ArrayList when adding at an iterator is still ilnear). 
		 Linked List |  Array List
size()  	|   O(1)     |	O(1)
get/set		|   O(n)     |  O(1)                                                                                 
add		|   O(n)     |	O(?)
remove		|   O(n)     |  O(?)
add & remove at	|   O(1)     |  O(1)
front or back	


* Binary Search Tree vs. Hash Table
 A binary search tree is a great data structure to store ordered lists, or information that needs to be inserted in a certain placed, or has to be retrieved by a given key. 
A hash table is made up of an array and a hash function, which is designed to assign data to spots in the array. A hash table is great
 for large amount of unsorted information. Unlike the binary tree which only creates as much space in the RAM as it requires as elements
 are added, the hash table takes up more memory space than elements added to it since adding to the table is more efficient than growing the table then adding to it. So, if wasted space is important and and the list is small it would be better to use a binary search tree. 
Binary search trees are also better if the contents of the tree need to be printed, because there are no empty nodes, and everything is in ascending order. Printing contents from a hash table takes more time, because every "bucket" in the array has to be checked to see if it's empty. That's why an area where a binary search tree is faster than the hash table is finding the minimum and maximum value in a set. Because the hash table is unsorted, without a key, it has to go through every bucket, comparing the value in the bucket to a variable of the lowest/highest value so far. A binary search tree's minimum value is the node at the farthest left point in the tree, and the maximum value is the farthest right. 
That being said, hash tables are much faster than binary search trees in almost everything else. It is constant time (O(1)) in find, add, delete, get, and set, while a balanced tree is on average O(log n). To pick which data structure is best depends on what kind of things the user has to do with it. For example, if there is a lot of searching (like a dictionary) a binary search tree would be better, but if there is a lot of data containing even more data, like a table containing gamer tags, holding high scores, achievements earned, and other player information, then a hash table would be better. 

* Adjacency List vs. Adjacency Matrix
An adjacency matrix is a 2D array with the dimensions of A x A. A graph is most helpful when trying to visualize a adjacency matrix.
 A 1 means there is an edge connecting the node (or vertex) in the column to the node in the row. 
   
   0 1 2 3  

0| 0 0 1 0 

1| 0 1 0 1

2| 1 0 0 1

3| 0 1 1 0 


<img src="m/ss1.png" alt="ss1" <br>
In this example there would be edges connecting vertex 2 to vertex 0. To find out if there is an edge (In code, in the table)
 we would use arr[2][0] to see if it returned a 1 or a 0 (in our example it returns a 1). 
An adjacency list is an array of linked lists.
 The number of vertices is the size of the array. The nodes in the linked list hold what vertices the ith vertex points to. Still using 
the example above, if we put it into an adjacency list we would get:

[0]-> 2

[1]-> 1 -> 3

[2]-> 0 -> 3

[3]-> 1 -> 2


An adjacency matrix takes up more space than an adjacency list, but it is much easier to search for a 
particular edge if you know the vertices. The reason to search for an edge would be to get its weight, and it would require an adjacency 
list to run check each node to see if it matched the vertices needed (O(n) running time). In general people tend to use adjacency lists 
because they don't use as much memory, and they tend to be faster. The adjacency list is constant time to add a vertex or an edge.The 
matrix runs 0(1) when its adding or removing an edge. It runs poorly when adding or removing a vertex (it's the number of vertices squared,
 so O(v^2). Removing anything is not very efficient, but not terrible in the adjacency list, with removing a vertex being O of the number 
of vertices and edges (O(v+e)), and removing an edge being O(e).
In conclusion, the adjacency matrix is amazing at searching, and adding 
or removing an edge, but is terrible when dealing with vertices. And the adjacency list is amazing at adding a vertex or an edge, but is
 just alright at searching, and removing a vertex or an edge.

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

* The call stack is the order in which operations get done. All commands (and local variables, objects, and operations) are stored in 
the computer's RAM. The stack is the reason we can perform recursive methods. It keeps track of everything we need, and puts it off to the
side, until it either runs out of space, or a command is performed. Once the function is completed all data is deleted from the stack.
* The heap is also stored in the computer's RAM. The heap is a giant space used for dynamic memory allocation. You can access any sort of 
information at any time from it, unlike the stack where there is an order of execution. It is the programmer's responsibility to delete
unused variables in the heap, because C++ will not do it for you (like Java does with the garbage collector). 
* An Address is the address of a variable stored in memory. It can be found using '&', and to access the value stored within that address of RAM 
you need to use a pointer. 
* As stated above, a pointer can be used to store the value of an address. Declaring a pointer involves a star; ClassType* foo (foo being the pointer).
Changing the value of the pointer would only require *foo="new value". 


* What is a memory leak, and why is it bad?
A memory leak is caused by programmers/developers not deleting variables they create in a function- so it is still accessible. It is important
to delete any objects not in use, so RAM isn't taken up by useless things. Also, since the data is still accessible it becomes a major
security issues, potentially allowing a breach, or random people getting into your information.

* What is a dangling pointer (or dangling reference), and why is it dangerous?
A dangling pointer is one that continues to point to an address after you delete the data that was there. To fix this, you would either delete
the pointer, or reassign it to point to data in use. 

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
This is called automatically (like how the constructor is called automatically). But instead of creating objects, the destructor
deletes them. This is where everything created and used in the function is erased, so there are no memory leaks (no one can access
items after the function ends). Java has something called a garbage collector, which deletes unused or data without pointers, for you.
C++ does not have this luxury, so it is done by hand. 


5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++
What is the main benefit of using templates when creating collection classes?
In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
My grocery list is the Notes app on my phone. In the app I am able to add, remove, and edit whatever I want. I can place certain things at various points in the list, and the “paper” is endless (the app doesn’t set a max of how many items I can have). Because of all these reasons, I would use a Linked List, since it will allow me to add items at any point in the list (I’m forgetful, and being in the bread section might remind me to get donuts). Also, if I start in a different part of the store (say I want to go clockwise), I can arrange my list easily to reflect my decision. If I find an item isn’t on sale, or is too expensive, I can delete it and there won’t be any blank spaces in my list. 

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
