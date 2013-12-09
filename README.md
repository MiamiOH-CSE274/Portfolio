Portfolio
=========

7 - Create an implementation of a Queue
----

To show suffecient knowledge of a Queue I will use my 03_Queue_Lab the link is https://github.com/kosirjm/03_Queue_Lab

You can see demonstration of the test code working at https://www.youtube.com/watch?v=sWNuNIQbCug

7 - Create an implementation of a List
----

To show suffecient knowledge of a List I will use my 04_Linked_List_Lab the link is https://github.com/kosirjm/04_Linked_List_Lab

You can see demonstration of the test code working at https://www.youtube.com/watch?v=-BxVjXBI6Y8

7 - Create an implementation of a Binary Search Tree
----

To show suffecient knowledge of a List I will use my 06_BST_Lab the link is https://github.com/kosirjm/06_BST_Lab

You can see demonstration of the test code working at https://www.youtube.com/watch?v=uv2G1KAsAvo

7 - Create an implementaiton of a Hash Table
----

To show suffecient knowledge of a Hash I will use my 05_Hash_Lab the link is https://github.com/kosirjm/05_Hash_Lab

You can see demonstration of the test code working at http://www.youtube.com/watch?v=lwgKVubCIVI

7 - Create an implementation of a Heap
----

To show suffecient knowledge of a List I will use my 07_heap_Lab the link is https://github.com/kosirjm/07_Heap_Lab

You can see demonstration of the test code working at https://www.youtube.com/watch?v=_U_GRiGsd0o

7 - Create an implementation of either Adjanency Lists or Adjacency Matrices
----
To show suffecient knowledge of a Graph I will use my 08_Graph_Lab the link is https://github.com/kosirjm/08_Graph_Lab

You can see demonstration of the test code working at http://www.youtube.com/watch?v=bEvpcSQRcLQ

7 - Implement graph algorithms
----

To show suffecient knowledge of a Graph  algorithm I will use my 08_Graph_Lab the link is https://github.com/kosirjm/08_Graph_Lab I have added a BFS function to the lab (While doing it changed the Graph.h file 
as well to add the BFS function 

There is no video demostration for this function


