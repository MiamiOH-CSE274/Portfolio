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
https://github.com/ernstcc/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
https://github.com/ernstcc/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
https://github.com/ernstcc/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
https://github.com/ernstcc/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
https://github.com/ernstcc/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/ernstcc/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
https://github.com/ernstcc/08_Graph_Lab/blob/master/Graph.cpp

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List
While there are numerous different variations of a List interface, Array-based and Linked Lists are two of the most common and useful.  The basis of an Array-based list is storing data in a single array that is organized in a manner such as a queue or stack.  As a result of being a single array, there is constant time access to any member data through the get and set functions.  Another result of all data being stored in a single array is that adding or removing an element is run, at worst case, in linear time because the array may need to relocate every piece of data.  Finally, the only way to resize the array is to completely allocate a larger array and move the current array into it which is a relatively expensive process.  Linked Lists work by using pointers to hold all data in successive order.  Each piece of data is given a spot in the list also known as a node and has a link to both the next and previous nodes.  Contrasting array-based lists, all linked list functions (add, remove, get, set) run in constant time once the relevant node has been determined, however, finding the relevant node can take up to linear time.  This results in the add and remove being faster in Linkedlists, but the get and set theoretically being faster in an array-based list.
	

* Binary Search Tree vs. Hash Table
Binary Search Trees and Hash Tables are both very useful data structures for storing data that needs to be quickly accessed.  Both data structures have much faster performance than using a traditional array.  Binary search trees algorithms are almost all based on a principle of comparing an input key with the root node and moving either left is it is less or right if it is greater.  The comparisons effectively cut the size of the tree in half for each comparison made which results in a runtime of O(log(n)).  All of a Binary Search Tree's member functions (add, remove, search, min/max, next/prev) run in O(log(n)) time.  This results in the Binary Search Tree being a very versitile data structure because every single one of its functions runs in relatively fast time.  The Hash Table, on the other hand, is very fast at certain operations, but markedly slower than the BST in others.  The basis of a hash table is a a large array with numerous open spots in which data can be stored.  A hashing function is used on the key of an object and the object is mapped to a location within the array.  Because of the nature of using the key as a lookup with the function, operations like add, remove, and search all run in constant O(1) time.  This means that for a program that utilized these functions numerous times it would be beneficial to use a hash table for the shorter runtime.  Where the Hash table falls short is operations such as min/max and next/prev.  Two objects with very similar keys can be mapped to completely different locations in the array through the work of the hashing function.  This results in a need to search through the entire array if min/max or next/prev are called which means they have a runtime of O(n).         

* Adjacency List vs. Adjacency Matrix
Adjacency Lists and Adjacency Matrix's are both unique implementations of the graph abstract data type.  An adjacency matrix is implemented by storing objects in a 2-d array with a size being the number of items^2.  This results in the array taking up a large amount of memory to be stored.  The benefits from using this implementation however is that adding, removing, or searching for an edge all run in constant time.  However, adding and removing a vertex runs in O(n^2) time.  This shows that the data structure can be beneficial if the graph is heavily populated and edges need to be found quickly.  An adjacency list is a way of implementing a graph without also listing all non-existant edges as well.  The adjacency list uses vectors to store each vertex which then contains another vector with each vertexes edges.  This means that the data structure is takes up much less memory than an adjacency matrix because non-existant edges are not stored.  Additionally, the nature of a vector allows new vertexes and edges to be added in constant time because the index is readily available.  Where the adjacency list performs more slowly, however, is when an edge or vertex needs to be removed in which cause the runtime is O(n).

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!) - The call stack is the memory set aside for the process currently being executed.  The stack stores all local variables and functions which will go out of scope and automatically be deleted.  Because the stack is implemented using an actual stack data structure, the last argument sent to the stack will be the first one removed.  Additionally, variable in the stack can be directly referenced without needing a pointer.  

* The heap (not to be confused with the heap data structure!) - The heap is the memory of the computer that is not set aside for current processes being executed.  As a result, the variable and objects never fall out of scope and must be manually created with the new() command and deleted with the delete command.  Additioanlly, variable cannot be directly accesses and must instead use a pointer. 

* Address - An address is the location in the heap where a specified variable is present.    

* Pointer - A variable that stores an address of memory.

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?
A memory leak is when a program uses excessive memory because inaccessible data is still stored on the heap.  Often times memory leaks are caused by forgetting to delete variables or arrays after use.  The result of memory leaks is slower code and potentially heavily taxing the computer by using all the RAM.

