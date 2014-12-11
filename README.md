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
https://github.com/richarkc/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
https://github.com/richarkc/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
https://github.com/richarkc/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
https://github.com/richarkc/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
https://github.com/richarkc/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/richarkc/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
Method DFT() is a depth-first traversal
https://github.com/richarkc/08_Graph_Lab/blob/master/Graph.cpp

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)
* Array-based list vs. Linked List

Array based lists and linked lists both have their various positives and negatives. An array based list is better at the set() and get() methods, being able to do them in O(1) time, however, add() and remove() both take O(n) time (unless the item is placed at the back of the array), as you must move every element behind the addition or removal backwards or forwards. On the other hand, a Linked list takes O(n) for get() and set() due to the fact that it has to iterate through the entire list in order but takes O(1) for add() and remove() because it only has to edit the pointers to the previous and next nodes to set it to that node. In the event that the element in a linked list has to add() or remove() to a specific element in a linked list, it will also take O(n) time, unless you use an iterator. With an iterator over the linked list you can do all of the operations in O(1) time if you have the iterator to the specific node you want to perform the operation at. A linked list also has the advantage of the fact that it does not need to be resized, as it is dyanamic in nature, so you can add as many nodes as you wish and not have to worry about creating and resizing the array. On the other hand, a linked list does use slightly more memory than an array based list due to having to store the pointers for the next and previous node(in a doubly linked list, just next in a singly linked list). If you're storing a large amount of chars, this extra data will be a pretty large factor, but if you're storing something like hash tables in a linked list, this will be negligible. Of course, with all data structures, it's all up to the problem at hand.

* Binary Search Tree vs. Hash Table

Hash tables and binary search trees are both very good data structures to implement a dictionary abstract data type, or anything that has a key to lookup. Hash tables are usually the faster data structure, being able to do get(), set(), and remove() all in O(1) time, while a binary search tree can only do the same operations in O(log n). The tradeoff for such speed is space. In a hash table, the machine must allocate a large amount of space, ideally at least 2 times larger, in order to avoid collisions, or two keys hashing to the same spot. Even with a large amount of space allocated, collisions are not guarenteed to not happen, they can still happen, and in the event of a collision the running times can increase, and depending on the type of collision handling the hash table is using the running times could get too large. For instance, in the case of linear probing, if multiple keys are hashed to the same spot, the key is put in the next available bucket. In the case that all keys are hashed to the same spot, running times reach O(n) for all functions, but such an event should not happen with a good hash function and proper sizing of the table. On the other hand, a binary search tree only allocates the amount of space that it needs to to store all of the items in the tree, or all the pointers of the nodes. Of course, a binary search tree runs into problems when the keys are put in order for example, where running times are now O(n) due to the tree being a strand. However, if the tree is properly balanced, which it almost always will be when the keys put in the tree are put in randomized order, the running times will be O(log n). A binary search tree also has the added advantage of being sorted, so you can traverse through the tree in order to get all of the items in order if you so need, so in the event of needing that operation, it would be better to use a binary search tree. A binary search tree can also get keys near the given key, i.e. can do next() and prev() operations easily due to the fact that it is sorted. However, if you do not need your data to be sorted at all, and you have the space, a hash table will be the better choice, otherwise a binary search tree would be a better choice.

* Adjacency List vs. Adjacency Matrix

An adjacency matrix is better at checking whether or not a given adjacency exists. An adjacency matrix is a matrix where you have all of the nodes on the x and y axes, and then a boolean value for each entry representing whether the adjacency exists. For checking a certain adjacency, all one has to do is go to the specific element representing the adjancency, and get the boolean. The tradeoff for this is space, an adjacency matrix has to hold a boolean for every single possible entry, O(n * n), while an adjacency list only has to store all existing adjacencies. While a matrix can get an adjacency in O(1) time, it is poor at iterating through all adjacencies. A list on the other hand, only stores the adjacency themselves. However, checking for a specific adjacency can be slow, especially in a large graph, where it has a worst case of O(n), in the event a node is adjacent to every other node. It has the added benefit of space, and it is easy to iterate through all adjacencies, or to find all adjacencies to or from a given node. 


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

* The call stack (not to be confused with the stack data structure!)

The call stack stores all statically allocated variables and any imformation relating to function calls (return address, parameters). Allows for fast and convenient access of memory. 
* The heap (not to be confused with the heap data structure!)

The heap stores all dynamically allocated memory, i.e. any variables allocated with the "new" keyword, and requires manual memory management, such as ensuring that the variable is deleted when it falls out of scope.
* Address

An address is the physical location of a variable in virtual memory.
* Pointer

A pointer is a variable that stores an address and type of another variable in memory, so that you can pass that specific item around in code.

* What is a memory leak, and why is it bad?

A memory leak is an item in memory that no longer has any pointers to it. It is bad because it is occupying memory space that could be freed for other resources in the OS, which is generally a behavior that is not preferred. A memory leak is simply wasting valuable resources for program, which in the worst case might cause a crash in your system, or simply slow it down.
* What is a dangling pointer (or dangling reference), and why is it dangerous?

A dangling pointer is a pointer to a point in memory that has already been deallocated by the program. It is dangerous because you can still try to access that memory, which may contain invalid data, leading you to have potentially unexpected behavior in your program and potential program crashes.

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why aren't they necessary in Java?

