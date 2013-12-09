Author
==========
"Bailey, Sam", baileys2
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
Source of Evidence:

Below is a link to my branch of the 03_Queue_Lab in MiamiOH-CSE274 (specifically the file ArrayQueue.ipp), where I successfully implemented a queue:

https://github.com/MiamiOH-CSE274/03_Queue_Lab/blob/baileys2/ArrayQueue.ipp

References used: the online text

7 - Create an implementation of a List
----
Source of Evidence:

Below is a link to my branch of the 04_Linked_List_Lab in MiamiOH-CSE274 (specifically the file LinkedList.ipp), where I successfully implemented a Doubly-Linked List:

https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/blob/baileys2/LinkedList.ipp

References used: the online text

7 - Create an implementation of a Binary Search Tree
----
Source of Evidence:

Below is a link to my branch of the 06_BST_Lab in MiamiOH-CSE274 (specifically the file BST.ipp), where I successfully implemented a binary search tree:

https://github.com/MiamiOH-CSE274/06_BST_Lab/blob/baileys2/BST.ipp

References used: the online text

7 - Create an implementaiton of a Hash Table
----
Source of Evidence:

Below is a link to my branch of the 05_Hashing_Lab in MiamiOH-CSE274 (specifically the file HashTable.ipp), where I successfully implemented a hash table:

https://github.com/MiamiOH-CSE274/05_Hashing_Lab/blob/baileys2/HashTable.ipp

References used: the online text

7 - Create an implementation of a Heap
----
Source of Evidence:

Below is a link to my branch of the 07_Heap_Lab in MiamiOH-CSE274 (specifically the file Heap.ipp), where I successfully implemented a heap priority queue:

https://github.com/MiamiOH-CSE274/07_Heap_Lab/blob/baileys2/Heap.ipp

References used: the online text

7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
Source of Evidence:

Below is a link to my branch of the Vise project in MiamiOH-CSE274, where we implemented an adjacency list data structure:

https://github.com/MiamiOH-CSE274/Vise/tree/ZirckleAndBailey

References used: Andrew Zirkle (project partner), the online text

7 - Implement graph algorithms
----
Source of Evidence:

Below is a link to my branch of the Vise project in MiamiOH-CSE274, where we implemented a depth-first search in the isConnected method of testApp.cpp:

https://github.com/MiamiOH-CSE274/Vise/tree/ZirckleAndBailey

This depth-first search did not function completely successfully, but I believe that most of the correct code is there and only minor errors are preventing it from functioning properly.

References used: Andrew Zirkle (project partner), the online text

21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

The three sources of evidence that I will be discussing in this section are the time and space requirements of a FIFO queue, a doulby-linked list, and a hash table.

1: Queue
Here is a link to the implemented queue being discussed: https://github.com/MiamiOH-CSE274/03_Queue_Lab/blob/baileys2/ArrayQueue.ipp
The main methods that will be discussed in this program all come from the ArrayQueue.ipp file, and consist of the add, remove, getNumItems, and grow methods. The add is almost always carried out in O(1) time, as the only operations that are performed in this method are to instantiate a variable that represents the location in the main array used for memory storage (called backingArray in this program) at which the new item will be added, to actually add the item in question to the recently determined location, and finally to update the number of items in the array (represented by the variable numItems) by increasing it by one.  All of these things take O(1) time, so the add method as a whole will usually take O(1) time. The only exception to this rule occurs when numItems is equal to the variable that represents the size of backingArray, called backingArraySize. This is checked at the beginning of the add method, and when this statement is true then the grow method is called. The grow method is run in O(n) time, with n being the number of items stored in the backingArray. When the grow method is called, the add method also has a run time of O(n) time because of this method call. The grow method is run in O(n) time because when it is called and run, a new array is created (called updatedArray) that is twice as large as the old backingArray (this new size is represented by a variable called updatedSize). In grow, all n items from the old backingArray must be copied over to updatedArray, which takes O(n) time. The front of the bakingArray is then updated to 0, the old backingArray is deleted in order to prevent memory leaks, and backingArray is set equal to updatedArray. The remove method, similar to the add method, takes O(1) time, as all of the actions is carries out take constant time. It begins by checking to see if there are any items already in backingArray, and if not it throws an error message telling the user that they must add at least one item to backingArray before trying to call remove. After this conditional statement has been satisfied, a variable (called itemToDelete) is instantiated to represent the item in backingArray that is located at the "front" of the list of items to be deleted (the variable front is used to keep track of this location in the array). Front is then set to be equal to one after the previous front location (or the first item in backingArray in the case that the previous front was the last item in backingArray), numItems is decremented by one, and itemToDelete is returned. All of these actions take constant time, which is why the remove method runs in O(1) time. Finally, the getNumItems method has a run time of O(1) time, as literally the only line of code in the method returns the value of the numItems variable.

