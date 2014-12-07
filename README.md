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
I have created a working queue program and my evidence is my ArrayQueue.ipp file.
https://github.com/dieterc2/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
I have created a working linked list data structure and my evidence is my LinkedList.h file.
https://github.com/dieterc2/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
I have created a working binary search tree data structure and my evidence is my BST.h file.
https://github.com/dieterc2/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
TODO: Provide a link to your completed 05_Hashing_Lab

7 - Create an implementation of a Heap
----
I have created a working heap data structure and my evidence is my Heap.h file.
https://github.com/dieterc2/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
I have created a working adjacecny list in my Graph.h file for a graph data structure.
https://github.com/dieterc2/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
TODO: Provide a link to your completed Vise project (only if you used graph traversal), or add a graph traversal to 08_Graph_Lab and provide a link

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List
	The biggest differences that array-based lists and linked lists have between each other is that the linked list does not use an array to store data while the array-based list does. In terms of running time, they 
	experience different runtimes for most operations because of their structures and how the program can access each data set. In the array-based list, for example, the add and remove funtions take O(n) time because 
	it has to iterate through the array to find which element to take out. The worst case run time would be dependant on every element in the array. In contrast, the add and remove functions of the linked list take 0(1)
	time because adding and removing do not depend on the number of elements in the data structure. Instead, node surgery is done on the list at a single point so that all of the other data sets do not have to be moved. 
	The get and set methods of a linked list do take 0(n) time to complete though because the program needs to iterate through the arrays in order to find the correct node to operate on. This is different than in the 
	array-based list because the program can access array elements with the preset array functions. This allows for 0(1) runtime for get and set functions in array-based lists. Finally, both the array-based list and the
	linked list have a size function with 0(1) time because all this function does is return a counter variable that is updated elsewhere in the program. Iterators can be implemented in a linked list 	
	to enhance some run times. For a linked list, geting and seting at an iterator takes 0(1) time, a huge improvement from the original 0(n) time. Unfortunately for the array based list, adding and removing elements cannot
	be sped up by iterators because once an element is added or removed at an iterator, the rest of the list must be modified to account for the added index or the empty index.  
* Binary Search Tree vs. Hash Table
	Like the main difference between array-based lists and linked lists, one of the major differences between the binary search tree and the hash table is that the hash table uses a backing array while the binary search 
	tree uses nodes. Moreover, additions into the hash table require a hash function, and are not sorted upon entry (instead, the hash function computes an index in the array). This creates 0(1) run time because adding at 
	an index in an array takes constant time. For the binary search tree, additions are made with regards to keeping the tree sorted. A node is first compared to the root node to see if it is larger or smaller, and then goes 
	down the directed path, effectively eliminating one half of the root’s sub-tree that it is currently being compared with. This takes 0(lg(n)) time. For remove, the hash table also takes 0(1) time if given a key, because 
	the hash can be performed on the key, finding the exact index at which the key is stored. The binary search tree still takes 0(lg(n)) time because  	of the time it takes to find the key of which to delete. This is done 
	by progressively going down a branch of the tree, comparing the key with a root and then proceeding down one of the roots’ sub-tree’s branches. This process of finding the key on which to operate is also why get and set, min 
	and max, and next and previous are 0(lg(n)) time, because at most half of the nodes must be touched upon to find the key. Hash tables run get and set in constant time because of their ability to compute the exact index of the 
	key in the array, but run min and max and next and previous in 0(n) time because of the unsorted nature of the hash table. Every value must be compared with the picked key in order to ensure that the right next or previous key 
	has been chosen. Finally, the min and max of an unsorted array can only be found by touching on every node, which is why hash tables have bad run times for these operations. 
* Adjacency List vs. Adjacency Matrix
	Adjacency lists and adjacency matrices differ in the way they present vertices and edges in a graph data structure. Adjacency matrices come with a more explicitly presented picture of edges and vertices using a two dimensional
	array with rows and columns for each vertices. Initially, if no edges are present, every index in the two dimensional array is set to a default value, and as edges are added, a weighted value is set to the row of the node that 
	the edge is coming from and the column that the edge is going to. Since adjacency matrices work with arrays, adding edges, removing them, and getting a weight of an edge all takes 0(1) time. The downfall of the adjacency matrix 
	is the amount of space in memory it takes up, which is precisely 0(n^2) (which is ok if the number of nodes equals the number of edges). Furthermore, the get neighbors function takes 0(1) time because it has to go to the node, 
	then check it against every other node to see if the value is a weighted edge. Adjacency lists use an array of lists to cut back on the space that a graph data structure can take. The size of an adjacency list is 0(n + m), where 
	n is the number of nodes and m is the number of edges, which will be much smaller than the adjacency matrix. Each node or vertices is an index in the array, and a list of its neighbors occupies the list of that index. Thus, get 
	neighbors takes 0(1) times because it is just returning an array index. Getting weight of an edge is 0(n) time because the function has to go through every value in the list to see if it is the corresponding node. Finally, adding 
	an edge and removing an edge in the adjacency list takes 0(d) time where d is the constant degree (no node has more than d neighbors). This makes sense because these functions have to find each node and its corresponding partner 
	of which to add or remove an edge with. Thus, adjacency matrices may have faster run times with adding and removing, but adjacency lists take up less space and return neighbors of vertices faster.

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!) - The call stack is a special portion of memory that the program uses during runtime. As the instructions from the program execute, local variables, parameters,
	and functions all get stored within this part of memory. It is a last in first out stucture, so as variables get stored and executed, they are popped off the list as soon as they are not needed anymore. This allows for their
	memory locations to be overwritten. A stack overflow can occur if the program puts more information into the stack than what it was originally allocated. 
