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
This is my implementation of an Array Queue.

https://github.com/stilgeki/03_Queue_Lab/tree/stilgeki


7 - Create an implementation of a List
----
This is a link to my implementation of a Linked List.

https://github.com/stilgeki/04_Linked_List_Lab


7 - Create an implementation of a Binary Search Tree
----
Sadly, I have a nature of procrastination.  Deadlines just don't register with my brain until they're slapping me in the face, and I didn't put myself in a position where I was able to finish the BST lab, Hash lab, Heap lab, or graph traversal.  That's 28 points worth of things I simply didn't do, but I hope you can still grade the rest of the Portfolio.  While I did enjoy many aspects of your class, this semester has taught me that programming simply doesn't click with me.  I like the idea of developing software, but I just don't enjoy the actual act of programming.  I intend to change my major, and am simply hoping I will escape with my GPA intact.  Thank you for a good semester, and I truly regret that I will not be taking another of your courses, despite my personal deficiencies in the subject matter.  I wish you all the best.  :)


7 - Create an implementaiton of a Hash Table
----
See the BST section.


7 - Create an implementation of a Heap
----
See the BST section.


7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
This is my implementation of an Adjacency List:

https://github.com/stilgeki/08_Graph_Lab


7 - Implement graph algorithms
----
See the BST section.


21 - Determine space and time requirements of common data structure methods
-----
For the Queue, my time analysis is in Question 1, parts 1-4 and 6:

https://github.com/stilgeki/03_Queue_Lab/tree/stilgeki

For the Linked List, my time analysis is in Question 1, parts 1 and 4: 

https://github.com/stilgeki/04_Linked_List_Lab

For the Adjacency List, my time analysis is in Question 2:

https://github.com/stilgeki/08_Graph_Lab


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
https://github.com/stilgeki/03_Queue_Lab/tree/stilgeki

My Queue Lab is a good example of memory management in C++.  In C++, unlike in Java, there is no garbage collection, so you have to manually delete things that have outlived their usefulness to prevent memory leaks.  Additionally, you need to avoid deleting something but not a pointer to it, leaving a dangling pointer that points to nothing.  When a piece of memory can no longer be accessed because there is no pointer pointing at it, that is a memory leak and the data should be deleted.  My Queue Lab does this by calling a destructor method.  The destructor is called whenever the backing array needs to grow, because the old array is deleted and a new one is created in its place.  Deleting the old backing array prevents a memory leak.  After the backing array is deleted, reassigning it to the new array prevents a dangling pointer.


5 - Create collection classes using templates in C++
----
https://github.com/stilgeki/03_Queue_Lab/tree/stilgeki

My Queue Lab is also an example of the use of templates in C++.  Templates become a necessity because of the way compilers function with C++.  To generalize your program to all data types, you must use templates to tell the compiler that it has to wait to find out what data type it is dealing with.  Templates are used in conjunction with inheritance to create template classes that are generalized and abstract, and therefore can be applied to many different programs.  This is a slightly confusing and unintuitive nuance of the language, but templates can also be very powerful when employed correctly.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Suppose I have a project to create a web site that stores scores for an online videogame.  Each player's individual top score should be stored, and the overall top 10 should be listed on the "wall of fame."  The game has over 3,000,000 players, and players have the ability to update their high score by typing in their name and their new top score.  The way I see it, there are two options for storing the scores, both using a data structure of the dictionary ADT: a hash table or a BST.  There will be lots of find and insert operations in this program, since there will constantly be people checking and updating their high score.  Therefore, the speed of these methods will be important in choosing a data structure for the project.  Hash tables perform insert and find operations in O(1) time, while BSTs are slower, clocking in at O(log(n)) for both.  This difference will be large, given the number of players.  Another key element to the project is the "wall of fame."  I think the best way to accomplish this with a hash table is actually to have a plain array that holds the top 10 scores from the hash table in order.  Every time a new score is added, it would be checked against the scores in the array, and if it is higher than one of them, then it would be added to the array in the correct spot.  This would push one of them out of the array, reflecting the current top 10 scores.  The new score would then be added to the hash table.  This process is significantly easier for a BST, which is already sorted.  The top 10 scores would merely be taken from the BST and displayed for the "wall of fame."  However, given the number of players, the hash table will be a better choice overall.  It is simply much faster for the frequent insert and find operations that will be required for this program.  Perhaps if there were fewer players, the BST's sorted nature would be more useful than the hash table's speed, but with the current situation, a hash table is much better.

* Suppose I am working on a project for a social networking site such as Twitter, and I have been given the responsibility of creating a data structure to hold all the current user IDs so that a new ID can be checked against them for uniqueness.  In this case, a hash table is a very good solution, because hash tables don't allow non-unique items and they have a fast find method.  However, even a simple array could suffice for this.  When a new ID is submitted, the program would iterate through the array to check if it was there already, and if it wasn't it would add it.  If the ID was already taken the program would simply return a value that indicated as much.  This solution is a bit simpler, and could even be just as good for small array sizes.  However, the hash table is simply faster at checking for uniqueness and scales much better.  Therefore, it is a better choice.  I do like the simplicity of the array solution, but it just can't match the speed of a hash table.