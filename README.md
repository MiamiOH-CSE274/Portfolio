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

* https://github.com/MiamiOH-CSE274/03_Queue_Lab

7 - Create an implementation of a List
----
Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab

7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

* Binary Search Tree Lab (TODO)

7 - Create an implementaiton of a Hash Table
----
Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/05_Hashing_Lab

7 - Create an implementation of a Heap
----
Possible sources of evidence (do any one of these):

* Heap lab (TODO)

7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
Possible sources of evidence (do any one of these):

* Graph lab

7 - Implement graph algorithms
----
Possible sources of evidence (do any one of these):

* Graph lab

21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)
* Linked List: 
* (1) find(): If the index of the item is out of boundary or the item is dummy node, assuming the exception call takes constant time, then find() will be O(1). Otherwise, find() can be O(n) because the line of code in for loop brackets takes linear time.  
* (2) set(): How much time set() can take really depends on the time find() takes, since assigning values only takes constant time. So, the worst case running time can be O(n).
* (3) add(): Just like set(), how much time add() takes depends on the running time of find(), since switching pointers and assigning values take constant time. add() can take linear time in the worst case.   
* (4) remove(): Assuming the exception call takes constant time, if there is no item in the linked list, remove() is O(1). Otherwise, the running time of find() plays an important role on deciding the running time of remove(), since switching pointers and updating the number of items take constant time. remove() can take up to linear time in the worst case. 
* (5) get(): The analyzing strategy of the running time of set() can apply here.    
* (6) size(): size() is O(1) because returning a value takes constant time.
----
* Hash Table: 
* (1) add(): If grow() does not get called, assuming hash() and modulus calculation take constant time, then add() would be O(n) theoretically in the worst case, since I implemented add() using linear probing, which could go through every bucket to search for an empty spot. However, in real-life cases, linear probing takes constant time and therefore add() should be O(1). If grow() gets called, then add() would be O(n). See (6) grow().  
* (2) remove(): 
* (3) find():
* (4) keyExists():
* (5) size(): size() takes constant time 
* (6) grow():
Graph(Adjacency List): getCost()--O(d) add()--O(d) remove()--O(d), where d is the maximum degree of any node in the graph

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.
Hash Table:(link)
I used the operator "new" to allocate a chunck of dynamic memory to store the array of HashRecords, and, to avoid memory leak, I implemented the destructor to deallocate the memory that stored whole array. In size() method, I switched the pointer, backingArray, from the old array that I deleted at the end to the new array in case the pointer became a dangling pointer. Through thoroughly testing, I claim there is no out-of-bound error in this lab.     

5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.
