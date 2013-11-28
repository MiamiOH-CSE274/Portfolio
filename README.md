Author
==========
"Bickley, Daniel", bickledb
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

An implementation of a Queue can be found at https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/bickledb

* https://github.com/MiamiOH-CSE274/03_Queue_Lab
* Use a queue as your data structure in https://github.com/MiamiOH-CSE274/Shuffle
* Consult with Dr. Brinkman on an alternative project

7 - Create an implementation of a List
----
Possible sources of evidence (do any one of these):

An implementation of a List can be found at:  https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/bickledb

* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab
* Use a linked list as your data structure in https://github.com/MiamiOH-CSE274/Shuffle
* Implement chaining instead of linear probing in https://github.com/MiamiOH-CSE274/05_Hashing_Lab
* Consult with Dr. Brinkman on an alternative project


7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

An implementation of a BST can be found at: https://github.com/MiamiOH-CSE274/06_BST_Lab/tree/bickledb

* Binary Search Tree Lab (TODO)
* Use a binary search tree or KD-Tree in the Starbucks project.
* Use a binary search tree in the Zeitgeist project
* Consult with Dr. Brinkman on an alternative project


7 - Create an implementaiton of a Hash Table
----
Possible sources of evidence (do any one of these):

An implemention of a Hash Table can be found at: https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/bickledb
* https://github.com/MiamiOH-CSE274/05_Hashing_Lab
* Use a hash table in the Zeitgeist project
* Use locality-preserving hashing on the Starbucks project (not recommended!)
* Consult with Dr. Brinkman on an alternative project

7 - Create an implementation of a Heap
----
Possible sources of evidence (do any one of these):

An implementation of a Heap can be found at: https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/bickledb

* Heap lab (TODO)
* Implement heap sort in the Sorting lab (TODO)
* Implement a heap as part of the Graph Algorithms lab (TODO)
* Implement a heap as part of the Graph Project (TODO)
* Consult with Dr. Brinkman on an alternative project

7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
Possible sources of evidence (do any one of these):

An Implementation of an Adjacency Matrix can be found at https://github.com/MiamiOH-CSE274/08_Graph_Lab/tree/bickledb
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

Queue: Implemented at https://github.com/MiamiOH-CSE274/03_Queue_Lab/blob/bickledb/ArrayQueue.ipp
	Constructor: Assuming memory allocation is constant, the constructor will have constant running time.
	Destructor: Because the delete[] method is called, the destructor will have either a linear or constant running time, depending on the data stored in the Queue. If the data requires a destructor to be dealocated, delete[] will have linear time. If delete does not have to be called for the data to be reallocated, it will take constant time.
	Add(): As the implementation is a circular ArrayQueue, the add() method is constant, unless it calls the grow() method. Without the call to grow(), the add method utilizes a constant running time, as the structure is an ArrayQueue, and the data can only be added to one spot in the array at a time, reguardless of size. However, if grow() is called, the add method has a linear running time, as the grow() method depends on the number of data points that are in the Queue.
	Remove(): In this implementation, Remove() utilizes constant time, as there is one spot where the data will be "removed" from, which is independent of the size of the Queue. 
	GetNumItems(): In this implementation, getNumItems() utilizes constant time, as the size of the Queue is stored as a variable and the running time is independent of the number of items in the queue.
	Grow(): In this implementation, grow() takes linear time, as it needs to allocate memory space for a tempoary array, write all of the data in the old array over to the new array, in order. This step will take linear time, and is then followed by a destructor for the old array, which takes constant time. Overall, the method should take linear time.

List:  Implemented at https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/blob/bickledb/LinkedList.ipp
	Constructor: Assuming memory allocation is constant, then the constructor will have a constant running time.
	Destructor: The destructor should take linear time. The call to the remove() method causes a call to the find() method, which normally takes linear time. But, because the destructor only calls remove() at zero, and concequently find() at 0, the method only takes linear time, as each iteration through the list takes constant time to remove and delete.
	Find(): The method takes linear time, as the method cycles through each node until it has the reached the ith node, and then returns it. In the worst case scenario, the method will loop through the entire list, and the running time is therefore dependent on the size of the List, so it takes linear time.
	Set(): The method takes linear time, because it contains a call to find(), which takes linear time. Because the rest of the method only sets variables or changes them, which all take constant time, the method is therefore linear.
	Add(): The method takes linear time, because it contains a call to find(), which takes linear time. If we assume that the call tob the Node constructor takes constant time, the overall running time will still be linear, as the rest of the method only changes variables, which only takes constant time.
	Remove(): The remove method takes linear time, because it contains a call to find(), which takes linear time. The rest of the method takes constant time, except for possibly delete, which will be assumed to take constant time, as the running time of delete is independent of the size of the List.
	Get(): The get method takes linear time, as it loops through the List, Node to Node, until it finds the Node at the index i, where it returns the Node's data. Because the loop used is dependent on the size of the List, the method has linear running time.
	Size(): The size method takes constant time, as the size of the List is stored in a variable, which can be accessed in constant time.
	
* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.

Evidence: https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/bickledb
	This example of a heap utilizes a dynamically allocated array. The size of the array is stored in a variable to prevent any reading out of the bounds of the array. Due to the nature of the Heap, the array must be able to be resized, and call a grow() method. This Heap's grow method 
	is located at https://github.com/MiamiOH-CSE274/07_Heap_Lab/blob/bickledb/Heap.ipp on line 17. To change the size of the array, a completely new array is allocated. The old array is copied over, and then to avoid leaking memory, the old array is deleted with delete[]. Then, when the heap
	needs to be deallocated. In the destuctor, the backing array is deleted with the delete[] function.

5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.
Evidence: https://github.com/MiamiOH-CSE274/07_Heap_Lab/blob/bickledb/Heap.ipp
	In this example, a template class is used to create a Heap.

30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):
List versus Queue:
	In the Shuffle project, there is an option to use either a Linked List or an ArrayQueue to be used to "shuffle" cards. The ArrayQueue is a reasonable approach because it offers constant time for almost all of the methods necessary to shuffle the cards. Add() and Remove() both take constant time, allowing for a conceptually easy way to emulate the riffle shuffle. If I wanted to emulate the riffle shuffle, I would create two arrayQueues, and read random segments of the inital deck into each of the queues.
	Then, taking both queues, I would read alternatively from each array into a Third, shuffling the order of the ArrayQueue. For this shuffle, ArrayQueue is the best method because it would have a much shorter running time than the Linked List, as most of the methods the Riffle Shuffle requires all take linear time in Linked List, such as the Add() and Remove() methods would take linear time, which would take much longer than the ArrayQueue implementation. However, if you wanted to implement at a different 
	kind of shuffle, such as the Hindu Shuffle, the Linked List is better at that particiuar task. In the Hindu Shuffle, a chunk of the middle of the deck is removed, and then the top of the original deck is added to the top of the second pile, and the sequence can continue for a large length of time or a large number of shuffles. The best way to implement the Hindu Shuffle, so you can use the splice() method to mve a large number of cards at one time, just like how the Hindu Shuffle works. The shuffle beings with the
	initialization of two LinkedLists, one which all of the cards are read into, and a second empty one to act as the second stack. Then, a chunk of the deck can be brought out of the large stack, utilizing the splice() method, and can be moved to the second stack. Then, a certain number of cards can be removed from the top of the originial list, and moved into the second list, until there are no cards in the first list left, exactly the same way as the Hindu Shuffle works. 

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.