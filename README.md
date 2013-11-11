Author
==========
"Contini, Nick", continnd
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
Proof:
https://github.com/MiamiOH-CSE274/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
Proof:
https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/blob/continnd/LinkedList.ipp


7 - Create an implementation of a Binary Search Tree
----
Proof:
https://github.com/MiamiOH-CSE274/06_BST_Lab/blob/continnd/BST.ipp

7 - Create an implementaiton of a Hash Table
----
Proof:
https://github.com/MiamiOH-CSE274/05_Hashing_Lab/blob/continnd/HashTable.ipp

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
Linked List:
Constructor-O(1), since it always creates just one node and then connects it to itself
Destructor-O(n), since the method visits every node to remove it, the destructor depends on the number of items in the list
find(i)-O(n), since in order to return the node that is right in the middle of the list you have to travel to every node before it, find relies on the number of items in the list. However, you can find an item at the beginning or the end of the list with O(1) time, since the list is circular, allowing you to move forward or backwards through the array.
set(i,x)-O(n), since it uses find(i) to change the data value of a node.
add(i,x)-O(n), since it uses find(i) to find the point where to add the new node. There will always be a constant number of links rearranged, thus meaning add(i,x)'s efficiency depends on the number of items. Adding to the beginning and end of the list, however, has a constant time due to the list's circular structure.
remove(i)-O(n), since it uses find(i) to find the node to remove. There will always be a constant number of links to rearrange, meaning delete(i)'s time depends on the number of items. Deleteing a node from the beginning or the end of the list, however, has a constant time due to the list's circular structure.
get(i)-O(n), since it uses find(i) to simply return the data held within a node.
splice(i,len,target,t)-O(n+m), where m is the index of the second list. First the method must use find(i) to find the beginning of the segment that will be remove, an then continue to the end. Then it must use find a second time to find the point to add the segment to the second list. The number of links to rearrange will be constant, making the the method's time depend on the number of items in both lists.
size()-O(1), since all this method does is simply return the value stored by the variable numItems.

Binary Search Tree:
BSTs are structured so that all nodes that have keys less than a specific node are all represented on the left side of that node and all nodes with keys larger than a specific node are all represented on the right of that node, methods must only check some of the values of a specific branch in the tree rather than all of them to travel to a specific key. The branches can range from height 0 to height n. In a perfectly balanced tree, the branches always have a height of log(n). This is due to the fact that the last row of nodes in a tree contains 1 more node than the rest of the tree.

Constructor-O(1), since all this does is set the variable root to NULL.
Destructor-O(n*h), since the method must first travel the height of the tree. It does this for every item in the tree.
size()-O(n), since the method first must visit every node and return 1 plus size(r) called on the adjacent nodes.
add(k,x)-O(h), since the method must travel to the bottom of a branch in order to create a new node to store the data.
remove(k)-O(h), since the method must first find the node to remove, the furthest one down requiring te method to travel th height of the tree. Even when removing an internal node, the method may have to travel further down a branch to find a node to replace the removed node.
find(k)-O(h), since the method must at maximum travel to the leaf of the tallest branch to find the key and return the node's value
keyExists(k,r)-O(h), since the method at maximum must travel to the leaf of the longest branch to check to see if the key exists
next(k)-O(h), since the lowest node in the tree that can be numerically next is the leaf of the longest branch.
prev(k)-O(h), since the lowest node in the tree that can be numerically previous is the leaf of the longest branch.
max(r)-O(h), since the method simply travels continually to the right until it reaches a leaf node. This leaf node can possibly be part of the longest branch.
min(r)-O(h), since the method simply travels continually to the left until it reaches a leaf node. This leaf node can possibly be part of the longest branch.

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.


5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.