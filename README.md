Portfolio
=========
Document completion of the course's learning outcomes.

Instructions
====
The goal of this is to make it very easy for me (or an employer, or a 

teaching assistant) to see whether or not you have mastered the material of 

the class. The hope is that I would be able to grade your work without 

downloading and compiling your code. For labs, I can grade them by inspecting 

the code. For projects you must provide a video demonstrations of your 

programs. Some questions require essay responses.

Important
=========
If you prefer, you may turn this in to me via email, instead of hosting it on 

GitHub. Please talk to me about it during office hours or before or after 

class.

Body of portfolio
====

7 - Create an implementation of a Queue
----
https://github.com/aryelle-player/03_Queue_Lab

7 - Create an implementation of a List
----
https://github.com/aryelle-player/04_Linked_List_Lab

7 - Create an implementation of a Binary Search Tree
----
https://github.com/aryelle-player/06_BST_Lab

7 - Create an implementation of a Hash Table
----
https://github.com/aryelle-player/05_Hashing_Lab

7 - Create an implementation of a Heap
----
https://github.com/aryelle-player/07_Heap_Lab

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/aryelle-player/08_Graph_Lab

7 - Implement graph algorithms
----
https://github.com/aryelle-player/08_Graph_Lab

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay 

comparing and contrasting them in terms of their running times for different 

operations. (7 points each)

* Array-based list vs. Linked List
	Array-based lists tend to run in constant time for all operations 

except add() and remove(). Add() and remove() for an array-based list run in 

linear time. tHe reason for this is because array-based lists offer constant 

time access to any value in an array but array-based lists aren't terribly 

dynamic therefore adding and removing elemetns require the array to be 

shifted. Linked lists that are singly-linked are the complete opposite of 

array-based lists in terms of running time for operations. For doubly-linked 

lists, instead of linear time, these lists take O(1+min{i,n-1}) time fr add

(), remove(), get(), and set().
			arraylist	linkedlist
add				o(n)	o(1)
get(given index)		o(1)	o(n)
set				o(1)	o(1)
get				o(1)	o(1)
remove				o(n)	o(1)
get(front or back)		o(1)	o(1)
add/remove(front or back)	o(1)	o(1)


* Binary Search Tree vs. Hash Table

			Hash Table	Binary Search Tree
add(key, val)			O(1)	O(lgn)
remove(key)			O(1)	O(lgn)
get/set(key)			O(1)	O(lgn)
min/max				O(n)	O(lgn)
next(key)/prev(key)		O(n)	O(lgn)


* Adjacency List vs. Adjacency Matrix

		Adjancency Matrix	Adjacency Lists
addEdge()			Θ(1)	Θ(d)
getWeight()			Θ(1)	Θ(n) or Θ(d)
removeEdge()			Θ(1)	Θ(d)
space()				Θ(n2)	Θ(n+m)
getNeighbors()			Θ(n)	Θ(1)


5 - Describe memory management in C++, and correctly use dynamic variables, 

including destructors
----
TODO: Define/describe each of the following terms, as they apply to memory 

management in C++

* The call stack (not to be confused with the stack data structure!)
	The call stack is the space in memory that has been allotted for use.
* The heap (not to be confused with the heap data structure!)
	The heap is the end of the call stack.
* Address
	The address of an object is the place where it is in memory, 

basically just where an object lives in memory, usually given by some random 

mix of letters, numbers, and other characters. the address can be accessed by 

use of a pointer.
 
* Pointer
	 A pointer is an object that points to another object. A pointer is 

an object that points to a space in memory or rather holds the address of the 

object. When a pointer is dereferenced, the actual object is accessed.


TODO: Answer the following questions about memory management and dynamic 

variables

* What is a memory leak, and why is it bad?
	Memory leak is allowing memory to still be used once a programs 

runtime is through. This is bad because it can allow someone to access 

something in memory even after the program has stopped running. (the reasons 

hackers can obtain things they shouldn't have)

* What is a dangling pointer (or dangling reference), and why is it 

dangerous?
	A dangling pointer is a pointer that points to a space in memory 

which no longer has an object in it. This is bad because this can cause 

variables to be changed unintentionally or memory to run out faster.

* What is a destructor, and why are they necessary (in C++) to prevent memory 

leaks? Why *aren't* they necessary in Java?
	A destructor is a method, opposite of a constructor, that destroys 

every object that is created during runtime. This prevents memory leak 

because there is now no way to access something in memory after runtime 

because the memory is no longer accessible. This is unnecessary in Java 

because Java's garbage collector does all of this work by constantly checking 

for live variables and getting rid of dead ones.

5 - Create collection classes using templates in C++
----
TODO: Answer the following questions about templates in C++


20 - Using time and space analysis, justify the selection of a data structure 

for a given application
----
TODO: Answer the following questions about choosing data structures. (5 

points each)

* If I needed a data structure to store a set of strings, which data 

structure (or data structures) that we learned this semester would be most 

appropriate? Carefully explain why. (Remember that a set doesn't have any 

order, and doesn't store duplicates. We can add items, remove items, and 

check to see if an item is already in the set.)
* If I needed a data structure to store a grocery list, which data structure 

(or data structures) that we learned this semester would be most appropriate? 

Carefully explain why.
* If I needed a data structure to store student records so that I could look 

students up by Banner number, which data structure (or data structures) that 

we learned this semester would be most appropriate? Carefully explain why.
* Imagine that I'm implementing a network router. It needs to keep a queue of 

packets waiting to be sent out over the network, but this queue need a 

special ability: Different companies are going to pay me different amounts of 

money, and the packets from the highest paying company should be sent out 

first. That is, if company X paid 20 and company Y paid 10, then X's packets 

always get sent before Y's packets. Y only gets to send packets if X doesn't 

have any waiting. Which data structure (or data structures) that we learned 

this semester would be most appropriate? Carefully explain why.
