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


Explanation of how I accomplished the requirements of the lab/answered questions on queues:
https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/gardnedn

Code of Circular based Queue:
https://github.com/MiamiOH-CSE274/03_Queue_Lab/blob/gardnedn/ArrayQueue.ipp

The Queue is circular, compiles, successfully adds and subtracts elements, grows when it is full, does not leak memory, throws exceptions when appropriate, and works in constant time when it is supposed to. 

7 - Create an implementation of a List
----
Explanation of how I accomplished the requirements of the lab/answered questions on Linked Lists:
* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/gardnedn
Code of Linked List:
* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/blob/gardnedn/LinkedList.ipp

Link List compiles, and is circular. Succesfuly adds, removes, sets and sets Nodes into Linked List. Remove, get, set work in constant time when supposed to, throws exceptions when appropriate, does not leak memory, and keeps track of the size of the list in O(1) time. 

7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

Explanation of how I accomplished the requirements of the lab/answered questions on Binary Search Tree.
https://github.com/MiamiOH-CSE274/06_BST_Lab/tree/gardnedn
code of Binary Search Tree:
https://github.com/MiamiOH-CSE274/06_BST_Lab/blob/gardnedn/BST.ipp

7 - Create an implementaiton of a Hash Table
----
Explanation of how I accomplished the requirements of the lab/answered questions on HashTable:
https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/gardnedn
code of Hash Table:
https://github.com/MiamiOH-CSE274/05_Hashing_Lab/blob/gardnedn/HashTable.ipp




7 - Create an implementation of a Heap
----
Possible sources of evidence (do any one of these):

Explanation of how I accomplished the requirements of the lab/ answered questions on Heap:
https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/gardnedn
code of Heap:
https://github.com/MiamiOH-CSE274/07_Heap_Lab/blob/gardnedn/Heap.ipp

7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
Explanation of Graph Lab:
https://github.com/MiamiOH-CSE274/08_Graph_Lab

Used adjacency List for Graph Lab. 
Code: https://github.com/MiamiOH-CSE274/08_Graph_Lab/blob/master/Graph.cpp 


7 - Implement graph algorithms
----
Possible sources of evidence (do any one of these):

added a depth first search to my graph Lab. Added a test of depth first search in main. 
https://github.com/MiamiOH-CSE274/08_Graph_Lab/blob/master/Graph.cpp

21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)

Hash Table: O(1) time for remove and find if load factor (n/m) < (1/2). O(1) time for add if grow is not called, and as grow is called it is called less frequently so O(1) for add as well.
grow takes O(n) as you have to loop through the old array and add it to the new array.

Linked List: add, get, and remove take O(1) time if at end or beginning to linked list. otherwise they take O(n).
find takes O(n) as it has to loop through the each node til it finds it.
set also take O(n) as it calls find.
size takes O(1) time as the variable numItems keeps track of the size. and size() returns numItems.

Queue:remove takes O(1) as we are only incrementing variables and instantiating T removedItem.
add takes O(1) time as we are using random access to change the array spot to toAdd.  unless grow is called in which case it takes O(n) because grow takes O(n) 
grow takes O(n) time as we have to add every item into the new array.

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.

https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/blob/gardnedn/LinkedList.ipp
The program does not leak memory as the remove function switches the pointers and then deletes the node that is to be removed. The add method creates a new node and the remove function deletes the nodes after switching the pointers appropriately.
 The destructor calls remove while the linked list is not empty and then finally deletes the dummyNode to make sure there are not any nodes "floating" after the program is done.
 


5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.


updated main of Linked List lab to showcase templates. Namely that we can switch the 
type of the linked list data, such as the how I changed it to doubles from ints. 
Templates are extremely useful in the sense that they can make code more reusable by using generic data structures that store arbitrary data types.
https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/blob/master/main.cpp


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.
