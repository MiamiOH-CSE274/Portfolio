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
https://github.com/MiamiOH-CSE274/03_Queue_Lab

7 - Create an implementation of a List
----
https://github.com/ethan2014/04_Linked_List_Lab

7 - Create an implementation of a Binary Search Tree
----
TODO: Provide a link to your completed 06_BST_Lab OR ClosestStarbucks project (only if you used a search tree)

7 - Create an implementation of a Hash Table
----
TODO: Provide a link to your completed 05_Hashing_Lab

7 - Create an implementation of a Heap
----
TODO: Provide a link to your completed 07_Heap_Lab OR Vise project (only if you implemented a heap for it)

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
TODO: Provide a link to your completed 08_Graph_Lab OR Vise project (only if you implemented a graph for it)

7 - Implement graph algorithms
----
TODO: Provide a link to your completed Vise project (only if you used graph traversal), or add a graph traversal to 08_Graph_Lab and provide a link

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List
* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

The Stack: A special part of RAM where local variables and objects are stored.  It stores informtion about the current function and where to return after the function is done.  Any variable declared in a function (ie. `int a[5]`) will be put on the Stack and will be deleted automatically when the function returns.

The Heap: The part of memory where dynamically allocated memory is stored.  Accessing this memory requires asking the OS for memory with the `new` operator (or `malloc()` in C) for example `int *a = new int[5]` will created an array of 5 `int`s on the Heap which will always exist until the program exits or it is explicitly deleted by the program with the `delete[]` operator (or `delete` for singal variables such as `Object *a = new Object()`).  forgetting about Heap memory is the most common way to cause memory leaks in a program, because any data an object created with `new` will still exist even after you are done with the object.

Address: the physical location of an object in RAM commonly represented as a hex number.  the address of an object can be found with the `&` operator, for example: `int *p = &a`, `p` will store the address of variable `a`.

Pointer: a special variable type in C and C++ for storing the address of another variable declared with the use of the `*` operator and dereferenced with the same operator `*`.  `int *p` will create a variable `p` that will be used to store the address of an `int` and using `*p` will allow you to manipulate the value of the data it is pointing to.

* The call stack (not to be confused with the stack data structure!)
* The heap (not to be confused with the heap data structure!)
* Address
* Pointer

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?
* What is a dangling pointer (or dangling reference), and why is it dangerous?
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
