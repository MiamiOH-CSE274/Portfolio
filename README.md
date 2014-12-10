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
This is where I created an implementation of a Queue: https://github.com/wilso199/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
This is where I created an implementation of a List: https://github.com/wilso199/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
TODO: Provide a link to your completed 06_BST_Lab OR ClosestStarbucks project (only if you used a search tree)

7 - Create an implementation of a Hash Table
----
This is where I created an implementation of a Hash Table: https://github.com/wilso199/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
This is where I created an implementation of a Heap: https://github.com/wilso199/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
This is where I created an implementation of a Adjacency List: https://github.com/wilso199/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
This is where I implemented a DFS graph algorithm: https://github.com/wilso199/08_Graph_Lab/blob/master/Graph.cpp

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List

When comparing an Array-based list to a Linked List it is important to look at the add(), remove(), get(), and set() functions. Array-based lists both add() and remove() at O(n) time because if you add() you may need to call the grow function which directly depends on the number of elements in the array and if you call the remove() function you will need to reassign the front value making it not run in constant time. Get() and set() are both at constant time because with get you are simply returning a value that you have kept track of the entire time with numItems and with set() you are simply placing a value at the given index which is also being stored in a variable. With the Linked List data structure get() and set() are at O(n) time because the find() function must be called in order to find the node to be modified. On the other hand, add() and remove() are done in constant time because there is no need to shift all elements in the array once a node is removed or deleted rather you just perform “list surgery” to change the Linked List.

				|   Array Based   |    Linked   
			——————————————————————————————————————————
			add	|	O(n)	  |	O(1)
			———————————————————————————————————————————	
			remove	|	O(n)	  |	O(1)
			——————————————————————————————————————————
			get	|	O(1)	  |	O(n)
			—————————————————————————————————————————-
			set	|	O(1)	  |	O(n)
			——————————————————————————————————————————
			size	|	O(1)	  |	O(1)

* Binary Search Tree vs. Hash Table

* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!) - the block of RAM that is used to store parameters and local variables. Also the stack keeps track of a function’s call to another function if it is needed to return a value.
* The heap (not to be confused with the heap data structure!)- a block of RAM that is used to store dynamic variables created by the keyword ‘new’. 
* Address - An objects location in memory. 
* Pointer - a variable that can hold an address. 

Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad? 
When memory is allocated but not released. This will cause the application to consume memory and reduce the available memory for other applications which could eventually use all of the RAM. This would make the computer start to use the hard drive for storing data.
  
* What is a dangling pointer (or dangling reference), and why is it dangerous?
A dangling pointer is a pointer that no longer points to a valid destination. Dangling Pointers normally occur when the destructor is called and the pointer is not assigned a new value. They are potentially dangerous because these can eventually crash your program or may be a security risk as hackers can access this pointer and assign it to a piece of malicious code. 

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java? 
You need a class destructor because C++ does not know when you are done with a class or an instance of that class. In Java the instance of the class would be automatically deleted once your program was done using it, in C++ the instance is kept until a destructor method is called.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?

Using a template when creating a collection class allows you to write one class that can handle any type of data the user may enter into your collection class. This way a class can be reused to handle string inputs and int inputs without having to be rewritten. By doing this you eliminate the difficulty of trying to accommodate for every type of data the user may enter. 

* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

You are unable to do this because when you use a template it allows for any data type to be entered. When using a template the compiler will have to create a new version of your class which means new function declarations and definitions for each function. If you implemented the function in a separate .cpp file, the compiler wouldn’t know where to find the implementation for the new functions it created because the .cpp file has already been compiled and won’t be able to add new information to the file. To avoid this you include the implementation in the .hpp file so whenever you #include that .hpp file all of the implementation will be included and compiled in the .cpp file.  

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)


* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. 

When I think of a grocery list I have the same vision that you do. I like to make sure everything from the same section are grouped together so I am not running around like a chicken with my head cut off. I also like to keep open spaces in case I remember something once I get to the store. With that being said, I would use a Linked List for making a grocery list. I think this is most fitting for the situation because if you wanted to add or remove an item from the list once you got to the store the action would be performed in constant time. Also if you wanted to leave empty space in your list you could do that in one of two ways: 1) by simply just doing “list surgery” once you find out that you forgot something or 2) leaving dummyNodes in the places where you feel you might have forgot something then add a value to the dummyNode once you remember what you forgot. Also you will not have to worry about the original size of your list because there will not be a grow function or limitation on the number of items in the List.  

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

