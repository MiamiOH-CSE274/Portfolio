Author
==========
"Griffith, David", griffid5
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
Possible sources of evidence (do any one of these):

By clicking on the link you will see that I have fully demonstrated my knowledge of a queue. The code within ArrayQueue.ipp has passed the tests that have been provided by Dr. Brinkman in main.cpp. Furthermore, to implement the queue in this assignment I used the circular array concept. In this code(ArrayQueue.ipp) you will find a constructor and destructor for a circular array. You will also find a add, remove, getNumItems and grow methods. All of these methods are fully functional. Link: https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/griffid5

7 - Create an implementation of a List
----
Possible sources of evidence (do any one of these):

By clicking on the link below you will see that I have fully demonstrated my knowledge of a linked list. Other than the splice method all other methods have passed the tests provided by Dr. Brinkman. In this assignment I used a dummyNode that allowed me to access the linked list in which the dummyNode's "next" and "prev" were itself. The methods that can be found in LinkedList.ipp are: find, set, add, remove, get and size. Link: https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/griffid5


7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

To satisfy this requirement of the portfolio I went ahead and did the BST_Lab. In this lab I have demonstrated my knowledge 
of a BST by implementing the following methods in BST.ipp: constructor, destructor, size, add, remove, find, keyExists, next, prev, max and min.
For most methods I used both a private and public method call so that recursion would be simplified. In this lab all my methods passed the test
that Dr. Brinkman had and all my methods except the destructor and size were O(h) because the height of the tree is the longest number
of edges that each method will have to travel. Finally size was O(n) instead of O(h) because I had to travel down both sides of the tree and 
visit every node. Link: https://github.com/MiamiOH-CSE274/06_BST_Lab/tree/griffid5


7 - Create an implementaiton of a Hash Table
----
Possible sources of evidence (do any one of these):

I completed the 05_Hashing_Lab to complete this part of the portfolio. In the HashTable.ipp you can find that I implemented the following methods: constructor, destructor, add, remove, find keyExists, size and grow. All of these methods passed Dr. Brinkman's tests that he had given us. Also keyExists, find, remove and size were all
constant time O(1). We know that size is constant time since we just return numItems. Additionally, we are using an array for the implementation of the hashtable so we know that the 3 other methods will be constant time as well, since we are using key k. 
The add method on the other hand has a worst case running time of linear time O(n) because we sometimes have to call grow, however, that is only required when the load factor becomes more than 1/2. Otherwise we don't have to call grow and the add method is O(1) on average since we are using linear probing to find an open slot in the hash table. 
Link: https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/griffid5

7 - Create an implementation of a Heap
----
Possible sources of evidence (do any one of these):

In my 07_Heap_Lab I was able to satify the first 4 tests that Dr. Brinkman had given us. The methods that worked in this lab were the constructor, destructor, grow, add, remove and getNumItems. The two methods that I couldn't get working were bubbleUp and TrickleDown. 
Since I was unable to get these two methods to work I was unable to pass Dr. Brinkman's last 3 tests. The add and remove methods are O(log n), except for when grow is called which makes the runtime O(n). Link: https://github.com/MiamiOH-CSE274/07_Heap_Lab/tree/griffid5

7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
Possible sources of evidence (do any one of these):

In my 08_Graph_Lab (Graph.cpp) you can see that I used an adjanency list to implement a representation of a graph. I was able to successful implement the following methods: getCost, addEdge and removeEdge. I used two vectors in which one vector kept track of the edges (edgeList) and the other kept track of the nodes (adjList). Finally, in this lab I learned that a graph is simply a list of nodes in which each node is supposed to keep a list of the edges that are adjacent to it. 

Link: https://github.com/MiamiOH-CSE274/08_Graph_Lab/tree/griffid5 

At time of submission of my portfolio my 08_Graph_Lab has not been merged to my repo in github.com/MiamiOH-CSE274/08_Graph_Lab/tree/griffid5 so here is the link to my local repo as well: https://github.com/LakersAllTheWay/08_Graph_Lab/tree/griffid5

7 - Implement graph algorithms
----
Possible sources of evidence (do any one of these):

