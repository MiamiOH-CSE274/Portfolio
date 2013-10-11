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
https://github.com/proctopj/03_Queue_Lab

Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/03_Queue_Lab
* Use a queue as your data structure in https://github.com/MiamiOH-CSE274/Shuffle
* Consult with Dr. Brinkman on an alternative project

7 - Create an implementation of a List
----
https://github.com/proctopj/04_Linked_List_Lab

Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab
* Use a linked list as your data structure in https://github.com/MiamiOH-CSE274/Shuffle
* Implement chaining instead of linear probing in https://github.com/MiamiOH-CSE274/05_Hashing_Lab
* Consult with Dr. Brinkman on an alternative project


7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

* Binary Search Tree Lab (TODO)
* Use a binary search tree or KD-Tree in the Starbucks project.
* Use a binary search tree in the Zeitgeist project
* Consult with Dr. Brinkman on an alternative project


7 - Create an implementaiton of a Hash Table
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

For Queue (Link provided above),

The running times for add() and remove() are constant, while the grow() function is linear where n is the number items in the initial
Queue which are then added to the new Queue after the array size has been doubled. The constructor and destructor are also both 
constant, but in reality if this Queue were to be applied for classes, it would become linear time as each item would need to be 
destructed according to its class parameters.


For Linked List (Link provided above),

The running time of size() is always constant due to existing control structures within other methods. find(), get(), add(), and 
remove() are selectively constant (for cases of an index of 0 or size-1 (where the size variable is actually numItems)) but 
otherwise will run in linear time. getAll is constant because it concatenates a LinkedList to the end of the main one, meaning 
an index of numItems-1 is used. The constructor method for these purposes is constant, but one could make a linear-time constructor
for a predetermined arrangement of data. In fact I should probably do that before the final iteration of this portfolio.


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.

For the LinkedList Lab(link provided above) we see dynamic memory allocation being used to construct and connect a data type of our own design
called Node which contains data of an unknown type until execution and address markers to other Nodes in the Linked List. The dummyNode is
generated first and made permanent by the new() function which gives it an address in the RAM which will not be changed or freed up until we 
specify by use of the delete() function. Each time an item is added to the LinkedList, a new Node is generated to contain that item and then 
link it to the adjacent Nodes at a given index in the LinkedList. Each time an item is removed, the nodes adjacent to the target restructure 
their links to each other, and then the target is deleted so no dangling pointer (address to nowhere) is left behind. The LinkedList destructor
employs a perfect loop of the Node destructor we call remove(), and it ensures not a single node, including the dummy, remains, and it doesn't 
go beyond the LinkedList into other parts of the RAM and accidentally deleting extraneous addresses. We must manage memory by hand because C++ 
does not automatically collect garbage the way Java does.

5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.

Again in the LinkedList lab we see a 2-layer usage of the template class. We have the abstract data type List with its own special template, 
then a LinkedList template which adds in specific functions needed for this particular implementation, such as the takeAll() function. This 
usage of templates keeps the project goals in mind as well as a convenient way to store directions for implementation while hiding the
implementation in our LinkedList.ipp file. It also shows the inheritance of LinkedList from List as well as the privately owned structure,
Node, on which it builds the collection as a whole, allowing any data type (labeled as T) to be entered into this collection. The implemented
type is decided at execution time of the program, thus giving the collection flexibility by this construction of the templates.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.
