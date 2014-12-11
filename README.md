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
The link below proves that I can implement a C++ Queue Data Structure that utilizes a circular-array.
https://github.com/GrasysER/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
The link below proves that I can implement a C++ List Data Structure.
https://github.com/GrasysER/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
The link below proves that I can implement a C++ Binary Search Tree.
https://github.com/GrasysER/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
The link below proves that I can implement a C++ Hash Table.
https://github.com/GrasysER/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
The link below proves that I can implement a C++ Heap.
https://github.com/GrasysER/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
The link below proves that I can implement a C++ Adjacancy List.
https://github.com/GrasysER/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
The link below proves that I can implement a depth first graph traversal. (Last method)
https://github.com/GrasysER/08_Graph_Lab/blob/master/Graph.cpp

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List

An Arraylist is generally faster for most uses. Arraylists support random access and keep track of each spot in the array. This allows for very fast manipulation of already present data. For adding and removing data, arraylists are much slower, due to having to recreate the arraylist if the array is nearing capacity, or having to shift elements over when removing. Linked lists are very slow when accessing or removing already present data, due to having to iterate over the entire linked list. On the other hand add is very fast as linked lists never have to be resized and use pointer manipulation to add data anywhere in the list. Linked lists become much better with the use of iterators as get, set, add, and remove all become O(1) by providing direct access to a node through an iterator. When adding and removing at the front or back, both arraylists and linked lists are constant time. 

star means at an iterator.
f/b means at front or back

                        Arraylist | Linkedlist
         add               O(n)         O(1)
         remove            O(n)         O(n)
         remove(*)         O(n)         O(1)  
         get               O(1)         O(n)
         get(*)            O(1)         O(1)
         set               O(1)         O(n)  
         set(*)            O(1)         O(1)    
         add/rem(f/b)      O(1)         O(1)  


* Binary Search Tree vs. Hash Table

Both the binary search tree (BST) and the hash table are examples of the dictionary abstract data type which stores (key, value) pairs. Through hashing, hash tables run in constant time for add/remove and get/set. Provided that a BST is balanced, run times are O(log n) for most operations, with run times degrading to O(n) if the BST is unbalanced. Hash tables suffer in the min/max and next/prev operations due to the hash table having no real structure to it, resulting in O(n) for those operations. A binary search trees nodes store the nodes children, which allows for min/max/next/prev to all run in O(log n) time by calling the nodes children to traverse the BST.


                       Hash Table  |    BST
         add               O(1)       O(lg n)
         remove            O(1)       O(lg n)
         get               O(1)       O(lg n)
         set               O(1)       O(lg n)    
         min/max           O(n)       O(lg n)    
         next/prev         O(n)       O(lg n)  


* Adjacency List vs. Adjacency Matrix

n = # of nodes
m = # of edges
d = max degree of graph

Adjacency lists and matrixes are used to represent the graph abstract data structure. An adjacancy matrix uses a 2D array to represent edges between rows and columns. Due to the ability to access a particular spot in the 2D array, adjacancy matrixes have O(1) add/remove edge and get weight. Adding a vertex is slower at O(n*n) because the 2D array might have to be grown in size and the old arrays values copied over to the new array. Adjacancy lists use an array of nodes, with the nodes acting as a list of connecting edges. Adding an edge, vertex, or getting the neighborhs runs in O(1) time due to the ability to access any spot in the array, then simply adding the edge/vertex to the end or returning the neighborhs. Removing an edge is slower due to the array not knowing if the edge exists or not, which requires iteration over the edge list, resulting in O(d) run time. Getweight is also O(d) due to the need for iteration over the adjacancy list to find the weight. Adjacancy lists are prefferable when the number of vertexes is low due to the space requirements being O(n+m) versus an adjacancy matrix which requires O(n*n) space. An adjacancy matrix is only preffered for storage of large amounts of data, such as the US highway system connections.

                         Adjacancy List | Adjacancy Matrix
         removeEdge            O(d)            O(1)
         addEdge               O(d)            O(1)
         addVertex             O(1)            O(n*n)
         getWeight             O(d)            O(1)
         getNeighborhs         O(1)            O(n)    
         SpaceReq              O(n+m)          O(n*n)   
        
          

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!) 