* The heap (not to be confused with the heap data structure!) - The heap is a portion of free memory for the program that is used to store dynamically allocated variables. Anytime the program delcares a new object, memory
	is allocated from the heap because that is where the free memory is stored. Once an object has been properly deleted, the memory is returned to the heap.
* Address - This is the actual location of where the data is stored in memory. For example, the address of a string variable 'c' could be 6626. 
* Pointer - A pointer is a type of variable assignment that stores the address of a variable. Any type can be a pointer, though a star must be added at the end to show it as a pointer. 

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad? A memory leak is when parts of the program have not be deallocated after they are used. So even if the program is finished running, the part in memory where the objects were stored would still
	be in use, not allowing that reserved memory to be overwritten. Memory leaks are bad because they cause the computer to use more memory than it has to, eventually causing the the RAM to run out entirely and rely on the hard disk to 
	store information.
* What is a dangling pointer (or dangling reference), and why is it dangerous? - A dangling pointer is a pointer that does not point to a valid object or data, in that what was stored in memory has been deleted (leaving the pointer behind). These are
	dangerous because they take up space in memory and can lead to unpredictable behavior in the program. Specifically, if the pointer is called to perform functions, many bugs will arise because the pointer is pointing to nothing. 
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java? - A deconstructor is a function that deallocates the memory that was used to store new objects and other parts of the program.4
	They are necessary in C++ because the language does not automatically deallocate memory when the program is done with it. We do not need these in Java because the JVM is smart enough to know when dynmically allocated variables have reached
	their lifespan and deletes it at this point. 

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++
* What is the main benefit of using templates when creating collection classes? - One of the main benefits of using templates for collection classes over using classes is that a template can be created to accept any data type unlike classes which
	have to be specialized to handle different types of data. Also, templates are typesafe because the compiler knows the data types before compile time, so it can check for errors before they occur.
* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes. - This is because whenever a template class is instantiated within a .cpp file, 
	a class is created with the argument of the template. When this class becomes instantiated, the compiler will have to find out where the private functions and variables are to create the class with the template arguments. Thus, it will look in the	
	.h file that is included with the program. Without the inclusion of the template within the .h file, the compiler will not be able to find the private functions and variables of the newly instantiated class. 


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
	From the requirements description of what will be stored in the data structure, it can be assumed that this problem most clearly needs a structure that operates well on an unordered set of data. I would then implement a hash table to handle this data set. A hash table is specifically designed for unordered sets, and does not allow 
	for duplicates (which is a requirement for this scenario). Furthermore, order does not matter in this data set. The strings will be added to the hash table in any order, and the hash function will take care of filling up the table while keeping collisions low. To do this, a hash function should be created so that small changes in the 
	key results in large changes in the computed hash index. For example, if the key is the string, it can be valued in its ascii value, then multiplied by a random number, then added with another random number (what we used in the hash table lab, a*key + b). Once the string is put in the table, all add, remove and get functions will operate 
	in 0(1) time. This is because in all these scenarios, the index is already known by the hash function. For instance, the get function will take a key and then compute its hash function which will be the index of where the string is stored in the array. Then, a simple array access operation takes place to complete the query. The only precaution 
	that should be taken when using a hash table for this scenario would be to proactively defend against collisions. Collisions happen when two different keys are hashed to the same index. To avoid this, I would implement an open addressing collision resolution system. Once a string is hashed to an index that is already occupied, the add function 
	continues linearly down the table until the first open index is available. Though this is not exactly 0(1) time, good hash functions will cut down the number of collisions so that the open addressing solution will only be implemented once the hash table is nearly filled. To get a key, the get function will have to implement linear probing to find 
	the correct element. Once a collision happens, the get function will find the index of the element without taking open addressing into account. So, it will have to compare the key it wants to the key that is stored in the table linearly down the table until the correct string is found. Again, the added time this takes should be negligible because 
	collisions will be low. A hash table is the best solution to this scenario of storing strings into a data structure because of its compatibility with unordered sets, assuming that the hash function is well written and collisions are low. 
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	I will first define a grocery list as the model I have been using all of my life. I start out by writing each individual product on its own separate line, starting at the top. Then, at the grocery store, I start at the top of the list and work my way down. This resembles a first in first out queue. If I remember a product that I had previously forgot, I add it to the bottom of the list, though this is a rare scenario. Because I will only use the add and remove functions a few times throughout the lifespan of this data structure, I will not mind a slower run time for these functions if it means a faster run time for get and set, which would be used much more often during the shopping trip as I go through the list and find the next grocery item on the list. An array based queue should work well for this if the add function is initially called in the beginning to fill the array, and then sparsely called throughout the duration of the trip. Moreover, I never have more than fifty items on my list, so an 0(n) run 	time for this data structure will be acceptable (even adding a thousand items to an array list is quite fast). Then, as I go down the list and access each item on the list, this get function will take 0(1) time and will be called much more frequently than the add and remove functions. Also, if I am in an aisle and want to find out if any of the other items on my list are in that aisle before moving on, the array based queue is very compatible with random access, such as getting an item in the middle of the list. The frequency of which I will be calling get during the lifetime of the data structure (and the low frequency of add and remove calls) makes the array based queue an obvious choice to implement for my grocery list scenario.
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	The banner id resembles a dictionary style data structure, in that given a banner id; one can look it up in the dictionary and find the data about the student next to the id. However, the way in which a banner number is assigned must be known in order to find out if there is an order to the data structure. For example, if the banner numbers are ordered then student A could be assigned +00000000, and student b would then be +00000001. Or, as I remember correctly was mentioned in class, the banner id system could be assigned as a hash from a student’s social security number. For this scenario, I will assume that the second form of banner id assignment is the way in which a student is actually assigned an id number. The hash table would then be a very reasonable approach to this scenario because the banner ids are not interdependent, thus making the whole collection of students an unordered set which is compatible with the hash table (all functions are 0(1) time except functions that deal with ordering – next, 	prev, etc…). Every query that the user makes with a banner id number will operate in 0(1) time with a good hash function. I would use the same collision resolution techniques as I explained earlier in the first essay question, with an added precaution of making the initial size of the hash table very large to account for the number of students that would be in the database. The whole situation would be flipped on its head, though, if the first assignment method for banner ids was used instead of the hash of the social security number. Then, all the data would be an ordered set and the hash table would be the worst data structure to traverse between students or to get a list of all students in order. I would use a binary search tree for this scenario because it offers the fastest runtimes for dealing with an ordered set (0(lg n)). Although lookup time of a student would be slower than the hash table, traversing through students sequentially would be quick and easy, something that the hash table is not able to 	do in an efficient manner. 
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	This scenario presents an ordered set that has key values as the amount of money that each company pays me to send out their packets, and those keys have a priority in favor of the highest bidder. A binary search tree could be useful here because of the order, though a priority queue seems more obvious because of the way the keys are ordered. In this case, a heap would be a safe data structure to use for implementing this scenario because of its aptitude with operating on ordered sets that have a priority. If I wanted to add a company to the priority queue, I would first add it the very end of the array, and then bubble it up the array until it falls into the right spot compared to the other keys in the array. This would take 0 (lg n) times. Since the heap implements an implicit binary tree, getting the packets of each company would be fairly easy and quick in a heap. The highest paying company would always be the first element of the array since their priority is the largest, so a simple array[0] call would 	suffice to get those packets. Furthermore, if it can be assumed that the highest paying company would also be the most frequent array access call, get would take 0(1) time and this company would be very happy with the speed at which their packets are received. All other get calls would follow the form of the binary tree, in that they would have to be found in one of the branches of the implicit binary tree which would take 0 (lg n) times again. If a company decided to back out, I would not be able to implement the original remove function of the heap because it only removes the first element of the array. That would only work in removing the highest priority company. Instead, I would modify the remove function to deal with random access calls by adding the company and its payment as a parameter to the remove function. Then, the heap would traverse down a branch in 0(lg n) time to find the correct index to remove. The reason why I have added the company as a parameter is because there could be duplicate keys 	if two companies decide to pay the same amount. Then, the remove function would have to check that the key corresponds to the right company once it has found a matched key with the parameter. Duplicates could pose a problem to the heap, unless two packets could be sent out at the same time. If not, a third priority could be added that corresponds to which company paid me first. This third priority would not have to be sorted, but could instead just be a parameter that comes with the company. If duplicate keys are found, the third priority is compared to see which company paid first, and then that company’s packets are sent out first. This should not take any extra time. Because of its quick running times for dealing with ordered sets with a priority, I believe that this implementation of a heap would be a good solution for this scenario.