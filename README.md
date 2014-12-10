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
Queue Lab code can be accessed at https://github.com/clarkdb/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
Linked List code can be accessed at https://github.com/clarkdb/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
Binary Tree code can be found at https://github.com/clarkdb/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
Hash table code can be found at https://github.com/clarkdb/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
Heap code can be found at https://github.com/clarkdb/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
TODO: Provide a link to your completed 08_Graph_Lab OR Vise project (only if you implemented a graph for it)

7 - Implement graph algorithms
----
TODO: Provide a link to your completed Vise project (only if you used graph traversal), or add a graph traversal to 08_Graph_Lab and provide a link

21 - Determine space and time requirements of common data structure methods
-----

* Array-based list vs. Linked List

Array based lists and Linked lists can be similar in theory, but very different to implement in code. An array based list has its advantages in that the order of the elements does not matter and so it is faster to run finding methods and getting/setting methods, since they do not have to loop through the entire array. In a linked list, these methods can take more time with larger lists since the linked list has locations of elements within it relative to other elements rather than using the index to find elements. However, the way to add/remove elements is much faster in  a linked list because the nearby elements in the list do not have to be shifted, there are always only two elements whose pointers need to be changed in order to accommodate a new element or to remove an existing element. In an array based list, with a new element being added, all the other elements after it in the list have to be shifted and can waste a lot of time with a large list and the same is true when removing, that all the other elements need to shift in order to take the place of the changed space in the list. Depending on the task that the list will serve, either type can be justified and both have positives and negatives associated with their implementation.
When adding and removing items, a Linked List will be faster, offering constant time to add and remove elements whereas an array based list will take linear time to complete a similar task. For getting the size of the list, both data structures will result in linear operating times. With any operation, the linked list will be faster or the same speed as the array based list since any array based list will need to loop through the array to use and element other than finding a single item, so in almost every situation a linked list will be better fit for the task.

* Binary Search Tree vs. Hash Table

A binary search tree is a very reliable data structure for a task that requires the use of all types of operations whereas a hash table is well suited for a task that requires adding a large number of items and storing them in a small amount of memory with fast running times on adding, removing, finding, and getting elements, but slow running times on finding a next or previous and minimum or maximum. A hash table is the best data structure for large groups of elements that need to be stored because it can keep constant running times for adding and removing elements similar to a random access table but can store large numbers of elements in a much smaller area if memory than a random access table. A binary search tree can execute all operations in logarithmic time if the tree stays balanced but can easily approach linear time if not properly maintained.

* Adjacency List vs. Adjacency Matrix

An adjacency list and an adjacency matrix are very similar in theory but are very different in construction. They both contain a list of edges between vertices of a graph, but an adjacency matrix is much faster to return results than an adjacency list at the cost of much more memory required to store the list. An adjacency matrix boasts constant time for adding and removing edges as well as for finding and getting edges to update, but takes up the square of the input data in memory to represent the data. An adjacency list requires roughly the same amount of memory as the input data to store, but will require running times proportional to the density of the graph.
With highly dense graphs in which the number of edges approaches the square of the number of vertices, an adjacency matrix will yield the best results; however, when a graph is less dense, it makes more sense to use an adjacency list to preserve space in memory.


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

* The call stack (not to be confused with the stack data structure!)

The call stack is the list of operations that the debugger console shows to allow you to see where in the code an error occurs. The call stack is important because it will tell you which operations are working and where the problem with your code occurs by showing each operation and what other places in the libraries or elsewhere in the code is being accessed, or "called".

* The heap (not to be confused with the heap data structure!)

The heap and the stack are the two separate areas of a computer's RAM that are used when allocating space for variables within a program. The stack is where statically allocated memory gets mapped to(when not using "new"), and the heap is where dynamically allocated memory gets mapped to. The stack and heap are kept separate for the ease of access to variables that are created differently and any memory allocated on the heap needs to use the delete function in order to avoid poor memory management. 

* Address

An address is the physical interpretation of where some data is being stored in the computer's RAM. An address is a hexadecimal representing the location but not contents of a spot in the computer's memory that can be accessed through the use of variables and pointers.

* Pointer

A pointer is a variable that contains an address of a certain type of variable data. A pointer must be the same type as the data stored at its address with an asterisk next to the type name to indicate that it is a pointer rather than a variable. A pointer only holds the address if a variable and does not store the data, but can be dereferenced in order to retrieve the data; moreover, when a pointer is deleted, the data remains in memory but the variable that stored the access of the data is lost, creating memory leak.



