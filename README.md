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
This is where I created an implementation of a Queue: https://github.com/wilso199/03_Queue_Lab/blob/master/ArrayQueue.ipp

7 - Create an implementation of a List
----
This is where I created an implementation of a List: https://github.com/wilso199/04_Linked_List_Lab/blob/master/LinkedList.h

7 - Create an implementation of a Binary Search Tree
----
This is where I created an implementation of a BST: https://github.com/wilso199/06_BST_Lab/blob/master/BST.h

7 - Create an implementation of a Hash Table
----
This is where I created an implementation of a Hash Table: https://github.com/wilso199/05_Hashing_Lab/blob/master/HashTable.h

7 - Create an implementation of a Heap
----
This is where I created an implementation of a Heap: https://github.com/wilso199/07_Heap_Lab/blob/master/Heap.h

7 - Create an implementation of either Adjacency Lists or Adjacency Matrices
----
This is where I created an implementation of a Adjacency List: https://github.com/wilso199/08_Graph_Lab/blob/master/Graph.cpp

7 - Implement graph algorithms
----
This is where I implemented a DFS graph algorithm: https://github.com/wilso199/08_Graph_Lab/blob/master/Graph.cpp

21 - Determine space and time requirements of common data structure methods
-----
TODO: For each pair of data structures listed here, write a short essay comparing and contrasting them in terms of their running times for different operations. (7 points each)

* Array-based list vs. Linked List

Array-based Lists and Linked Lists are both used to store data in a linear fashion. Adding an element to an Array-based List will take O(n) time because even if you know where you are going to place the value, you will have to shit every element in the array 1 place to right. Adding an item to a Linked list however, can be done in O(1) time if you are using an iterator to hold the location you need to place the value at because all you would have to do is change the pointers of the nodes to the left and the right of what you are adding. Removing an item is the same running time as adding for both lists. This allows the Linked list to be the better option when it comes to adding/removing an element as long as you have an iterator pointing to the location. With both lists you can also set a value at O(1) time if the Linked List has an iterator. If the linked List does not have an iterator however, you will have to call find which is O(n) time for a Linked List. The size of both data structures can also be found at O(1) time because they are kept externally as an integer value. This makes Linked List the better option if you are able to use iterators. However, it is important to remember that Linked Lists are not random access, so you will need to always increase/decrease the iterator based on which location you want to access. If you remember that though, almost all functions can be run in O(1) time, which runs more efficiently than an Array-Based List.

						|   Array Based   |    Linked   | Linked with Iterator |  
			———————————————————————————————————————————————————————————————————————————————
			add/remove		|	O(n)	  |	O(n)	|	O(1)
			———————————————————————————————————————————————————————————————————————————————
			get/set			|	O(1)	  |	O(n)	|	O(1)	
			———————————————————————————————————————————————————————————————————————————————
			find (value)		| 	O(n)	  |	O(n)	|	O(n)
			———————————————————————————————————————————————————————————————————————————————
			find (Index)		|	O(1)	  |	O(n)	|	O(1)
			———————————————————————————————————————————————————————————————————————————————
			size			|	O(1)	  |	O(1)	|	O(1)

* Binary Search Tree vs. Hash Table

Binary Search Tree and Hash Tables are both dictionary data structures that store key value pairs. One main difference between the BST and the Hash Table is the BST has to uphold a certain structure and set order, while a Hash Table simple just stores pairs are simply a set of key value pairs in no particular order. For Hash Tables most operations are completed at a running time of O(1) because through hashing you are very easily able to find a value and make changes to it. Meanwhile, most operations for a BST are completed at a running time of O(log n) because a binary search tree implements a binary search to find the value in order to make changes. If you want to find a value in the Hash Table you simply hash the key and you have the value, so this is O(1) time. If you wanted to do the same thing in a BST you would have to do a binary search as mentioned above, so this will take O(log n) time. Because find is O(1) for a Hash Table, add/remove are also O(1) because you simply just have to call find with a given key to add or remove that value form the table. With a BST it takes O(log n) time to add because you need to binary search for the value or an empty position in the tree and then update the value or add the value if there is an empty space. Equally remove has the same running time. When comparing the BST and the Hash Table data structures it is important to look at the running times for Min/Max and Next/Prev functions. As you can see form the chart below the running times for the Hash table are O(n) for both Min/Max and Next/Prev while the running times for the BST are O(log n) for both. The differences in running time are a direct result of the difference in structure. Because BST’s have an order and structure to them, finding the next node is a simple operation: find the node and then look at its children. However, in the Hash Table because of lack of structure, you would have to iterate over the entire set of data to find the value you are looking for. Similarly with the min and max functions, with a BST you have to simply navigate one direction through the tree until you reach a leaf, while in a Hash Table you would have to check every single element and compare them to find the min or max of the set. 

					|   Hash Table    |   BST  
			————————————————————————————————————————————————
			Find		|	O(1)	  |	O(Log n)
			—————————————————————————————————————————————————	
			Set		|	O(1)	  |	O(Log n)
			—————————————————————————————————————————————————
			Add/Remove	|	O(1)	  |	O(Log n)
			——————————————————————————————————————————————————
			Next/Prev	|	O(n)	  |	O(Log n)
			——————————————————————————————————————————————————
			Min/Max		|	O(n)	  |	O(Log n)
 

