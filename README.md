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
https://github.com/dazeycm/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
https://github.com/dazeycm/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
https://github.com/dazeycm/06_BST_Lab

7 - Create an implementation of a Hash Table
----
https://github.com/dazeycm/05_Hashing_Lab/blob/master/HashTable.ipp

7 - Create an implementation of a Heap
----
https://github.com/dazeycm/07_Heap_Lab

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/dazeycm/08_Graph_Lab

7 - Implement graph algorithms
----
TODO: Add a graph traversal (DFS or BFS) to 08_Graph_Lab and provide a link

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* **Array-based list vs. Linked List** - Generally, an array will allow for faster look up in most cases. This is because arrays support random access, and if you want to get or set a value in a certain index, it's trivial to pull up that element and make changes to it. The problem with Arrays is that to add and remove requires the shifting of data, resulting in a runtime of O(n). Linked list initially don't seem much better. To find something in a Linked list you have to traverse through possibly every node, meaning O(n) time, to find a value. To get or set a value you have to first find it, and then return it. To add or remove nodes, you also have to find it first and then make the changes. This can be remedied, however, through the use of iterators. If you have an iterator to a node in a Linked List, get and set can be done in constant time. Add and remove can also be done in constant time, greatly improving the efficiency of the Linked List Data structure.   

  |              | Array | Linked List |
  |--------------|-------|-------------|
  | Find (Value) | O(n)  | O(n)        | 
  | Find (Index) | O(1)  | O(n)        |
  | Get/Set      | O(1)  | O(n)        |
  | Get/Set (Iterator) | O(1) | O(n)   |
  | Add/Remove   | O(n)  | O(1)        |
  | Add/Remove (Iterator) | O(n) | O(1)|
  
* **Binary Search Tree vs. Hash Table** - Both binary search trees and hash tables store key value pairs, making them dictionary data structures. Binary search trees must uphold a certain structure and set order, while hash tables allow for fast indexing of values by hashing them. Overall, a hash table has a running time fo O(1) for most operations. Through hashing, it's very simple to find a a value in a hash table and make changes to it. A binary search tree is a little more tricky to navigate through. In general, for a balanced tree, the running time of most operartions will be O(log n). This is because a binary search is performed on the tree to find a value in order to make changes to it. One area that BST beat hash tables is in Min/Max and Next/Prev. Because BST have an order and structure to them, finding the next node is as simple as finding the node and then looking at its children, while in a hash table, which has no order, you have to iterate over the entire set of data. Similarly to find the min or max you just have to continually navigate one direction through the tree until you find the end, while in a hash table you need to check every single element. 

  |             | HashTable | BST |
  |-------------|-----------|-----|
  |Find|O(1)|O(log n)|
  |Set|O(1)|O(log n)|
  |Add/Remove|O(1)|O(log n)|
  |Prev/Next|O(n)|O(log n)|
  |Min/Max|O(n)|O(log n)|
  
* **Adjacency List vs. Adjacency Matrix** - Both an adjaceny list and an adjacency matrix are used to represent a graph abstract data type. An adjacency list is comprised of an array of nodes, each containing a list of it's edges to other nodes. An adjacency matrix is a 2d array, where each space in the array is a possible edge between the row and column node. The adjacency matrix has the benefit of being fast when modifying edges and querying the data. It's major downfall lies it its size and adding new vertex. The size of the matrix will always be O(V^2) because of the 2d array structure. Additionally, to add a new vertex, since the matrix is an array, you need to grow the array and then move the data around resulting in a time of O(V^2). Adjacency list support the quick addition of new vertex and edges by simply pushing them to the end of the current node array or edge array. Removing an edge in an adjacency list is a little more complicated because you have to iterate through the entirety of the edge list to see if it exists before deleting it. Ajacency list are often used when dealing with sparse graphs because their storage is much lower at O(V + E). If the data was more dense then an adjacency matrix would be used because more of the edges would be populated, resulting in less wasted space.

  |         |Adjacency List| Adjacency Matrix|
  |---------|--------------|-----------------|
  |Add Vertex| O(1) | O(V^2)|
  |Add Edge| O(1) | O(1)|
  |Remove Edge| O(E) | O(1)
  |Get Weight| O(V) | O(1) |
  |Space| O(V + E)|O(V^2)|

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----


* **The call stack** - The stack is an area where, when we run our program, all of the local variables and functions are stored and ran. This is done in a LIFO order.
* **The heap** - The heap is the area where we can dynamically allocate memory. This data in C++ is initialized using the `new` keyword and then must be deleted using some variation of the `delete` keyword. There is no set order of data storage in the heap.
* **Address** - The address of a variable is where that variable is stored in memory. The address of a variable can be obtain by using the `&` reference operator. 
* **Pointer** - A pointer is an object that points directly to another value's memory address stored somewhere in a computer's memory.

* **What is a memory leak, and why is it bad?** - A memory leak occurs space is allioted in memory but then never freed. This could potentially cause you to run out of space for memory.
* **What is a dangling pointer (or dangling reference), and why is it dangerous?** - A dangling pointer is a pointer that references  a space in memory that is no longer being used by our program. This is dangerous because the data could be overwritten and if the pointer is used, it will point to data that we did not intend it to.
* **What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?** - A destructor is a method that is called when an object is deleted. In this way, it is possible to deallocate space in memory, preventing memory leaks. They're necessary in C++, because the language has no means of automatically deallocating space. This isn't the case with Java, which has garbage collection, because data that is no longer being used it automatically freed **TODO: OBJECT CLEANS UP AFTER ITSELF**. 

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?
* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* **If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.** - I believe that a linked list would be the best data type available. Assuming that you group the objects next to each other on your shopping list in accordance with where they are in the store (as any sane person should), there is some order to the objects on your list. There is also the need to be able to add and remove items from the list as you aquire them and remember things you've forgotten. Since add and remove take O(1) time, it is quick and efficient to add and remove items. The time to get or set an item to the list would be O(n) time, but once you've added everything to the list, there won't be a need to look up the items in the list, as you'll always be getting the first item from the list which is constant time in a linked list **THOUGHT PROCESS: WHAT DO I THINK A GROCERY LIST IS? HOW SHOULD I DECIDE WHICH DATA STRUCTURE - EFFICIENCY, FIT TO PROBLEM (what ops do they support?), EASIEST ACCEPTABLE SOLUTION, RUNNING TIME WILL NOT MATTER BECAUSE.... THREE APROACHES 1. Efficieny doesn't matter 2. paper list 3. really old hardware <--first paragraph**. 
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
