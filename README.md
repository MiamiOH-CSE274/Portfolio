Author
==========
"Mullins, Harrison", mullingh
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

* https://github.com/mullinz/03_Queue_Lab/tree/mullingh
* The reason I deserve credit for this learning outcome is because I successfully completed the Queue Lab.  I implemented an array based queue (through a circular array) and completed all of the assignment's requirements.

7 - Create an implementation of a List
----

* https://github.com/mullinz/04_Linked_List_Lab/tree/mullingh
* The reason I deserve credit for this learning outcome is because I successfully completed the Linked List lab.  I was able to implement a simple linked list through the use of pointers and classes, and completed all of the necessary requirements.  I also completed the optional splice() method.


7 - Create an implementation of a Binary Search Tree
----

* https://github.com/MiamiOH-CSE274/06_BST_Lab/tree/mullingh

7 - Create an implementation of a Hash Table
----

* https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/mullingh

7 - Create an implementation of a Heap
----

* https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/mullingh

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----

* https://github.com/MiamiOH-CSE274/Vise/tree/GriffithAndMullins

7 - Implement graph algorithms
----
Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/Vise/tree/GriffithAndMullins

21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)
Binary Search Tree:
	* Since we did not balance the tree the running times are as follows: search is O(h), add is O(h), remove is O(h), and grow is O(h).  The space complexity at its worst would be O(n log(n)).  If we had balanced the tree we could have averaged O(log(n)) for all the methods(except possibly grow).
Linked List:
	*Get is O(1), add is O(1), remove is O(1), set is O(1), and search is O(n).  The space complexity is O(n).
Hash Table:
	*Add and remove are O(1), hash is (n), and grow(at its worst at the beginning) is O(n).

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

* In C++ we get full access to allocating memory on the heap and the stack.  This can cause issues because with poor logic or incorrect usage control of these things can lead to memory leaks.  In my hashing lab(linked above) I had to de-allocate the space the hashtable was stored in the destructor to ensure that my program wouldn't leak memory.  

5 - Create collection classes using templates in C++
----

* The hashing lab is what I feel represents one of the better uses of the template class.  We were able to use the template class to create a hash table that could store any form of data(slightly exaggerated) that we need which is really practical in a real world sense.  In reality hash tables need to store various forms of data so the implementation of the template class in this instance was greatly warranted.  Also it in general just makes code, especially data structures, re-usable which is always a good thing in development.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

* Vise Project: The reason we chose an adjacency list data structure for this project was that we knew we would frequently have to be adding "vertices" to the game board and we wanted that to be fast after the board creation.  Since storage wasn't necessarily an issue for this and an adjacency list is relatively efficient in storage space being O(vertices + edges) we chose to go this route.  This data structure allowed us to add vertices in constant time, which if this game scaled up would be a significant feature.  So direct and constant access to nodes was what we thought the major value that adjacency lists brought us.  If we had simply used an array instead we would not have had that constant running time access to adding nodes.
* Shuffle Project: 