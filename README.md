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
* ArrayQueue:
* https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/liy28?source=cbc 

7 - Create an implementation of a List
----
* Linked List:
* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/liy28?source=cbc 

7 - Create an implementation of a Binary Search Tree
----
* Binary Search Tree Lab: 
* https://github.com/MiamiOH-CSE274/06_BST_Lab/tree/liy28?source=cbc 

7 - Create an implementaiton of a Hash Table
* Hash Table Lab;
* https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/liy28?source=cbc 

7 - Create an implementation of a Heap
----
* Heap lab:
* https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/liy28?source=cbc 

7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
* Graph lab
* https://github.com/MiamiOH-CSE274/08_Graph_Lab/tree/liy28?source=cbc 

7 - Implement graph algorithms
----
* Graph lab: 
* https://github.com/MiamiOH-CSE274/08_Graph_Lab/tree/liy28?source=cbc 

21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)

* Linked List: 
* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/liy28?source=cbc 
* (1) find(): If the index of the item is out of boundary or the item is dummy node, assuming the exception call takes constant time, then find() will be O(1). Otherwise, find() can be O(n) because the line of code in for loop brackets takes linear time.  
* (2) set(): How much time set() can take really depends on the time find() takes, since assigning values only takes constant time. So, the worst case running time can be O(n).
* (3) add(): Just like set(), how much time add() takes depends on the running time of find(), since switching pointers and assigning values take constant time. add() can take linear time in the worst case.   
* (4) remove(): Assuming the exception call takes constant time, if there is no item in the linked list, remove() is O(1). Otherwise, the running time of find() plays an important role on deciding the running time of remove(), since switching pointers and updating the number of items take constant time. remove() can take up to linear time in the worst case. 
* (5) get(): The analyzing strategy of the running time of set() can apply here.    
* (6) size(): size() is O(1) because returning a value takes constant time.

* HashTable:
* https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/liy28?source=cbc 
* (1) add(): If grow() does not get called, assuming hash() and modulus calculation take constant time, then add() would be O(n) theoretically in the worst case, since I implemented add() using linear probing, which could go through every bucket to search for an empty spot. However, in real-life cases, linear probing takes constant time and therefore add() should be O(1) on average. If grow() gets called, then add() would be O(n). See (6) grow().
* (2) remove(): The running time of remove() really depends on how much time linear probing takes and, as I analyzed above, linear probing takes constant time in real-life cases. So, remove() is O(1), providing hash() and modulus calculation take constant time.
* (3) find(): If we assume exception call takes constant time, find() would be constant, considering the analysis above about the running time of linear probing and hash() as well as modulus calculation.
* (4) keyExists(): find() plays an essential role on deciding how much time keyExists() take, so keyExists() is O(1).
* (5) size(): Returning a value takes constant time and therefore size() is O(1).
* (6) grow(): If we assume making a new array with double size of the old array takes constant time, looping through the old array to find appropriate items takes linear time.  

* Graph (Adjacency List):
* https://github.com/MiamiOH-CSE274/08_Graph_Lab/tree/liy28?source=cbc 
* getCost(): Following the given index(node name) to find a certain node takes constant time, but looping through the edge list of the node to find a certain edge can be O(d)* in the worst case.
* add(): When cost < 0, assuming the exception call takes constant time, addEdge() is O(1). Otherwise, the larger degree between node1 and node2 decides the worst running time of add(), because add() uses the searching strategy of find() and therefore has the similar running time performance. Since node1 and node2 are arbitrary nodes, in the worst case, add() is O(d), considering two function calls to getCost() could be up to O(d).
* remove(): When there is no connection between node1 and node2, remove() takes constant time. Otherwise, two function calls to getCost() could be up to O(d). Moreover, like add() method, remove() also uses the searching strategy of find(), and therefore remove() could be O(d) in the worst case. 
* d is the maximum degree of any node in the graph

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):
* Hash Table:
* https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/liy28?source=cbc

