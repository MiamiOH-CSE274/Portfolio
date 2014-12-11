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
https://github.com/samsab/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
https://github.com/samsab/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
https://github.com/samsab/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
https://github.com/samsab/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
https://github.com/samsab/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/samsab/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
https://github.com/samsab/08_Graph_Lab/blob/master/Graph.cpp

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List

Linked lists are, at their core, an entirely different concept from array-based lists. Each value or 'node' in a linked list contains a variable assigned to the next node, and another for previous if doubly linked. Therefore, in get(i) and set(i,x), we must iterate through each of the elements in the list until we find i. The worst case running time for these methods would therefore be O(n), n being the number of nodes. An array-based list, however, can be accessed at any point to find any element. Say we had an array 'ray' of 10 objects. Calling get(4) would result in one line: 'return ray[4];'. As arrays can be accessed randomly, get(i) and set(i,x) would take constant time, or O(1). That means for larger lists which must be accessed or edited often, an array list would be preferred. However, there are many other differences between the two.

When adding elements to an array, the list must iterate through all elements behind the new addition, pushing them back one index. When removing elements from an array, the list must push all elements behind the deletion forward one index to fill in the gap. These processes are not desirable to a list with many additions and deletions, as they each take O(n) time due to mass iteration. Linked lists not only have add and remove, but also push(x) and pop(). While add places the new node at the end (or 'tail') of the list, push places it at the front (or 'head'). Pop has the same operations as remove. Since all of this takes place around the head and tail, add, remove, push, and pop all take O(1) time. This would be preferable to arrays with more addition and removal than accessing the actual elements.

A linked list is dynamic in nature. As adding new elements only requires the addition of new links and some changes to existing links, it never needs to be resized. Array-based lists have a strict size, and when adding elements to the list, it may occasionally have to call the grow() method, which stores a new array with the same elements into the current array. Due to the iteration involved in copying a temporary array back into the original array, the method takes O(n) time. This is not desirable for rapidly growing lists. A linked list also has an iterator, which arrays do not as they can be accessed randomly. An iterator can shorten the time taken to find one location in an array and if the iterator is in the desired location, add, remove, get, set, pop, push, and other methods dealing with location could be O(1). This is assuming the iterator would always be in the right place. Iterators do require memory to keep track of, and when using linked lists, memory is already being used to keep track of each link between nodes. This is not present in array lists, so when memory is crucial, linked lists should not be the first choice.

To add a new element at a certain index would be O(n) worst case for both linked lists and arrays. Arrays would have to iterate through all elements behind the addition to move them forward. A linked list would have to iterate through each element to find the correct index, which would take linear time or O(n) and then adding the element would take constant time. For the same reasons, we can see that worst case for linked lists and arrays when removing an item at a designated index would be O(n). Adding an object to or removing an object from the back of an array would take O(1) time, as would getting or setting the first element of a linked list. So best case running time for get, set, add, and remove would be O(1), but arrays still have grow() which takes O(n).

* Binary Search Tree vs. Hash Table

Hash tables and binary search trees are more complex data structures. Hash tables require hashing, which involves complex number theory to ensure hashing two different values has a low likelihood of resulting in the same hash code. Chained hash tables and linear hash tables are similar in many ways. They both implement the USet interface, resizing them during any sequence of m takes O(m) time, and without resizing, add(x), remove(x), and find(x) each take O(1) time. This shows that hash tables are very good for small amounts of data which require frequent access. For a large number of small lists of data, many hash tables would be good, as little would have to be done to each one, but all three essential methods would each take constant time.

Binary search trees are very useful because of recursion. This creates very clean, understandable code. While searching through a binary search tree, adding to it, or removing nodes from it, we may look through all nodes to complete one task. However, with a sorted binary search tree, we typically need only navigate through one side of the tree. Therefore, the average time taken is the same as the height of the tree, which is log n, so our add, remove, and find take O(log n) time on average. The advantage over hash tables comes when our tree grows to enormous size. Hash tables become cluttered and overly-complicated when we are storing mass amounts of data. Regardless of how big our tree gets, however, it will always take O(log n) on average to call these essential methods.

Hash tables and binary search trees can both become cluttered and complicated to the point that they find their worst case scenarios. For each data structure, the absolute worst case for add, remove, and find is that we must iterate through each member, giving us O(n) time. This can happen to both hash tables and binary trees, but only in certain situations. The key is to find the right data structure for the right situation so that we never have to face a running time of O(n) for either of these two structures.

* Adjacency List vs. Adjacency Matrix

Adjacency lists and adjacency matrix are very similar structures which implement the Graph interface. An adjacency matrix is a matrix representation of a vertex graph of objects linked to each other. Given a graph of n objects, the corresponding adjacency matrix would be a matrix of size (n,n). Each location (i,j) in the matrix holds either a 1 or a 0, a 1 denoting that there is an edge between node i and j and a 0 denoting that there is not. An adjacency list does not hold 1s and 0s, but rather is an array of lists of nodes which are linked. Each index in the array holds a list of nodes which are adjacent to the node at the list's index. So the list at index b contains all nodes linked to node b.

For a matrix, removing an edge and checking for an edge are quite simple operations. These methods would simply access one vertex in the array and either read it or change it. These operations take O(1) time. In an adjacency list, however, we must iterate through the entire list of linked nodes when we remove or locate one edge. Therefore, the run time for these two methods would be O(deg i), deg i meaning the number of edges which link to node i. The outEdges method also takes O(deg i) time for the list, as it only has to output the list at index i. In this case, however, the list is actually better than the matrix, because the matrix must iterate through one entire row or column to output all edges at index i. Therefore, outEdges runs at O(n) for the matrix. The inEdges is actually the same for the matrix, as it must iterate through n items, so the run time is also O(n). The list must iterate through each index AND each list in the index to find all in edges, so the run time is even worse than the matrix: O(n+m).