2: Linked List
Here is a link to the implemented linked list being discussed: https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/blob/baileys2/LinkedList.ipp
The main methods that will be discussed in this program all come from the LinkedList.ipp file, and consist of 

3: Hash Table
Here is a link to the implemented hash table being discussed: https://github.com/MiamiOH-CSE274/05_Hashing_Lab/blob/baileys2/HashTable.ipp


* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

Below is a link to my 03_Queue_Lab, where I correctly used dynamic variables, including the destructor: 

https://github.com/MiamiOH-CSE274/03_Queue_Lab/blob/baileys2/ArrayQueue.ipp

This code not only uses dynamic variables correctly, but also does not leak any memory or suffer from any dangling pointers, out of bounds array access, or any other similar errors. There is no memory leakage because delete[] is used on the backingArray array in both the destructor and the grow() method to completely erase the old backingArray before a new one is created. This ensures that the pointer to the backingArray memory is not simply changed to a new location, as this would mean that the old information was still stored in memory but simply no longer being used by the program. This in turn would cause more and more memory leakage over time, and drastically reduce the run-time and overall functionality of the program. Luckily the destructor and grow() method handle this case very well and without memory leakage. Measures have also been taken in this program to ensure that no out of bounds or other similar errors occur.  For example, in the add() method there is a statement at the very beginning that calls the grow() method if the number of items in the array is equal to the size of the backing array. This makes sure that the queue will grow in size along with the number of items being stored and kept track of appropriately, and that the program will never try to add an item to the queue outside of its given memory space. Also, in the remove() method there is a statement at the beginning that checks to see how many items are currently in the queue. If there are no items and the remove method is called, an error will be thrown preventing the action from being carried out. This ensures that the program will not attempt to delete memory that is not there, which could lead to memory leakage or the deletion of other memory located outside of the queue. As can be seen from this explanation, the memory in this program has been managed very well, with correct usage of dynamic variables (including the destructor).

5 - Create collection classes using templates in C++
----

Below is a link to my 03_Queue_Lab, where I successfully implemented templates: 

https://github.com/MiamiOH-CSE274/03_Queue_Lab/blob/baileys2/ArrayQueue.ipp

The purpose of template classes in C++ is to essentially make code more reusable, as they are extremely useful when you have to perform tasks that are pretty much identical, but must be done with multiple types of variables. For example, in the queue that I implemented in the link above, a template class "T" was used. Obviously there is no acutal variable type "T", but rather this is simply used as a placeholder that tells the program that the type "T" will eventually be filled with an actual variable type. This type is determined when the data structure is constructed, and also when variables are passed back and forth between the various methods in the program. Using template classes simply allowed for more flexibility with what can be done with the code (as the queue could hold ints, doubles, chars, etc.) and makes it easier for the code to be adapted to a wider variety of possible use cases without having to write a whole new method for each desired variable type that performs the same exact action as the original. In the end, using template classes is a more efficient way to write code that makes things more streamlined and can be used in a much wider range of possibilities without haveing to rewrite anything.

30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.


Extra Credit
----
This is just a reminder that I attended the CSE Research Fair this fall semester and listened to talks about several different research topics, including augmented reality and computer security.