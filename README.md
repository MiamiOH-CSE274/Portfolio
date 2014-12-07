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

7 - Create an implementation of a Queue using a circular array-based list
----
https://github.com/dazeycm/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
https://github.com/dazeycm/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
https://github.com/dazeycm/06_BST_Lab

7 - Create an implementation of a Hash Table
----
https://github.com/dazeycm/05_Hashing_Lab/blob/master/HashTable.ipp

7 - Create an implementation of a Heap
----
https://github.com/dazeycm/07_Heap_Lab

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
https://github.com/dazeycm/08_Graph_Lab

7 - Implement graph algorithms
----
Link to lab containing BFS and DFS:

https://github.com/dazeycm/08_Graph_Lab/blob/master/Graph.cpp

Link to actual BFS and DFS code:

https://gist.github.com/dazeycm/9be0b9ece7f2f0c6e08b


21 - Determine space and time requirements of common data structure methods
-----
* **Array-based list vs. Linked List** - Generally, an array will allow for faster look up in most cases. This is because arrays support random access, and if you want to get or set a value in a certain index, it's trivial to pull up that element and make changes to it. The problem with Arrays is that to add and remove requires the shifting of data, resulting in a runtime of O(n). Linked list initially don't seem much better. To find something in a Linked list you have to traverse through possibly every node, meaning O(n) time, to find a value. To get or set a value you have to first find it, and then return it. To add or remove nodes, you also have to find it first and then make the changes. This can be remedied, however, through the use of iterators. If you have an iterator to a node in a Linked List, get and set can be done in constant time. Add and remove can also be done in constant time, greatly improving the efficiency of the Linked List Data structure.

  |              | Array | Linked List |
  |--------------|-------|-------------|
  | Find (Value) | O(n)  | O(n)        |
  | Find (Index) | O(1)  | O(n)        |
  | Get/Set      | O(1)  | O(n)        |
  | Get/Set (Iterator) | O(1) | O(1)   |
  | Add/Remove   | O(n)  | O(n)        |
  | Add/Remove (Iterator) | O(n) | O(1)|

* **Binary Search Tree vs. Hash Table** - Both binary search trees and hash tables store key value pairs, making them dictionary data structures. Binary search trees must uphold a certain structure and set order, while hash tables allow for fast indexing of values by hashing them. Overall, a hash table has a running time fo O(1) for most operations. Through hashing, it's very simple to find a a value in a hash table and make changes to it. A binary search tree is a little more tricky to navigate through. In general, for a balanced tree, the running time of most operartions will be O(log n). This is because a binary search is performed on the tree to find a value in order to make changes to it. One area that BST beat hash tables is in Min/Max and Next/Prev. Because BST have an order and structure to them, finding the next node is as simple as finding the node and then looking at its children, while in a hash table, which has no order, you have to iterate over the entire set of data. Similarly to find the min or max you just have to continually navigate one direction through the tree until you find the end, while in a hash table you need to check every single element.

  |             | HashTable | BST |
  |-------------|-----------|-----|
  |Find|O(1)|O(log n)|
  |Set|O(1)|O(log n)|
  |Add/Remove|O(1)|O(log n)|
  |Prev/Next|O(n)|O(log n)|
  |Min/Max|O(n)|O(log n)|

* **Adjacency List vs. Adjacency Matrix** - Both an adjaceny list and an adjacency matrix are used to represent a graph abstract data type. An adjacency list is comprised of an array of nodes, each containing a list of it's edges to other nodes. An adjacency matrix is a 2d array, where each space in the array is a possible edge between the row and column node. The adjacency matrix has the benefit of being fast when modifying edges and querying the data. It's major downfall lies it its size and adding new vertex. The size of the matrix will always be O(V^2) because of the 2d array structure. Additionally, to add a new vertex, since the matrix is an array, you need to grow the array and then move the data around resulting in a time of O(V^2). Adjacency list support the quick addition of new vertex and edges by simply pushing them to the end of the current node array or edge array. Removing an edge in an adjacency list is a little more complicated because you have to iterate through the entirety of the edge list to see if it exists before deleting it. Ajacency list are often used when dealing with sparse graphs because their storage is much lower at O(V + E). If the data was more dense then an adjacency matrix would be used because more of the edges would be populated, resulting in less wasted space.

  |         |Adjacency List| Adjacency Matrix|
  |---------|--------------|-----------------|
  |Add Vertex| O(1) | O(V^2)|
  |Add Edge| O(1) | O(1)|
  |Remove Edge| O(E) | O(1)
  |Get Weight| O(V) | O(1) |
  |Space| O(V + E)|O(V^2)|