21 - Determine space and time requirements of common data structure methods
-----
<b>Queue</b> (We did a circular Queue https://github.com/kosirjm/03_Queue_Lab)
              
          Add - Took a time complexity of O(1) typically this is because we were adding the items
                to the next avaliable spot in line.  Since we knew what that was because we knew 
                the number of items which was kept track of everytime we added and removed an item,
                we could simply just add the item to that position with out looping through and looking
                for an empty spot.  Still, if the number of items exceeded the size of the list grow()
                had to be called and our time complexity is O(n) since we have to loop through to copy
                all the items in the list to a new temp queue.
                    
          Remove - Took time complexity of O(1), we simply just removed the item from the last spot in the list
                   and subtracted one from our number of items counter.
                       
          Grow - Took O(n) time complexity.  This is due to the fact of iterating through the items in the list with
                 a for loop to copy them over to a temp array so we could resize the old array.
                     
          Size - Size is an O(10 time complexity.  This is because everytime we remove or add an item we have a 
                 counter which is incremented appropriately.
                     
                     
<b>Linked List</b> (We did a Doubly-Linked list https://github.com/kosirjm/04_Linked_List_Lab)
                    
        Find - Find is an O(n) complexity for doubly-linked-list it must iterate though all of the items 
               using a loop to see if the item matches the search.  This is of course unless the item is the
               first or last item then it is an O(1).
               
        Set -  Is the same as find O(n) unless it is the first or last item then it is O(1).  This is because you
               must find the item and then add the item which is only O(1).
              
        Add - In our program it was O(n) unless the item was in the first or last position. This is because the find                  function was called to remove a certain index.
              
        Remove - In our program it was O(n) unless the item was in the first or last position. This is because the find                  function was called to remove a certain index.
        
        Size - Was O(1) this is because the number of items was tracked as we addded or subtracted the items from the                  list giving us the ability to return the value without counting the items by using a loop.
        
        
<b>Binary Search Tree</b> (https://github.com/kosirjm/06_BST_Lab)
          
        (h = The hieght of the tree.  In worst case h = n being that all nodes just go one way creating
        an unbalanced tree.  Best case for h is log(n) being that the tree is perfectly balanced)
        
        Add - The time complexity for this is function was O(h).  This is because you must traverse down the 
              tree recursively in the correct path to find the place correct place which equals NULL to input the item. 
        
        Remove - The time complexity for this is function was O(h).  This is because you must traverse down the 
                 tree recursively in the correct direction to find the item which must be remove, which at worst is at                   the very bottom
              
        Prev - The time complexity for this is function was O(h).  This is because you must traverse down the 
               tree recursively in the correct path to find the right function that is less than the key given to you,                 which at worst is at the very bottom
        
        Next - The time complexity for this is function was O(h).  This is because you must traverse down the 
               tree recursively in the correct path to find the right function that is greater than the key given to                   you, which at worst is at the very bottom.
          
        Find - The time complexity for this is function was O(h).  This is because you must traverse down the 
               tree recursively in the correct path to find the right function that is equal to the key given to                       you, which at worst is at the very bottom.
          
        KeyExists - The time complexity for this is function was O(h).  This is because you must traverse down the 
                    tree recursively in the correct path to find the right function that is equal to the key given to                       you, which at worst it does not exist therefor would go all the way to the bottom and reach NULL.
          
        Max - The time complexity for this is function was O(h).  This is because you must traverse down the 
              tree recursively to the farthest item on the right side of the tree.  This function is always O(h)
              because it does not end until it hits NULL.
          
        Min - The time complexity for this is function was O(h).  This is because you must traverse down the 
              tree recursively to the farthest item on the left side of the tree.  This function is always O(h)
              because it does not end until it hits NULL.
      


5 - Describe memory management in C++, and correctly use dynamic variables, including destructors
----
Possible sources of evidence (do one):


5 - Create collection classes using templates in C++
----
Possible sources of evidence (do one):

* Any of the labs or projects, provided it uses templates in an interesting way.


30 - Using time and space analysis, justify the selection of a data structure for a given application
----
<b><u>Shuffle Project</u></b>


              For this project two choices of an ADT were given to us at the beginning, a linked list or a queue. In the   next few paragraphs I will talk about what I believe would be the better choice to use. First off they both can easily   be used to implement the structure, or movement, of shuffling a deck, so there is no issues there.  With linked         lists you are able to move, set, add, remove, and find items by a specific index, while in queues you cannot.  These    functions that the linked list offer are not needed.  In shuffling a deck there is no need to do anything to a          specific index or find a specific index
              With this in mind knowing that we do not need the special abilities that the linked lists give us let’s     look at   the time complexities of both ADTs.  All of the queues functions are of time complexity O(1), this            is of course if that when adding an item the number of items do not exceed the size of the queue, because then the      grow function   is called which is of time complexity O(n).  With this in mind a deck only had 52 cards there will      never be any more then that in the deck.  Therefor in this project using a queue would make it always O(1).             Manipulation of the items in the queue can be hard if you need to change a specific item or add or remove at a          specific index.  In this instance depending on how you would implement the items to shuffle, there should not be too    much resizing and calling certain indexes.
              On the other hand all the functions in our linked list are O(n) except for size() which is O(1).  Linked    lists are much easier to modify certain indexes as well as change the size of the list.  If you were doing   a lot of   that or needed it for whatever reason I would suggest the linked list.  Though if implemented correctly this should     not be needed and therefor the queue would be faster in all instances.  So as you can see the queue is the clear        winner to be chosen in this project.

              
<b><u>Shuffle Project</u></b>
