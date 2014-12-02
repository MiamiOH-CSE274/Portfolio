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
https://github.com/MiamiOH-CSE274/03_Queue_Lab

7 - Create an implementation of a List
----
https://github.com/ethan2014/04_Linked_List_Lab

7 - Create an implementation of a Binary Search Tree
----
https://github.com/ethan2014/06_BST_Lab

7 - Create an implementation of a Hash Table
----
https://github.com/ethan2014/05_Hashing_Lab

7 - Create an implementation of a Heap
----
https://github.com/ethan2014/07_Heap_Lab

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/ethan2014/08_Graph_Lab

7 - Implement graph algorithms
----
https://github.com/ethan2014/08_Graph_Lab

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List

Array-based lists and Linked Lists are both used to store data in a linear fashion.  The main difference between the two is that the elements in an Array-based list
are stored next to each other in continuous chunks of memory, while Linked list elements are not stored next to each other in memory, they are stored all
throughout memory.  Because of this, finding a random element in an array-based list (such as element 135) can be done in O(1) time because element 135 is 135
'spaces' in memory away from the first element, so its similar to doing `*(array + 135) = 10;`.  To find that same element number in a linked list, you have to
iterate through each element in the list until you are at element number 135, which takes O(k) time, with O(n) in the worst case.  So for accessing a random value
array-based lists are much faster than linked lists because there running times are O(1) and O(n) respectively.  To add an element into an array-based list,
you can easily find where it goes (with find() being O(1)) but adding that element to the space requires you to move every element to its right by 1 space, which
takes O(n) time, because the elements in an array-based list must be kept in continuous slots in memory.  Adding an item to a linked list, assuming you are using
an iterator to point to the location you need, can be done in O(1) time because all you have to do is change the pointers of the items to the left and right of
the node you are trying to insert.  Removing an item is the same running time as adding an item for both lists, so when it comes to adding/removing, a linked list
beats array-based lists with running times of O(1) vs O(n).  If you are setting the value of an item that already exists, array-based lists can do this in O(1) time
because you just have to use find (O(1)) to get the item you want to change and update its value; with an iterator, linked lists can also do set in O(1) time
because you just have to update the value pointed to by the iterator, without an iterator, you would need to call find() which is O(n), which would make set also O(n).  For both, size can be stored internally as an integer value, so size would be O(1)
	
```
| array-based | linked list | linked list (iterator) |
| O(1)        | O(n)        | O(1)                   |	find
| O(1)        |	O(n)        | O(1)                   |	set
| O(n)        |	O(n)        | O(1)                   |	add/remove
| O(1)        |	O(1)        | O(1)                   |	size
```

* Binary Search Tree vs. Hash Table

Both a hashtable and a binary search tree are used to store key, value pairs, the way they store them and how they are used within the data structure is what
differentiates them.  To find an item by its key in a hashtable, you hash the key, calculate an index based on the hash, then (assuming there are no conflicts)
that location is where the value is in the hashtable, so find takes O(1) time.  To do the same thing in a BST tree, you have to (obviously) do a binary search
with the key until you find an item with a matching key, so find for a BST takes O(log n) time.  This makes a hashtable faster for finding a random value by its
key than a BST with running times of O(1) vs O(log n).  Because find is O(1) in a hashtable, add/remove is also O(1) time, because you simply have to call find
with the given key to add or remove and delete that item from the table or add it to the empty space.  Add for a BST takes O(log n) time, because you have to
binary search for the empty position (or key that already exists) in the tree to add that value there (or update an existing value) which again takes O(log n).
remove in a BST is very similar to add in that it also takes O(log n) time, but there are a few other steps that have to be taken, because removing an item
from the middle of a list is different than adding an item to the middle because you simply update the value if you want to add a key that already exists.
If you want to find the max/min values in a BST, you can do this in O(log n) time because you just keep looking left or right until you find the last item, but
a hashtable requires you to iterate over the entire list to find the max or min, because a hashtable is not sorted at all, so it takes O(n) time.  Similar to
max/min, finding the next/prev item in a BST can also be done in O(log n) time, and just like with max/min for a hashtable, next/prev requires you to iterate
over the entire table to find the next or prev key to the one given, so it takes O(n) time.  Size is one of the places that hashtable beats BST, because a simple
counter can be stored internally for the size of the hashtable, which would take O(1) time to return, where as a BST has to count every item in the tree to get
the size of it, which takes O(n) time (this is one of the few methods in a BST that takes O(n) time).  The primary advantage of a BST is that elements are
automtically stored in a sorted order by their key, whereas a hashtable stores them in random order.

```
| hashtable | BST 
| O(1)      | O(log n)  |	find
| O(1)      | O(log n)  |	set
| O(1)      | O(log n)  |	add/remove
| O(1)      | O(n)      |	size
| O(n)      | O(log n)  |	min/max
| O(n)      | O(log n)  |	prev/next
```

* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

The Stack: A special part of RAM where local variables and objects are stored.  It stores informtion about the current function and where to return after the function is done.  Any variable declared in a function (ie. `int a[5]`) will be put on the Stack and will be deleted automatically when the function returns.

The Heap: The part of memory where dynamically allocated memory is stored.  Accessing this memory requires asking the OS for memory with the `new` operator (or `malloc()` in C) for example `int *a = new int[5]` will creat an array of 5 `int`'s on the Heap which will always exist until the program exits or it is explicitly deleted by the program with the `delete[]` operator (or `delete` for singal variables such as `Object *a = new Object()`).  forgetting about Heap memory is the most common way to cause memory leaks in a program, because any data an object created with `new` will still exist even after you are done with the object.

Address: the physical location of an object in RAM commonly represented as a hex number.  the address of an object can be found with the `&` operator, for example: `int *p = &a` will create a variable `p` that stores the address of variable `a`.

Pointer: a special variable type in C and C++ for storing the address of another variable declared with the use of the `*` operator and dereferenced with the same operator `*`.  `int *p` will create a variable `p` that will be used to store the address of an `int` and using `*p` will allow you to manipulate the value of the data it is pointing to.

```
int a = 10;
int *p = &a;
*p = 20;
```

after this code executes, the value of `a` will be `20`.

Memory Leak: when data that was dynamically allocated by a class persits after the class that created it is no longer being used.  it is most common when someone creates an object in the constructor with `new` but doesnt `delete` it in the destructor.  It is harmful because you will have data you were once using just sitting in RAM with no "owner" which can lead to a program using a very large amount of memory and in some cases can lead to very dangerous security holes.

Dangling pointer: After you `delete` dynamically allocated memory, the pointer that was pointing to that memory still points to the same address, but there is no longer any usefull data there anymore, so that pointer needs to be reassigned before it can be used after a `delete`.

Destructor: A function in a C++ class that is automatically called when you are done with the object, it is used to free up any memory that was created by the class thoughout its lifetime with the `new` operator by using the `delete` operator.  Java doesnt need them because Java has automatic Garbage Collection, meaning that any data that isnt being used any more will eventually be freed by the JVM for later use.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++


*What is the main benefit of using templates when creating collection classes?
*In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.


20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

For a grocery list I would use a Doubly Linked list.  I made this decision because using a doubly linked list allows you to easily add and remove items anywhere in the list, for example, if you realised after writing your list that you didn't need a certain item anymore, removing that item from the list would be doable in O(1) time.  Similarly, if you forgot to write an item down after creating the list, you can easily insert that list anywhere in the list again in O(1) time.  Being able to easily remove an item would also be very helpful because after you have gotten the item while at the store, you can simply remove that item from the list.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.
