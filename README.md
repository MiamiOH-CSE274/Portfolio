Author
==========
"Stilgenbauer, Kendall", stilgeki
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
This is my implementation of an Array Queue.  All the logic seems sound to me, but it doesn't run properly.  I am still awaiting feedback on this lab, which will hopefully help me figure out my problem.

https://github.com/stilgeki/03_Queue_Lab/tree/stilgeki


7 - Create an implementation of a List
----
This is a link to my implementation of a Linked List.  As with the Queue, my logic and code seem correct, but I still get errors.  When I attempt to debug it, Visual Studio directs me to a file that isn't even a part of the program and that I don't understand.  As with the Queue, I am awaiting feedback that will hopefully help me to fix this.

https://github.com/stilgeki/04_Linked_List_Lab


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
For the Queue, my time analysis is in Question 1, parts 1-4 and 6:

https://github.com/stilgeki/03_Queue_Lab/tree/stilgeki

For the Linked List, my time analysis is in Question 1, parts 1 and 4: 

https://github.com/stilgeki/04_Linked_List_Lab


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.


5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Suppose I have a project to create a web site that stores scores for an online videogame.  Each player's individual top score should be stored, and the overall top 10 should be listed on the "wall of fame."  The game has over 3,000,000 players, and players have the ability to update their high score by typing in their name and their new top score.  The way I see it, there are two options for storing the scores, both using a data structure of the dictionary ADT: a hash table or a BST.  There will be lots of find and insert operations in this program, since there will constantly be people checking and updating their high score.  Therefore, the speed of these methods will be important in choosing a data structure for the project.  Hash tables perform insert and find operations in O(1) time, while BSTs are slower, clocking in at O(log(n)) for both.  This difference will be large, given the number of players.  Another key element to the project is the "wall of fame."  I think the best way to accomplish this with a hash table is actually to have a plain array that holds the top 10 scores from the hash table in order.  Every time a new score is added, it would be checked against the scores in the array, and if it is higher than one of them, then it would be added to the array in the correct spot.  This would push one of them out of the array, reflecting the current top 10 scores.  The new score would then be added to the hash table.  This process is significantly easier for a BST, which is already sorted.  The top 10 scores would merely be taken from the BST and displayed for the "wall of fame."  However, given the number of players, the hash table will be a better choice overall.  It is simply much faster for the frequent insert and find operations that will be required for this program.  Perhaps if there were fewer players, the BST's sorted nature would be more useful than the hash table's speed, but with the current situation, a hash table is much better.

* Suppose I am working on a project for a social networking site such as Twitter, and I have been given the responsibility of creating a data structure to hold all the current user IDs so that a new ID can be checked against them for uniqueness.  In this case, a hash table is a very good solution, because hash tables don't allow non-unique items and they have a fast find method.  However, even a simple array could suffice for this.  When a new ID is submitted, the program would iterate through the array to check if it was there already, and if it wasn't it would add it.  If the ID was already taken the program would simply return a value that indicated as much.  This solution is a bit simpler, and could even be just as good for small array sizes.  However, the hash table is simply faster at checking for uniqueness and scales much better.  Therefore, it is a better choice.  I do like the simplicity of the array solution, but it just can't match the speed of a hash table.