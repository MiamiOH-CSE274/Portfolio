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
https://github.com/ethan2014/03_Queue_Lab

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
because you just have to update the value pointed to by the iterator, without an iterator, you would need to call find() which is O(n), which would make set also O(n).
For both, size can be stored internally as an integer value, so size would be O(1).  In general, linked lists are a very good data structure if you can use an iterator,
because you already know which item to work with in each method, however, linked list iterators are not random access, so you can not arbitrarily jump to locations in the
linked list, you must continually increment/decrement the iterator (ex: `list_iterator++;`) to get to a position you want, but once you are there, anything can be done in
O(1) time
	
```
                      | array-based | linked list | linked list (iterator) |
find (by value)       | O(n)        | O(n)        | O(n)                   |
find (index/iterator) | O(1)        | O(n) (index)| O(1)                   |
set/get               | O(1)        | O(n)        | O(1)                   |
add/remove            | O(n)        | O(n)        | O(1)                   |
size                  | O(1)        | O(1)        | O(1)                   |
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
find       | O(1)      | O(log n)  |
set        | O(1)      | O(log n)  |
add/remove | O(1)      | O(log n)  |
size       | O(1)      | O(n)      |
min/max    | O(n)      | O(log n)  |
prev/next  | O(n)      | O(log n)  |
```

* Adjacency List vs. Adjacency Matrix

