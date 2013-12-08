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
My source of evidence is going to be my LinkedList Lab, as well as an implementation of it in my Zeitgeist project to keep track of the top words in the documents. This may change in the future, based on how the cache actually works. If it still runs efficiently while adding/getting indexes from the array without using the LinkedList part, then this will stay. Based on the performance, I may use an alternative method I further describe in the Portfolio project to hopefully speed up the program dramatically.


* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/emrickgj


7 - Create an implementation of a Binary Search Tree
----
My source of evidence is going to be my Binary Search tree lab. In the lab, one can see I clearly implement a binary search tree, and all the functions work as they should!

* https://github.com/MiamiOH-CSE274/06_BST_Lab/tree/emrickgj


7 - Create an implementaiton of a Hash Table
----

I plan on implementing the hash table as part of my Zeitgeist project, and may end up doing the Hashing Lab as well. I am working on it tonight, sometime this weekend, and next weekend as well. More information can be found in my Zeitgiest repository.


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
One can see an implementation of my Graph algorithms in my Graph project. 

* https://github.com/MiamiOH_CSE274/08_Graph_Lab/tree/emrickgj

21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

Looking at my Linked_List_Lab and Queue lab, I believe I have the space and time requirements of these common data structure methods. I also have the Heap Lab, which also takes into consideration the space and time requirements, and analyzes them as well. 


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

Possible sources of evidence (do one):

* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/emrickgj

5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

I'm not entirely sure what an interesting implementation exactly is, as it's kind of vague, but the two projects I have done so far use templates. Not sure if the Linked_List and Queue labs count here or not though.

* Any of the labs or projects, provided it uses templates in an interesting way.
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


Zeitgeist