* What is a dangling pointer (or dangling reference), and why is it dangerous?
A dangling pointer is a pointer that references data that has already been deleted by the program.  The danger in dangling pointers comes from the memory manipulation potential of C++.  By using a reference into the memory, one could access any part of the program or system. 

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?
A destructor flags the location of the object to be deleted that is stored on the heap so that it can be overwritten when necessary.  This functionality is not needed in Java because Java automatically deletes an object that is no longer referenced anywhere in the code.  This process known as garbage collection.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
If a data structure was needed to store a set of strings, a hash table would be an appropriate data structure to use.  Hash tables can perform all the necessary operations of a set and because order should not matter with the strings, a hash table will be the most efficient.  The nature of a hash table is to run a key through a hashing function in order to generate an index location for the object.  In this example, the string itself could be used as the key and it could be stored in an array at the index to which it's key mapped.  This solves the issue of not allowing duplicates because any strings with identical values will map to the same index and a quick comparison can be made to ensure the the index is not occupied.  What becomes more complex is when keys with different strings map to the same index, but this issue can be solved by implementing a probing method such as looking for the next open slot of the array by adding 1 to the index and taking the % of the array size and storing the string there.  Once the strings are stored within the hash table, all necessary operations of a set (add, remove, search) will run in constant time.  This is a benefit over using either a Binary Search Tree or arrayList which will both have slower runtimes for the necessary operations.  Finally, a hash table is known to be a good implementation of a USet because it is the data structure used in the C++ unorder set class.    

* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
In order to store a grocery list, a doubly circular linked list would be the most effective data structure.  The reasoning behind this decision is that the add and remove functions run in almost constant time, so crossing items off the list would be very efficient.  Additionally, adding items to the list would be at least as efficient as an array-based list and very likely much more efficient.  The basis of a doubly circular linkedList is that each node connects to both the next and previous nodes which makes each easily accessable.  In this manner, one could use the next function to traverse through the entire shopping list in constant time for each operation. 

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
The most appropriate data structure to store student records and be able to search by banner number is a hash table.  A hash table operates by having an array to store objects that map to a certain index from their unique key.  The key for each object is passed through a hashing function and an index for the object is returned.  In this particular example, a banner number could be used as the key and the student's information would be stored in the index to which the banner number mapped with the hash function.  If there is a conflict with two keys mapping to the same index, a probing method can be implemented such as adding 1 to the index and taking the % by the array size until an open index is found.  Additionally, since no two banner numbers are the same, there is not a concern over having duplicate objects within the table.  The reason why a hash table is beneficial to use for storing student information is the very fast runtime of its search, add, and remove functions.  Miami has a very large student body so a relatively large hash table would be needed to store the entire student body.  Because of the implementation of a hash table, however, the runtime to search for a student would still be constant time O(1).  If a new student needed to be added to the table, their insertion would also be in constant time O(1).  Graduating students could also easily be removed by running the remove function with their banner numbers.  This would remove each graduating student from the table in constant time and clear space for later students so the table does not become too space-complex.    

* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
The most appropriate data structure for the implementation of the network router would be a heap-based priority queue.  The heap would be implemented with an array to store the objects.  The heap itself would need to be organized in a minimun fashion such that the smallest priority element is always at the top of the heap.  Next each company that uses the router could be rated by how much money they pay for the service and the results put into a list.  The company that pays the most money will be located at index 0 on the list and the company that pays the least amount of money will be located at index n-1 on the list where n is the number of companies.  Each incoming packet from a company will be referenced with the payment list and the priority of the packet will be equal to the company's location on the list.  In this manner, the companies that pay the most will always have higher priority than companies that do not.  Whenever a packet is sent in by a company, it will be added to the bottom row of the heap in the furthest left possible location.  Next the priority of the packet will be compared to its parent packets within the heap and if the priority of the new packet is lower (the company paid more money) the locations will be swapped.  This process will repeat until the priority is in the correct location.  When removing packets from the heap, the highest priority packet will always be the first removed.  Next the object stored at the end of the array, which is the furthest right object on the bottom row, will be moved to the top, highest priority spot of the array.  Next the object at the top of the array's priority will be recursively compared with both its children's priorites and swapped with whichever is the smallest.  The process stops once the object has found a location in which its priority is smaller than its children.  
