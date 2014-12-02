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
I showed how to implement a Queue in my Queue lab from lines 78-144. Here is the link. https://github.com/meslerke/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
I proved that I can implement a list in lines 81-194 of the Linked List Lab. This is the link.
https://github.com/meslerke/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
TODO: Provide a link to your completed 06_BST_Lab OR ClosestStarbucks project (only if you used a search tree)

7 - Create an implementation of a Hash Table
----
TODO: Provide a link to your completed 05_Hashing_Lab

7 - Create an implementation of a Heap
----
TODO: Provide a link to your completed 07_Heap_Lab

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
* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

* Array-based list vs. Linked List
An Array-based list runs O(1) time when performing operations like get(), set(), and size() while a Linked List runs O(n) time. A Linked List runs O(1) time when performing operations like add() and remove() while an Array-based list runs O(n) time. This is because an Array-based list doesn't need to go through every element that it has to get or set an element, and the length is stored in a variable so that you don't have to figure it out. In a Linked List, you have to loop through the list to access elements for the get, set, and size methods, which takes much longer. The opposite goes for the add() and remove() methods. To add or remove an element from an Array-based list, you may need to shift all of the other elements in the list to make room for it. In a Linked List, you just need to change the pointers so that they include another node, which is faster.


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
* The call stack is similar to the data structure stack but it can only hold a limited amount of information.
* The heap is where the memory comes from that is used when allocating memory using 'new'. It is like a large pool of memory.
* An address is something that everything that is stored in memory has. The address tells you exactly where that piece of memory is stored.
* A pointer is an object that refers to (or points) a specific piece of memory using its address.


* A memory leak is when you allocate memory but don't deallocate it when you are done. The memory isn't free to use again until you deallocate it, which means that you aren't using it anymore. This is dangerous because if you don't tell the computer that you are done with a piece of memory, that memory won't be available to be used later and eventually you will run out of memory!
* A dangling pointer is created when you create a pointer for something and then delete what it was pointing to. This is dangerous because you don't know how your computer will act to this in the long run.
* A destructor essentially cleans up after you when you are done with a program. It deallocates the memory that you have allocated so that you can use it again at another time. This is necessary in C++ to prevent memory leaks because if you don't deallocate the memory that you have used, then that will create a leak in your memory and you can eventually run out of memory. These aren't necessary in Java because Java is designed to automatically do this for you when you are done with a program.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++

* What is the main benefit of using templates when creating collection classes?
* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.


* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

I imagine a grocery list as a list that is kept on paper. The first item that you write on the list goes at the top of the page, and as you add more and more items to the list, they go as close to the top as they can without being higher than the previous item. Looking at a grocery list this way, I think that a Queue would be the best data structure to use. This is because it has a first in, first out order. If you are at the grocery store, you would look at the top of your list (first added) and find that item. Then you would remove that item from the list and look for the next item below it (second added to the list, etc.) This means that the first item on the list is naturally the first one off of the list as well, which is why a queue would be a good representation of this list.
