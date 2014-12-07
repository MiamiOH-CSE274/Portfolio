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
https://github.com/laufengd/03_Queue_Lab/blob/master/ArrayQueue.h

7 - Create an implementation of a List
----
https://github.com/laufengd/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
TODO: Provide a link to your completed 06_BST_Lab OR ClosestStarbucks project (only if you used a search tree)

7 - Create an implementation of a Hash Table
----
https://github.com/laufengd/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
https://github.com/laufengd/07_Heap_Lab

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/laufengd/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
https://github.com/laufengd/08_Graph_Lab/blob/master/Graph.cpp

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List

In an Array-Based list, add() and remove() take O(n) operational time because the items in the list need to be shifted in order for more items to be added.
Array-Based size(1), get(1) and set(1) run in 0(1) time. For Linked lists, getNode(i) takes O(1+ min{i, n-i}) time, other than that all the other
functions run in O(1) time.

* Binary Search Tree vs. Hash Table
* Adjacency List vs. Adjacency Matrix

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory management in C++

* Call Stack: A Stack data structure on the computer's RAM that is used to store parameters and local variables for the subroutines of an active program.
* heap: A data structure on the RAM used for storing dynamically allocated variables
* Address: A location on the RAM where data is stored denoted by a number and can be referenced or pointed to.
* Pointer: A variable that points to an Address on the RAM

TODO: Answer the following questions about memory management and dynamic variables

* A memory leak is when data stored on the RAM can no longer be accessed and therefore takes up unnesesary space
* A dangling pointer is a pointer that references an address of an invalid data type and often times is the result of when data in a address is deleted or deallocated without deleting the pointer.
These are dangerous because often times other data can fill into the address being pointed to and cause the code to break.
* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java? Destructors deallocate memory and delete dangling pointers.
Java does not need destructors as much because the java compiler is very good and figuring out when something is no longer in use and getting rid of it automatically.

5 - Create collection classes using templates in C++
----
(Answers found on a Microsoft Developer Network Page:  http://msdn.microsoft.com/en-us/library/z3f89ch8.aspx)
The main benefit of using Template collection classes is that it is an efficient way of abstracting functions and variables with flexibility on what data type is used as parameters.
When someone instantiates a template-class in another file, compiler will create separate versions of the function for the data-type specified by the user when instantiated.(See example below)

(Answer found on stack overflow: http://stackoverflow.com/questions/495021/why-can-templates-only-be-implemented-in-the-header-file)
When instantiating a template, the compiler creates a new class with the given template argument. For example if a template class foo uses a template <typename T>,
and somewhere in a .cpp file foo<int> is instantiated, then a new class is created and every T parameter used in the template class will be compiled as an integer in the new class.
As a result, the compiler needs all functions to be defined in order to create this new foo<int> class; if these function definitions were not in the header then the compiler could not
access them.

//taken from a stackoverflow comment
template<typename T>
struct Foo
{
    T bar;
    void doSomething(T param) {/* do stuff using T */}
};

// somewhere in a .cpp
Foo<int> f; 
//compiler creates new class equivalent to this
struct FooInt
{
    int bar;
    void doSomething(int param) {/* do stuff using int */}
}

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)

If I were to create a data structure to store a set of unordered strings I would undoubtedly implement a hash table because after putting the string through a hash function; adding, finding, removing and 
checking if a string exists would run in constant time. However, if the set were to have some kind of order such as by most searches or occurrences(Zeitgeist project), I would probably implement 
an array instead of, or in addition to, my hash table. That way, the retrieval of a string based on its order would run in constant time; whereas if I were to solely implement a hash table, it would take O(n) time.

* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

If I were to implement a data structure for a grocery list I would probably used a Linked list. Linked lists allow for more convenient adding and removing of items in between one another which is optimal
for when I think of things I want to add or remove at different times.If I were to use an Array-Based list, I would have to grow() the list if I added too many items, which would usually mean doubling
the size of my list. I would not want to carry an abnormally large list around the supermarket if I wasn't going to use all of the space on it.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.




* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.