By looking at my 08_Graph_Lab (Graph.cpp) you can see that I implemented the proper graph algorithms for getCost(), addEdge() and  removeEdge() methods. Each of these methods worked correctly because they passed the tests that Dr. Brinkman gave us. Lastly, I showed my knowledge of graph algorithms by using two vectors in which one vector kept track of the edges (edgeList) and the other kept track of the nodes (adjList).

Link: https://github.com/MiamiOH-CSE274/08_Graph_Lab/tree/griffid5 

At time of submission of my portfolio my 08_Graph_Lab has not been merged to my repo in github.com/MiamiOH-CSE274/08_Graph_Lab/tree/griffid5 so here is the link to my local repo as well: https://github.com/LakersAllTheWay/08_Graph_Lab/tree/griffid5

21 - Determine space and time requirements of common data structure methods
-----
Possible sources of evidence (do up to 3 of these, up to 7 points for each):

In General the time complexity of an algorithm/method for a program is how the time complexity scales when the input size changes. 

__________________________________________________________________________________________________________
03_Queue_Lab

Link: https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/griffid5

Space Requirement: Since we are using a circular array the space requirement is the size of the array at any given moment which is going to be "linear". 

Constructor: The constructor has a runtime that is "constant time" since we only allocating memory. 

Destructor: The destructor has a runtime that is "constatn time" as well since we are just deleting the pointer to the array.

add: The worst case runtime for the add method is "linear" and that is only when grow is called otherwise it is constant time since we are adding the item to the back of the array.

remove: Remove has a runtime that is "constant time" since we are just removing the first item in the queue. 

grow: Grow takes "linear time" since we have to copy each element from the old array into the new array one at a time.

__________________________________________________________________________________________________________
04_Linked_List_Lab

Link: https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/griffid5

Space Requirement: The space requirement for this linked list is based on its three pointers which are next, prev and data. This gives us a space requirement of "constant time."

Constructor: The constructor has a runtime that is "constant time" since we only allocating memory. 

Destructor: The destructor has a runtime of "linear" since we have to loop through the list while numItems > 0.

add, remove, get, set: The add, remove, get and set methods have a worst case running time of "linear" because I call the find method which also has a worst case running time of "linear," unless the item is at the front or end of the list, in which the runtime would be "constant" if
it is.  

find: Since we may have to go through each item in the linked list this gives us a worst case runtime of "linear." However, if the item is in the first or last spot then we have a runtime of "constant time."

size: We are just returning the numItems variable so this method is going to be "constant time."

__________________________________________________________________________________________________________
05_Hashing_Lab

Link: https://github.com/MiamiOH-CSE274/05_Hashing_Lab/tree/griffid5

Space Requirement: Since we are using an array the space requirment is going to be the size of the array at any given moment which is going to be "linear." 

Constructor: The constructor has a runtime that is "constant time" since we only allocating memory. 

Destructor: The destructor has a runtime that is "constatn time" as well since we are just deleting the pointer to the array.

keyExists, find and remove: We are using an array for the implementation of the hashtable so we know that these 3 methods will be "constant time" since we are using key k as the parameter. 

size: We are just returning the numItems variable so this method is going to be "constant time."

add: Add is going to be "constant" unless grow() has to be called in which add will become "linear time."

grow: Grow takes "linear time" since we have to copy each element from the old array into the new array one at a time.



5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):

By looking at my 03_Quere_Lab you can see that I know how to manage memory in C++ by not having my program leak memory, suffer from dangling pointers or out of bounds array access. In C++ we don't have a garbage collection that automatically cleans up like we do in Java. Because of this
fact we as the programmer must do it our self. When every we use the key word "new" in C++ we must call "delete" at some point in the following code. By calling "new" we create a pointer to a new variable an create some memory space. This means that the variable doesn't have a scope
and won't be deleted until we specifically call delete on that variable. This can be seen in my grow method of ArrayQueue.ipp:
  
 template <class T>
 void ArrayQueue<T>::grow(){
 
        T* newBackingArray = new T[backingArraySize*2];
        if(newBackingArray == NULL) {
                throw std::string("There was an error in execution");
        }
        for (unsigned long i = 0; i < backingArraySize; i++) {
                newBackingArray[front + i] = backingArray[(front + i)%backingArraySize];
        }
        backingArraySize = backingArraySize * 2;
        delete [] backingArray;
        backingArray = newBackingArray;
 }
  
