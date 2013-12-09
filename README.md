Portfolio
=========

Document completion of the course's learning outcomes.

Name: Garrett Emrick

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
My source of evidence is going to be my Queue Lab. By going to the link below, one can see I have done all required functions, and through feedback and my own personal code inspection, everything works as it should in the program.

* https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/emrickgj

7 - Create an implementation of a List
----
My source of evidence is going to be my LinkedList Lab which shows a proper use of a List, and has all the functions and requirements working as they should. 


* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/emrickgj


7 - Create an implementation of a Binary Search Tree
----
My source of evidence is going to be my Binary Search tree lab. In the lab, one can see I clearly implement a binary search tree, and all the functions work as they should!

* https://github.com/MiamiOH-CSE274/06_BST_Lab/tree/emrickgj


7 - Create an implementaiton of a Hash Table
----

An implementation of a Hash Table can be seen in my Zeitgeist project, as well as a hashing function that I think works very effectively. It shows that I am able to not only create hash functions that work somewhat well, but can also implement them in a data structure.


* https://github.com/MiamiOH_CSE274/Zeitgeist/tree/emrickgj


7 - Create an implementation of a Heap
----
Possible sources of evidence (do any one of these):

My source of evidence for implementation of a heap will be my heap lab! I correctly created a heap as described, and it works as it should! Because of this, and handling memory as appropriate so there are no leaks, I believe it is worth the full 7 points.

* https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/emrickgj

7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
I create an adjacency list in my Graph Lab! I create an array index for each node, and within each node one can easily see what nodes it points to, in a very fast and efficient matter! I believe this is an adequate source of evidence for an implementation of an adjacency list!

* https://github.com/MiamiOH_CSE274/08_Graph_Lab/tree/emrickgj

7 - Implement graph algorithms
----
One can see an implementation of my Graph algorithms in my Graph project, showing I have both an understanding of how they should work and how to implement them correctly.

* https://github.com/MiamiOH_CSE274/08_Graph_Lab/tree/emrickgj

21 - Determine space and time requirements of common data structure methods
-----

Looking at my Linked_List_Lab and Queue lab, I believe I have the space and time requirements of these common data structure methods. I also have the Heap Lab, which also takes into consideration the space and time requirements, and analyzes them as well. 

Each of them will detail on the best/worst of each data structure.


* https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/emrickgj
* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/emrickgj
* https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/emrickgj


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

Memory in C++ is handled much differently than memory in a language such as Java. In Java, all dynamic variables and are automatically handled by the garbage collector. Dynamic variables meaning any created variable using the "new" keyword, i.e. Object o = "new" Object(); 

When dynamic allocation happens, one needs to use the delete key to clear up that memory. If one forgets to release that memory, it is what is commonly known as a "memory leak". There is no way to fix it once it has already been done, which is why it is important to not forget to do it in your program,
and also make sure the delete key is happening. One location many classes that use dynamic allocation, such as our Linked_List_Lab, is the destructor which will allow one to free up all memory being held, before the class itself is released from memory. The Linked_List_Lab can clearly be seen using the 
destructor correctly.

The destructor looks similar to the constructor, which is used for initialization, but has a "~" in front of it. The key difference between this and the destructor, is that the destructor is called upon the objects deletion. Because this is called before the object is "deleted", is that it allows you to free
up any memory that was dynamically allocated within the object, such as member variables, so that memory leak is not an issue. 

It's also important to remember the equivalent for an array. For deleting an array that was dynamically allocated, one will use the "delete[]" instead of using "delete"!


* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/emrickgj

5 - Create collection classes using templates in C++
----

The following project show implementation of collection classes using templates in C++, showing that I understand the concept. They both work correctly, and both utilize templates effectively.


* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/emrickgj
* https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/emrickgj


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Vise:

For my Vise project, I decided to use a 1D array as my data structure to hold the board. Because I am using this 1D array, accessing, deleting, re-writing, all take O(1) time. There is not need to iterate or loop, if there is a specific space that you are looking for, it will always be extremely fast. 

The downsides of this data structure, is trying to find a cluster or group of points, and when trying to compare to all possible spaces on the board, as it will have to loop through all of them. However, since this board is only 20x20, I think this is rather insignificant since it is such a small number.

The other downside would be the increased mathmatical calculations on my part to get everything working as it should, specifically finding neighboring spaces, although it wasn't too difficult and I did figure it out (also makes getting neighbors constant time). 

As for space, it uses only the space necessary, and holds 1 integer for every space in the array. I could even shrink the usage down to a short, and maximize the efficiency of the space. Because I have no pointers, there is not space required for those as well, making this array just about as small as possible.

Because of the points mentioned above, I believe that this design choice was good for this project, and was a suitable datastructure to use. My Vise project is located at:

* https://github.com/MiamiOH-CSE274/Vise/tree/emrickgj 
* I can't push my code into the repo for some reason, so I'm giving a link to my local one as well
* https://github.com/emrickgarrett/Vise/tree/emrickgj


Zeitgeist:

For my Zeigeist project, I am using a combination of a Hashmap and a Linked List, using arrays. It will first generate a hash based on the word given, and then check for a collision, if there is a collision, it stores it in the next open slot of the collision array and stores that index in the data item located in the hashtable. Then every time a collision happens, it will update each of their next indexes appropriately so it can be found for retrieval later.

The upsides is that (essentially) add, remove, and get functions will at most take n-time, although it is arguably lower due to an efficient hash function. It's able to be this fast also because it can get the bucket it's supposed to be in, and then immediately get the next, next, and next collisions very quickly using indexes in the collision array, instead of using pointers to find the next one (utilizing the benefits of how arrays are stored and retrieved vs. Linked list). 

I also have it set up to only grow when appropriate, reducing the amount of space needed, and growing when needed. The slowest part of the process is the growing, although this is rare. The biggest downside is the complexity, and it resulted in the project not working essentially as it should.

I could have done other options, such as a hash table with "jump" methods for collisions, or a "cuckoo" hash table setup, but these result in having to search repeatedly for an item, and can cause more collisions to occur from non-related data items. Doing it this way, I can help reduce the amount of collisions, but when there are collisions, they are bunched together and are easily sorted through without affecting the other entries. Because of this, while I don't have mathmatical proof, I believe it will reduce the amount of collisions if the hash function is efficient, which I believe mine is.

The other reason for using this structure vs. a straight hash table or linked list, was the requirement for a sorted order of what are the most populated words in the documents. Using just a hash table wouldn't work, as it doesn't preserve any sort of order. Using a Linked List or plain array to find a word would make it very slow. Another option I thought of was a binary search tree, in which the worst case scenario would be O(logn) time if balanced correctly, but I believe this method is much faster as it uses both the benefits of the hash table, and linked list. As mentioned earlier, the worst case for finding, updating, removing, is O(n), but due to the hash table functioned it will in practice be much, much faster.

My project can be found at:

* https://github.com/MiamiOH-CSE274/Zeitgeist/tree/emrickgj 
