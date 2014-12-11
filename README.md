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

7 - Create an implementation of a Queue
----
https://github.com/SamHausfeld/03_Queue_Lab

7 - Create an implementation of a List
----
https://github.com/SamHausfeld/04_Linked_List_Lab

7 - Create an implementation of a Binary Search Tree
----

https://github.com/SamHausfeld/06_BST_Lab

7 - Create an implementation of a Hash Table
----
https://github.com/SamHausfeld/05_Hashing_Lab

7 - Create an implementation of a Heap
----
https://github.com/SamHausfeld/07_Heap_Lab

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/SamHausfeld/08_Graph_Lab

7 - Implement graph algorithms
----
https://github.com/SamHausfeld/08_Graph_Lab

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List

In terms of running times, Array-based Lists and Linked Lists are virtually opposites.  All the things that one does in constant time, the other can do in linear time and vice versa. (With an exception for the size function which is always constant time, due to it's simplicity.)
For example, in an Array-based List; the get, set and size methods all run in constant time, where as add and remove take linear time.
Vice versa, in a LinkedList, the add and remove (and size) methods are constant instead.
The difference here is due to each data structures approach to the particular methods.  A fair rule for this that I've observed, is that a method is slower whenever it needs to use a loop to search through the entirity/majority of an array.
The reasoning behind this has to do with iterators.  An iterator is like a bookmark that you can use to keep track of things in data structures, a feature with many uses.  With my basic understanding, the more times you have to move/manipulate an iterator(s), the slower your method.
LinkedLists can place at an iterator very quickly, making their add and remove functions constant time.  However, to find data at a certain iterator to either get or set it is in linear time.  It is easy for Linked Lists to tie, untie, and insert before or after making them useful when you don't know how big the List needs to be.  The opposite is true for iterators in Array Lists.  Getting/setting the iterator at a certain index is much faster here due to the speediness of arrays in this frontier. 


* Binary Search Tree vs. Hash Table

When one is deciding to use either a HashTable or Binary Search Tree (BST) it's probably a good idea to consider which functions you will be performing the most often.  Provided that the key has been hashed, a HashTable can add, remove, and set in constant time.  The disadvantage being that a HashTable can only find the min, max, next, and prev of (lets say a dictionary class) in linear time O(n) (since they'd have to loop through the entire backing array).  Meanwhile, BST's have a relatively consistent running time across all these functions of O(lg n) because of the binary nature of the tree.  What I mean by binary nature is that whenever you're searching for a certain node, and you move from one node to the next down the tree, you eliminate half of the remaining options.  It's worth noting that add and remove in a BST dictionary can be written in O(h) time where h is the height.

* Adjacency List vs. Adjacency Matrix

Adjacency lists and matrices are essentially two different methods to organize a relatively similar concept (by which I mean graphs). Although they are more similar (in my opinion) than any other two data structures, the differences between them are fundamental.  For starters, a graph matrix is a square grid with each space bearing either a 1 (meaning this coordinate is an edge) or a 0 (it is not).  Meanwhile, an adjacency list is, well, a series of lists (I kind of think of them as buckets) that correspond to each node in the graph and hold their own edge lists.  For the most part, the adjacency matrix seems faster to me.  Or at least faster at the more common operations, as it can add an edge, get the cost of an edge, and remove an edge all in constant time.  The list can do do these same functions at a speed near constant time but at O(d), where d is some constant larger than 1. (I'm aware that O and theta are not the same thing, but..I was told to treat them as if they were!).  The reason for this is that a matrix can simply take the address' of two nodes and change their coordinate pair from 1 to 0 (to remove an edge) or 0 to 1 (to add one).  To do the same function, the adjacency list would need to update the edge list of the first node, and then the second node.
The thing that adjacency lists are dramatically faster at is getting their neighbors, which depending on your goal may be the most commonly used method.  The adjacency list keeps edge lists to allow this to be done in constant time.  A matrix would have to loop through an entire column (or row) to find all of a node's neighbors.

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!)

The call stack is a region in memory that sort of functions as a list of actions the computer needs to perform and the order in which those actions are to be completed. Variables created in the stack are statically allocated (basic declarations of ints and stuff).  They only exist within scope of their particular methods and then are deleted immediately afterwards.  The stack is used with a FILO mentality, it is memory associated with performing processes.

* The heap (not to be confused with the heap data structure!)

