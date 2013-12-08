Portfolio
=========

Document completion of the course's learning outcomes.

Instructions
====
The goal of this is to make it very easy for me (or an employer, or a teaching assistant) to see whether or not you have mastered the material of the class. The hope is that I would be able to grade your work without downloading and compiling your code. If you have recorded proper video demonstrations of your programs, that should be sufficient. You will also want to write a paragraph or so making your case for why you deserve full credit for particular learning outcome (or if you don't, then you should say so).

Important
=========
If you prefer, you may turn this in to me via email, instead of hosting it on GitHub. Please talk to me about it during office hours or before or after class.

Body of portfolio
====

7 - Create an implementation of a Queue
----
Possible sources of evidence (do any one of these):

I have accomplished this through my completion of the Queue Lab, found here. https://github.com/db4soundman/03_Queue_Lab/tree/blasedd


7 - Create an implementation of a List
----

I have implemented a List, specifically, a Linked List, in the Linked List Lab, found here. https://github.com/db4soundman/04_Linked_List_Lab/tree/blasedd


7 - Create an implementation of a Binary Search Tree
----

See my implementation of a BST: https://github.com/MiamiOH-CSE274/06_BST_Lab/blob/blasedd/BST.ipp



7 - Create an implementation of a Hash Table
----

See my implementation of a Hash Table: https://github.com/MiamiOH-CSE274/05_Hashing_Lab/blob/blasedd/HashTable.ipp


7 - Create an implementation of a Heap
----

See my implementation of a Heap here: https://github.com/MiamiOH-CSE274/07_Heap_Lab/blob/blasedd/Heap.ipp

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----

See my implementation of a Graph here: https://github.com/MiamiOH-CSE274/08_Graph_Lab/blob/blasedd/Graph.cpp

7 - Implement graph algorithms
----
Possible sources of evidence (do any one of these):

See my implementation of a depth-first search (incorrectly named “dijkstraTotal/dijkstraRecrusive”) here: https://github.com/MiamiOH-CSE274/Vise/blob/BlaseAndBickley/src/GameBoard.cpp


21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)