* Select any of your labs or projects that uses dynamic memory, and explain how memory is managed. In particular, you must show that your program does not leak memory, and does not suffer from dangling pointers or out of bounds array access. This will probably require referring to your code, providing links.
 
In the constructor, the operator new is used to allocate dynamic memory on Heap in order to store an array of HashRecords. Unlike Stack memory, memory have been allocated on Heap need to be deallocated to avoid memory leak, which reduces the available memory and causes software aging. The destructor uses the operator delete for memory deallocations, and so doe grow(). In grow(), a chunk of dynamic memory are allocated by using the operator new to store a new array with double size of the old one, and thus the operator delete has to be applied here for memory deallocations. Moreover, the pointer used to point to the old array is switched to point to the new array in case of being a dangling pointer, which points to where memory has been deallocated and thus cause memory safety issues. Last but not the least, when looping through hashPrime and the old backing array, the bound is set to be the size of each array in case out-of-bound error happens.           

5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):
* Linked List: 
* https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/liy28?source=cbc 

* Any of the labs or projects, provided it uses templates in an interesting way.

Templates make code reusable, and they are instantiated at complier-time with the source code. A class template, often used to make generic containers, is actually applied to the linked list lab. The scope resolution operator is used to define a template constructor as well as the template methods. Also, T, type parameter, is applied to the lab as well, so this allows users to specify what kind of data the user wants to store in the linked list. The complier is totally fine with this type of syntax.

30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):
* Old exam problem 1: pic.twitter.com/UzJxw2O0kJ  
* Old exam problem 2: pic.twitter.com/ZvPLV6SlGV  

* For the old exam problem 1, it requires a dictionary as the abstract data type because the names the players type into are the keys to which the players information are stored. To satisfy the requirement, two common data structure I come up with would be Binary Search Tree (BST) and Hash Table. I prefer Hash Table to BST.
* First of all, when implemented with Hash Table, the video game allows the players to update their score much faster than it is implemented with BST. The two data structure all take players names as the keys, but BST and Hash Table have different performance on the running time of accessing a player info with his or her key. BST can take up to log(N) time to update a person info, while Hash Table takes constant time on average if it is implemented with double hashing. Hash Table beats BST by a lot.
* Although BST updates top 10 scores a little faster than Hash Table does, the changes to top 10 scores less often than the changes to personal scores. Once top 10 scores change, the video game implemented with Hash Table loops through each HashRecord. This process takes linear time. On the other hand, the video game swap nodes if changes happen and this can take up to linear time in the worst case, which is the smallest score gets changed to the largest score. However, as I mentioned, the changes to top 10 scores rarely happen, BST beats Hash Table by a little. 
* To conclude, the video game would be better to be implemented with Hash Table rather than BST.

* For the old exam problem 2, it requires a dictionary as the abstract data type because each unique user id can be viewed as a key to according person info. To check if the new id is good to use, I have to exclude Binary Search Tree (BST). Although a user id can probably compare with other user ids, each iteration of searching for duplicates takes up to log(N) time in the worst case, whereas the other data structure, Hash Table and Random Access Table (RAT), takes linear time to search for duplicates.(See explanations below) Between these two data structure, I prefer Hash Table to RAT.
* Hash function converts each user id into a hash value, and Hash Table implemented with double hashing searches duplicates until it find an empty spot, which means the new id is unique and has been added into the table yet. The searching process takes constant on average. On the other hand, RAT uses the user ids as keys, so if provided a new id and RAT can find an empty spot, then the new user id is unique. Otherwise, it is not.
* The drawback of RAT is that it takes way too much space than Hash Table does when the user ids are made by wide range of numbers and characters. For example, abc12345 would take 26x26x26x10x10x10x10x10-byte memory at least, whereas hash function can view abc12345 as 1+2+3+1+2+3+4+5 and then only need 26x3+10x5-byte memory at least. 
* Considering that social networking user names are made by wide range of data, Hash Table is better than RAT and BST.   
