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

7 - Create an implementation of a Queue using a circular array-based list
----
I showed how to implement a Queue in my Queue lab from lines 78-144. Here is the link. 
https://github.com/meslerke/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
I proved that I can implement a list in lines 81-171 of the Linked List Lab. This is the link.
https://github.com/meslerke/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
This 06_BST_Lab shows that I can implement a Binary Search Tree from lines 83-324. Here is the link.
https://github.com/meslerke/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
I proved that I could implement a Hash Table in lines 90-212 of the 05_Hashing_Lab. Here is the link.
https://github.com/meslerke/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
This 07_Heap_Lab shows that I can implement a Heap from lines 58-152. Here is the link.
https://github.com/meslerke/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
Here is the link to my completed 08_Graph_Lab.
https://github.com/meslerke/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
Here is the link to my completed 08_Graph_Lab.
https://github.com/meslerke/08_Graph_Lab/blob/master/Graph.cpp

21 - Determine space and time requirements of common data structure methods
-----
* Array-based list vs. Linked List

                		| Array | Linked List
:------------------------------ | :---: | :---------:
add/remove  			| O(n)  | O(n)
add/remove with an iterator	| O(n)  | O(1)
get/set			      	| O(1)  | O(n)     
get/set with an iterator      	| O(1)  | O(1)     
find an index		      	| O(1)  | O(n)     
find a value 	              	| O(n)  | O(n)     

-add/remove - In an array, you would need to shift all of the other items in the array everytime you wanted to do one of these functions. In a linked list, you would have to search through every value in the list by going through the pointers forwards and backwards to get where you want to add or remove an item.

-add/remove with an iterator - In an array, you would still have to shift all of the other items to perform one of these methods. In a linked list, you would be able to go right where you wanted to be, which would make for a faster running time.

-get/set - In an array, you can just look up where an item is and go straight to it, but in a linked list, you have to loop through the list to find the item.

-get/set with an iterator - Both an array and a linked list can have a constant running time because they will both be able to direct you to the item you want.

-find an index - An array holds its own index which makes it easy to find objects, but a linked list does not.

-find a value - For both of these data structures, you would need to iterate through it to find the item you were looking for.

* Binary Search Tree vs. Hash Table

	       | BST    | Hash Table 
:------------- | :----: | :---------:
add/remove     | O(lgn) |  O(1)    
find	       | O(lgn) |  O(1)    
get/set	       | O(lgn) |  O(1)    
min/max	       | O(lgn) |  O(n)    
next/previous  | O(lgn) |  O(n)    

-add/remove - To add or remove a node from a BST, you would need to find it. The running time for this depends on the height of the tree because you would start at the top of the tree and work your way down, getting closer to the item you are searching for. In a hash table, the location of the item is stored with the item, so it is easy to locate that particular item.

-find - In a BST the running time for this method is based off of the height of the tree, and in a hash table, it is easy to just look up the items position

-get/set - In a BST, the height tells you how long it could take for you to find the item to get and set it. In a hast table, you can look it up immediately.

-min/max - In a BST, again you have to search through the height of the tree to find the min or the max value. In a hash table, you have to go through every item, which costs a lot of time.

-next/previous - In a BST, you again have to find the item first, which depends on the height of the tree. In a hash table, you have to search the entire table to find the item you are looking for before finding its next or previous.

* Adjacency List vs. Adjacency Matrix

	            | Adj List | Adj Matrix 
:------------------ | :------: | :--------:
add/remove edge	    | O(d)     |  O(1)     
add vertex	    | O(d)     |  O(1)     
get/set weight	    | O(d)     |  O(1)     
space	            | O(n+m)   |  O(n^2)   
getNeighbors	    | O(1)     |  O(n)     

-add/remove edge - In an adj list, the run time depends on the distance it is from the starting point. In an adj matrix, you just have to look up the item in the table and change it accordingly, which takes much less time.

-add vertex - This also depends on the distance it is away from the starting point in an adj list, and can be easily looked up in an adj matrix.

-get/set weight - This works the same way as the add vertex method for both data structures

-space - an adj matrix takes up a substantial amount of space more than an adj list, which could be a very negative aspect.

-getNeighbors - This takes much more time to perform in a matrix because you would have to search through every entry to determine the neighbors.

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
* The call stack stores the statically allocated variables and their functions.
* The heap is where the memory comes from that is used when allocating memory using 'new'. (dynamically allocated) It is like a large pool of memory.
* An address is something that everything that is stored in memory has. The address tells you exactly where that piece of memory is stored.
* A pointer is an object that refers to (or points) a specific piece of memory using its address.
* A memory leak is when something in the memory isn't pointed to by a pointer anymore. This means that this object is taking up space in the memory that could be used for something else. This is dangerous because if you don't tell the computer that you are done with a piece of memory, that memory won't be available to be used later and eventually you will run out of memory!
* A dangling pointer is created when you create a pointer for something and then delete what it was pointing to. This is dangerous because you don't know how your computer will act to this in the long run. The pointer could end up pointing to a different variable in your program, which would mess it up and would also be a lot harder to find to fix.
* A destructor essentially cleans up after you when you are done with a program. It deallocates the memory that you have allocated so that you can use it again at another time. This is necessary in C++ to prevent memory leaks because if you don't deallocate the memory that you have used, then that will create a leak in your memory and you can eventually run out of memory. These aren't necessary in Java because Java is designed to automatically do this for you when you are done with a program.

5 - Create collection classes using templates in C++
----
* What is the main benefit of using templates when creating collection classes?

The main benefit of using templates is that you only need to create one version of your code, and it will work for all data types.

* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

This is because .cpp files don't have enough information to compile with a template because it doesn't know the data type that you are going to use. This will compile in a header because it does not require the knowledge of the data type to compile.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)

For this problem, I would use a hash table to store the strings. This would be good for easily finding strings that have been stored in the data structure, and would also be good for recording that there is a duplicate of a string without actually storing the string more than once. In the hash table, I would make the string the key, and the number of times that the string appears the data corresponding to it. This way we can easily look up the string when we come across it to see if it is already stored somewhere, and it would be just as easy to update the data of that string as necessary. (This is also assuming that the strings would not need to be stored in any particular order.)

* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

I imagine a grocery list as a list that is kept on paper. The first items that you think of will be the first on the list and you can add and remove items from the list in any order. Looking at a grocery list this way, I think that a Linked List would be the best data structure to use. This is because it does not require a certain order for adding and removing items. If you are at the grocery store, you would look at all of the items on your list and determine which items are the closest to you to pick up. With a linked list, you would then be able to add and remove items from the list in any order and it would run in constant time. Also, as you think of items that you need to get, you can add them anywhere on the list, while still being efficient.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

For this problem, I would use a hash table because it is very easy to look up something by the key and modify the data while still running in constant time. I would store the banner number of the student as the key, and the records for that student in the data corresponding to that key. This allows for a very efficient program.

* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: 
Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

A heap used as a priority queue sounds like the best way to work out this situation. In a heap, the items are prioritized with the highest priority on the top of the heap, and then extending from that are the next highest, and so on. The highest priority item is always the first item to be removed from the heap, and is then replaced by the next highest priority. The process of removing the highest priority item runs in constant time, which is ideal for this situation. Using this data structure, we would prioritize the packets by the price that the company has payed for them. This will ensure that the companies paying the most to send out their packets will have them sent out before the packets belonging to the rest of the companies.