Both adjacency lists and maticies are used to represent the Graph abstract data type.  For an adjacency list, you store an array to represent each node, then
each node stores an array of the edges to the nodes it connects too.  And for a matrix, you store a 2D array of size O(V^2) where the values in the array are
booleans representing an edge (or edge weight can be stored, with 0 used to denote no edge) and a value at a row,column position indicates an edge between the
node at row and the node at column, so `array[0][1] = 1;` means there is a node (or node of weight 1, either way, there is a node) from node 0 to node 1.  Although
graphs dont support very many functions, these differences in the way data is stored produce large differences in time and space complexities.  If you want to know
if an edge exists between two nodes with a matrix, you simply have to look at that position in the 2D array and return the value there (`return array[node1][node2];`)
which takes O(1) time.  If you want to do the same with an adjacency list you must iterate over its array of edges to find one with a node destination that matches
the node you want, which means in the worst case it will take O(V) time, where V = the number of nodes in the graph.  This can obviously be very slow if your edge count
is very high for the node you are searching from which makes an adjacency matrix must faster for findng out if an edge exists between two arbitrary nodes.  Adding an edge
between two nodes looks a bit better for adjacency lists because all you have to do is add the edge to each of the nodes' edge arrays, which takes O(1) time, regardless
of V (node count) or E, because looking getting a node is done by looking at that position in the array that stores all the nodes, which again is O(1) time.  For
an adjacency matrix, adding an item is (no surprise) also O(1) time, because just like getting the weight of an edge, you just have to look up an item in the 2D
array by its row and column and set the value with `array[node1][node2] = 1;`; this also happens to be the same for remove with a matrix, but instead of setting
the value to 1 or a weight, you just set it to 0 or false with `array[node1][node2] = 0;`.  Removing an item with an adjacency list is a bit more work, and just like
getEdgeCost(), ends up being O(V) time; first, you have to find the second node in the first nodes list of edges and remove if you find it (you are done if you dont
find it), then look for the first node in the second nodes list of edges and remove it if you find it.  If you wish to add a node to the graph, you can do this in
O(1) time with an adjacency list because all you have to do is push a new node onto the array that stores the nodes, but to do this with a matrix requires O(n^2)
(the worst time complexity we've seen with a graph so far) because you have to increase the size of both arrays in the 2D array which requires copying the data
in the old array to the new one, which with two array of equal size n takes O(V^2) time.  One very usefull operation for a graph is the ability to get all the neighbours
of a node, which can be done in O(1) time with an adjacency list because all you have to do is return the list of edge connections for that specific node.  To get the
neighbours of a node with an adjacency matrix you have to iterator over the entire column for that node to get every possible edge from the node you are looking at,
which will always take O(V) time, because even if there are no neighbours, you still have to loop over the height of the matrix to check.  One of the other biggest
differences between adjacency lists and matrices is how much space they take, a list will only take O(V + E) space, where as a matrix will requires O(n^2) space,
so if you need to store a large amount of data (1 million nodes) an adjacency list will be the better option, because the matrix will take 1,000,000^2 space
to store that, which is 1,000,000,000,000 (1 Terabyte if each node took the smallest amount of memory physically possible!).

```
           | adjacency list | adjacency matrix 
edge exists| O(V)           | O(1)
add edge   | O(1)           | O(1)
remove edge| O(V)           | O(1)
add vertex | O(1)           | O(V^2)
neighbours | O(1)           | O(V)
space	   | O(V + E)       | O(V^2)

```

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

The Stack: A special part of RAM where local variables and objects are stored.  It stores informtion about the current function and where to return after the
function is done.  Any variable declared in a function (ie. `int a[5]`) will be put on the Stack and will be deleted automatically when the function returns.

The Heap: The part of memory where dynamically allocated memory is stored.  Accessing this memory requires asking the OS for memory with the `new` operator
(or `malloc()` in C) for example `int *a = new int[5]` will creat an array of 5 `int`'s on the Heap which will always exist until the program exits or it is
explicitly deleted by the program with the `delete[]` operator (or `delete` for singal variables such as `Object *a = new Object()`).  forgetting about Heap
memory is the most common way to cause memory leaks in a program, because any data an object created with `new` will still exist even after you are done with the object.

Address: the physical location of an object in RAM commonly represented as a hex number.  the address of an object can be found with the `&` operator, for
example: `int *p = &a` will create a variable `p` that stores the address of variable `a`.

Pointer: a special variable type in C and C++ for storing the address of another variable declared with the use of the `*` operator and dereferenced with
the same operator `*`.  `int *p` will create a variable `p` that will be used to store the address of an `int` and using `*p` will allow you to manipulate the value of the data it is pointing to.

```
int a = 10;
int *p = &a;
*p = 20;
```

after this code executes, the value of `a` will be `20`.

Memory Leak: when data that was dynamically allocated by a class persits after the class that created it is no longer being used.  it is most common when
someone creates an object in the constructor with `new` but doesnt `delete` it in the destructor.  It is harmful because you will have data you were once using
just sitting in RAM with no "owner" which can lead to a program using a very large amount of memory and in some cases can lead to very dangerous security holes.

Dangling pointer: After you `delete` dynamically allocated memory, the pointer that was pointing to that memory still points to the same address, but there is
no longer any usefull data there anymore, so that pointer needs to be reassigned before it can be used after a `delete`.

Destructor: A function in a C++ class that is automatically called when you are done with the object, it is used to free up any memory that was created by the
class thoughout its lifetime with the `new` operator by using the `delete` operator.  Java doesnt need them because Java has automatic Garbage Collection,
meaning that any data that isnt being used any more will eventually be freed by the JVM for later use.

5 - Create collection classes using templates in C++
----

* What is the main benefit of using templates when creating collection classes?

Using templates means you can write one class that can handle any kind of data the user wants to use with your collection class, whether it be `int`, `double`, `std::string`,
`std::vector`, or even there own classes.  when you use a template, the compiler will create a new specialized version of your class to handle each different type of data
the user wants to use, so if you use a `std::vector<int>` and a `std::vector<std::string>` the compiler will create a `std::vector` class that only handles `int`s and another one
that only handles `std::string`s.  using templates allows you to very easily abstract away the difficult problem of handling the many different types of data a person might want
to use with your collection class.  For example, in the olden days before templates and generic programming, if you wanted a hashtable that stored keys as a `char*` and values as a `double`, but all
you had was one that stored keys as a `char*` and values as an `int`, then you were writing an entirely new structure to handle your new case (or creating some ugly abomination
of preprocessor hacks that 'works', which ever you prefer).  Templates allow for truly generic and reusable code, if done correctly, your collection class will no absolutely nothing
about the data it will even be working with before you compile it!

* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

You can't create template classes in the conventional c++ style of seperate .hpp and .cpp files because when you use templates, the compiler will create a new version
of your class to handle the data types you use with it throughout the program, which means different functions declerations and definitions for each case.  if the implementation
of the class was in a seperate .cpp file, when the compiler went to create a new class (for example, one that handles `MyClass<int>`) it wouldn't know where to find the implementation
for those new functions, because the .cpp file may have already been compiled and it can't add new things to the file and compile it again.  So you include the implementation in the
.hpp file so whenever the user of your code `#include`s your header file, all of the templated implementations of your functions will be included in the users source file, so it will
know where to find them when new code needs to be generated, then the entire file will be compiled along with all the implementations of each version of your template class that are needed.

20 - Using time and space analysis, justify the selection of a data structure for a given application
----

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)

If I wanted to store strings in an unordered set, I would actually do what most compilers do for the implementation of the c++ standard template library class
std::unordered_set.  in the std::unordered_set class, elements are stored using a hashtable, where the key of an item is found by passing the string through
a hash function then calculating its position from the hash, and the values associated with every key is the actual string itself.  I believe this is the best way
to store an unordered set of strings (not just because thats how the c++ STL does it) because the most important functions of this use case, add, remove and key_exists
can all be done in O(1) time with a hashtable.  key_exists is O(1) because all you have to do is caculate a keys position in the hashtable using the hash function,
as well as handle collisions whenever needed, which takes O(1) (unless you have a terrible hash function that produces the same result for many different inputs).  because
key_exists is so fast, checking if we actually are supposed to add a value when add_item is called can also be done in o(1) time, because you just have to check if the string
the user wants to add already exists, and if it does, dont add it.  remove_item is also O(1) for the same reasons find and add_item are, all you have to do is hash the input
string, and if there is something in that position with a matching key, you simply remove it, both of which can be done in constant time.  Because add, remove and find are all O(1)
time, a hashtable is definitely the best solution for this problem, because some of the short comings of hashtables such as find by value (although that would be easy in this
specific use case because the values are the keys), finding max and min values, and finding the next and prev keys of a given key because none of that functionality is
needed to store a simple unordered set of strings.

* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

When I make a list for the grocerty store, I dont list item in any kind of order, I just write down items as I realise that I need them, I also dont get the items at the store
in any particular order, I just walk down every isle and get items off my list that are in that isle.  Because of this, the only features I would need out of a data structure
would be adding items to the end of the list and finding and removing items at arbitrary positions in the list.  If I was at the store and has already bought a few item then realised
I needed something else, I would just write that new item at the bottom of the list, so I don't need to be able to insert item into the list.  Because of these two requirements I believe
the best data structure to use would be a doubly linked list.  The main reason for this is that you can add an item to the end of a doubly linked list in O(1) time because you obviously
dont need to iterate over every item in the list to find whats at the end, its just the node to the left of the root.  And a doubly linked list would keep everything in the same order that
I added it, unlike say a hashtable or a heap that would move things to different positions.  The other benefit of a doubly linked list is that once you know which item you want to remove
from the list, you can do so in O(1) time, although finding that item takes O(n) time.  Since I would be removing items as I am getting them at the store, the time it takes to find and remove
each additional item will take less and less time as `n` goes to 0, and because my grocerty lists never contain more than say 10-15 items, the time it takes to find an item would not even
be noticeable on a modern computer.  I am also assuming that I would actually be using a computer to implement this data structure, if this was being done with a pencil and paper a doubly linked
list wouldn't really make sense, because humans dont need to store "links" on the paper to the next and previous item.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

To store every students' records, searchable by their banner number, I would use a hashtable with there banner number as the key, and a custom `StudentRecord` class as the value
associated with each key.  I believe this is the best solution to this problem because the most important function of a data structure in this case would be the ability to quickly
find a students record by their banner number, for example `StudentRecord student = students.find(banner_number);`.  Because of this, a hashtable is the best option because you can
find a value by its key in a hashtable in O(1) time, a feature that almost no other data structure has, at best you can do that in O(log n) time with a BST.  Besides finding a students
record by their banner number, the other most important requirements of this problem are adding a new student or removing an old one (assuming Miami doesnt keep old student records, I'm
not sure if they do).  Adding a new student with a given banner number is a trivial task for a hashtable, because every student is guaranteed to have a unique banner number, so collisions
in the hashtable would be very minimal as they would only arise due to the size constraints on the backing array of the table itself.  With this in mind, we know that adding a new student would
take O(1) time.  Removing a student would be the same as adding one, except instead of adding a students record to that spot in the hashtable, you simple remove it which will always take O(1) time.
I believe these three functions, finding, adding and removing are the only ones that are really important for this situation because there isnt really a reason you would need to find the min or max banner
number or find the next/prev banner number from another students', so you can eliminate the 4 functions that hashtable performs poorly at.  There is no other data structure that allows you to
find a value by its key and add/remove new entries all in constant time.

* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

For this problem, I am assuming that a company can have more than 1 packet waiting at a time and different companies can pay the same amount for their packets, so duplicate keys would
be necessary to solve this problem.   So, to solve this problem I would use a max-heap that allows for duplicate keys to store each packet with the amount the company paid as its key.
This is the best solution to this problem because all you would have to do to get the current packet that needs to be sent (the one that paid the most money) all you would have to do
is get the item from the top of the heap, which takes O(1) time if you are simply getting its value, but O(log n) time if you are removing it.  A max heap would work for this because
lets say you have 3 different companies, X, Y and Z; first, you add a packet from company X which paid $10, since this is the only item in the heap, it would be at the top, then you add
company Y which paid $20, because of the heap rule this item will be "bubbled" up to the top item in the heap because 20 > 10, and finally you add company Z which also paid $10 so it would
stay at the same level as company X.  In this case, when company Y's packet was sent out because it has the highest priority, company Z's packet will be moved up to the top of the heap because
it was to the right of the top item.  The only other function that would be necessary for this problem would be adding new item to the heap which is guaranteed to be O(log n) time.  This is a very
simple application that needs to be made, all you have to be able to do is add new packets to the queue and get the one that has the highest priority, so none of the other functions of most
abstract data types such as remove, find by key, find by value, min/max or next/prev would ever need to be used.  Using a max-heap is the only data structure that allows us to keep the packets in
the order we need and allow removing and adding to always be in O(log n) time, anything else like a hashtable  or just a plain old array would have to be manually sorted every time a packet was
added which the heap does for us automatically.