* Adjacency List vs. Adjacency Matrix

An Adjacency Matrix and an Adjacency List both implement the graph abstract data type. An Adjacency Matrix is a 2D array where each space in the array is a possible edge between the row and column nodes.  An Adjacency List is made up of an array of nodes, each containing a list of it’s edges to other nodes. If you want to add a new vertex to an Adjacency Matrix you will have to grow the array and copy over the original data which will result in a running time equal to the size of the matrix which is O(V^2). Adjacency Lists however, better accommodate the addition of a new vertex because all you have to do is simply add it to the end of the current node array or edge array which takes O(1) time. Removing a vertex from an Adjacency Matrix will be O(1) time because all you need to do is access the row column combination of the edge and set the value to either 0 or null depending on how you implemented the matrix. This is also why add edge and get weight are also O(1) time. Removing an edge from an Adjacency List is a little more complicated because you have to iterate through each edge node to find the edge you are looking to remove. this causes the running time to be O(E). An Adjacency Matrix has a major flaw when it comes to size. The size of the matrix will always be O(V^2) which can become a major concern if you are using a matrix for a large number of vertices. With that being said, if you are working with a large number of data it would be a better option to use an Adjacency List because it only uses O(V + E) space. 

					| Adjacency List  |   Adjacency Matrix   
			——————————————————————————————————————————————————————————
			add Vertex	|	O(1)	  |	O(V^2)
			——————————————————————————————————————————————————————————	
			add Edge	|	O(1)	  |	O(1)
			——————————————————————————————————————————————————————————
			Remove Edge	|	O(E)	  |	O(1)
			——————————————————————————————————————————————————————————
			Get Weight	|	O(V)	  |	O(1)
			————————————————————————————————————————————————————————————
			Space		|	O(V + E)  |	O(V^2)


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Define/describe each of the following terms, as they apply to memory management in C++

* The call stack (not to be confused with the stack data structure!) - the block of RAM that is used to store parameters and local variables. Also the stack keeps track of a function’s call to another function if it is needed to return a value.
* The heap (not to be confused with the heap data structure!)- a block of RAM that is used to store dynamic variables created by the keyword ‘new’. 

* Address - An objects location in memory. 

* Pointer - a variable that can hold an address. 

Answer the following questions about memory management and dynamic variables

* What is a memory leak, and why is it bad? 

When memory is allocated but not released. This will cause the application to consume memory and reduce the available memory for other applications which could eventually use all of the RAM. This would make the computer start to use the hard drive for storing data.
  
* What is a dangling pointer (or dangling reference), and why is it dangerous?

A dangling pointer is a pointer that no longer points to a valid destination. Dangling Pointers normally occur when the destructor is called and the pointer is not assigned a new value. They are potentially dangerous because these can eventually crash your program or may be a security risk as hackers can access this pointer and assign it to a piece of malicious code. 

* What is a destructor, and why are they necessary (in C++) to prevent memory leaks? Why *aren't* they necessary in Java? 

You need a class destructor because C++ does not know when you are done with a class or an instance of that class. A destructor is a function that is automatically called when you are done with the object. It is used to free up any memory that was created by the class. In Java the instance of the class would be automatically deleted once your program was done using it, also known as automatic garbage collection.
5 - Create collection classes using templates in C++
----
* What is the main benefit of using templates when creating collection classes?

Using a template when creating a collection class allows you to write one class that can handle any type of data the user may enter into your collection class. This way a class can be reused to handle string inputs and int inputs without having to be rewritten. By doing this you eliminate the difficulty of trying to accommodate for every type of data the user may enter. 

* In normal C++ code the .h file contains the declarations, and the .cpp file contains implementations. Explain why this isn't the case with template-based collection classes.

You are unable to do this because when you use a template it allows for any data type to be entered. When using a template the compiler will have to create a new version of your class which means new function declarations and definitions for each function. If you implemented the function in a separate .cpp file, the compiler wouldn’t know where to find the implementation for the new functions it created because the .cpp file has already been compiled and won’t be able to add new information to the file. To avoid this you include the implementation in the .hpp file so whenever you #include that .hpp file all of the implementation will be included and compiled in the .cpp file.  

