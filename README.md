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
Here is the link to the Queue I implemented: <br> https://github.com/eaglesonA/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
An example of a List is in our Linked List Lab, in the header file, located here: <br>
https://github.com/eaglesonA/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
The link to the Binary Search Tree Lab: <br>
https://github.com/eaglesonA/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
https://github.com/eaglesonA/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
A heap was implemented in our 07_Heap_Lab: <br>
https://github.com/eaglesonA/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
An adjacency list is implemented in: <br>
 https://github.com/eaglesonA/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
A graph algorithm with a depth first traversal (at the end): <br>
https://github.com/eaglesonA/08_Graph_Lab/blob/master/Graph.cpp

21 - Determine space and time requirements of common data structure methods
-----

* Array-based list vs. Linked List<br>
There are pros and cons to using Array Lists or Linked Lists. LinkedList is wonderful if you have a lot of items you need to add, and need to put those in a particular
order. The add and remove methods in a Linked List are constant time, much better than ArrayList's linear time. ArrayList, however, has the advantage in the get and set
methods, running with constant time, instead of Linked list's linear time. Getting and setting at an iterator is constant time for both data structures. An iterator keeps 
track of where you are in a data structure. So, getting, setting, and adding are constant time (except in ArrayList when adding at an iterator is still linear). 
	
                | Linked List |  Array List |
|--------- | ---------- | -----------
size()  	| O(1) | O(1)|
get/set		| O(n) | O(1)                                                                               
add		| O(n) | O(n)
remove		| O(n) | O(n)
add & remove at front or back		| O(1) | O(1)



* Binary Search Tree vs. Hash Table<br>
 A binary search tree is a great data structure to store ordered lists, or information that needs to be inserted in a certain placed, or has to be retrieved by a given key. 
A hash table is made up of an array and a hash function, which is designed to assign data to spots in the array. A hash table is great
 for large amount of unsorted information. Unlike the binary tree which only creates as much space in the RAM as it requires as elements
 are added, the hash table takes up more memory space than elements added to it since adding to the table is more efficient than growing the table then adding to it. So, if wasted space is important and the list is small it would be better to use a binary search tree. 
Binary search trees are also better if the contents of the tree need to be printed, because there are no empty nodes, and everything is in ascending order. Printing contents from a hash table takes more time, because every "bucket" in the array has to be checked to see if it's empty. That's why an area where a binary search tree is faster than the hash table is finding the minimum and maximum value in a set. Because the hash table is unsorted, without a key, it has to go through every bucket, comparing the value in the bucket to a variable of the lowest/highest value so far. A binary search tree's minimum value is the node at the farthest left point in the tree, and the maximum value is the farthest right. 
That being said, hash tables are much faster than binary search trees in almost everything else. It is constant time (O(1)) in find, add, delete, get, and set, while a balanced tree is on average O(log n). To pick which data structure is best depends on what kind of things the user has to do with it. For example, if there is a lot of searching (like a dictionary) a binary search tree would be better, but if there is a lot of data containing even more data, like a table containing gamer tags, holding high scores, achievements earned, and other player information, then a hash table would be better. 

* Adjacency List vs. Adjacency Matrix<br>
An adjacency matrix is a 2D array with the dimensions of A x A. A graph is most helpful when trying to visualize a adjacency matrix.
 A 1 means there is an edge connecting the node (or vertex) in the column to the node in the row. 
   

| . | 0 | 1 | 2 | 3 |
| --- | --- | --- | --- | --- | 
**0** | 0 | 0 | 1 | 0
**1** | 0 | 1 | 0 | 1
**2** | 1 | 0 | 0 | 1
**3** | 0 | 1 | 1 | 0
In this example there would be edges connecting vertex 2 to vertex 0. To find out if there is an edge (In code, in the table)
 we would use arr[2][0] to see if it returned a 1 or a 0 (in our example it returns a 1). 
An adjacency list is an array of linked lists.
 The number of vertices is the size of the array. The nodes in the linked list hold what vertices the ith vertex points to. Still using 
the example above, if we put it into an adjacency list we would get:

[0]-> 2

[1]-> 1 -> 3

[2]-> 0 -> 3

[3]-> 1 -> 2


