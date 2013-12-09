Author
==========
"Bickley, Daniel", bickledb
Portfolio
=========

Document completion of the course's learning outcomes.

Instructions
====
The goal of this is to make it very easy for me (or an employer, or a teaching assistant) to see whether or not you have mastered the material of the class. The hope is that I would be able to grade your work without downloading and compiling your code. If you have recorded proper video demonstrations of your programs, that should be sufficient. You will also want to write a paragraph or so making your case for why you deserve full credit for particular learning outcome (or if you don't, then you should say so).

Important
=========
If you prefer, you may turn this in to me via email, instead of hosting it on GitHub. Please talk to me about it during office hours or before or after class.

Body of portfolio
====

7 - Create an implementation of a Queue
----
Possible sources of evidence (do any one of these):

An implementation of a Queue can be found at https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/bickledb

7 - Create an implementation of a List
----
Possible sources of evidence (do any one of these):

An implementation of a List can be found at:  https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/bickledb

*  https://github.com/MiamiOH-CSE274/04_Linked_List_Lab

7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

An implementation of a BST can be found at: https://github.com/MiamiOH-CSE274/06_BST_Lab/tree/bickledb

7 - Create an implementaiton of a Hash Table
----
Possible sources of evidence (do any one of these):

An implemention of a Hash Table can be found at: https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/bickledb

7 - Create an implementation of a Heap
----

An implementation of a Heap can be found at: https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/bickledb


7 - Create an implementation of either Adjanency Lists or Adjacency Matrices

An Implementation of an Adjacency Matrix can be found at https://github.com/MiamiOH-CSE274/08_Graph_Lab/tree/bickledb

7 - Implement graph algorithms
----

An implement of Graph Algorithms can be found at https://github.com/MiamiOH-CSE274/Vise/tree/BlaseAndBickley.
Specifically, lines 290 - 332 of GameBoard.cpp

21 - Determine space and time requirements of common data structure methods
-----

Queue: Implemented at https://github.com/MiamiOH-CSE274/03_Queue_Lab/blob/bickledb/ArrayQueue.ipp
* Constructor: Assuming memory allocation is constant, the constructor will have constant running time.
* Destructor: Because the delete[] method is called, the destructor will have either a linear or constant running time, depending on the data stored in the Queue. If the data requires a destructor to be deallocated, delete[] will have linear time. If delete does not have to be called for the data to be reallocated, it will take constant time.
* Add(): As the implementation is a circular ArrayQueue, the add() method is constant, unless it calls the grow() method. Without the call to grow(), the add method utilizes a constant running time, as the structure is an ArrayQueue, and the data can only be added to one spot in the array at a time, regardless of size. However, if grow() is called, the add method has a linear running time, as the grow() method depends on the number of data points that are in the Queue.
* Remove(): In this implementation, Remove() utilizes constant time, as there is one spot where the data will be "removed" from, which is independent of the size of the Queue. 
* GetNumItems(): In this implementation, getNumItems() utilizes constant time, as the size of the Queue is stored as a variable and the running time is independent of the number of items in the queue.
* Grow(): In this implementation, grow() takes linear time, as it needs to allocate memory space for a temporary array, write all of the data in the old array over to the new array, in order. This step will take linear time, and is then followed by a destructor for the old array, which takes constant time. Overall, the method should take linear time.

List:  Implemented at https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/blob/bickledb/LinkedList.ipp
* Constructor: Assuming memory allocation is constant, then the constructor will have a constant running time.
* Destructor: The destructor should take linear time. The call to the remove() method causes a call to the find() method, which normally takes linear time. But, because the destructor only calls remove() at zero, and consequently find() at 0, the method only takes linear time, as each iteration through the list takes constant time to remove and delete.
* Find(): The method takes linear time, as the method cycles through each node until it has the reached the ith node, and then returns it. In the worst case scenario, the method will loop through the entire list, and the running time is therefore dependent on the size of the List, so it takes linear time.
* Set(): The method takes linear time, because it contains a call to find(), which takes linear time. Because the rest of the method only sets variables or changes them, which all take constant time, the method is therefore linear.
* Add(): The method takes linear time, because it contains a call to find(), which takes linear time. If we assume that the call to the Node constructor takes constant time, the overall running time will still be linear, as the rest of the method only changes variables, which only takes constant time.
* Remove(): The remove method takes linear time, because it contains a call to find(), which takes linear time. The rest of the method takes constant time, except for possibly delete, which will be assumed to take constant time, as the running time of delete is independent of the size of the List.
* Get(): The get method takes linear time, as it loops through the List, Node to Node, until it finds the Node at the index i, where it returns the Node's data. Because the loop used is dependent on the size of the List, the method has linear running time.
* Size(): The size method takes constant time, as the size of the List is stored in a variable, which can be accessed in constant time.
	
Heap: Implemented at https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/bickledb
* Constructor: Assuming memory allocation is constant, then the constructor will have constant running time.
* Destructor: Because the delete[] method is called, the destructor will have either a linear or constant running time, depending on the data stored in the heap. If the data requires a destructor to be deleted, delete[] will take linear time, and if does not, the destructor should take constant time.
* Grow(): This method takes linear time. When it is called, it allocates an array that is twice as long as the previous array. Then, every item in the old array is added to the new array, one by one, taking linear time. Then, the old array is deleted with the delete function, and a pointer is reset, which takes constant time. Therefore, the method will take overall linear time.
* BubbleUp(): This method takes lg(n) time, as each time bubbleUp() is called, it checks the parameter's parent and swaps them if needed and continues to move up the heap until the item is in it's correct position. In the worst case scenario, the method has to move a data item up an entire "branch" of the heap, and because of the Heap's properties, the branch will be lg(n) nodes long. Therefore, the method will take lg(n) time in the worst possible scenario.
* Add() : This method will take up to lg(n)+n time, assuming the bubbleUp() method has a worst-case scenario running time and grow() is called. The method can take lg(n) time because when the new item is added to the array, which takes constant time, the item has to bubble up the heap to reach the correct position. The bubbleUp() method takes lg(n) running time, which can be coupled with grow() to have lg(n)+n running time. If grow is not called, add will take lg(n) time assuming the worst case scenario for bubbleUp().
* TrickleDown(): This method will take lg(n) time, as when trickleDown() is called, it moves the parameter down the heap to find the correct location for it by swapping it with one of the Node's children. Due to the properties of the heap, the branch the parameter node is swapped down is lg(n) nodes tall. Therefore, the overall running time of the method will be lg(n).
* Remove(): This method will take lg(n) time, because it initially starts by swapping the root Node with the node at the end of the array, and then proceeds to call trickleDown() on the root node. Then, the item at the end of the array is returned. Because remove() contains a call to trickleDown(), the method will take lg(n) time overall.
* getNumItems(): This method takes constant time, as the size is kept track of in other methods, and all getNumItems does is returns the variable, without looking at any other data.
	
5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

 Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.

Evidence: https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/bickledb
	This example of a heap utilizes a dynamically allocated array. The backingArray corresponds to a series of memory addresses allocated in the "heap" section of memory. The memory allocation occurs when the keyword "new" is called, in this case, "new" is called when the Heap Structure is initialized and when grow() is called. The memory is allocated in the heap because the heap area of memory is much larger than the stack. The stack contains the local variables and the call stack, which is what calls each method when the program is run. Every method that will be 
	called by the program lies within the stack, along with any local variables that need to be initialized for the method. The local variables last as long as the method that creates them is running. When the method ends, the local variables are deleted from memory. If there are any global variables that are created, they last the length of the program, and are deleted when the program ends. However, for the dynamically allocated variables that are stored in the Heap space of memory they should be deallocated utilizing the "delete" or the "delete[]" command.
	The keywords should be used to deallocate memory to prevent dangling pointers and other memory management issues. When the memory is deallocated, it prevents the program from re-accessing the same slots of memory, unless they are reallocated. This takes care of issues such as dangling pointers, as the program can not accidentally change data in memory addresses it is not supposed. In the given example of the Heap Lab, memory is deallocated in the grow() method as well as the destructor. It is called in grow() to remove the previous backingArray and prevent the program
	from accidentally accessing any of the data stored within those addresses. It is also called in the destructor, to delete the backingArray and release the memory and allow it to be reallocated. In large scale projects, neglecting deallocation of memory can cause problems when the memory allocator must search through a large amount of memory to find enough space to allocate memory. If there is barely any space, the running time of programs can be much longer than what they would normally be, and could cause the computer to crash.

5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

Evidence: https://github.com/MiamiOH-CSE274/07_Heap_Lab/blob/bickledb/Heap.ipp
	This collection class takes in two objects, one for the data of each Node in the Heap, and one for the priority of each item. The reason why a collection class is used in this case is so that the data structure is flexible, and can be used with any classes that are created. When the project is compiled, the collection class is compiled with the rest of the program, but with the program specified
	classes as the data types instead of the generic declarations. The compiler will do this for any and all type declarations for each instance of the data structure. The main benefit of creating collection classes is to create code that is flexible and does not have to be rewritten each time a new data type is created or needs to be placed into a data structure. The only problem with collection classes is 
	that when they are created by the compiler, the compiler creates a one to one copy of the code, with the desired data types copied and pasted into the correct locations. This can lead to a lot of bloated code and a surprisingly large amount of wasted space.

30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):
List versus Queue:
---
	In the Shuffle project, there is an option to use either a Linked List or an ArrayQueue to be used to "shuffle" cards. The ArrayQueue is a reasonable approach because it offers constant time for almost all of the methods necessary to shuffle the cards. Add() and Remove() both take constant time, allowing for a conceptually easy way to emulate the riffle shuffle. If I wanted to emulate the riffle shuffle, I would create two arrayQueues, and read random segments of the initial deck into each of the queues.
	Then, taking both queues, I would read alternatively from each array into a Third, shuffling the order of the ArrayQueue. A LinkedList implementation is also possible, following a similar pattern as the ArrayQueue. The implementation would start with creating two Linked Lists, adding around half of the cards to one list and half into the other, and creating a third list to add all of the cards into, alternating between the initial two LinkedLists. The running time of the methods would both be constant for adding and removing cards from the ArrayQueue and the LinkedList, as adding items in an ArrayQueue always takes constant time, and
	adding to the ends of the Linked List will take constant time as well. The space constraints are also similar, as implementation does not require dynamic memory allocation for the items in the ArrayQueue or LinkedList. Overall, either data structure would work well for the Riffle Shuffle. The main reason to use one structure over the other is either ease of programming or the similarity of the data structure to how the shuffle works in real life. However, if you wanted to implement at a different  kind of shuffle, such as the Hindu Shuffle, the Linked List is better at that particular task.
	In the Hindu Shuffle, a chunk of the middle of the deck is removed, and then the top of the original deck is added to the top of the second pile, and the sequence can continue for a large length of time or a large number of shuffles. The best way to implement the Hindu Shuffle is a LinkedList, as you can use the splice() method to move a large number of cards at one time, just like how the Hindu Shuffle works. The shuffle begins with the initialization of two LinkedLists, one which all of the cards are read into, and a second empty one to act as the second stack.
	Then, a chunk of the deck can be brought out of the large stack, utilizing the splice() method, and can be moved to the second stack. Then, a certain number of cards can be removed from the top of the original list, and moved into the second list, until there are no cards in the first list left, exactly the same way as the Hindu Shuffle works. 

