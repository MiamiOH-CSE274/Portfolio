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
I showed how to implement a Queue in my Queue lab from lines 78-144. Here is the link. https://github.com/meslerke/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
I proved that I can implement a list in lines 81-194 of the Linked List Lab. This is the link.
https://github.com/meslerke/04_Linked_List_Lab/blob/master/LinkedList.h


7 - Determine space and time requirements of common data structure methods
-----
* Array-based list vs. Linked List

An Array-based list runs O(1) time when performing operations like get(), set(), and size() while a Linked List runs O(n) time. A Linked List runs O(1) time when performing operations like add() and remove() while an Array-based list runs O(n) time. This is because an Array-based list doesn't need to go through every element that it has to get or set an element, and the length is stored in a variable so that you don't have to figure it out. In a Linked List, you have to loop through the list to access elements for the get, set, and size methods, which takes much longer. The opposite goes for the add() and remove() methods. To add or remove an element from an Array-based list, you may need to shift all of the other elements in the list to make room for it. In a Linked List, you just need to change the pointers so that they include another node, which is faster.


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!)
* The heap (not to be confused with the heap data structure!)
* Address
* Pointer

TODO: Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad?
* What is a dangling pointer (or dangling reference), and why is it dangerous?
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?


5 - Using time and space analysis, justify the selection of a data structure for a given application
----
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

I imagine a grocery list as a list that is kept on paper. The first item that you write on the list goes at the top of the page, and as you add more and more items to the list, they go as close to the top as they can without being higher than the previous item. Looking at a grocery list this way, I think that a Queue would be the best data structure to use. This is because it has a first in, first out order. If you are at the grocery store, you would look at the top of your list (first added) and find that item. Then you would remove that item from the list and look for the next item below it (second added to the list, etc.) This means that the first item on the list is naturally the first one off of the list as well, which is why a queue would be a good representation of this list.
