Author
=======
"Proctor, Patrick", proctopj

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
https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/proctopj

Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/03_Queue_Lab
* Use a queue as your data structure in https://github.com/MiamiOH-CSE274/Shuffle
* Consult with Dr. Brinkman on an alternative project

7 - Create an implementation of a List
----
https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/proctopj

Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab
* Use a linked list as your data structure in https://github.com/MiamiOH-CSE274/Shuffle
* Implement chaining instead of linear probing in https://github.com/MiamiOH-CSE274/05_Hashing_Lab
* Consult with Dr. Brinkman on an alternative project


7 - Create an implementation of a Binary Search Tree
----
https://github.com/MiamiOH-CSE274/06_BST_Lab/tree/proctopj

Possible sources of evidence (do any one of these):

* Binary Search Tree Lab (TODO)
* Use a binary search tree or KD-Tree in the Starbucks project.
* Use a binary search tree in the Zeitgeist project
* Consult with Dr. Brinkman on an alternative project


7 - Create an implementation of a Hash Table
----
https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/proctopj

Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/05_Hashing_Lab
* Use a hash table in the Zeitgeist project
* Use locality-preserving hashing on the Starbucks project (not recommended!)
* Consult with Dr. Brinkman on an alternative project

7 - Create an implementation of a Heap
----
https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/proctopj

Possible sources of evidence (do any one of these):

* Heap lab
* Implement heap sort in the Sorting lab (TODO)
* Implement a heap as part of the Graph Algorithms lab (TODO)
* Implement a heap as part of the Graph Project (TODO)
* Consult with Dr. Brinkman on an alternative project

7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
https://github.com/MiamiOH-CSE274/08_Graph_Lab/tree/proctopj

Possible sources of evidence (do any one of these):

* Graph lab 
* Graph Algorithms lab
* Graph project
* Consult with Dr. Brinkman on an alternative project

7 - Implement graph algorithms
----
Possible sources of evidence (do any one of these):
https://github.com/MiamiOH-CSE274/08_Graph_Lab/tree/proctopj -Dijkstra Adaptation in the function shortestPath()

* Graph lab
* Graph Algorithms lab
* Graph project
* Consult with Dr. Brinkman on an alternative project

21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)

For Queue https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/proctopj,

The running times for add() and remove() are constant, while the grow() function is linear where n is the number items in the initial
Queue which are then added to the new Queue after the array size has been doubled. The constructor and destructor are also both 
constant, but in reality if this Queue were to be applied for classes, it would become linear time as each item would need to be 
destructed according to its class parameters. In terms of space requirements, the data structure has exactly n records(array spaces), 
1 for each stored item.


For Linked List https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/proctopj,

The running time of size() is always constant due to existing control structures within other methods. find(), get(), add(), and 
remove() are selectively constant (for cases of an index of 0 or size-1 (where the size variable is actually numItems)) but 
otherwise will run in linear time. getAll is constant because it concatenates a LinkedList to the end of the main one, meaning 
an index of numItems-1 is used. The constructor method for these purposes is constant, but one could make a linear-time constructor
for a predetermined arrangement of data. In fact I should probably do that before the final iteration of this portfolio.In terms of 
space requirements, the data structure has exactly n records(nodes), 1 for each stored item.


For Binary Search Tree https://github.com/MiamiOH-CSE274/06_BST_Lab/tree/proctopj

The running time of size() can be made constant if you store the variable numItems and increment it in add(). Otherwise it is O(n) 
by way of using a depth-first search (also featured in my code for this lab, but not utilized). Add() is effectively O(h) where h is
the height of BST. This height can be expressed as base2 log(n) where n is the number of nodes in the tree. Note the log-base changes
as the number of children per node changes. If each node has 3 children, then height is base3 log(n). So, in short, Add() runs in O(lg(n)) time.

Remove() runs in O(2lg(n)), 2 because the node must be found if it exists O(lg(n)), and then according to the implementation, bubble to the 
bottom O(lg(n)), and then be set to NULL and deleted (each O(1)).

max() and min() run in O(lg(n)) time on average, but the balance of the tree can affect this and all methods in this lab except size()

next() and prev() run in O(lg(n)) time as well, as they are based on the same flavor of algorithm as add.

In terms of space requirements, the data structure has exactly n records(nodes), 1 for each stored item.


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.

