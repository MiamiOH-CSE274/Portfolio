Author
==========
"Turner, Chace", turnerce
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


My implementation of a queue here: https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/turnerce

Based on positive feedback from our class' TA and success in all tester methods and personal testing, I feel that my implementation of a Queue was successful.  The largest issue I faced in this assignment was understanding how to use Xcode as a compiler, and after realizing the mistakes I had made in Xcode, my array based queue and it's methods began operating exactly how I had expected them to.

7 - Create an implementation of a List
----
Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/turnerce
* Use a linked list as your data structure in https://github.com/MiamiOH-CSE274/Shuffle/tree/turnerce


The linked list lab has been the most beneficial and enjoyable assignment to me so far.  Spending the time to implement splice  helped me to understand, as well as force myself to visualize, the methods involved with a linked list.  Implementing this data structure using nodes also helped me to better understand the differences between Java and C++ regarding the amount of control you have on data storage.  I believe my implementation of the Linked List was successful.


7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

* Binary Search Tree Lab https://github.com/MiamiOH-CSE274/06_BST_Lab/tree/turnerce

7 - Create an implementaiton of a Hash Table
----
Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/turnerce


7 - Create an implementation of a Heap
----
Possible sources of evidence (do any one of these):

* Heap lab https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/turnerce


7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
Possible sources of evidence (do any one of these):

* Graph lab - https://github.com/MiamiOH-CSE274/08_Graph_Lab/tree/turnerce


7 - Implement graph algorithms
----
Possible sources of evidence (do any one of these):

* Graph lab - https://github.com/MiamiOH-CSE274/08_Graph_Lab/tree/turnerce

21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)

Linked List
	find() - Ø(n) worst case running time.  Iterates through the entire list until it
		gets to the specified node.
	set() - performs constant time operations, but uses find() to assign a value to
		setter.  Also Ø(n).
	add() - Ideally runs in O(1) if i == 0 or i == size()-1, but has the possibility
		of Ø(n) because I call find() to find the location to add the new node.
	remove() - Same as add, it calls find() to carry out it's operations.  Otherwise
		it would be constant time
	get() - also depends on runtime of find()
	splice() - Operates in Ø(len + n).  We must first find(i), then we carry out
		functions in constant time for each element until we have moved
		'len' elements
	size() - Ø(1).  Just returns a member variable's data

Heap
	grow() - Uses a loop to allocate pairs from existing array into a new array that
		is twice the size.  Gives us Ø(n) running time for the looping, plus the
		some constant time operations for creating a new array and deleting the old one.
	add() - Ø(log n) running time unless grow is called. Since numItems has the same numerical
		value as our next available index, we add at numItems then simply increment it
		by one to keep it up to date (constant time). We also factor in the runtime of
		bubbleUp();
	remove() - Ø(log n).  Constant time, other than the call to trickleDown().
	bubbleup() - Ø(log n) run time. At worst case, it iterates log n times while trying to place
		the element at the correct index in terms of priority.
	trickledown() - Same as bubbleUp, it takes log n time to place the element in the correct
		index after switching the least prioritized element to the top of the heap.
	hasLessChild() - Constant time.  I created this method to incorporate into by do-while
		statement to make the coding a little easier to follow
	getNumItems() - Ø(1).  Just returns a member variable's data
Graph
	getCost() - Worst case run time for getCost should be Ø(d) for the number of edges in the
		edge list of node1.  If the loop doesn't find an edge that we're looking for, it
		will have spent time looking at each edge element for node1.
	addEdge() - Worst-case running time should be Ø(1).  Adding a new edge doesn't depend on the
		degree of any other node, number of edges, or number of nodes. It directly accesses
		and adds data to an edgeList vector.
	removeEdge() - The worst case running time for remove is Ø(3d).  Remove() uses getCost to make
		sure a connection exists between node1 and node2 (Ø(d) for node1), then loops through
		the edgeList of each node to find the correct edge, and erases it (Ø(d) for each node).
	

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.

Linked List Lab	   https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/blob/turnerce/LinkedList.ipp

The linked list lab uses Dynamic memory in a way that is very easy to see.  Each node that is added to the list requires a new pointer to be created.  At creation of a node, we are reserving more memory to store that object's data. In order to correctly free all of the memory we have used, we must tell the program to delete those objects before terminating.

In line 21-22 in LinkedList.ipp, you can see that the program calls remove() on all of it's nodes before deleting the dummyNode.  remove() deletes the node you are calling it on in line 77.  Deleting all of our pointers that have been created (most easily recognized by anything that was created using the 'new' operator) is a key element of managing memory and preventing memory leaks.


5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.

https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/turnerce

In the Heap Lab, we used a template to specify that we wanted our heap queue to hold pairs that consisted of a Priority and some piece of data (T or Typeparameter).  I think our implementation is interesting because we don't really use T at all; all we ever put in it is the same number we use for 'Pri' for each data.

Because we have done this, the same code can be used to handle any type of data a user would want to store in T.  This is the main advantage of using templates.  We can reuse code for multiple purposes if we make it generic it terms of what it will store.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

//Can use analysis of game score storage from exam

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.

SHUFFLE PROJECT - 
	For the shuffle project, it was recommended that we use either a queue or a linked list as a data structure to represent the deck being shuffled.  Between these two choices, there are some clear differences in their functionality.  If I were to use a queue it would be most beneficial when using add/remove/getNumItems because they all run in constant time.  The big downside is the time you sacrifice when grow is called, since it's worst case run-time is O(n).
	If we look at a linked list, the biggest downside is the slow run-time of find().  The rest of the methods also take O(1), so they're the same as a queue.  The biggest piece of support we have for the linked list is that even though find() has a bad run-time, we have no reason to use it in Shuffle.  That is, we have no reason to be trying to find a certain card, we are blind shuffling the deck.  On the other hand, the linked list's get() function also runs in O(n).  Since we use it quite often when shuffling, I'd have to say that a queue is the better choice for our data structure. (Even though I used a linked-list)

STORING TOP SCORES FOR ONLINE GAME
	In an exam from a previous year, there was a question about storing high score data for over 300,000 players of an online video game, and what type of data structure you should use to store them.  Users could store their name and top score, as well as display 10 scores at a time from whatever place the user specifies.  The two biggest choices in data structure for this problem were a hash table and a BST.  For the BST, we would probably use the score as the key, since we are most often looking for scores rather than names.  The big problem with the BST is next/prev would require an expensive amount of time in calling up 10 scores in order.  Much more efficient would be updating top scores if we were to use the player's name as the key in a BST.  O(h) search time to find the player's name, and constant time to update their top score is pretty good. If we think about the time it takes for a new player to add top score data, we still see a O(h) time requirement.
	On the other hand, we could use a Hash table.  Same as before, we will most often be trying to find 10 scores in a row, as well as adding new scores to our data.  Add takes constant time so long as grow() isn't called, and find() keyExists() also operate in constant time, making it fast for us to call up certain scores if we use the hash value of a player's score as the index.  The big downside for the hash table is searching and replacing data based on the user's name (O(n)).
	I think since we're using a very large amount of data (would be difficult to keep a BST balanced) and we're usually looking up data by score, the hash table is the better choice for this player data storage.