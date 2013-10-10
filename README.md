Author
==========
"Blase, Douglas", blasedd
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
Possible sources of evidence (do any one of these):

* Binary Search Tree Lab (TODO)
* Use a binary search tree or KD-Tree in the Starbucks project.
* Use a binary search tree in the Zeitgeist project
* Consult with Dr. Brinkman on an alternative project


7 - Create an implementation of a Hash Table
----
Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/05_Hashing_Lab
* Use a hash table in the Zeitgeist project
* Use locality-preserving hashing on the Starbucks project (not recommended!)
* Consult with Dr. Brinkman on an alternative project

7 - Create an implementation of a Heap
----
Possible sources of evidence (do any one of these):

* Heap lab (TODO)
* Implement heap sort in the Sorting lab (TODO)
* Implement a heap as part of the Graph Algorithms lab (TODO)
* Implement a heap as part of the Graph Project (TODO)
* Consult with Dr. Brinkman on an alternative project

7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
Possible sources of evidence (do any one of these):

* Graph lab
* Graph Algorithms lab
* Graph project
* Consult with Dr. Brinkman on an alternative project

7 - Implement graph algorithms
----
Possible sources of evidence (do any one of these):

* Graph lab
* Graph Algorithms lab
* Graph project
* Consult with Dr. Brinkman on an alternative project

21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)

For the ArrayQueue (found here https://github.com/db4soundman/03_Queue_Lab/blob/blasedd/ArrayQueue.ipp ), the running times of the methods are as follows.

The constructor is constant time, since space is only being set aside to store data in the array, nothing is being added. The destructor is constant time as well, assuming that the `delete[]` method is constant. `Add()` is constant time as well, unless `grow()` is called, in which case it's running time is based on `grow()` (see below). `Remove()` is constant time as well, since the first item in the queue is always removed from the array. `getNumItems()` is constant time, as the method only returns `numItems`. Finally, `grow()` runs in linear time since the items in the backingArray need to be copied to a new and larger array.



For the Linked List (found here https://github.com/db4soundman/04_Linked_List_Lab/blob/blasedd/LinkedList.ipp ), the running times for the methods are as follows. 
	The constructor is constant time, as there is nothing that relies on the size of the list to execute code. 
	The destructor is linear time, despite the fact that the `remove()` is called. A while loop is used to iterate through the entire list, and the remove method is called within the loop, but the remove method is always removing the first item in the list, so this does not add to the running time of the destructor. As a result, the destructor runs in linear time.
	The `find()` is a linear (technically n-1) function except when the user asks for the very first, or very last, item in the list because I have an if statement that checks to see if the user is asking for the last item on the list, and if they are, it accesses the node that the dummyNode's `prev` points to and returns it. Otherwise it iterates through the list and finds the correct node.
	The `set()` method is the same running time as `find()` because a call to find is used to access the pointer of the node that the user wishes to change, and then it is returned (if found) to have its data changed.
	For similar reasons, `add()`, `remove()`, and `splice()` are the same running time as `find()` (linear), as all three methods have calls to `find()`, and then perform operations that are not based on the size of the LinkedList.
	`Size()` is constant time; it only returns the numItems variable.



5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.


5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.