For the LinkedList Lab (https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/proctopj) we see dynamic memory allocation being used to construct 
and connect a data type of our own design called Node which contains data of an unknown type until execution and address markers to other Nodes in 
the Linked List. The dummyNode is generated first and made permanent by the new() function which gives it an address in the RAM which will not be 
changed or freed up until we specify by use of the delete() function. Each time an item is added to the LinkedList, a new Node is generated to contain 
that item and then link it to the adjacent Nodes at a given index in the LinkedList. Each time an item is removed, the nodes adjacent to the target 
restructure their links to each other, and then the target is deleted so no dangling pointer (address to nowhere) is left behind. The LinkedList destructor
employs a perfect loop of the Node destructor we call remove(), and it ensures not a single node, including the dummy, remains, and it doesn't go beyond 
the LinkedList into other parts of the RAM and accidentally deleting extraneous addresses. We must manage memory by hand because C++ does not automatically 
collect garbage the way Java does.

5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.

If we look at the Heap Lab (https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/proctopj) We see a template containing two 
classes: T is the data we wish to store, and Pri stands for priority: how important it is. Since a Heap is an implementation 
of the Priority Queue ADT, the variable Pri is particularly important for this class. That said, the class Pri in this case 
is implemented generally. This means one can technically set anything to be the data type used for priority here, even if
it makes no sense, so long as there is a way to compare the data. 

T has become a standard generic variable for us to hold any type of data, but the data in our case is for proprietary use
only, so we the designers of the heap can ignore it. The point of generic variables is to create a collection class which can
handle anything (within reason, hence the caveat of Pri needing to be a data type which can be compared to other Pri data).

And I suppose the nestling of the data inside the C++ standard 'pair<a,b>' class is noteworthy, because otherwise I wouldn't
have known the thing existed.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.

https://github.com/MiamiOH-CSE274/Shuffle/tree/proctopj
* For the Shuffle Project I personally used an array-based DEQueue to hold random numbers and build the "deck", because all functions for 
this data structure are O(1) time except when grow() is called. Also, the array-number structure is less expensive in terms of memory 
than a node-based linked list, another structure which would have been appropriate to use here. That said, it was by no means an easy
implementation. The logic is arguably much tougher to use arrays/queues for this project than a linked list, and because I used multiple
queues, I believe in the end I may have even botched the memory saving with my queue implementation of Shuffle.

I believe I erred when I chose to use queues for implementing the Pharaoh Shuffle actually, because I wasted a lot of time copying data
from two queues into a third, which is costly in terms of memory and time. For the same size data set I would have only needed two linked lists, 
and then the process of building the final sequence of nodes would have been as simple as reassigning pointers in each node of each list
based on a sequence of random numbers. Without having to copy data, I believe this would have run much faster than my queue implementation.

And because copying the data from the queues back to the central array is equally as expensive as copying from a single linked list structure,
I would suffer no other time loss for this particular project. And I would have saved dynamic memory space as well. All function times except
the destructor and iterating through the structures (which isn't applicable for comparison here due to the loss of time in copying for the queues
vs. the time it takes to rearrange addresses in the linked list) being equal for both data structures, I must admit Linked List was the superior
structure to use here, and I assumed incorrectly about the benefits of array-based structures for this application. And no arrangement of data
in my opinion would change this if all it is doing is changing the order of cards in a deck.


* For Zeitgeist (I did not complete this one) the obvious solution to a ranked dictionary problem is an array-based hash table which holds the 
words, keys, and a reference to a numeric variable stored in a separate array which solely keeps track of rank (how many times each word appears). 
Under double hashing, add() takes O(s+1) where s is the length of the word (in letters) we must hash before actually going into the hash table. Now, 
add may take n (length of the backing array) secondary hashes, which are each O(s) time and change for mathematical calculations. So, this method 
COULD in fact take O(s*n) time. With high probability, this is unlikely, but regardless the risk is worth mentioning. Searching for the word to 
exist has the same timing structure because it is still based on the hash function which is always O(s).

Upon adding, if the word already exists in the hash table, find() again takes O(s) and again possible O(s*n) time, and then modifying the number of 
occurences is a O(1) function, because even if the rank necessarily changes, it can only change by one place at a time. A single comparison and a 
single swap are all that would take place.

One could theoretically store the words themselves in a Binary Search Tree using the characters in words as the key. Aardvark < Abash < Accelerate
If one can keep the tree balanced (which is its own separate juggling act in terms of time), the times for add() keyExists() and find() become O(lg(n))
time, but if a near perfectly balanced tree is impossible to achieve, then the times all average toward O(n) time. Given the distribution of words in
the English dictionary, perfect balance is not obviously possible(to me anyway, and n becomes much larger than the average s in hashing), but one could 
get close. There's no reason to store rank in anything except an array due to constant access time and simple storage, but nevertheless, one could use 
a DLList to do it.  Adding more and more words as well as ranks would make the structure steadily more expensive and time consuming, even though swaps 
would essentially still be O(1) time. I still overall believe using a hashtable with double hashing and secondary array is the most elegant solution.