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

Unless Otherwise specified, all answers given were based off of notes from Dr. Brinkman's lectures, notes from the course text: http://opendatastructures.org/, or from my own
knowledge from completing the course labs.



7 - Create an implementation of a Queue
----
https://github.com/laufengd/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
https://github.com/laufengd/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
https://github.com/laufengd/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
https://github.com/laufengd/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
https://github.com/laufengd/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/laufengd/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
https://github.com/laufengd/08_Graph_Lab/blob/master/Graph.cpp

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List

In an Array-Based list, add() and remove() take O(n) operational time because the items in the list need to be shifted in order for more items to be added. 
Array-Based size(), get() and set() run in 0(1) time. For Linked lists, getNode(i) takes O(1+ min{i, n-i}) time, other than that all the other functions run 
in O(1) time. When using an iterator, adding to, removing, getting, and setting the iterator runs in O(1) after the iterator has been found.


* Binary Search Tree vs. Hash Table

The average runtime for find(), add(), and remove() for a hash table is O(1) time. The reason find() runs in constant time is because the key, when stored, is passed through a hash function which gives each key a drastically unique value.
Another way to describe this would be searching for a blue item amongst many items that are different shades of blue versus searching for it amongst items that are all different colors.
Although statistically unlikely to occur, the worse case runtimes of a hash table for these functions is O(n). The average runtimes of binary search trees for find(), add(), and remove() are O(log n).
This is because each level of the tree has twice as many nodes as the previous, so the 4th level has 2^(4) times more nodes than the root(The level being defined how many connectors there are between the root and the last ancestor).
When searching for node in a binary search tree, the function only needs to traverse one level at a time to find the node its looking for, thus the runtime is proportional to log n (with base 2).
In the worst case scenario these functions will run in o(n) time, which when there is an unbalanced tree. One instance in which this could occur is when every item added is greater than the last.