For the ArrayQueue (found here https://github.com/db4soundman/03_Queue_Lab/blob/blasedd/ArrayQueue.ipp ), the running times of the methods are as follows.

The constructor is constant time, since space is only being set aside to store data in the array, nothing is being added. The destructor is constant time as well, assuming that the `delete[]` method is constant. The two claims just made are true only if the data being stored in the Queue do not have defined constructors. If they do, then the constructor for the data is called as well, making those two methods have a linear running time based on the size of the backing array. `Add()` is constant time as well, unless `grow()` is called, in which case it's running time is based on `grow()` (see below). `Remove()` is constant time as well, since the first item in the queue is always removed from the array. `getNumItems()` is constant time, as the method only returns `numItems`. Finally, `grow()` runs in linear time since the items in the backingArray need to be copied to a new and larger array.

In terms of space requirements, the ArrayQueue only stores primitive data, so the largest space requirement is the size of the array.


For the Linked List (found here https://github.com/db4soundman/04_Linked_List_Lab/blob/blasedd/LinkedList.ipp ), the running times for the methods are as follows. 
	The constructor is constant time, as there is nothing that relies on the size of the list to execute code. 
	The destructor is linear time, despite the fact that the `remove()` is called. A while loop is used to iterate through the entire list, and the remove method is called within the loop, but the remove method is always removing the first item in the list, so this does not add to the running time of the destructor. As a result, the destructor runs in linear time.
	The `find()` is a linear (technically n-1) function except when the user asks for the very first, or very last, item in the list because I have an if statement that checks to see if the user is asking for the last item on the list, and if they are, it accesses the node that the dummyNode's `prev` points to and returns it. Otherwise it iterates through the list and finds the correct node.
	The `set()` method is the same running time as `find()` because a call to find is used to access the pointer of the node that the user wishes to change, and then it is returned (if found) to have its data changed.
	For similar reasons, `add()`, `remove()`, and `splice()` are the same running time as `find()` (linear), as all three methods have calls to `find()`, and then perform operations that are not based on the size of the LinkedList.
	`Size()` is constant time; it only returns the numItems variable.

For LinkedLists, the space requirement is based on the type of data being stored. Otherwise, the instance variables are an unsigned long, and Node* variables.

For Graph data structures (see the adjacency matrix version here: https://github.com/MiamiOH-CSE274/08_Graph_Lab/blob/blasedd/Graph.cpp ), the comparison is as follows.

An adjacency list consists of an array for each point in the graph, and each index of the array contains a linked list of all of the other points it intersects. With this method, you have instant access to any individual point, but the running time of finding a particular intersection is linear in terms of the number of edges that point intersects.

An adjacency matrix, on the other hand, is essentially a 2-d array (though, vectors are used), with a spot for each possible intersection in the graph data structure. Due to the array-like nature of the adjacency matrix, we have constant time access to both an individual point, and the intersecting point we are interested in, since we can go directly to that point instead of looping through each spot in the array.

Just from the above description, it sounds like the adjacency matrix is the hands-down better way to implement a graph structure. It’s not, due to the space requirements of the two options. With an adjacency list, the space requirement is the number of items (n) + the number of intersections (m), which would be the size of the linked list found at each index of the array. For the adjacency matrix, the space requirement is n^2, since every possible intersection is stored in the 2-d array. So, depending on the size of the data and the number of intersections any particular point can have, it is better to take the performance “hit” of the adjacency list to save large amounts of space on the memory/hard drive. If the number of intersections is brings the overall space requirement to be close to n^2, it is better to use an adjacency matrix to get the performance boost.


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.

In a LinkedList ( https://github.com/db4soundman/04_Linked_List_Lab/blob/blasedd/LinkedList.ipp ), the dynamic memory that is allotted are Nodes. Nodes are created in the constructor for the linkedlist (it creates the dummyNode), as well as in the `add()` method. In these two methods, `new` is used to create an instance of the Node, with its data being created in the Heap of RAM. The heap is searched for the contiguous space that is required to store the data initialized by `new`. As seen in the add method, the `next` and `prev` pointers within the nodes are updated appropriately to maintain the structure of the list and ensures that no data is lost in memory. The `remove()` method acts similarly, by updating the pointers before and after the Node being deleted so that the list remains connected. Once that has been done, `delete` is called, effectively freeing up the memory on the Heap that the Node was using. The destructor method calls `remove()` in a loop until all the nodes except the dummyNode is gone, and then calls `delete` on the dummyNode, freeing up all dynamically allocated memory back to the system.

The stack stores local variables and the stack of method calls (which are return addresses so the program knows where it left off). Any local variable not created with new is stored here until it goes out of scope, and is no longer accessible to the program once this happens.


5 - Create collection classes using templates in C++
----

https://github.com/db4soundman/04_Linked_List_Lab/blob/blasedd/LinkedList.ipp

Templates are a way of saving time when coding. This is the case because templates allow the user to create collection classes without specifying the data types of its instance variables. By doing this, the user can create an instance of the collection class using any class type they need to use, and at compile time, the compiler creates a new copy of the class with the types of the instance variables specified by the user filled in to the file of the collection class. If the compiler didn’t do this, the programmer would have to copy and paste the collection class into a new file for each combination of data types that the programmer would want to use the collection class for, which can be a waste of time.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.

In the Shuffle project, there are two reasonable data structures that can be used: an array-based queue, or a linked list. The feasibility of each structure depends on the method chosen for shuffling the deck of cards. An array-based queue has constant time operations on adding (as long as the array is not entirely filled up) and removing from the array. If the array is at capacity when another item is added to it, the running time becomes linear for that particular instance of adding to the array. 

A linked list, comparatively, has a nearly linear `add()` running time, unless the first or last “index” of the list is the target of the new data. `remove()` in a linked list could also potentially take linear time, depending on the location of the data that is to be removed. Splicing the list can also take linear time depending on the portion of the list that is to be removed. All of these running times are a result of the `find()`, since the list can only be traversed in a linear fashion.

Despite these running time comparisons, there is no clear-cut preferred choice for data structure; it depends on the shuffling style selected. The typical bridge shuffle, for instance, is the perfect task for an array-queue, since it is only the bottom cards of two-halves of the deck that need to be taken out to combine into a shuffled deck. A linked list would require more operations to reset the pointers of the list, which causes the list to be less efficient for this particular shuffle. For shuffles similar to the Hindu shuffle, where the middle of the deck is separated and then the rest of the deck is added to the pile, the linked list is more efficient. It is technically not possible to remove the middle of a queue, since a queue by nature removes the front of the array every time. Using the splice method of linked lists makes the Hindu shuffle very practical.


Analysis 2:
----
For social networking sites, the company needs to be able access usernames quickly. To accomplish this problem, there are two logical choices for storing a listing of all of the usernames of a website: a BST, or a hash table. Each data structure has its own strengths and weaknesses, but both can be used for the website.

A BST would be preferred over a hash table when the user is searching for friends to connect with on the site. This is because BSTs are more efficient at accessing user names that share the same string of characters that the user typed into the search box. Once the  searching algorithm has reached the first node that matches what the user is typing, then all of the possibilities for what the person is searching for are the child nodes, and easily accessible. With a hash table, it would be much more difficult to find all of the users that share a similar username because once the first match is found, the other usernames are not necessarily going to be immediately following the first one. As a result, the search algorithm would have to iterate through the backing array to guarantee that all of the matching usernames are found, which leads to a linear running time. The BST would have a running time less than that. It would be log n, where n is the number of items in the tree, worst case.

The hash table, on the other hand, is better suited for searching for a specific username to see if it is in use. This is the case because hash tables use a hashing function to give each input its own unique identifier, which corresponds to an index in the backing array. Once the calculation is made, the program has constant time access to that specific index of the array. If the item at the array index is not what it was looking for, a second hashing function is used to determine how many indices to advance past to try and find the data item (known as a “jump”). Since hash tables have a load factor, which limits the number of items that can be in the backing array before the array needs to grow. By doing this, it is likely that there will only be a handful of jumps before an index is called that has nothing stored in it, which indicates to the program that the username does not exit. As a result, it can be argued that the searching process takes constant time. A BST takes log n time, as described above, as the search will have to look at numerous nodes before determining if the desired username is already taken or not.

Extra Credit for attending the research fair.
----