A destructor is a method that is called when an item is destroyed for whatever reason, and is used to deallocate dynamic memory in that object, due to the fact the c++ does not have its own garbage collector. Without a destructor memory leaks are very common. An example of a destructor preventing memory leaks is that of a linked list, where if the linked list is destroyed then the destructor will be called and all of the nodes in the linked lists are then deallocated through the destructor. It is not necessary in java because the java garbage collector automatically deallocates an object whenever it cannot be referenced anymore (goes out of scope).

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?

The main benefit of using templates when creating collection classes is the ability to use generics. With templates, you can specify a generic, which then the user of that collection class can specify that generic to be the specific object that they want to use in their code, rather than restricting them to using one type. This flexibility allows many different users to use your collection class in many different situations, rather than coding a different class for every possible data type to achieve the same result.

* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

In template-based collection classes the compiler needs to have access to the implementation of the class so that it can compile it with the specified class at compile time. If we seperated it into a .cpp file then the compiler would not know how to compile the collection class with the given type. This is due to the way a compiler handles templates. The compiler will compile a new class with the specified data type every time that it is instantiated with that given data type. This does require us to put the code in the .h file so that the compiler only looks there to compile it, but most of the time this is circumvented by making a .ipp file and #include that .ipp file to the end of the .h file in order to obfuscate that code into a different file.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)

For this problem I would approach it with a hash table data structure. Assuming that the only functions that the set will do for the purposes of this program is to adding string, removing strings, and checking existence of a string. Considering that the hash table can do adding and removing, the two operations that will be used the most in this program, will take O(1) time. The added benefit of using a hash table is that it will also be able to check the existence of a given key whenever it adds another string to the set. One problem to using a hash table to store a set is that if the hash table is not at least 2 times bigger than the amount of entries than the chance of collisions(two keys behind hashed to the same bucket) is large, so it would use a lot of memory, but the trade off of speed is more than worth it. In the event of using linear probing for collision resolution, one can simply check for either an empty bucket, or for an exact key match, otherwise move to the next available bucket. However since we can't store duplicates, we must probe over deleted values so that we can find a possible matching key, and then if we do not find the key place it in the deleted bucket. Another downside to using a hash table is that if we have to actually view the entire set, we must iterate through the entire backing array in order to print all keys, however the problem did not state this, so hash table is definitely the best data structure for this problem.

* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

A doubly linked list with iterators would be the best data structure to store a grocery list. The reason being is that while shopping, one would have to frequently delete or add specific items within the list, and linkedlist provides the greatest efficiency for it, being O(1) for both those operations. By far, adding and removing will be the two most used operations and as such efficiency for those are the most important. An array, which also provides the same efficiency for those operations, has weaknesses in the case that people wish to change the order of the list, which could be potentially important for some people, as an array you must move all the other elements behind where you move the object, and you would also have to size the array fairly large so as to not overflow the bounds of the array or force you to resize it, where as a linked list only has space for all elements and the pointer to the next and last elements. With an iterator, it also allows for get() for certain items, but that operation will not be called very often, so it's not nearly as important. With the addition of an iterator for the linked list, one can access certain elements very quickly, provided you know the location in terms of the iterator. A grocery list also likely won't be very large, so storing extra space for something like a hash table, which also provides O(1) for adding, removing, and lookup, would be very inefficient in terms of space, so it wouldn't be a good choice, leaving a doubly linked list as the best available data structure.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

A hash table would likely be the best data structure for this problem, with the Banner number being the key and the record being the value. For this problem, we know that banner numbers are unique, so we are guarenteed a unique key, so a Hash table should provide O(1) performance when looking up, adding, or deleting. Assuming that looking up, adding, and removing will be the most common operations, we want the most efficiency with those operations. Since our keys are unique, with a good hash function and a properly sized backing array for our hash table, bucket collisions should be fairly low keeping our running times low. For collisions doing linear probing would probably be the best solution since collisions will likely be fairly low for given reasons. The only tradeoff for the speed of using a hash table would be space, however considering that space is fairly cheap and the person using this data structure would likely have a large amount of space to store all the student records to begin with, space is not a huge concern. This makes the Hash table the best data structure for this problem. If space is a concern, a binary search tree would also be a good option, providing O(log n) for the same operations, however only allocates the space that it needs for the items, where as a hash table has to allocate a large amount of size, ideally  2 to 3 times bigger than the expected amount of entries so as to avoid collisions. The speed tradeoff, however, would likely not be worth it as O(1) is considerably faster than O(log n), especially when dealing with a large amount of data, such as we would be when dealing with students, leaving a Hash table as the likely best choice.

* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

A heap implemented as a priority queue would definitely be the best option for this situation. The only thing that the router really cares about is the priority of the item it needs to send, so a priority queue is definitely the ADT needed for this. The heap is usually the best data structure for implementing a priority queue, as it provides O(log n) for all operations, except for looking up that highest priority member, which is O(1), and it does not need to be fully sorted, only partially sorted so that all objects of lesser priority is below the node. Giving the amount of money as a priority so that the highest priority member is the root (max-heap), at allows the priority queue to be easily built and maintained. Since looking up the maximum priority value is O(1), this will allow the router to quickly get the next packet that it needs to send and send it out as fast as possible. Giving O(log n) time for the other operations is the best that we can get out of almost any data structure that we have learned due to the fact that the priority queue has to be at least partially sorted so that the max priority item will always be at the front of the queue, and a heap provides that best function for that. 