* Adjacency List vs. Adjacency Matrix (Answer paraphrased from http://www.brpreiss.com/books/opus5/html/page547.html)

In an adjacency list, finding all edges printing them takes a minimum of O(n) operational time and a maximum of O(n+e), where e is the number of edges. 
This is because you must cycle through all the nodes and when encountering a new edge, print it out. If you find an edge between 1 and 2 in node1's edgelist, 
the same edge exists in node2's edgelist. It is important to make sure you do not print that node twice when examining node2. For an adjacency matrix, finding 
all edges takes O(n^2) time because there is a X vertex containing n nodes and a Y vertex containing n nodes. Together, these make n^2 vertices. To find all edges,
each vertices must be examined. In an adjacency list, finding whether an edge exists between node1 and node2 has a worst-case running time of O(n) or O(n-1). In an adjacency list,
all nodes have a list of edges containing keys of other nodes with whom they have edges with. As a result, finding an edge has a worst case running time of O(n) or O(n-1) depending on
whether or not you allow a node to have an edge with itself. In an adjacency matrix, seeing whether or not node1 and node2 have an edge runs in O(1) time because it 
is just a matter of whether or not that spot in the matrix has a value of true.

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* Call Stack: A Stack data structure on the computer's RAM that is used to store parameters and local variables for the subroutines of an active program.
* heap: A data structure on the RAM used for storing dynamically allocated variables
* Address: A location on the RAM where data is stored denoted by a number and can be referenced or pointed to.
* Pointer: A variable that points to an Address on the RAM

TODO: Answer the following questions about memory management and dynamic variables

* A memory leak is when data stored on the RAM can no longer be accessed and therefore takes up unnesesary space
* A dangling pointer is a pointer that references an address of an invalid data type and often times is the result of when data in a address is deleted or deallocated without deleting the pointer.
These are dangerous because often times other data can fill into the address being pointed to and cause the code to break.
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java? Destructors deallocate memory and delete dangling pointers.
Java does not need destructors as much because the java compiler is very proficient at figuring out when something is no longer in use and getting rid of it automatically.

5 - Create collection classes using templates in C++
----
(Answer paraphrased from a Microsoft Developer Network Page:  http://msdn.microsoft.com/en-us/library/z3f89ch8.aspx)
The main benefit of using Template collection classes is that it is an efficient way of abstracting functions and variables with flexibility on what data type is used as parameters.
When someone instantiates a template-class in another file, the compiler will create separate versions of the function for the data-type specified by the user when instantiated.(See example below)
This is especially helpful for implementing data structures because it is not always certain what type of data is being stored. For example, in our arrayQueue, lab if we were
to implement the functions in the class to take parameter with data-type int instead of data-type T, we would only be allowed to have create arrayQueue that store integers. We would not be able to store 
doubles, floats, longs, or any other data-type you can think of.

(Answer paraphrased from a stack overflow comment: http://stackoverflow.com/questions/495021/why-can-templates-only-be-implemented-in-the-header-file)
When instantiating a template, the compiler creates a new class with the given template argument. For example if a template class foo uses a template <typename T>,
and somewhere in a .cpp file foo<int> is instantiated, then a new class is created and every T parameter used in the template class will be compiled as an integer in the new class.
As a result, the compiler needs all functions to be defined in order to create this new foo<int> class; if these function definitions were not in the header then the compiler could not
access them.

//taken from a stackoverflow comment

<typename T>

struct Foo
{
    T bar;
    
	void doSomething(T param) {/* do stuff using T */}
};

// somewhere in a .cpp
Foo<int> f; 

//compiler creates new class equivalent to this

struct FooInt
{
    int bar;
    
	void doSomething(int param) {/* do stuff using int */}
}

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)

If I were to create a data structure to store a set of unordered strings I would undoubtedly implement a hash table because after putting the string through a hash function; adding, finding, removing and 
checking if a string exists would run in constant time. However, if the set were to have some kind of order such as by most searches or occurrences(Zeitgeist project), I would probably implement 
an array instead of, or in addition to, my hash table. That way, the retrieval of a string based on its order would run in constant time; whereas if I were to solely implement a hash table, it would take O(n) time.

* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

If I were to implement a data structure for a grocery list I would use a Linked list. Linked lists allow for more convenient adding and removing of items in between one another which is optimal
for when I think of things I want to add or remove at different times. Placing items in between one another is important because I might want to group one category 
together such as vegetables or cereals. So if I were to think of a vegetable I want to add at a later time, I would want to put it at the end and take the time to have it bubble up, 
I want to be able to insert it with other vegetables right away. If I were to use an array-based list, trying to place an item in the middle would require shifting the whole list.
In addition, I would have to grow() the list if I added too many items, which would usually mean doubling the size of my list. I would not want to carry an abnormally large list around the supermarket
if I wasn't going to use all of the space on it. All other data-structures, such as bst, heap, or hashtable, might work but have overly-complicated implementations that are unlikely to yield much improvement
for a simple grocery list. A linked list such as this would most resemble the notes application on an iPhone.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

Once again, I would use a hash function for this data structure because after passing the banner number through a hash function, adding, removing, and finding the records would run in constant time. 
One of the flaws of a hash table is that you cannot add identical items, however, since no banner number is the same that issue is eliminated. If each banner number were in some sort of numerical order, 
you could store the nodes in an array with the banner number being the index and you could find records in constant time as well. However, my guess is that banner numbers are randomly generated 
which would make the array a very inefficient idea. Another possible data structure would be a bst, however, the performances of the add, remove, and find functions would not be as fast as a hash table.



* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
 
For a network router where certain packets have priority over others I would implement an implicit binary tree as a Heap. While(index > 0 && backingArray[index] < backingArray[p]), 
the key of a packet will continue to bubbleUp. This means that packets of the same key will not bubbleUp past one another, thus allowing multiple packets of the same key to
 be parents and children of one another. The end result is that all the highest keys are at the top, and ensuring that a packet with a greater key will be sent before one with a lesser key. 
 When company X adds a packet to send, I would give it a key value of how ever much they paid and when company Y added a packet to send I would give it a key of their payment 
 value and so on. This data-structure is preferable to all other data structures this semester. A simple list as an array might work but its bubbleUp() and trickleDown() would run in O(n) instead of O(log n) like my tree. 
 A normal bst would not work at all because all smaller items are meant to be to the left and all larger items to the right; when popping off the root it would send some
 value in between which is something we do not want. No other data-structure can ordering keys from greatest to least or least to greatest with the same efficiency.










