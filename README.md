Author
==========
"Griffith, David", griffid5
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

By clicking on the link you will see that I have fully demonstrated my knowledge of a queue. The code within ArrayQueue.ipp has passed the tests that have been provided by Dr. Brinkman in main.cpp. Furthermore, to implement the queue in this assignment I used the circular array concept. In this code(ArrayQueue.ipp) you will find a constructor and destructor for a circular array. You will also find a add, remove, getNumItems and grow methods. All of these methods are fully functional. Link: https://github.com/LakersAllTheWay/03_Queue_Lab/tree/griffid5

7 - Create an implementation of a List
----
Possible sources of evidence (do any one of these):

By clicking on the link below you will see that I have fully demonstrated my knowledge of a linked list. Other than the splice method all other methods have passed the tests provided by Dr. Brinkman. In this assignment I used a dummyNode that allowed me to access the linked list in which the dummyNode's "next" and "prev" were itself. The methods that can be found in LinkedList.ipp are: find, set, add, remove, get and size. Link: https://github.com/LakersAllTheWay/04_Linked_List_Lab/tree/griffid5


7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

To satisfy this requirement of the portfolio I went ahead and did the BST_Lab. In this lab I have demonstrated my knowledge 
of a BST by implementing the following methods in BST.ipp: constructor, destructor, size, add, remove, find, keyExists, next, prev, max and min.
For most methods I used both a private and public method call so that recursion would be simplified. In this lab all my methods passed the test
that Dr. Brinkman had and all my methods except the destructor and size were O(h) because the height of the tree is the longest number
of edges that each method will have to travel. Finally size was O(n) instead of O(h) because we had to tavel down both sides of the tree and 
visit every node. Link: https://github.com/LakersAllTheWay/06_BST_Lab/tree/griffid5


7 - Create an implementaiton of a Hash Table
----
Possible sources of evidence (do any one of these):


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
