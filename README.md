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
Here is a link to my source code on my branch in Brinkman's repository on github: https://github.com/MiamiOH-CSE274/03_Queue_Lab/blob/kojsmn/ArrayQueue.ipp

My methods for the Queue Lab were 0(1) or constant time except for grow which was 0(n) or linear time.
I used the array in a circular fashion. I also made sure to not leak memory.

7 - Create an implementation of a List
----
Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab
* Use a linked list as your data structure in https://github.com/MiamiOH-CSE274/Shuffle
* Implement chaining instead of linear probing in https://github.com/MiamiOH-CSE274/05_Hashing_Lab
* Consult with Dr. Brinkman on an alternative project

I chose to do the Linked List Lab for the implementation of a List.
Here is a link to my source code on my branch in Brinkman's repository on github: https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/blob/kojsmn/LinkedList.ipp

I implemented a doubly-linked list that had pointers to the next and previous nodes. I was able to have add, remove, get and set be 0(1) or constant time when i was 0 or i was size()-1.
Memory is not leaked and I was able to use a Linked List in my Shuffle project.

I also used a linked list as my data structure in the Shuffle project. 
Here is a link to my branch on Brinkman's repository: https://github.com/MiamiOH-CSE274/Shuffle/tree/kojsmn
At the bottom of my repository there is a video link which shows the Shuffle project working.

7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

* Binary Search Tree Lab
* Use a binary search tree or KD-Tree in the Starbucks project.
* Use a binary search tree in the Zeitgeist project
* Consult with Dr. Brinkman on an alternative project

I chose to do the Binary Search Tree Lab for the implementation of a Binary Search Tree.
Here is a link to my source code on my branch in Brinkman's repository on github: https://github.com/MiamiOH-CSE274/06_BST_Lab/blob/kojsmn/BST.ipp

In my Binary Search Tree all the methods were of 0(h) running time where h is the height of the tree. 
In the best case, if the tree is balanced then h is log(n).  In the worst case, if the tree is unbalanced then h is n.
Most of the methods are recursive.

7 - Create an implementation of a Hash Table
----
Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/05_Hashing_Lab
* Use a hash table in the Zeitgeist project
* Use locality-preserving hashing on the Starbucks project (not recommended!)
* Consult with Dr. Brinkman on an alternative project

I chose to do the Hashing Lab for the implementation of a Hash Table.
Here is a link to my source code on my branch in Brinkman's repository on github: https://github.com/MiamiOH-CSE274/05_Hashing_Lab/blob/kojsmn/HashTable.ipp

In my hash table I used double hashing to find an open slot in the hash table. 
This is where a jump value is calculated with the formula jump = 1 + (key%(m-1)).
This is used when data is already stored in the initial index value calculated from the hash function.
In this case the jump value is used until an empty spot is found.

7 - Create an implementation of a Heap
----
Possible sources of evidence (do any one of these):

* Heap lab
* Implement heap sort in the Sorting lab
* Implement a heap as part of the Graph Algorithms lab
* Implement a heap as part of the Graph Project
* Consult with Dr. Brinkman on an alternative project

I chose to do the Heap Lab for the implementation of a Heap.
Here is a link to my source code on my branch in Brinkman's repository on github: https://github.com/MiamiOH-CSE274/07_Heap_Lab/blob/kojsmn/Heap.ipp

7 - Create an implementation of either Adjancency Lists or Adjacency Matrices
----
Possible sources of evidence (do any one of these):

* Graph lab
* Graph Algorithms lab
* Graph project
* Consult with Dr. Brinkman on an alternative project

I chose to do the Graph Algorithms Lab for the implementation of an Adjacency Lists.
Here is a link to my source code on my branch in Brinkman's repository on github: https://github.com/MiamiOH-CSE274/08_Graph_Lab/blob/kojsmn/Graph.cpp

7 - Implement graph algorithms
----
Possible sources of evidence (do any one of these):

* Graph lab
* Graph Algorithms lab
* Graph project
* Consult with Dr. Brinkman on an alternative project

I chose to do the Vise project for the implementation of graph algorithms.
In the Vise project, my partner, Nick Contini, and I did a depth-first traversal of the graph.