The only method which is the same for both an adjacency matrix and an adjacency list is addEdge. The matrix needs only to change two vertices to 1 (if they are not 1 already) which is obviously O(1). The adjacency list only needs to add one element to the list at the corresponding index, which also obviously takes O(1) time. Where both of these structures fail is in storage. The matrix created is of size (n,n) meaning we need n^2 vertices and therefore O(n^2) bytes of memory. Each index in the list has a list of linked nodes, meaning it takes up O(n+m) memory. These are terrible figures for memory, but these Graph-like structures are good ways to create and store virtual graphs or virtual linked lists.

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!) - The call stack holds all statically allocated variables like an array, but stores in a LIFO structure. The stack hold local variables.

* The heap (not to be confused with the heap data structure!) - The heap is a pool of memory used for dynamic allocation.

* Address - The location of a variable's memory stored in the computer.

* Pointer - A variable which stores the address to a variable and can reference the address at any time.

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?

Memory which is allocated but not released is said to have 'leaked'. This leaked memory takes up space on the computer and will slow applications on the computer unless handled correctly.

* What is a dangling pointer (or dangling reference), and why is it dangerous?

Dangling pointers are those which point to invalid data or data which is no longer valid as it has been removed. These references are bugs which typically crash the program, and do so in a way which makes them difficult to find, as they usually do not crash right away.

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?

Destructors delete unneeded memory to prevent memory leakage. In Java, developers need not worry about this, as the built-in garbage collector cleans up the program for the user.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?

The use of generics is the most beneficial part of templates. Another programmer can use your generics and implement his or her own algorithms or design patterns, while still maintaining the core essence of your template code. This cuts down on time heavily when a user wants to use the same object type and resulting classes as in your program. Instead of re-writing all the code, one can just open a template and fill in the gaps.

* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

Template-based collection classes are compiled differently than a normal project. They handle the .h files rather than .cpp, so the program will not be able to compile code from a .cpp file. Instead, we can either put our code in the .h file or use .ipp files, and can include the .ipp files at the end of our .h files by using #include. If we try to compile a .cpp, it will ignore it and attempt to compile the .h file instead. Therefore, that is where our code must go.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)

For this short set of strings, we will need to use add, remove, and find methods. Being that this is the extent of our structure's needs, I would recommend a hash table. Hash tables are made for exactly this scenario. The add(x), remove(x), and find(x) methods all take O(1) time, so these operations will be quick. That means by using a hash table, all of our necessary methods run in constant time. However, depending on how big the set of strings are, we may run into problems if the set is too large. As hash tables resize, they have a larger chance of collisions. By forcing the hash table to resize, we must endure O(m) time each call, and run the risk of decreasing the table's efficiency. We could use linear probing to detect any collisions, and as long as the hash table doesn't resize a great number of times, this would be the best choice.


* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

Grocery lists are comprised of string values in a random order. New strings can be added at the back of the list, and when items are bought, they are taken off of the list. By this description, we would want a linked list. With add(x), we can enter new items at the end of the list, and with pop(), we can take out the item at the head. This way, we have a FIFO-structured list, where the first item we wrote down or added to the list gets taken off first. As groceries run out, we add them to the list. Then we go grocery shopping and with each item we get from the top of the list, we call pop() to remove it. Since all we are doing is adding to the bottom, reading the top node, and removing the head node, we only need three methods: add(x), pop(), and peek(), a getter method which returns the value at the head node. Since all operations only pertain to the head and tail of the list, all methods used by this linked list would run at constant time. Therefore, this would be the best choice of data structure.


* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

For this problem, we would need a key-value pair structure, or dictionary type structure. The Banner number would be the key, while the value would be a string containing the associated student's name. In this case, a hash table would be best. A hash table is capable of hashing values like the Banner number. When a new student is added, their name will be located at hash(x), where x is their Banner number. This way, any student's information can be accessed randomly with O(1) time. Also, disregarding resize(), adding and removing students would run at O(1). For those reasons, a hash table would be perfectly suited to solve this problem. The only bad thing about using a hash table as a solution for this would be that with the sheer number of students, the hash table would have to be fairly big. This would cost a lot of memory, but the speed at which one could retrieve student information would be worth the memory usage. Also, since every student has a unique Banner number, there is less of a chance that the hash function would cause collisions, and a repeated hashcode value would not happen often. For all of these reasons, I believe a hash table would be the best fit for this situation.


* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

In this problem, the solution lies in a heap for certain. The heap will contain the queue of packets, and will send the correct packets at the correct time. Since we are dealing with prioritized packets, it would make most sense to implement a heap-based priority queue. This way, the program can determine which packets are more 'important', sending those first whenever there are any present, and then sending the rest when no remaining packets have a higher priority. To add new packets, the program could call push(x), and sort it by priority. This would take logarithmic time, O(log n). Sending the packets could be done by calling pop(), which happens in constant time. All we are doing in this scenario is receiving and then sending packets, so this is really all that we need. When we push new packets to the heap, we must sort the list again to make sure all packets are in order of priority. Then, we send them out by calling pop() and removing the item at the top of the list, in other words, the packet with the highest priority. This would assure that the packets with the highest priority get sent first. This situation is basically what the priority queue was made for.
