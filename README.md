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
Link to my 03_Queue_Lab: https://github.com/mccarts3/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
Link to my 04_Linked_List_Lab: https://github.com/mccarts3/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
TODO: Provide a link to your completed 06_BST_Lab

7 - Create an implementation of a Hash Table
----
Link to my 05_Hashing_Lab: https://github.com/mccarts3/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
Link to my 07_Heap_Lab: https://github.com/mccarts3/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
TODO: Provide a link to your completed 08_Graph_Lab

7 - Implement graph algorithms
----
TODO: Add a graph traversal (DFS or BFS) to 08_Graph_Lab and provide a link

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List
	- Array Lists and Linked Lists both implement the List interface, but their efficiencies for their methods they implement are different.  Linked Lists work by linking different nodes containing objects together by pointers to the previous and next nodes.  This leads to an efficient remove() method because we just link the previous node to the next, and vice versa, and allocate the deleted node in memory.  This is a constant (O(n)) time method, unlike Array Lists, which are only able to remove the first index efficiently.  If you want to delete anything other than that, you must copy all the elements but that into a new array, which is O(n) linear time.  Array Lists have a grow() method that is called if space in the array runs low.  This requires the tedious task of copying all the elements into a new array at O(n) time, but Linked Lists never have a grow() method because you can infinitely add new nodes by simply changing the pointers of the previous and next node at O(1) time, making add() a more efficent method for Linked Lists than Array Lists.  Linked Lists have a find() method that is tedious though, because you have to go from node to node through pointers looking for the proper node if you want to manipulate it.  This find() method runs at O(n) time, but Array Lists are very rarely concerned with find(), and instead manipulate numItems and front variables to find the beginning and end of the array to manipulate. For both Array Lists and Linked Lists, the size() method is a constant O(1) time because we keep track of numItems in their respective add() and remove() methods.

* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

* The call stack (not to be confused with the stack data structure!)
 	- The call stack, or "stack", is a portion of memory that deals with variables, parameters, and other short-lived data in the running of our program.  It is also very important in recursion, as recursion relies on the last method call's basecase to answer all the previous computations.  The stack is Last-in-First-Out, meaning the most recent data is the first to be allocated again for more use.  The stack, since it is filled as a program runs, has the posibility of being filled by a surplus of local variables and parameters, leading to a "stack overflow" and a crash.
* The heap (not to be confused with the heap data structure!)
	- The heap holds dynamically allocated variables.  After it is compiled, and right as it runs, dynamically allocated variables have spaces in memory prepared for them to be filled in the heap.  An int in the heap will have 4 bytes prepared in memory, an array will have n-bytes for it, and etc.
* Address
 	- An address is the actual place in memory in which data is stored or allocated.  It is stored by variables/objects to find data we want to use.
* Pointer
	- A pointer is a variable that holds the address of data or objects.  Pointers are used in our program code to manipulate or use our data, but need the correct address to find the data we mean to use.


* What is a memory leak, and why is it bad?
	- A memory leak is when memory that you have used in your program continues to remain even after your use for it has ended.  If you created an object or something in which you have not properly deleted or allocated it as usable memory, it will remain and not be reused by your program's limited memory, leading to the possibility of memory overflow.  This could crash your program if too much memory is leaked and not able to be reused, or lead to memory being accessible when it is not meant to be.
* What is a dangling pointer (or dangling reference), and why is it dangerous?
	- A dangling pointer is a pointer variable that no longer points to memory that is allocated in memory by the program.  If you delete the object or data the pointer references, but not the pointer variable, you can still use the pointer variable.  If the deallocated memory it points to is replaced by something else by the computer, the pointer variable will have extremely unpredictable results, most likely leading to a crash or misinterpretation of your program.
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
	- In C++, efficiency comes at a cost.  Lots of stuff under the hood in Java that takes extra time because it's just extra memory/security precautions is left out of c++ so the programmer only includes it when needed, making the code sleeker and faster.  Java includes the destructor, even when c++ programmers might not deem it necessary.  In c++, we must include the destructor when it IS necessary.  When we won't use things again, we call the destructor so that memory can be allocated again.  If we don't use the destructor, c++ won't automatically do it like java, and a memory leak (as described in the question above) will occur, as variables we aren't using anymore remain allocated in memory until eventually there is no available memory left. 



5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?
	- In C++, templates are helpful in handling variables whose type isn't known until the running of the code.  The compiler creates a version of the function with the correct variable type in place of the template variable when called.  Template classes allow the code to be more flexible when the variable is unknown, or when the collection class needs to be able to handle several different variable types for a single function.  Having a single template collection class is much more efficient than rewriting the same operations for functions where only the parameter variable is changed.
* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.
	- Unlike normal C++ code, the implementation of a template-based collection class must be in the .h header file instead of a .cpp file.  When a template class is called with a given parameter for T, a new class is created with that given parameter and compiled.  All operations involving the template must be defined in the template collection class so the compiler can have access to them.  This requires both the declaration and implementation of a template collection class to be within the .h header file.  The .cpp file creates an instance of the template collection class with a specific variable type in place of the template, with the .h file having the implementation and operations to do with that variable type.


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
	- For grocery lists, where we add and remove elements as we acquire them throughout the store, the two most suitable data structures would be an Array List or a Linked List. I keep my grocery list on my phone, adding items I need throughout the week with no real concern for order.  As I walk through the store and get an item, I read through, find the item, and delete it from the list, leaving no "null" spots between two items.  The most important methods we would need for this grocery list are add() at the end of the list as I think of new methods, and remove().  I would choose Linked List for this grocery list task because adding a new element at the end runs in O(1) constant time.  All we do is create a new node, and make sure it points to the dummyNode and the previous one, and vice versa, which takes a constant, small number of steps, no matter how big the list gets.  If we used an ArrayList, we would run at constant time until our list gets too big for our array to hold, meaning we would have to call a separate grow() method, increasing our method to O(n) linear time, much less efficient for our task than a Linked List.  Remove() for a Linked List requires going from node to node through the list to find the item you just got, which takes O(n) constant time.  The main benefit of an Array List is a fast remove() method, but that only works if you have your list in order of the store's layout, otherwise you'll be running from one end of the store to the other to remove the first item off your list, making it significantly less efficient than a Linked List.  A Linked List also gives me the ability to have no gaps between items, because remove has the previous node to the item you want to remove point to the following item, therefore creating a nice, structured grocery list that is easily accessible and able to efficiently add items to the list and keep track of which items you already have.
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
--Hash Table? find() is constant, add() is pretty fast--
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