Here is a link to mine and Nick's Vise project in Brinkman's repository on github: https://github.com/MiamiOH-CSE274/Vise/tree/ContiniAndKojs

We used a vector of hexSpaces with pointers to upleft, left, downleft, downright, right, and upright. 

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

	The size() method takes O(n) time or linear time since each node is visited in order to determine the number of items.

	The add() method takes O(h) time, where h is the height of the tree.  If the tree is balanced then h is log(n) and if the tree is unbalanced then h is n.

	The remove() method takes O(h) time, where h is the height of the tree.  If the tree is balanced then h is log(n) and if the tree is unbalanced then h is n.

	The find() method takes take O(h) time, where h is the height of the tree. See the remove method for explanation of h.

	The keyExists() method takes 0(h) time, where h is the height of the tree. See the remove method for explanation of h. keyExists() calls find which takes O(h) time.

	The next() method takes O(h) time, where h is the height of the tree. See the remove method for explanation of h.

	The prev() method takes O(h) time, where h is the height of the tree. See the remove method for explanation of h.

	The max() method takes O(h) time, where h is the height of the tree. See the remove method for explanation of h.

	The min() method takes O(h) time, where h is the height of the tree. See the remove method for explanation of h.
	
	The height of the tree is at most n and at least log(n). It is n when the tree is unbalanced and it is log(n) when the tree is balanced. The reason it is log(n) is because the bottom level of the balanced tree will have one more node than the total number of nodes in the tree.
	
	Link to the methods: https://github.com/MiamiOH-CSE274/06_BST_Lab/blob/kojsmn/BST.ipp#L88	


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. 
In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. 
This will probably require referring to your code, providing links.

Memory management in C++ is manual memory management and must be controlled by the programmer. Memory is allocated using new and deallocated using the delete operator.  
In the Hashing Lab memory is managed. Here is the link to my Hashing Lab source code in Brinkman's repository on github, which I will be referring to: https://github.com/MiamiOH-CSE274/05_Hashing_Lab/blob/kojsmn/HashTable.ipp
In line 10, memory is allocated with the new operator. In line 18 memory is deallocated with the delete[] operator.
To make sure that there is no out of bounds array access, the indexes are determined through the formula hash(k) % backingArraySize.
This makes sure that an index is not out of bounds. Lines 29, 61, 81, and 90 show this. 
In the grow() method a new HashRecord is created in Line 116. The backingArray data is copied into the new backingArray. Then in line 130 the old backingArray is deleted using the delete[] operator.
There are no dangling pointers. No pointers point to a memory location of deallocated memory.  

5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.

The Hashing Lab uses templates in an interesting way. The link to my Hashing Lab branch in Brinkman's repository on github is: https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/kojsmn

Templates allow easy reuse of code. Templates can handle many different data types. This allows the programmer to decide what type of data type they would like to use.
In the Hashing Lab, I use a template that looks like template <class Key, class T>.  This allows the user to specify what data type they would like Key to be and what 
data type they would like T(data) to be. In the main.cpp file this line:  HashTable < std::string,int > testTable; tells the compiler that Key is a string type and T is an int type.
With this template, we could change Key and T to be whatever data types we would like without having to change the HashTable.ipp file that contains the methods. Since this is a template
the methods in the HashTable.ipp file will run with different data types as Key and T. 
However, a new hash function would have to be created that would take the new data type of Key.

30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. 
Describe two reasonable options, and explain the trade-offs between them. 
For each, describe an application where the data structure would be better. 
For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better 
really depends on the input data set. Explain what the data would have to look like for the 
Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.

