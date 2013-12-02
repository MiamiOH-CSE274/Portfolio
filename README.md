Portfolio
=========

Document completion of the course's learning outcomes.

Author
==========
"Kojs, Michelle", kojsmn

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

* https://github.com/MiamiOH-CSE274/03_Queue_Lab
* Use a queue as your data structure in https://github.com/MiamiOH-CSE274/Shuffle
* Consult with Dr. Brinkman on an alternative project

I chose to do the Queue Lab for the implementation of a Queue.
Here is a link to my repository on github which includes the source code: https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/kojsmn

7 - Create an implementation of a List
----
Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab
* Use a linked list as your data structure in https://github.com/MiamiOH-CSE274/Shuffle
* Implement chaining instead of linear probing in https://github.com/MiamiOH-CSE274/05_Hashing_Lab
* Consult with Dr. Brinkman on an alternative project

I chose to do the Linked List Lab for the implementation of a List.
Here is a link to my repository on github which includes the source code: https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/kojsmn

I also used a linked list as my data structure in the Shuffle project. 
Here is a link to my repository on github: https://github.com/MiamiOH-CSE274/Shuffle/tree/kojsmn
At the bottom of my repository there is a video link which shows the Shuffle project working.

7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

* Binary Search Tree Lab (TODO)
* Use a binary search tree or KD-Tree in the Starbucks project.
* Use a binary search tree in the Zeitgeist project
* Consult with Dr. Brinkman on an alternative project

I chose to do the Binary Search Tree Lab for the implementation of a Binary Search Tree.
Here is a link to my repository on github which includes the source code: https://github.com/MiamiOH-CSE274/06_BST_Lab/tree/kojsmn

7 - Create an implementation of a Hash Table
----
Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/05_Hashing_Lab
* Use a hash table in the Zeitgeist project
* Use locality-preserving hashing on the Starbucks project (not recommended!)
* Consult with Dr. Brinkman on an alternative project

I chose to do the Hashing Lab for the implementation of a Hash Table.
Here is a link to my repository on github which includes the source code: https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/kojsmn

7 - Create an implementation of a Heap
----
Possible sources of evidence (do any one of these):

* Heap lab (TODO)
* Implement heap sort in the Sorting lab (TODO)
* Implement a heap as part of the Graph Algorithms lab (TODO)
* Implement a heap as part of the Graph Project (TODO)
* Consult with Dr. Brinkman on an alternative project

I chose to do the Heap Lab for the implementation of a Heap.
Here is a link to my repository on github which includes the source code: https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/kojsmn

7 - Create an implementation of either Adjancency Lists or Adjacency Matrices
----
Possible sources of evidence (do any one of these):

* Graph lab
* Graph Algorithms lab
* Graph project
* Consult with Dr. Brinkman on an alternative project

I chose to do the Graph Algorithms Lab for the implementation of an Adjancency Lists.
Here is a link to my repository on github which includes the source code: https://github.com/MiamiOH-CSE274/08_Graph_Lab/tree/kojsmn

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

Queue Lab:

	The add() method takes O(1) time or constant time unless grow is called, then it takes O(n) time since grow takes O(n) time.

	The remove() method takes O(1) time or constant time unless grow is called, then it takes O(n) time since grow takes O(n) time.

	The getNumItems() method takes O(1) time or constant time.

	The grow() method takes O(n) time or linear time.

	Link to the methods: https://github.com/MiamiOH-CSE274/03_Queue_Lab/blob/kojsmn/ArrayQueue.ipp

Linked List Lab:

	The find() method takes O(n) time or linear time since there is a for loop, unless the first or last item is being found. If the first or last item is being found it takes 0(1) or constant time.

	The set() method takes O(n) time since find is called and find takes O(n) time.

	The add() method takes O(n) time since find is called and find takes O(n) time.

	The remove() method takes O(n) time since find is called and find takes O(n) time.

	The get() method takes O(n) time since find is called and find takes O(n) time.

	The splice() method takes O(n) time since find is called and find takes O(n) time.

	The size() method takes O(1) time or constant time.

	Link to the methods: https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/blob/kojsmn/LinkedList.ipp

Binary Search Tree Lab:

	The size() method takes O(n) time or linear time since each node is visited in orer to determine the number of items.

	The add() method takes O(h) time, where h is the height of the tree.  If the tree is balanced then h is logn and if the tree is unbalanced then h is n.

	The remove() method takes O(h) time, where h is the height of the tree.  If the tree is balanced then h is log n and if the tree is unbalanced then h is n.

	The find() method takes take O(h) time, where h is the height of the tree. See the remove method for explanation of h.

	The keyExists() method takes 0(h) time, where h is the height of the tree. See the remove method for explanation of h. keyExists() calls find which takes O(h) time.

	The next() method takes O(h) time, where h is the height of the tree. See the remove method for explanation of h.

	The prev() method takes O(h) time, where h is the height of the tree. See the remove method for explanation of h.

	The max() method takes O(h) time, where h is the height of the tree. See the remove method for explanation of h.

	The min() method takes O(h) time, where h is the height of the tree. See the remove method for explanation of h.

	Link to the methods: https://github.com/MiamiOH-CSE274/06_BST_Lab/blob/kojsmn/BST.ipp#L88	

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.


5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.
The Hashing Lab uses templates in an interesting way. The link to my Hashing Lab repository on github is: https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/kojsmn

Templates allow easy reuse of code. Templates can handle many different data types. This allows the programmer to decide what type of data type they would like to use.
In the Hashing Lab, I use a template where that looks like template <class Key, class T>.  This allows the user to specify what data type they would like K(key) to be and what 
data type they would like T(data) to be. In the main.cpp file this line:  HashTable<std::string,int> testTable; tells the compiler that K is a string type and T is an int type.
With this template, we could change K and T to be whatever data types we would like without having to change the HashTable.ipp file that contains the methods. Since this is a template
the methods in the HashTable.ipp file will run with different data types as K and T.

30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.


Extra Credit - 5

I attended the Research Fair. I talked to Mr. Stanley about Computer Security as well as other professors that attended. 