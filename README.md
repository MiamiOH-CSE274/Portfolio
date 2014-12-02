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
Here is an implementation of a queue: 
https://github.com/dazeycm/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
Here is an example of the implementation of a list:
https://github.com/dazeycm/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
Here is an example of a Binary Search Tree:
https://github.com/dazeycm/06_BST_Lab

7 - Create an implementation of a Hash Table
----
The code for the implementation of a hash table can be found at:
https://github.com/dazeycm/05_Hashing_Lab/blob/master/HashTable.ipp

7 - Create an implementation of a Heap
----
An implementation of a heap:
https://github.com/dazeycm/07_Heap_Lab

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
An implementation of an adjacency list:
https://github.com/dazeycm/08_Graph_Lab

7 - Implement graph algorithms
----
TODO: Add a graph traversal (DFS or BFS) to 08_Graph_Lab and provide a link

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* **Array-based list vs. Linked List** - Looking at the four methods of add, remove, set, and get, there are distinct differences in array-based lists and linked lists. A queue's add method takes O(n) time. This is because the values of the array need to be shifted to accomodate for the new value. A linked list is caple of adding a value in O(1) time. This is because you can easily change the references at each node. The queue's remove function is similar to the add function in that it takes O(n) time. This is because once you remove the value, you have have an empty space and need to move the other values in the array over to accomodate for this hole. A linked list's remove function is done in O(1) time because like the add function, it is trivial to change the references of the node. Get and set for the queue take O(1) time because it is a simple index lookup for each method. A linked list takes O(n) time to complete the get and set method. This is because in a linked list you start at the first node and advance through them until you arrive at the destination node. **TODO: ADD TABLE, SHORTEN ESSAY.. LL SEQUENTIAL.. ITERATORS - WHAT ARE THEY, WHAT DO THEY DO? IN TABLE, ALONG WITH METHOD NAMES HAVE ITERATOR STUFF LIKE add() at an iterator (IS O(1) for linked list and O(n) for arraylist) and get an iterator for given index - IS O(1) for arraylist and O(n) for linkedlist.. set at an iterator is O(1) for both... get at an iterator is O(1) for both... remove is O(n) for arraylist, O(1) for linkedlist.. get iterator at front and back is O(1) for both.. add/remove at front or back is O(1) time for both**
* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----


* **The call stack** - The stack is an area where, when we run our program, all of the local variables and functions are stored and ran. This is done in a LIFO order.
* **The heap** - The heap is the area where we can dynamically allocate memory. This data in C++ is initialized using the `new` keyword and then must be deleted using some variation of the `delete` keyword. There is no set order of data storage in the heap.
* **Address** - The address of a variable is where that variable is stored in memory. The address of a variable can be obtain by using the `&` reference operator. 
* **Pointer** - A pointer is an object that points directly to another value's memory address stored somewhere in a computer's memory.



* **What is a memory leak, and why is it bad?** - A memory leak occurs space is allioted in memory but then never freed. This could potentially cause you to run out of space for memory.
* **What is a dangling pointer (or dangling reference), and why is it dangerous?** - A dangling pointer is a pointer that references  a space in memory that is no longer being used by our program. This is dangerous because the data could be overwritten and if the pointer is used, it will point to data that we did not intend it to.
* **What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?** - A destructor is a method that is called when an object is deleted. In this way, it is possible to deallocate space in memory, preventing memory leaks. They're necessary in C++, because the language has no means of automatically deallocating space. This isn't the case with Java, which has garbage collection, because data that is no longer being used it automatically freed **TODO: OBJECT CLEANS UP AFTER ITSELF**. 

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?
* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* **If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.** - I believe that a linked list would be the best data type available. Assuming that you group the objects next to each other on your shopping list in accordance with where they are in the store (as any sane person should), there is some order to the objects on your list. There is also the need to be able to add and remove items from the list as you aquire them and remember things you've forgotten. Since add and remove take O(1) time, it is quick and efficient to add and remove items. The time to get or set an item to the list would be O(n) time, but once you've added everything to the list, there won't be a need to look up the items in the list, as you'll always be getting the first item from the list which is constant time in a linked list **THOUGHT PROCESS: WHAT DO I THINK A GROCERY LIST IS? HOW SHOULD I DECIDE WHICH DATA STRUCTURE - EFFICIENCY, FIT TO PROBLEM (what ops do they support?), EASIEST ACCEPTABLE SOLUTION, RUNNING TIME WILL NOT MATTER BECAUSE.... THREE APROACHES 1. Efficieny doesn't matter 2. paper list 3. really old hardware <--first paragraph**. 
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