* What is a memory leak, and why is it bad?

Memory leak is caused by having a space in memory allocated with data but not having a pointer assigned to the space in memory so the data is essentially lost. Memory leak will cause the space to stay allocated and force the computer to use that portion of RAM for data with no pointer and therefore can be very difficult to access by the user, causing a loss of usable RAM and eventually will crash the program.

* What is a dangling pointer (or dangling reference), and why is it dangerous?

A dangling pointer is a pointer whose address stored does not contain the data that is used by the program or contains no data at all. This can cause either an issue when using the pointer because it will use whatever data was left in that address when dereferenced or can leave the computer vulnerable to hacking because the pointer will show the space in memory where data was being stored and can allow someone to get the location of any other areas of memory that should not normally be accessible if the pointer's data crashes the program.

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?

A destructor in C++ is a class that is opposite the constructor in the fact that it deallocates the memory that was initialized by the variables in the class' constructor. The destructor is important because it helps to avoid memory leak and dangling pointers and is an important programming practice to help maintain good memory management. In C++, when a variables goes out of scope and is no longer used, its value remains and any pointers remain and so without the destructor will leave many problems with dangling pointers and memory leaks; however, in Java, the memory used in a program is automatically reset to default values after the program runs and when the variables go out of scope so that programmers do not have to worry as much about their memory management while creating classes.

5 - Create collection classes using templates in C++
----

* What is the main benefit of using templates when creating collection classes?

Templates allow collection classes to be reused and made to work in many situations with different requirements. Templates allow several classes to be used in a similar fashion with the same functions through the use of templates that allow a function to accept a template data type in construction and in use will be initialized with a data type and will execute the functions in the same way.

* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

With collection classes, the implementations are contained in a .h file because the functions can be run with many data types and the implementation of the functions must be initialized with a data type. The collection class with a template gives its implementation in the .h file but cannot be run from that state and must be initialized in order to fill the template and allow the program to run.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)

With a set of strings that do not need to keep any order, it would be simple to find a data structure well suited for the purpose. With almost any unordered set, it would be best to implement a hash table to get the fastest possible running times and memory management. With few possible strings or shorter strings, it may be better suited to use a random access table, but with more possible strings, a hash table will offer similarly fast running times while using up much less memory storing items. To add, remove, and get items from the set, a hash table will offer constant time to run regardless of the number of strings. However, depending on the use cases of this set, a hash table may need to be combined with another data structure in order to get the best results as in the zeitgeist project in which my partner and I believed that the best data structure combination would be a hash table with a heap since we needed to get information about the items in an ordered set and hash tables are slow for finding next and previous elements.

* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

With a grocery list, I would implement the task with the way that I am used to using a grocery list, as a paper with all of the items that are needed. However, it would be nice to order the items in the list so that I can go from one side of the store to the other without wasting a lot of time going back and forth across the store looking for items. For this reason, I would use a Linked List so that the elements can have a next and a previous item relating their location in the store so that I do not waste a lot of time between items in the store. THe linked list would also allow for a fast way to add or remove items depending on how often I change my mind on groceries within the store. With a linked list, it would not be a downside to have a slower time to find elements, since I am most likely going to use them in order and even if not, I can use the previous item to find what I am looking for within my shopping list.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

For student records, the fastest solution would be to use a random access table, but a random access table uses a lot of memory and takes up a lot of unnecessary space. In any implementation of this problem, it will be beneficial to use a dictionary abstract data type to use keys and data to store the records and be able to look the records up by a student identification number. A hash table will also yield fast running times in this case when there are a large number of possible keys and a random access table no longer is worth the amount of memory that it needs to store the elements. The random access table will have constant running times for every operation that it supports, but will take a lot of space if the keys are spread out. A hash table will give constant running times for most functions but will have trouble when finding the next or previous and minimum or maximum elements compared to the time that the same function takes in a random access table. 

* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

In order to make this use case work correctly, I believe that the implementation will need to include a priority queue of some type, possibly within a heap. With a heap, the priority can be determined by having a value set equal to the highest amount of money paid by a company subtracted by the company's money paid. This way, the top node of the heap will be taken and then the rest of the tree will need to be balanced so that the next highest priority item will be taken next. The heap will remain balanced and will allow the packets sent by a lower priority company to be held in the tree until all of the packets of higher priority companies are sent. This will offer constant time to run because the tree is only using the top element, but will take logarithmic time to adjust the balance between companies since the function to adjust the tree will need to look at all the items in a subtree.