5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----


* **The call stack** - The stack is an area where, when we run our program, all of the local variables and functions are stored and ran. This is done in a LIFO order.
* **The heap** - The heap is the area where we can dynamically allocate memory. This data in C++ is initialized using the `new` keyword and then must be deleted using some variation of the `delete` keyword. There is no set order of data storage in the heap.
* **Address** - The address of a variable is where that variable is stored in memory. The address of a variable can be obtain by using the `&` reference operator.
* **Pointer** - A pointer is an object that points directly to another value's memory address stored somewhere in a computer's memory.

* **What is a memory leak, and why is it bad?** - A memory leak occurs space is allioted in memory but then never freed. This could potentially cause you to run out of space for memory.
* **What is a dangling pointer (or dangling reference), and why is it dangerous?** - A dangling pointer is a pointer that references  a space in memory that is no longer being used by our program. This is dangerous because the data could be overwritten and if the pointer is used, it will point to data that we did not intend it to.
* **What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java?** - A destructor is a method that is called when an object is deleted. In this way, it is possible to deallocate space in memory, preventing memory leaks. They're necessary in C++, because the language has no means of automatically deallocating space. Instead, when an object is no longer needed, the `delete` method is called to try and free the memory in the specified way. In a way, the object tries to clean up after itself. This isn't the case with Java, which has garbage collection. In java, data that is no longer being used is automatically freed when it goes out of scope or is no longer being accessed.

5 - Create collection classes using templates in C++
----

* **What is the main benefit of using templates when creating collection classes?** - When developing a new collection class, you want it to be universal. That is, it would be best if the collection could hold any type of data. This is where templates come in. Templates allow us to omit specifying a data type in our collection. In this way, the collection can be used by any of the default data types, or data types we create. This also saves us a lot of time that would be required to implement the data structure for the standard data types as well as the types we create.
* **In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.** - The point of a template is that it should work with any type of data you can imagine. To do this, whenever instantiating a template, the compiler creates a version of the template specifically for the data type that you want. The template code goes in the header file since the compiler needs to know everything about the template at the point it is instantiated.

<sub>Source used to understand how templates are changed to work for different data types: http://stackoverflow.com/questions/495021/why-can-templates-only-be-implemented-in-the-header-file</sub>

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* **If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)**

  To solve this problem I would use a hashset. For this data structure I assume that speed will be important. This means that all of the functions I need to support should be as quick as possible. The functions we need to support are add, remove, and checkExist(keyExist), all of which are very quick in a hashset. For the hash of the hashset, we can hash the string, and place it in the resulting index. This makes adding a new string to the hashset occur in O(1) time. Similarly, to remove something from the hashset, we hash the string to find the index and delete the value in that index from the hashset, making remove take O(1) time. Lastly, to check if a string exists in the hashset, we hash the string and check the index to see if it contains the string we want. This will also be done in constant time.

  Since a hashset is a set it does not allow duplicates, which is what's required. Hashsets also don't have an order to them which is fine since we don't need one. Coincidentally, the requirements for this data structure gracefully tip-toed everything that makes hashsets bad. For example, if we needed to have a min/max or next/prev function a hashset might not be the best choice since all of these functions take O(n) time. If we were told that min/max or next/prev were sometimes going to be called, I would still argue that a hashset would be the best data structure. However, if we were told those methods would be called a lot, I would consider using something like a BST which can complete all of the methods mentioned in O(log n) time.