20 - Using time and space analysis, justify the selection of a data structure for a given application
----
TODO: Answer the following questions about choosing data structures. (5 points each)

* If I needed a data structure to store a set of strings, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. (Remember that a set doesn't have any order, and doesn't store duplicates. We can add items, remove items, and check to see if an item is already in the set.)

Based on the requirements of this question it seems we need to be able to add, remove, and check if a string exists. To this in the most efficient way possible, I would use a hash table for this question. Using this data structure we would be able to hash the string and place the string depending in the resulting index. This would make adding strings O(1) time. Similar to addition, Remove would be O(1) time because you would be able to hash the string given and, if a string exists at that value, delete that value. Lastly, if we wanted to check if a string exists at in the hash table, we would again hash the string and check the index to see if it contains the string we are looking for. This can be done at O(1) or constant time. Also because we are using a hash table it would not allow for duplicates which is what is required by this question. This is what makes a hash table the best choice for this problem. If there were other requirements such as find the next/prev of a certain string or find the max/min values, I would definitely choose a different data structure because these functions do not run as efficiently with a hash table. If these were part of the question I would consider using a BST.  


* If I needed a data structure to store a grocery list, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why. 

When I think of a grocery list I have the same vision that you do. I like to make sure everything from the same section are grouped together so I am not running around like a chicken with my head cut off. I also like to keep open spaces in case I remember something once I get to the store. With that being said, I would use a Doubly-Linked List for making a grocery list. I think this is most fitting for the situation because if you wanted to add or remove an item from the list once you got to the store the action would be performed in O(1) time. Also if you wanted to leave empty space in your list you could do that in one of two ways: 1) by simply just doing “list surgery” once you find out that you forgot something or 2) leaving dummyNodes in the places where you feel you might have forgot something then add a value to the dummyNode once you remember what you forgot. Also you will not have to worry about the original size of your list because there will not be a grow function or limitation on the number of items in the List. 

Another possibility is that you could also make the first list be the sections of the grocery list. Then have the second linked list (the buckets) be a list of the items that you need in each section. As discussed above, add and remove would be done in O(1) time, and it would make the list work the way that you described in class. 

* If I needed a data structure to store student records so that I could look students up by Banner number, which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

By reading this question I am going to assume that the most important function of the data structure is the ability to look up students. If this is the case, I would use a hash table with the key being the students banner number and the value being either a custom class with the students information or simply just a GPA value or anything you would like. A hash table would allow you to find a student in O(1) time; something that no other data structure can do for you. The closest running time to that is the BST run time of O(log n). I can also assume that adding a student and removing a students would be an important function to the data structure. This is an easy task for a hash table because if every student has a unique banner number and we implement a good hash function/pick the correct size for the array there would be minimal collision in the hash table. This would allow for adding a student and removing a student to work at O(1) time. With these running times in mind and no other functions really being necessary for this problem, I cannot see another data structure being better to solve this problem. Again, if you needed more functionality from the data structure such as the next or previous student from the given banner number, then I would have to consider other data structures, but with my assumptions, there is no better data structure than a hash table for this question.   

* Imagine that I'm implementing a network router. It needs to keep a queue of packets waiting to be sent out over the network, but this queue need a special ability: Different companies are going to pay me different amounts of money, and the packets from the highest paying company should be sent out first. That is, if company X paid 20 and company Y paid 10, then X's packets always get sent before Y's packets. Y only gets to send packets if X doesn't have any waiting. Which data structure (or data structures) that we learned this semester would be most appropriate? Carefully explain why.

For this problem in particular, I am would say that a heap is the best data structure. Initially looking at this problem it seems that companies can have multiple packages waiting to be delivered and that companies could possible pay the same amount for 2 different packages. So because this could be concern, I would make it so that my heap could have duplicate keys. The key would be how much the company paid for the package. This data structure would make deciding which package to send easy because all you would have to do is send the package that is at the top of the heap, which would take O(1) time or O(log n) time if you wanted to remove it after delivering it. This would work because, for example, if you have a company that ordered a package for 5 dollars and then another company comes along and pays 10 dollars for a package you would add that 10 dollar package to the heap, but you would have to make sure to bubble up the 10 dollar package because its key could be larger than the previously entered keys above it and break the heap rule. After bubbling up, the top of the heap would now be 10 dollars which would work as the question states that it should. Once the 10 dollar package is shipped and removed from the heap, the 5 dollar package would return to the top of the heap and be ready to be sent off next. The only other function that I could see being used in this situation would be to add a new package to the heap which will always be done in O(log n) time. Another reason a heap is the best option is because it keeps our packages in order based on the amount the company paid for the package (the priority). If we used any other data structure we would have to call a sort function which would be a O(n) run time function. This would drastically slow down the operation of the program and we don’t want that! 