Vise:
---
	In the Vise Project, there are several different data structures possible. The data structure I chose was to combine a 2D vector containing nodes which have neighbor pointers to the northeast, east, southeast, southwest, west, and northwest. The reason why I selected this was because it offered most of the functionality of the game board at O(1) time. The neighbor pointers allow checking if adjacent spaces in the gameboard have pieces on them, used when moving new pieces onto the game board and when moving old pieces. It also
	makes implementing Dijkstra's Algorithm easier, as it breaks down the possible nodes to check into six recursive calls, which is conceptually easy. Further more, because the gameboard is based on a 2D vector, running through the vector to find groups of playing pieces takes linear time. From there, the program can use neighbor pointers to utilize a graph traversal algorithm. This implementation of Dijkstra's Algorithm takes n^2 + n lg n time, where n is the number of pieces that have been played. Another possible data structure is to simply use an adjacency list, which 
	would entail each node containing a list of neighbor pointers. I did not utilize an adjacency list because finding each edge connected to each node would take linear time, opposed to simply using neighbor pointers, which takes constant time. Due to the sheer number of times that the board is searched through, I wanted traversal to be as fast as possible. Running through each data structure to find nodes with pieces on them takes linear time for the adjacency list and as well as vectors with neighbor pointers. The constructor of each also takes 
	linear time, as each node has to be created individually, and then assigned the correct pointers. Vise could also be implemented without pointers, purely using math to determine which nodes connect to which other nodes. This method would take linear time in the constructor, as each node would have to be created. Overall, due to the relatively small amount of data that needed to be stored, the choice was greatly influenced by how we could code the structure and how we could visualize and implement the correct algorithms. 