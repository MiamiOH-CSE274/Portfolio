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
https://github.com/MiamiOH-CSE274/03_Queue_Lab/blob/continnd/ArrayQueue.ipp

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
Proof:
https://github.com/MiamiOH-CSE274/07_Heap_Lab/blob/continnd/HashTable.ipp

7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
Proof:
https://github.com/MiamiOH-CSE274/08_Graph_Lab/blob/continnd/Graph.cpp

7 - Implement graph algorithms
----
Proof:
https://github.com/MiamiOH-CSE274/Vise/blob/ContiniAndKojs/src/testApp.cpp

21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)

Linked List:

* Constructor-O(1), since it always creates just one node and then connects it to itself
* Destructor-O(n), since the method visits every node to remove it, the destructor depends on the number of items in the list
* find(i)-O(n), since in order to return the node that is right in the middle of the list you have to travel to every node before it, find relies on the number of items in the list. However, you can find an item at the beginning or the end of the list with O(1) time, since the list is circular, allowing you to move forward or backwards through the array.
* set(i,x)-O(n), since it uses find(i) to change the data value of a node.
* add(i,x)-O(n), since it uses find(i) to find the point where to add the new node. There will always be a constant number of links rearranged, thus meaning add(i,x)'s efficiency depends on the number of items. Adding to the beginning and end of the list, however, has a constant time due to the list's circular structure.
* remove(i)-O(n), since it uses find(i) to find the node to remove. There will always be a constant number of links to rearrange, meaning delete(i)'s time depends on the number of items. Deleting a node from the beginning or the end of the list, however, has a constant time due to the list's circular structure.
* get(i)-O(n), since it uses find(i) to simply return the data held within a node.
* splice(i,len,target,t)-O(n+m), where m is the index of the second list. First the method must use find(i) to find the beginning of the segment that will be remove, an then continue to the end. Then it must use find a second time to find the point to add the segment to the second list. The number of links to rearrange will be constant, making the the method's time depend on the number of items in both lists.
* size()-O(1), since all this method does is simply return the value stored by the variable numItems.

Binary Search Tree:

* BSTs are structured so that all nodes that have keys less than a specific node are all represented on the left side of that node and all nodes with keys larger than a specific node are all represented on the right of that node, methods must only check some of the values of a specific branch in the tree rather than all of them to travel to a specific key. The branches can range from height 0 to height n. In a perfectly balanced tree, the branches always have a height of log(n). This is due to the fact that the last row of nodes in a tree contains 1 more node than the rest of the tree.

* Constructor-O(1), since all this does is set the variable root to NULL.
* Destructor-O(n), since the method visits every node to remove it, the destructor depends on the number of items in the list
* size()-O(n), since the method first must visit every node and return 1 plus size(r) called on the adjacent nodes.
* add(k,x)-O(h), since the method must travel to the bottom of a branch in order to create a new node to store the data.
* remove(k)-O(h), since the method must first find the node to remove, the furthest one down requiring thee method to travel the height of the tree. Even when removing an internal node, the method may have to travel further down a branch to find a node to replace the removed node.
* find(k)-O(h), since the method must at maximum travel to the leaf of the tallest branch to find the key and return the node's value
* keyExists(k,r)-O(h), since the method at maximum must travel to the leaf of the longest branch to check to see if the key exists
* next(k)-O(h), since the lowest node in the tree that can be numerically next is the leaf of the longest branch.
* prev(k)-O(h), since the lowest node in the tree that can be numerically previous is the leaf of the longest branch.
* max(r)-O(h), since the method simply travels continually to the right until it reaches a leaf node. This leaf node can possibly be part of the longest branch.
* min(r)-O(h), since the method simply travels continually to the left until it reaches a leaf node. This leaf node can possibly be part of the longest branch.

Hash Table:

