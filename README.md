Author
==========
"Zhong, Mingwei", zhongm2
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

Implementing array-based Queue:

https://github.com/JohnneyMing/03_Queue_Lab


* https://github.com/MiamiOH-CSE274/03_Queue_Lab
* Use a queue as your data structure in https://github.com/MiamiOH-CSE274/Shuffle
* Consult with Dr. Brinkman on an alternative project



7 - Create an implementation of a List
----
Possible sources of evidence (do any one of these):

Implementing Linked_List:

https://github.com/JohnneyMing/04_Linked_List_Lab


* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab
* Use a linked list as your data structure in https://github.com/MiamiOH-CSE274/Shuffle
* Implement chaining instead of linear probing in https://github.com/MiamiOH-CSE274/05_Hashing_Lab
* Consult with Dr. Brinkman on an alternative project



7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

Implementing Binary Search tree:

https://github.com/JohnneyMing/06_BST_Lab


* Binary Search Tree Lab (TODO)
* Use a binary search tree or KD-Tree in the Starbucks project.
* Use a binary search tree in the Zeitgeist project
* Consult with Dr. Brinkman on an alternative project


7 - Create an implementaiton of a Hash Table
----
Possible sources of evidence (do any one of these):

Implementing hash table:

https://github.com/JohnneyMing/05_Hashing_Lab


* https://github.com/MiamiOH-CSE274/05_Hashing_Lab
* Use a hash table in the Zeitgeist project
* Use locality-preserving hashing on the Starbucks project (not recommended!)
* Consult with Dr. Brinkman on an alternative project

7 - Create an implementation of a Heap
----
Possible sources of evidence (do any one of these):

Heap lab: https://github.com/MiamiOH-CSE274/07_Heap_Lab

* Heap lab (TODO)
* Implement heap sort in the Sorting lab (TODO)
* Implement a heap as part of the Graph Algorithms lab (TODO)
* Implement a heap as part of the Graph Project (TODO)
* Consult with Dr. Brinkman on an alternative project

7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
Possible sources of evidence (do any one of these):

Graph lab: https://github.com/MiamiOH-CSE274/08_Graph_Lab

* Graph lab
* Graph Algorithms lab
* Graph project
* Consult with Dr. Brinkman on an alternative project

7 - Implement graph algorithms
----
Possible sources of evidence (do any one of these):

Graph lab: https://github.com/MiamiOH-CSE274/08_Graph_Lab

* Graph lab
* Graph Algorithms lab
* Graph project
* Consult with Dr. Brinkman on an alternative project

21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)

*******************************************************************************

Queue Implementation:

https://github.com/JohnneyMing/03_Queue_Lab


The running time for `add()` method is constant, unless `grow()` is called.

The running time for `remove()` method is constant. Since this method is to
remove the first element from array.

The running time for constructor is constant if the type parameter is basic 
type. But it might take linear time if type parameter is a class, because
a class can handle more than one datatype.

The running time for destructor is constant if the type parameter is basic
type. Same as `constructor`, it might take linear time if type parameter
is a class.

The running time for `grow()` method is linear, because you need to copy the 
number of N elements from original array and add them to new array.


Space requirement:

I used circular array, the space is the initial size of array. 


*******************************************************************************


Linked-list Implementation:

https://github.com/JohnneyMing/04_Linked_List_Lab

The running time for constructor is constant.

The running time for destructor is linear time, since you need to loop through
entire list by using while loop and call `remove()` method.

The running time for `find()` method is linear, except you are looking for the
last item or the first time in the list, which will be constant time.

The running time for `set()` method is linear, since you need to invoke 
`find()` method to access the node that you want to make changes.

The running time for `splice()` method is linear, since it invokes `find()`
method.

The running time for `remove()` method is linear, since it invokes `find()`
method.

The running time for `get()` method is linear, since it invokes `find()` method.

The running time for `add()` method is linear, since it invokes `find()` method.

The running time for `size()` method is constant, since it simply returns the 
the number of item in the list.


Space requirement:

Classical double-linked list, it has three pointers: pre, next and data.


*******************************************************************************

HashTable Implementation:

https://github.com/JohnneyMing/05_Hashing_Lab/tree/zhongm2

The running time for constructor is constant. 

The running time for destructor is constant.

The running time for `size()` method is constant, it only returns the number
of element in the array.

The running time for `keyExists()`, `find()`, `remove()` and `add()` are 
constant time if the hashtable was designed approritately.

The running time for `grow()` is linear, because you need to copy N elements 
from original hash table to new hash table.


Space requirement:

The largest space is the size of hash table.


*******************************************************************************


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.

My linked-list lab(https://github.com/JohnneyMing/04_Linked_list_Lab) uses
dynamic memory allocation. 

1. In the constructor in LinkedList.ipp file, `dummyNode = new Node()` is using dynamic memory allocation by using `new`,it created a memory block on heap. 
In Java, when you use `new`, an object will be created on JVM heap.

2. The local variables in each function are allocated on the `Stack` of the
program. In Java, local variables are also stored on the `Stack`.

3. Memory leaking in C++ means an object is stored in memory can not be accessed by the running code. Dangling pointers are pointers that do not point to a 
valid object of the appropriate type(WIKIPEDIA). This program does not leak
memory, and does not suffer from dangling pointers. In `remove()` method, once  you find the node that needs to be removed, `delete` it (memory freed up). And 
set the node to be `NULL` to avoid suffering from dangling pointers. 

4. Java allocates memory by using `new` operator, and dellocate memory by 
relying on the garbage collector. The garbage collector performs memory 
management automatically. It can deallocate memory occupied by objects that are
no longeer in use by the program.



********************************************************************************


5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.

For instance, in my Queue lab:

https://github.com/JohnneyMing/03_Queue_Lab

Using template to mimic an intreface in C++.



30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):



* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.