Shuffle: https://github.com/MiamiOH-CSE274/Shuffle/tree/kojsmn

	For the Shuffle project there are two obvious data structure designs. The two reasonable options are Linked Lists and Array Queues. The Shuffle project requires implementing a realistic shuffle method of cards.

	The trade-offs between Linked Lists and Array Queues are in the ease of insertion and removal of items.
	The running times for Array Queues and Linked Lists are walked through below. However, when used in the Shuffle project neither data structure has an advantage with running times.
	It takes 0(n) or linear time for both data structures to implement the Shuffle project.
	The Array Queue has to call grow which takes 0(n) time and the Linked List's splice method, which takes items from one Linked List
	and inserts them at an index in another, also takes 0(n) time.

	In Array Queues the get method take O(1) time. The remove and add methods in ArrayQueues are O(1) time or constant time unless grow is called then they are O(n) or linear time. If an ArrayQueue was used for the Shuffle project the process of adding and removing items would be slow. When adding and removing the array needs to either grow or be shrunk. This is done by allocating a new array of the desired size and copying the data over.

	The LinkedList methods of get, set, splice, and find take O(n) or linear time. The remove and add methods take O(n) time or linear time. LinkedLists do not need to copy any data when adding or removing. The place where the add or remove is desired needs to be found and then the data is inserted by updating the links.
	This is what the splice method does. The splice method takes two Linke

	If an Array Queue was used for the Shuffle project, new arrays would need to allocated and data copied and then old arrays deleted.
	The manipulation of Array Queues is not as easy as Linked Lists.

	For the Shuffle project I choose to use Linked Lists as my data structure. The reason I choose this data structure was because insertion and removal is easier with LinkedLists than with ArrayQueues. With ArrayQueues my running time would be worse because I would have to create new arrays to deal with the addition and removal of cards. 
	With LinkedLists I do not have to deal with resizing my data structure, like I would have to with ArrayQueues. LinkedLists are easy to manipulate and the Shuffle project requires easy manipulation of cards in order to get a realistic shuffle that produces a shuffled deck.


Vise: https://github.com/MiamiOH-CSE274/Vise/tree/ContiniAndKojs

	For the Vise project there are two obvious data structure designs. The two reasonable options are Adjacency Matrix and Adjacency Lists.

	The Adjacency Matrix is a matrix that has the columns as the vertices and the rows as all the possible edges. At each row and column, there is a value that tells whether there is an edge from that vertex to that edge.

	The Adjacency List is an array with the vertices. Each vertex contains a list of the edges that are connected to that vertex. The list can be in Linked List form or array form or another type of list data structure.

	The tradeoffs between Adjacency Matrix and Adjacency List are in the storage and running times of the methods.

	Adjacency Lists take up less space than Adjacency Matrix.  The storage size of an Adjacency Matrix is 0(n^2) and the storage size of an Adjacency List is at worst 0(n+m) but at best 0(n+dn), where n is the number of vertices, m is the number of edges, and d is the degree of the graph.
	Adjacency Lists save more space than Adjacency Matrix.
	
	The running times of Adjacency List determining the neighbors of one node is a lot faster than when the Adjacency Matrix determines the neighbors of one node.

	In the Adjacency List, the neighbors are linked to the vertex so the vertex needs to be found and then all of the neighbors are there.

	In the Adjacency Matrix, the vertex must be found and then you must go through each spot in the row to determine the neighbors of that vertex.

	With Adjacency Matrices, the question about a specific edge can be found easily, as well as inserting and deleting edges.

	With Adjacency Lists it is harder to check whether a specific edge is in the graph. The list pointed to by the vertex has to be searched through to determine
	if that edge is in the graph.

	An application where Adjacency Lists would be better is in this Vise project or in Road Map applications. 

	An application where Adjacency Matrix would be better is where you want to determine if a specific edge is in the graph.

	Otherwise Adjacency Lists are the clear winners especially if space is an issue.

	In the Vise project, Adjacency Lists are the better data structure because there needs to be fast access to all the neighbors of a vertex, in order to run isCompleted and doVise methods easily.
	Also this allows the depth-first search to be ran faster, which is an algorithm needed for this project.

	In our Vise project we used a vector of hexSpaces with pointers to upleft, left, downleft, downright, right, and upright hexes. 
	We used this data structure instead of an Adjacency Matrix because it was easier for us to understand how to access certain hexes. 
	There are no major running time differences between our data structure and Adjacency Lists.


Extra Credit - 5

I attended the Research Fair. I talked to Mr. Stanley about Computer Security as well as other professors that attended. 