*Constructor-O(1) Simply allocates an array, sets numItems to 0, numRemoved to 0, and backingArraySize to the size of the array. (This is assuming that it is an array of primitives, if it were an array of objects, each index would have to be initialized meaning efficiency would be O(m) where m is the size of the array).
*Destructor-O(1) Simply deletes the array. This may be O(m) if the array is an array of Objects, since every object must be deleted as well.
*add-O(1) Running the hash method will always be constant, since it has a fixed number of operators. The likeliness of a collision is so low that you can ignore the possibility. Even if there is a collision, using the jump method decreases the likeliness of a collision happening again, so the most collisions you could probably have is about 3. After all the hashing/jumping, all the method has to do is set the data and key to the correct values. Grow may have to be called, meaning this would bring the method to O(m) efficiency, but it will have to be called less and less as it gets called making the method negligible.
*remove-O(1) As said above, hash and jump help the hash table find the key that you are looking for and delete those values, as well as setting isDel to true. All of this has a constant number of operations.
*find-O(1) Once again, hash and jump making finding the data point in the array constant time, as the number of collisions will be minimal in most realistic situations.
*keyExists-O(1) Simply must find the index the key would be stored at and return true if it finds it, otherwise returns false. Finding a key and returning a value are constant.
*size-O(1) Simply returns the class variable numItems which is constant
*grow-O(m) Since the method has to go through the whole array to ensure that every value gets copied to the new array, this method's time will be based on the size of the array.
*jump-O(1) Jump essentially is a bunch of mathematical operations that all take constant time.


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Proof:
https://github.com/MiamiOH-CSE274/05_Hashing_Lab/blob/continnd/HashTable.ipp

The dynamic memory portion of the hash tables has to increasing the capacity of the array. Grow will create a new array to avoid increasing the number of collisions, so once all the data is copied to the new array, it is important to delete the old array to avoid having a memory leak. There are no dangling pointers in my code either since my backingArray pointer will always point to an array after deleting the old array. Any pointer not being used (i.e. oldBackingArray) are deleted.


5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.

https://github.com/MiamiOH-CSE274/Vise/tree/ContiniAndKojs/src

I used a template to create my hexSpace class in order to create an easy way to set up a gameboard using a vector. There was probably many other things I also should have done, such as creating a gameBoard class that included the setup, traversal, and other methods of the gameboard.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.

Shuffle:
		For Shuffle, both an Array-Based Queue and a Doubly-Ended Linked List seem like good options for shuffling. In most generic shuffles, neither seem to have significant advantages. This is due to the fact that splitting the queue into two queues will not be much faster than if the queue were substituted for an linked list. Same goes for taking one or more cards from the top of the deck to mix back into the deck. So for most shuffles such as riffle and faro efficiency trade off is mostly negligible. The only time I could think of a situation where a Linked List might have an advantage is a shuffle that simply takes a portion of the deck and places it on the top or bottom of the deck. The issue with those type of shuffles is that it takes many repetitions to result in a truly randomly ordered deck (it may be even possible that the deck never becomes randomly ordered!). Queues cannot take a chunk of cards from the middle of the deck, so any shuffles requiring taking cards anywhere other than from the top of the deck can't be implemented with Queues, since they use FIFO structure.

				Queue								Array List
Copy current deck
from array

to data structure:	O(n) (technically O(1) since n is always 52)		   O(n) (technically O(1) since n is always 52)

Peeling of c cards
from top of deck:		O(c)								   O(c)

Adding c cards back
to the array			O(c)								   O(c)

*take note that moving the cards left in the array, c, to the front is also O(c). Also since the number of cards 

Vise: 

	Two potential data structures one could use are adjacency lists or adjacency matrices. Adjacency lists have an advantage in that they don't unnecessarily require more memory. Adjacency matrices use a two dimensional matrix where one dimension represents the current node, and the second dimension represents a potenial edge to another node. Adjacency lists are similar in that they use matrices that contain linked lists that contain every edge in the system. This means adjancency matrices have to reserve memory for every possible edge, wherease adjacency lists use up memory for edges only when the edge is added. This also means when searching for edges, adding edges, and removing edges, adjacency matrices are less effecient, running at Theta(n). Adjacency lists do these operations at Theta(d), d being the maximum number of edges on a node. This disadvantage is also seen when doing graph traversals (Theta(n^2) for matrices and Theta(n+m), since during the traversal you must search for every node. One advantage the matrix does have is that it is much quicker looking at a specific edge. So if I specifically want to see if there is an edge between two nodes, the efficiency will be Theta(1) for matrices, but still Theta(d) for lists. This advantage is of no help while implementing vise though, so the best choice for vise is an adjacency list or a structure based on an adjacency list.

extra credit: I went to the research fair. I saw your research in Augmented Reality, Mr. Stanley's computer security research, someone's AI linguistics research, and many others.