Since I called "T* newBackingArray = new T[backingArraySize*2];" I had to make sure I called "delete [] backingArray;" at some point so I could reset backingArray to the newBackingArray without having any memory problems. 
If I didn't properly know how to use memory management in C++ then my program would have crashed or given me an error in which it does not.

Here is the code in my destructor method that proves a memory leak doesn't occur as well:

    template <class T>
     ArrayQueue<T>::~ArrayQueue() {
         delete [] backingArray;
    }
 
For arrays we have to call "delete [] backingArray;" instead of "delete backingArray." "delete backingArray" would only work if the backingArray was an object rather than an array. Destructors in C++ are used to deallocate memory and do the cleanup that we don't get automatically in C++. The destructor gets called for a class object when 
the object passes out of scope or is explicitly deleted. Finally, by looking at the information above you can see that I know the importance of memory management in C++ and how it works.

 Link: https://github.com/MiamiOH-CSE274/03_Queue_Lab/tree/griffid5

5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

By looking at my 04_Linked_List_Lab you can see that Dr. Brinkman gave us a template which was defined as: template <class T> in which in main.cpp this was changed to: LinkedList<int> testList; In this case "T" is a place holder and Dr. Brinkman
decided to replace it with "int" in main.cpp which does all the testing of our code. Templates allow for us to use different data types for methods that do similar things for other data types. So in this example Dr. Brinkman could have went with a "double" instead of an "int" type and our methods would have still worked because we used "T" as 
a place holder instead of using "int" or some other data type. By using templates we have the flexability to use many data types instead of having to code the same method for each different data type that we may be given. Also with templates we must declare our implementaion class as .ipp instead of the standard .cpp because the compiler can't handle template
classes when we place them in a .cpp file. Finally, when using templates the data type is choosen at time of execuation instead of compile time like it would be if we were not using templates. Link: https://github.com/MiamiOH-CSE274/04_Linked_List_Lab/tree/griffid5


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.

* Shuffle Project:

For the shuffle project there were two reasonable data structures that we could have used. The two options were an array-based queue or a linked list. To compare these two data structures we need to decide what operations/methods that we would be using most often to simulate shuffling a deck of cards. The two that come to my mind are that of adding and removing. The data structure that would be optimal is dependent upon what style of shuffling you choose to represent.

If you choose to simulate the riffle shuffle you would want to pick the array-based queue. An array-based queue has the runtime of O(1) for adding and removing items. The only time that the runtime isn't constant for the add method is when you need to call grow in which the new runtime would become O(n). If we choose a linked list for this style of shuffling we would get a runtime that is O(n) for add and remove which is clearly slower than that for the array queue.
  
You would want to choose a linked list for a shuffling simulation if you were to use the hindu style of shuffling because you are removing a little more than the bottom half of the deck then taking a random number of the cards off the top of that chunk and placing them back onto the top of the deck that you didn't take off and repeat. You would represent this by doing a splice method within you code which takes O(n). Lastly, Since an array-based queue follows FIFO we couldn't even use this data structure to simulate this style of shuffling since we are removing the bottom of the deck. 
  
  
* Vise Project:

For the vise project there were many data structures that we could have choosen. The two that I am going to look at are a 1D array and a graph structure made of node objects and each node object having 6 edges. 
  
The advantages of using a 1D array as the board data structure are that you have O(1) access to any value in the array in which this gives us getting and setting to be O(1). However, the disadvantage to a sorted array is that adding and removing take O(n). Another disadvantage to this structure when used as a game board is that you have to use some math to calculate the neighbors of the specific index.  
  
The advantages of using the graph structure is that once the board was initialized most things afterwards would run in O(1) such as, adding or removing a piece to the board. Since we had 6 pointers that pointed to the neighbors of a specific position we could easily tell if its neighbors were empty, an enemy or one of its own pieces in constant time. Also another reason we choose this data structure is because we figured by using pointers we could avoid doing computations for locating neighbors in the board during game play. The disadvantage to this data structure is that it takes O(n) to setup the game board initially. Also if you don't know pointers very well then it would be difficult to implement this data structure. 
  
  