The heap is a section of memory associated with storing data for later. Things here are carried out when they are needed.  These variables are dynamically allocated, meaning that they have to be created on the heap with the "new" command and removed from the heap with "delete." (Although never really deleted, the space they took up is merely marked as reusable.)

* Address

The "location" of a variable, object or some other element within the disk space.  We can use the & command to access these.

* Pointer

An unique type of element that points to the addresses of other specified elements.

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?

Personally I find "leak" to be an innappropriate word to use here.  Memory leak generally happens when you forget to delete an object off the heap when you are done using it.  If you get rid of a pointer to something on the heap without deleting it, you've now lost your ability to access that spot in memory but that spot in memory is still taking up space. Enough situations like this and you can seriously muck up your computer.

* What is a dangling pointer (or dangling reference), and why is it dangerous?

These dangling pointers are pointers that no longer "point" to anything, and they can be used by hackers to infiltrate complex systems.

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?

Java is intelligent, and basically...knows when to delete the information it no longer needs.  C++, quite simply doesn't.  But the reason C++ is so barebones is so that it can operate at absolute maximum efficiency.  A destructor is exactly like a constructor, except it deletes any data that is no longer needed by the programming.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

- What is the main benefit of using templates when creating collection classes?


I think the best way to explain the use of templates is with an example.  Let's suppose I'm making a Dictionary-like data structure with both a key and a certain kind of data -- but I don't know what kind of data.  This dictionary could be storing words as strings, or student ID numbers as integers, or anything else.  Templates allow me to not worry about what the final use of the class I'm making is and instead focus on a well made and extremely flexible data structure that could be implemented in many different classes each storing a different kind of data.

- In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

The caveat we're dealing with here is that templates must be implemented in the header file.  When supplying a template argument in some .cpp file, the template class is going to create a new class specific to that argument modeled after the template.  But in order to create a model of the template, it will need the template methods and those would be inaccessible by the compiler anywhere other than from the header file.




20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)

When I think of storing a set of strings, I tend to think of a dictionary.  What else is a dictionary besides a highly sorted set of strings?  The main stipulation here being that we're dealing with an unsorted set instead of a sorted one, I'll bring that up a bit later.  Whichever structure we choose to implement needs to fill some requirements.  I'd like it to be efficient at the tasks it's going to perform the most often, ideally in constant time.  These tasks include adding, removing, and checking strings within the structure.  With a regular dictionary, one that's sorted, I would use an ArrayList but if I choose not to sort it I can go from the O(n) time of the ArrayList to the O(1) time I can get when using a HashTable! A HashTable can do all three of those tasks (adding, removing, and checking) in constant time when implementing an unsorted set, making it, in my opinion, the best choice for the job.


* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.


The first thing I need to consider is how I want to decide my data structure.  When I have a grocery list (for the sake of this exercise) I use a pen and pad of paper so, much like a slow computer, the efficiency of my data structure will matter.  Next, I'll stop to think about what sort of operations I want my data structure to support.  Since this grocery list example is being written with a pen and paper, I'll need a "write-only" sort of data structure that is compatible.  The easiest way to decide which structure is best may be to eliminate the structures that won't work.  I want to cross off things from my list as I find them, and even be capable of adding things between items should I remember them.  Ideally I'd also create my list in an order that's optimal for the layout of the store.  A queue structure would be a bad fit since I couldn't add between lines, only on the one end.  Stack is a bad choice as well.  But I wouldn't need anything complicated so, ironically, using a List data structure seems to be the best choice.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

The concept of banner numbers seems like a perfect reason to use a hash table.  After passing the the banner number through the hash function you can find, add and remove all in constant time.  You could also use a binary search tree but not with quite as much speed. Additionally, if the banner numbers were proceduraly generated you could have constant time using an array; however, the banner numbers randomly generated. One minor problem with hash tables is that you cant have any identical items, but due to the randomized nature of our banner numbers we would never have to worry about that factor.


* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.


In my opinion the best way to approach a situation like this one would be to implement an implicit binary tree as a Heap structure.  Heaps are uniquely fit for this scenario because no other structure can prioritize it's contents with the same amount of efficiency.  I could add things into the tree and bubble them up to their proper priority within the heap. Company X would get a key value of 1, Y would get 2 and so on where X,Y,Z,etc. can change based on their priority (aka how much they pay me).


Originality Statement
===
- All code is original unless stated otherwise within the various labs accordingly