The call stack in C++ is the portion of the RAM used for statically allocated variables. Variables in the stack only live as long as that particular variable stays in scope, or in other words while the funtion that created that variable is still running. The stack is a LIFO data structure and can grow too large, resulting in the popular saying "stack overflow".

* The heap (not to be confused with the heap data structure!)

The heap is a pool of memory used for dynamic memory allocation. When the new keyword is used, the object uses memory from the heap. Variables in the heap must be deleted with delete to prevent memory problems.

* Address

The location in memory of a variable. &, or the adress of operator, can be used to return the address of a variable by preceding the variable with &.

* Pointer

A pointer is a type of variable used for storing addresses.

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?

Memory leaks occur when memory is no longer in use, but still has information allocated to it.
Memory leaks slow down performance, introduce bugs to the program, or in the worst case scenario, result in the program crashing due to insufficient free memory. 

* What is a dangling pointer (or dangling reference), and why is it dangerous?

A dangling pointer is a pointer that points to unallocated memory.

Dangling pointers are dangerous because they introduce bugs to programs without crashing them, and can also create security risks if the dangling pointer is used to access other data or overwrite memory.

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?

Destructor's are used to free up memory that is no longer in use, which prevents memory leaks by deleting variables and other data that are no longer needed/in use. Destructor's are necessary in C++, but not Java because objects in Java automatically clean up after themselves by checking the heap to see if the object is in use. If  the object is no longer in use, the object is deleted. C++ does not run automatic garbage collection and leaves it up to the user to manage memory.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?

The main benefit of using templates for creating collection classes is that a template allows for typesafe collection classes. Typesafe collection classes work with any type of data, bypassing the need to create many specialized classes for each type of data.

* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

The compiler must know both the template definition and the type of data to fill in the template. When the compiler gets down to the .cpp code it must already know both or else the compiler won't know what to do with the .cpp code. In other words, the compiler must know the type, so we have to include the whole source code. 

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.

A hash table would be a very easy way to accomplish what is asked for in this problem. We do not know how many strings we will need to store, but a hash table grows as more data is added, which is very useful for something like string storage. Seeing as the only requirements are add, remove, checkExists, and for the data structure to be a set, a hashset is the obvious choice. 

Returning the min/max and next/prev is not required which eliminates the only major weakness of a hashset. All other operations for a hashset are O(1), which would make the string storage very fast. The other major requirement is also met, as a hashset does not allow duplicates. Since there are no duplicates, adding each string would run in O(1) by hashing each string then placing the string at the location specified by the hash value. Finally, remove and checkExists would also run in O(1) time by hashing the index for the string, then using that index to remove or check the string located at the index.

* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

A grocery list keeps track of a list of items to buy at a store. My grocery list would be designed as an application for a cellphone, and nowadays even the weakest cellphones have enough memory for a grocery list app. A grocery list will never get bigger than a few hundred items, thus efficiency is not important, as even the slowest data structure will be very fast at operating on such a small number of items. The operations supported by the data structure is the most important point to consider. A good cellphone application must also have an easy to use GUI that is backed by a data structure that supports any operation that the user would want to do with that particular application.

With all of that said, a doubly linked list would be a great option for a grocery list. A doubly linked list uses pointers to point to the next and previous item, and thus would allow the user to easily update the grocery list as it is used through pointer manipulation. My application would allow users to click in between two items in their grocery list, which would allow the user to enter in a new item anywhere in the list. If the user wanted to cross off an item from the list, the user would simply drag the item to either side, which would remove the item. Usability is very important with a grocery list, and a doubly linked list supports all of the operations needed for a grocery list while also being fast.


* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

The major requirement asked for by this question is for the ability to look up students by their banner number. 

* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

BST
