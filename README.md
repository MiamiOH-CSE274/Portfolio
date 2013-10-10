Author
==========
"Emrick, Garrett", emrickgj
Portfolio
=========

Document completion of the course's learning outcomes.

Name: Garrett Emrick

I'm not entirely sure what state the portfolio is supposed to be in, or what all is supposed to be done, so I hope what I have is sufficient.

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

* https://github.com/emrickgarrett/03_Queue_Lab

7 - Create an implementation of a List
----
My source of evidence is going to be my LinkedList Lab, as well as an implementation of it in my Zeitgeist project to keep track of the top words in the documents. This may change in the future, based on how the cache actually works. If it still runs efficiently while adding/getting indexes from the array without using the LinkedList part, then this will stay. Based on the performance, I may use an alternative method I further describe in the Portfolio project to hopefully speed up the program dramatically.


* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab


7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

* Binary Search Tree Lab (TODO)
* Use a binary search tree or KD-Tree in the Starbucks project.
* Use a binary search tree in the Zeitgeist project
* Consult with Dr. Brinkman on an alternative project


7 - Create an implementaiton of a Hash Table
----

I plan on implementing the hash table as part of my Zeitgeist project, and may end up doing the Hashing Lab as well. I am working on it tonight, sometime this weekend, and next weekend as well. More information can be found in my Zeitgiest repository.


* https://github.com/emrickgarrett/Zeitgeist


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

Looking at my Linked_List_Lab and Queue lab, I believe I have the space and time requirements of these common data structure methods, although I'm not sure. If this is incorrect, I'd like to know or if I need to go into more detail.


* https://github.com/emrickgarrett/03_Queue_Lab
* https://github.com/emrickgarrett/04_Linked_List_Lab
* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----

Memory in C++ is handled much differently than memory in a language such as Java. In Java, all dynamic variables and are automatically handled by the garbage collector. Dynamic variables meaning any created variable using the "new" keyword, i.e. Object o = "new" Object(); 

When dynamic allocation happens, one needs to use the delete key to clear up that memory. If one forgets to release that memory, it is what is commonly known as a "memory leak". There is no way to fix it once it has already been done, which is why it is important to not forget to do it in your program,
and also make sure the delete key is happening. One location many classes that use dynamic allocation, such as our Linked_List_Lab, is the destructor which will allow one to free up all memory being held, before the class itself is released from memory. The Linked_List_Lab can clearly be seen using the 
destructor correctly, and makes use of the destructor.

Possible sources of evidence (do one):

* https://github.com/emrickgarrett/04_Linked_List_Lab


5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

I'm not entirely sure what an interesting implementation exactly is, as it's kind of vague, but the two projects I have done so far use templates. Not sure if the Linked_List and Queue labs count here or not though.

* Any of the labs or projects, provided it uses templates in an interesting way.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

I plan on using this to go over two different projects that have different problems, with comparison to help justify the selection of the data structures and why a certain data structure is better for either situation. The first one I plan on using is the Zeitgeist, the other will be a future project.

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.