An adjacency matrix takes up more space than an adjacency list, but it is much easier to search for a 
particular edge if you know the vertices. The reason to search for an edge would be to get its weight, and it would require an adjacency 
list to run check each node to see if it matched the vertices needed (O(n) running time). In general people tend to use adjacency lists 
because they don't use as much memory, and they tend to be faster. The adjacency list is constant time to add a vertex or an edge. The 
matrix runs 0(1) when its adding or removing an edge. It runs poorly when adding or removing a vertex (it's the number of vertices squared,
 so O(n^2). Removing anything is not very efficient, but not terrible in the adjacency list, with removing a vertex being O of the number 
of vertices and edges (O(n+m)), and removing an edge being O(e).
In conclusion, the adjacency matrix is amazing at searching, and adding 
or removing an edge, but is terrible when dealing with vertices. And the adjacency list is amazing at adding a vertex or an edge, but is
 just alright at searching, and removing a ver bgmtex or an edge.

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

* The call stack is the order in which operations get done. All commands (and local variables, objects, and operations) are stored in 
the computer's RAM. The stack is the reason we can perform recursive methods. It keeps track of everything we need, and puts it off to the
side, until it either runs out of space, or a command is performed. Once the function is completed all data is deleted from the stack.
* The heap is also stored in the computer's RAM. The heap is a giant space used for dynamic memory allocation. You can access any sort of 
information at any time from it, unlike the stack where there is an order of execution. It is the programmer's responsibility to delete
unused variables in the heap, because C++ will not do it for you (like Java does with the garbage collector). 
* An Address is the address of a variable stored in memory. It can be found using '&', and to access the value stored within that address of RAM 
you need to use a pointer. 
* As stated above, a pointer can be used to store the value of an address. Declaring a pointer involves a star; ClassType* foo (foo being the pointer).
Changing the value of the pointer would only require *foo="new value". 


* What is a memory leak, and why is it bad?
A memory leak is caused by programmers/developers not deleting variables they create in a function- so it is still accessible. It is important
to delete any objects not in use, so RAM isn't taken up by useless things. Also, since the data is still accessible it becomes a major
security issues, potentially allowing a breach, or random people getting into your information.

* What is a dangling pointer (or dangling reference), and why is it dangerous?
A dangling pointer is one that continues to point to an address after you delete the data that was there. To fix this, you would either delete
the pointer, or reassign it to point to data in use. 

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
This is called automatically (like how the constructor is called automatically). But instead of creating objects, the destructor
deletes them. This is where everything created and used in the function is erased, so there are no memory leaks (no one can access
items after the function ends). Java has something called a garbage collector, which deletes unused or data without pointers, for you.
C++ does not have this luxury, so it is done by hand. 


5 - Create collection classes using templates in C++
----
What is the main benefit of using templates when creating collection classes?<br>
A template allows a programmer to use any data type in a function or class. This cuts down on code duplication since there would be no need to 
write almost the same thing, but taking in a different type and manipulating it. An advantage to writing templates is the ability
to make one general skeleton of a class instead of creating specializations. When it's time to compile, the compiler will create a separate
version of the function for each type you used. So if you were to create: template <class T> class Foo, then when you substitute
a real value for T (we can use string as an example), then the compiler will make a Foo<String> version. It does this for each function
that is called/performed. 
<br><br>
In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. 
Explain why this isn't the case with template-based collection classes.<br>
The compiler needs to know where variables and functions are stored and implemented in order for the program to run. Each time a template
class calls a function, the compiler makes a new version of your class with whatever datatype was passed in. If the new version doesn't
have access to certain variables (they would need to be in the .h file), or the template is called again in another file, then it won't compile.
That's why it's best to put a template class in the header, so all .cpp files have access and the compiler can instantiate different versions of the code.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
<br> First we need to determine what functions are most important so we can choose a data type that's most efficient in those same areas. 
It needs to have a good running time when adding, removing, and searching. Because the list is unordered I would suggest using a hash table, 
since it has O(1) for all the desired functions. A binary tree would be okay to handle this because it would be balanced so it's time would 
be O(log n) for everything, which isn't nearly as fast as the hash table. Hash functions won't allow any duplicates, and don't require the data 
set to be in order for a better running time. A hash function will always have collisions though. A way to handle similar, but not duplicate strings, is by linear probing. 
This is when a random index is chosen, and if it's occupied we would keep moving down the list ( arr[i+1] ) until an open spot is found. This isn't constant time, but collisions 
shouldn't happen very often, so the extra time is negligible.<br> 
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
My grocery list is the Notes app on my phone. In the app I am able to add, remove, and edit whatever I want. I can place certain things at various points in the list, and the “paper” is endless (the app doesn’t set a max of how many items I can have). Because of all these reasons, I would use a Linked List, since it will allow me to add items at any point in the list (I’m forgetful, and being in the bread section might remind me to get donuts). Also, if I start in a different part of the store (say I want to go clockwise), I can arrange my list easily to reflect my decision. If I find an item isn’t on sale, or is too expensive, I can delete it and there won’t be any blank spaces in my list. 
<br> 
The most important function of a grocery list is the ability to add items.You don't have to necessarily remove items; 
you could cross them off, or mark them as useless and put a new item in the old one's spot. Because the grocery list has a max, a hash table would be a bit extreme, even though it
 is constant for add/deleting. We have to determine if running time is a top priority, or efficient use of space, or what the easiest is to implement. Since grocery lists are usually 
under 50 items (always for college students, maybe not for everyone else) time is negligible. A binary search tree wouldn't be a good structure either, since you can't find a specific 
key without going through the whole list. Unless you memorized the store's layout, it would also be hard to add items in the correct place (unless you created a grocerySort to do it for you). This leaves either an ArrayList or LinkedList (an adjacency list/matrix would be 
too extreme, like the hash table). Both of these data structures are simple to create, however, it would be much easier to add to a linked list instead of an array list. If anything, 
the most common thing that happens to a grocery list is that extra items are added. If you wanted to follow the list in order, after each item you checked off, a node would be deleted 
(you could do a queue type of list, deleting from the front, or a stack, deleting from the back). It really depends on how the list is organized. The best way to organize would probably
 to be by food category, since that's most like a grocery store. If you're in the dairy section then you can look at your list, and cross off the things you come across first, so it doesn't 