* **If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.**

  To solve this problem, I would use a doubly linked list. For me, my grocery list is, and will likely always be on paper. Before I go shopping, I will make a list, roughly grouping the objects in the order that I'll pick them up in the store. Because of the way I do this, I'd make the argument that efficiency really doesn't matter. The list will almost never be longer than ~30 items, and my grocery list will never be something that is widely used by others, so how fast I can move through the list and find things is largely irrelevant. Additionally, I sometimes find going grocery shopping to be therapeutic so I don't mind spending a little extra time looking for food. Regardless, when using iterators and linked lists, the running time of a linked list is actually quite good, something I will get into a bit later. Additionally, linked lists support all of the functions I would need.

  A linked list would also be nice because the items in a linked list are sequential, meaning they follow each other. When making the list, similar items in similar locations would be close to each other in the store, and in my list. This means that as I'm working my way through the list in the store, I will almost never have to go back to previous items, and as such, won't be bouncing around the store trying to find what I want. Linked Lists do not have to be sorted, but the way in which I create the list would cause it be relatively sorted by location in the store.

  Lastly, I would choose a double linked list because often times I will forget things when making the list, and I'll only remember them once I get to the store. In situations like this it's nice to be able to quickly add things to a list. I would argue that speed is important in this situation as I don't want to be standing in the isle in other people's way, or take the chance of forgetting what I want to add. Now normally adding something to the list requires me to look through possibly the entire list, but this isn't the case with a short list on paper like I would use. This is because we have an iterator - our eyes. I don't believe our eyes are efficient as an iterator, but with a small grocery list, I can near instantly look at my list and find an item on it (especially since I'll likely be deleting things as I acquire them). Our eyes aren't actually an iterator as they don't instantly let me find something, but the time it takes is still much more quick than if I were to start at the top of the list and work my way down. Say for example that I'm in the frozen food isle, and I remember that I want pizza rolls but forgot to put them on my list. It takes only a glance to find the frozen brocolli I just picked up, and then I can add pizza rolls to my list, all in O(1) time.

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.


* **Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue needs a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.**

  To solve this problem I made many assumptions, one of which needs to be addressed fairly quickly. I'm assuming the packets are sent in certain set intervals. This means that each company will put in requests, and at a set time all of the requests will be handled. I made this assumption because the concurrency between the companys would be a tricky problem to solve. If for example company x was sending packets and company y tried to send packets with a higher priority, do I stop company x's transmission or do I make company y wait? Because the problem doesn't require I directly address this, I will omit doing so for the sake of simplicity. Regardless, I believe that more than one data structure would be necessary to accomplish that.

  First I would use some kind of graph to store connections between locations on the network. I would use a graph because it's a quick and effective means of portraying network locations and the links between the networks. Graphs have two popular data structures to choose from - adjacency lists and adjacency matrix. Between the two, I would probably choose the adjacency list. The problem doesn't identify how densely populated the edges interconnecting the graph will be, but I'll assume that the graph will be sparsely populated, which is perfect for an adjacency list. When choosing which of the graph data structures I would use I really only took into account the running time of adding, removing, and getting the cost edges. I believe that new nodes on the network will rarely be added or removed as hundreds of companies will not be trying to join the network at the same time (again, this is just my assumption). This just leaves the adding and removing of new edges, as well as getting the cost of an edge. For an adjacency list, adding an edge can be done in O(1) time, and querying for the cost as well as removing an edge can be done in O(E) time, where E is number of edges a node has. Another reason I would choose a list as opposed to the matrix is because of size. A matrix takes up O(V^2) space while a list only takes O(V + E). Assuming that I will run the servers that host this data, I wouldn't want a matrix that uses more space than I need, especially since more space costs more money.

  An extra benefit of using the graph in general is that graph theory can be applied to our data. One example of this is Dijkstra's algorithim. Dijkstra's would allow us to calculate the shortest path between two nodes. If different connections had different costs based on length, we could find the shortest, and therefore cheapest, connection between two nodes in our network. This would would make our network a popular because it'd being fast, and at the same time allows us to save money.

  To solve the issue of companies paying different amounts to have their packets sent more quickly, I would use some kind of priority queue - likely a max heap. My main reason for this is that in the priority queue, I could store the priorities of the different companies. The packets they want to send could be stored in the priority queue with the company's priority. Companies that pay the most will have the highest priority. In fact, I could probably use how much they pay as the actual priority assuming all else equal. This way if company x payed 50, and company y payed 100, company y would have a priority of 100, while company x had a priority of 50. This means that company Y would have a higher priority and be processed before company x. Inserting and deleting in a heap can be done in O(log n) time. This actually isn't bad considering the data structure has an order to it. If we used something like a hashTable it would take O(n) time to find the max value and remove it, which would be awful.

  If we used a heap and graph in this way, it'd be an efficient way to solve this problem. When packets need to be sent between two places we would add the company to the priority queue. How much they pay would dictate their position in the queue. Once it came time to process the requests, I would pop the first item from the queue. I would then go to the graph and find the path from the company to it's destination and send the packets that I got from the priority queue on their way. After doing so I would go back to queue and pop the next item and send it along the path from the graph.
