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

Proof of Queue implementation here: 
* https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/zirkleac

My queue adds to the queue and removes the first in the queue when called. it gets the correct number
items in the queue and does all of it in the correct length of time.

7 - Create an implementation of a List
----
Possible sources of evidence (do any one of these):

Proof of List implementation here: 
* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/zirkleac

My list is a doubly linked list which allows an add, remove, get and set in constant time, throwing errors where
appropriate. Not leaking memory


7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/06_BST_Lab/tree/zirkleac
* This works for some cases but required more work in the next and previous methods
* https://github.com/MiamiOH-CSE274/ClosestStarbucks/tree/zirkleac
* This is a 4 way b tree which checks for the closest starbucks given a latitude and longitude


7 - Create an implementation of a Hash Table
----
Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/zirkleac
This is just a basic hashtable wihc works in constant time most of the time, O(n) at the worst

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

* https://github.com/MiamiOH-CSE274/08_Graph_Lab/tree/zirkleac
* https://github.com/aczirkle/Vise


7 - Implement graph algorithms
----
Possible sources of evidence (do any one of these):

* https://github.com/aczirkle/Vise
* The vise project uses graph algoithms to find if the pieces remain connected

21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

*  Graph:
*  Space would be dependant on the number of connections and size of the aarray
*  Creation would be dependant on the size of the array you are creating
*  Adding and removing connections are O(n)
*  Searching is O(1)

*  Linked List:
*  Space depends on the number of items in the array
*  Creation is O(1)
*  Adding and removing from the array is O(n) because it depends on the size of the array
*  Searching is O(n)

*  Hash Table:
*  Space is dependant on the size
*  Creation is O(1) because the dummy node is just
*  Adding a new item is dependant on the number of collosions but effectively becomes O(1)
*  Searching is dependant on the number of collisions but effectively becomes O(1)


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.

The linked list lab is a good example of usage of dynamic memory as it creates a new section of memory for each object that is added and pointers are added to the next in the list and the previous in the list. When the object is deleted the data stored is deleted, and the object's position pointers for the previous and next reference each other rather than the deleted object.

5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.

The shuffle project was one that could have had different data structures as there are multiple types of shuffling. A linked list would be the first I can think of which would work and a hash table would work as well. They would both take about the same amount of time to create, but I think the hash table would be easier to shuffle if you just created two hashtables each with half the data in it and mixed them back together into the first hashtable while linked list would require either doing the same thing or adding a dummy node somewhere in the list and then adding the data into new list. The linked list might be less memory intensive in that case.


EC  
----
I went the research fair.

And here is a CS (related) limrick

There was a man whose life was a mess

which he blamed on his GPS

he was never on time,

it was the design

it used binary search was total BS