need to be in any order besides being in the correct food group. This type of list could be used on a smartphone, or a piece of paper, or anything really. I would personally use a smartphone, 
since I tend to add things while I'm there (and it's easier to carry than paper and pencil). To make the paper neat while inserting would be to leave space at the end of each food group, so you wouldn't have things written on the margins, 
or lots of eraser marks. <br>
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
<br>

Banner id numbers are 9 character "numbers" assigned to each student. There are 8 actual numbers, but a + sign in front making it 9 characters. The best data structure 
for this is the hash table. There are a large amount of student ids that have to be put in a table, and there will be no duplicates. If there are collisions (since there always are), linear 
probing can be used to find the next open space. The constant running times for each main function (find, add, delete, get/set) should outweigh any slow times from collisions/linear probing. 
Because each student has a key (their banner id number), all their data is easily accessible. You wouldn't have to wait for an algorithm to sift through thousands of students to get to yours. 
 Even grow wouldn't be bad since it's only called once every year (if Miami continues to expand). 

In this scenario the priority is very important in considering which structure to implement. 
<br>
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
<br>The heap data structure comes to mind since it specifically deals with priorities, and organizing its tree based on highest priority. 
So, the highest priority item would be the root of the tree, and when that is removed the second highest replaces it. Since company X 
is paying a larger amount, their packets would always get the higher priority compared to company Y. Giving the packets a higher priority 
will always send them to the top of the tree, allowing company X to always have their packets sent before company Y's packets. If there was
 a company paying even more than company X, then they would get highest priority. So their packets would always be sent before X and Y 
(and so on for every company you're in business with). 
To do this X and Y would be assigned a priority value. So all incoming packets would
 be labeled with either X or Y's value depending on who they belong to. Since X has a higher value, its packets would be towards the top of
 the tree, allowing for an easy remove. The next highest priority would BubbleUp() in order to get to the top of the tree. If new packets arrived, 
their priority would be checked with nodes around them to see if it needed to bubbleUp.