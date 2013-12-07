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

By clicking on the link you will see that I have fully demonstrated my knowledge of a queue. The code within ArrayQueue.ipp has passed the tests that have been provided by Dr. Brinkman in main.cpp. Furthermore, to implement the queue in this assignment I used the circular array concept. In this code(ArrayQueue.ipp) you will find a constructor and destructor for a circular array. You will also find a add, remove, getNumItems and grow methods. All of these methods are fully functional. Link: https://github.com/LakersAllTheWay/03_Queue_Lab/tree/griffid5

7 - Create an implementation of a List
----
Possible sources of evidence (do any one of these):

By clicking on the link below you will see that I have fully demonstrated my knowledge of a linked list. Other than the splice method all other methods have passed the tests provided by Dr. Brinkman. In this assignment I used a dummyNode that allowed me to access the linked list in which the dummyNode's "next" and "prev" were itself. The methods that can be found in LinkedList.ipp are: find, set, add, remove, get and size. Link: https://github.com/LakersAllTheWay/04_Linked_List_Lab/tree/griffid5


7 - Create an implementation of a Binary Search Tree
----
Possible sources of evidence (do any one of these):

To satisfy this requirement of the portfolio I went ahead and did the BST_Lab. In this lab I have demonstrated my knowledge 
of a BST by implementing the following methods in BST.ipp: constructor, destructor, size, add, remove, find, keyExists, next, prev, max and min.
For most methods I used both a private and public method call so that recursion would be simplified. In this lab all my methods passed the test
that Dr. Brinkman had and all my methods except the destructor and size were O(h) because the height of the tree is the longest number
of edges that each method will have to travel. Finally size was O(n) instead of O(h) because I had to travel down both sides of the tree and 
visit every node. Link: https://github.com/LakersAllTheWay/06_BST_Lab/tree/griffid5


7 - Create an implementaiton of a Hash Table
----
Possible sources of evidence (do any one of these):

I completed the 05_Hashing_Lab to complete this part of the portfolio. In the HashTable.ipp you can find that I implemented the following methods: constructor, destructor, add, remove, find keyExists, size and grow. All of these methods passed Dr. Brinkman's tests that he had given us. Also keyExists, find, remove and size were all
constant time O(1). We know that size is constant time since we just return numItems. Additionally, we are using an array for the implementation of the hashtable so we know that the 3 other methods will be constant time as well, since we are using key k. 
The add method on the other hand has a worst case running time of linear time O(n) because we sometimes have to call grow, however, that is only required when the load factor becomes more than 1/2. Otherwise we don't have to call grow and the add method is O(1) on average since we are using linear probing to find an open slot in the hash table. 
Link: https://github.com/LakersAllTheWay/05_Hashing_Lab/tree/griffid5

7 - Create an implementation of a Heap
----
Possible sources of evidence (do any one of these):

In my 07_Heap_Lab I was able to satify the first 4 tests that Dr. Brinkman had given us. The methods that worked in this lab were the constructor, destructor, grow, add, remove and getNumItems. The two methods that I couldn't get working were bubbleUp and TrickleDown. 
Since I was unable to get these two methods to work I was unable to pass Dr. Brinkman's last 3 tests. The add and remove methods are O(log n), except for when grow is called which makes the runtime O(n). Link: https://github.com/LakersAllTheWay/07_Heap_Lab/tree/griffid5

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

* Select any of the following labs, and analyze the running times for each of your methods of your data structure: Queue, Linked List, Binary Search Tree, Heap, Hash Table, Graph (Adjacency List or Adjacency Matrix, you don't have to do both, but you can if you want)


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

 Link: https://github.com/LakersAllTheWay/03_Queue_Lab/blob/griffid5/ArrayQueue.ipp

5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----

Possible sources of evidence (do up to 2 of these, up to 15 points for each):

* Select a project for which there are multiple reasonable data structure designs. Describe two reasonable options, and explain the trade-offs between them. For each, describe an application where the data structure would be better. For example, if comparing KD-Trees to a Grid in the Starbucks problem, which one is better really depends on the input data set. Explain what the data would have to look like for the Grid to be a clear winner, and also what type of data would lead you to use a KD-Tree instead.
