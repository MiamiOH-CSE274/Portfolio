Author
==========
"Zhong, Mingwei", zhongm2
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

* https://github.com/MiamiOH-CSE274/03_Queue_Lab
* Use a queue as your data structure in https://github.com/MiamiOH-CSE274/Shuffle
* Consult with Dr. Brinkman on an alternative project

Here is a link to my repository on github, it includes my source code:

https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/zhongm2

Shuffle project:

https://github.com/JohnneyMing/Shuffle/tree/zhongm2



7 - Create an implementation of a List
----
Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab
* Use a linked list as your data structure in https://github.com/MiamiOH-CSE274/Shuffle
* Implement chaining instead of linear probing in https://github.com/MiamiOH-CSE274/05_Hashing_Lab
* Consult with Dr. Brinkman on an alternative project


Here is a linke to my repository on github, it includes my source code:

https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/zhongm2



7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

* Binary Search Tree Lab (TODO)
* Use a binary search tree or KD-Tree in the Starbucks project.
* Use a binary search tree in the Zeitgeist project
* Consult with Dr. Brinkman on an alternative project


7 - Create an implementaiton of a Hash Table
----
Possible sources of evidence (do any one of these):

* https://github.com/MiamiOH-CSE274/05_Hashing_Lab
* Use a hash table in the Zeitgeist project
* Use locality-preserving hashing on the Starbucks project (not recommended!)
* Consult with Dr. Brinkman on an alternative project

7 - Create an implementation of a Heap
----
Possible sources of evidence (do any one of these):

* Heap lab (TODO)
* Implement heap sort in the Sorting lab (TODO)
* Implement a heap as part of the Graph Algorithms lab (TODO)
* Implement a heap as part of the Graph Project (TODO)
* Consult with Dr. Brinkman on an alternative project

7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
Possible sources of evidence (do any one of these):

* Graph lab
* Graph Algorithms lab
* Graph project
* Consult with Dr. Brinkman on an alternative project

7 - Implement graph algorithms
----
Possible sources of evidence (do any one of these):

* Graph lab
* Graph Algorithms lab
* Graph project
* Consult with Dr. Brinkman on an alternative project

21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)

Queue: 
Remove() method:

1.Create an return variable: T rm. (n = 1)

2.Check if array has elements in it. (n = 1)

3.If it doesn't, throw an exception. (n = 1 or n = 0).

4.Set the return variable as backingArray[front]. (n = 1).

5.Increase the first index of array as one by doing:

front = ( ( front + 1) % backingArraySize)). (n = 1)

6.Decrease the number of element in array as one. ( n = 1)

7.Return.(n = 1).

Therefore: the remove() method takes constant time O(1).


grow() method:

1.Creating integer variable: int count = 0;(N = 1).

2.Creating an new array, size twice larger than original array.

T *newArray = new T[2 * backingArraySize]. (N = 1).

3.Do a while loop to loop through the entire array and copy elements from
original array to new array: while(count < numItems).
Assume the number of element in array is n. (N = n - 1 + n - 1 = 2n-2).

4.backingArraySize = 2 * backingArraySize. (N = 1)

5.Deallocate the memory: delete[]backingArray. (N = 1).

6.Set backingArray to be NULL: backingArray = NULL (N = 1).

7.backingArray = newArray. (N = 1)

Therefore: T(n) = 1 + 1 + 2n-2 + 1 + 1 + 1 = 2n + 3.
Which is O(n).


add() method:

If array is not full, then it takes O(1). Otherwise it takes O(n), because 
you need to call grow() method if the array is full.

getNumItems() method:

It takes O(1) time because it simply just return number of element in array.


Summary:

I implemented Queue by using circular array, program runs successfully, memory
has been managed appropriately.


/*****************************************/


Linked list:

add() method:

It takes O(1) time. Because creating a new memory block for storing the element
which you want to add on the list and switch pointer take constant time.
So the running time of this method is O(1).

remove() method:

It is same as add() method, O(1).

find() method:

It takes O(n) time, because it needs to make a loop to find the
memory address of element in array, and return that memory address.

get() method:

It takes O(n) time, because it involved find() method, and then return the
data in that memory address.

set() method:

It takes O(n) time because it also involved find() method, and then set the 
data in that memory address.

size() method:

It takes O(1) time because it returned the number of element in array.


Summary: 
The prorgam runs successfully, memory has been managed appropriately.


If you want to find out more details, click the links below:


Queue: 

https://github.com/JohnneyMing/03_Queue_Lab/tree/patch-1

List:

https://github.com/JohnneyMing/04_Linked_List_Lab/tree/zhongm2







5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.


Queue lab:

https://github.com/MiamiOH-CSE274/03_Queue_Lab/blob/zhongm2/ArrayQueue.ipp

In my constructor, I allocated memory on line 26.

In my destructor, I deallocated the memory and set it to be NULL.

Summary:

My program does not leak meemory, and does not suffer from dangling pointers.




5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.

For instance, in my Queue lab:

https://github.com/MiamiOH-CSE274/03_Queue_Lab/blob/zhongm2/Queue.h

Using template to mimic an intreface in C++.



30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):



* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.


Queue Lab:


1.We could use regular array instead of using circular-array, you could make 
the array big enough in order to avoid using grow() when your array is full.
Because grow() method will lower your program's running time. However, if the numbre of data you need to add to the array is gigantic, it is possible to run out of your RAM. But if you use circular array, this situation will not happen.

2.We also could use linked-list to implement Queue. But it still has some 
disvantages. For instance, if you implement add() method by using linked-list, 
it means you need to keep adding elements at the end of linked-list. As the elements get larger, the longer will become longer.  But using circular-array, you 
could avoid this condition.


