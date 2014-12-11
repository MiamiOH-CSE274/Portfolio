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
https://github.com/aryelle-player/03_Queue_Lab

7 - Create an implementation of a List
----
https://github.com/aryelle-player/04_Linked_List_Lab

7 - Create an implementation of a Binary Search Tree
----
https://github.com/aryelle-player/06_BST_Lab

7 - Create an implementation of a Hash Table
----
https://github.com/aryelle-player/05_Hashing_Lab

7 - Create an implementation of a Heap
----
https://github.com/aryelle-player/07_Heap_Lab

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/aryelle-player/08_Graph_Lab

7 - Implement graph algorithms
----
https://github.com/aryelle-player/08_Graph_Lab


21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List
	Array-based lists tend to run in constant time for all operations 
except add() and remove(). Add() and remove() for an array-based list run
in linear time. tHe reason for this is because array-based lists offer
constant time access to any value in an array but array-based lists aren't
terribly dynamic therefore adding and removing elements require the array 
to be shifted. Linked lists that are singly-linked are the complete 
opposite of array-based lists in terms of running time for operations. For
doubly-linked lists, instead of linear time, these lists take 
O(1+min{i,n-1}) time for add(), remove(), get(), and set().
			arraylist	linkedlist
add				o(n)	o(1)
get(given index)		o(1)	o(n)
set				o(1)	o(1)
get				o(1)	o(1)
remove				o(n)	o(1)
get(front or back)		o(1)	o(1)
add/remove(front or back)	o(1)	o(1)

* Binary Search Tree vs. Hash Table
	Hash tables are typically faster for add(), remove(), and get()/set()
opertations. Hashtables are constant time for these operations while binary 
search trees are log(n) time for these operations. Binary search trees are 
log(n) for all operations so they are faster for min()/max() and next()/prev()
operations.
			Hash Table	Binary Search Tree
add(key, val)			O(1)	O(lgn)
remove(key)			O(1)	O(lgn)
get/set(key)			O(1)	O(lgn)
min/max				O(n)	O(lgn)
next(key)/prev(key)		O(n)	O(lgn)


* Adjacency List vs. Adjacency Matrix
	Adjancency matrices are constant time for addEdge(), getWeight(),
and removeEdge() operations while adjancency lists are d time which is
the length of the graph. Depending on how the graph is implemented, the
getWeight() operation can take linear time in an adjacency list. The
getNeighbors() operation takes linear time with an adjancency matrix and
constant with an adjancency list. Adjancency matrices are typically faster.
		Adjancency Matrix	Adjacency Lists
addEdge()		Theta(1)	Theta(d)
getWeight()		Theta(1)	Theta(n) or Theta(d)
removeEdge()		Theta(1)	Theta(d)
space()			Theta(n2)	Theta(n+m)
getNeighbors()		Theta(n)	Theta(1)



5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

 * The call stack (not to be confused with the stack data structure!)
	The call stack is the space in memory where parameters and static variables are stored.
* The heap (not to be confused with the heap data structure!)
The heap is the space in memory where dynamically allocated variables are stored.
* Address
	An address is basically a memory location. The address of an object is the place where it is in memory, basically just where an object lives in memory, usually given by some random mix of letters, numbers, and other characters. The address can be accessed by use of a pointer.

* Pointer
	A pointer is an object that points to a space in memory. It holds the address of this space. When a pointer is de-referenced, the object that is in this space is accessed. If there is no object, this is then a dangling pointer.


TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?
	Memory leak is allowing memory to still be used once a programs runtime is through. This is bad because it can allow someone to access something in memory even after the program has stopped running. (the reasons hackers can obtain things they shouldn't have)

* What is a dangling pointer (or dangling reference), and why is it dangerous?
	A dangling pointer is a pointer that points to a space in memory which no longer has an object in it. This is bad because this can cause variables to be changed unintentionally or memory to run out faster.

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
	A destructor is a method, opposite of a constructor, that destroys  every object that is created during runtime. This prevents memory leak  because there is now no way to access something in memory after runtime  because the memory is no longer accessible. This is unnecessary in Java  because Java's garbage collector does all of this work by constantly checking  for live variables and getting rid of dead ones.
	

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?
	When creating collection classes, templates are very beneficial when you want your class to be able to use any data type, they are easier to write, and are safer because they check for errors regarding any kind of object.

* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.
	With template-based collection classes, this isn't the case because the declarations and implementations don't need to be seperate files.


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
	A set of strings is just simply a randomly-ordered list of strings. A set of strings is made by randomly adding a string to the end of a list. The list grows as you add strings and shrinks as you remove them. To remove a string, you must first find it in the list, and then erase it from the list. When you are looking for the string, you would check each string until you come across the string that you are looking for. An important thing about this list is that there are no duplicates; therefore, if you want to add a string that is already in the list, you would not add it.  Deciding what data structure to use would depend on what operations need to be quickest and in this case, that would make a USet the most appropriate data structure. A USet is exactly an unordered set of templates, in this case the templates would be strings. An array-list would be best efficient at implementing a set of strings. The most used operations are adding, removing, and finding. Adding and finding are both constant time while removing is linear time.

* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	A grocery list is, usually, a list of randomly ordered items. Most people, however, decide to order their grocery lists by department or how the grocery store is set up. In this case, the grocery list becomes a bit more complicated. When adding an item to the list, you would want to add it in the appropriate section of the list(with items that are in the same department). When removing items from the list, you would need to find the section that contains the item you just found. Therefore, finding items in the list is fairly quick. You would need to find the appropriate section (department) of your list and then find the correct item within it. An important thing about this list is that, like a set of strings, there are also no duplicates. Deciding what data structure to use would, again, depend on the operations that need to be the quickest, that would make a dictionary most appropriate for a grocery list. A dictionary has a key and value pair. The key would be the section or department and the value would be a string representing the item in the section/department. In particular, a hash-table would be extremely efficient for implementing a grocery list. Adding items, removing items, and finding items are the really the only operations needed and are all constant time.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	A student record is a list of student information. Student records are usually ordered alphabetically. In this case, each student has a unique characteristic: their Banner number. Students are added based on the value of their Banner number. Students are removed the same way; however, removal from student records is a very uncommon operation. Since we want to look students up by Banner number, this is how a specific student is found. The most appropriate data structure for student records would be a dictionary. For the same key and value pair reason as above, the best way to implement this would be a hash-table. With the only operations needed being add and get, a hash-table being constant time for these operations would be best.

* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	With this network router, it seems that the queue of packets is like a central node and the various companies are connecting nodes. The connection, an edge, that has the highest number, determines the order by which to visit each company node, unless there are no packets waiting. The most appropriate data structure seems to be a graph. Graphs have nodes and edges. Each node has a weight which in this case would represent the packets waiting. 
