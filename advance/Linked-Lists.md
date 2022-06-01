# **Linked Lists**
>## ***Big O: Analysis of Algorithm Efficiency***
#### Big O(oh) notation is used to describe the efficiency of an algorithm or function.
#### Big O’s role in algorithm efficiency is to describe the Worst Case of efficiency an algorithm can have in performing it’s job. It specifically looks at the factors mentioned above, which we often refer to as Space and Time.In order to analyze these limiting factors, we should consider 4 Key Areas for analysis:
### `Input Size`
#### Input Size refers to the size of the parameter values that are read by the algorithm. This does not simply refer to the number of parameters an algorithm reads, but takes into account the size of each parameter value as well.
### `Units of Measurement`
### `Orders of Growth`
### `Best Case, Worst Case, and Average Case`
#### -Worst Case: The efficiency for the worst possible input of size n
#### -Best Case: The efficiency for the best possible input of size n
#### Average Case: The efficiency for a “typical” or “random” input of size n
### **[Reference](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html)**
***
>## ***Linked Lists***
#### A Linked List is a sequence of Nodes that are connected/linked to each other. The most defining feature of a Linked List is that each Node references the next Node in the link.

#### There are two types of Linked List - Singly and Doubly.

### `Traversal`
#### When traversing a linked list, you are not able to use a foreach or for loop. We depend on the Next value in each node to guide us where the next reference is pointing. The Next property is exceptionally important because it will lead us where the next node is and allow us to extract the data appropriately.
#### `Traversal Big O`
#### The Big O of time for Includes would be O(n). This is because, at its worse case, the node we are looking for will be the very last node in the linked list. n represents the number of nodes in the linked list.

#### The Big O of space for Includes would be O(1). This is because there is no additional space being used than what is already given to us with the linked list input.
### `Adding a Node`
#### Adding O(1)
#### Order of operations is extremely important when it comes to working with a Linked List. What I mean by this is you must be careful that all references to each link/node is properly assigned.

#### If we want to add a node with an O(1) efficiency, we have to replace the current Head of the linked list with the new node, without losing the reference to the next node in the list.
### `Print Out Nodes`
#### Printing out all of the nodes in a Linked List is very similar to what we did in the Includes() method. This is because we are leveraging our Current node and a while loop to traverse through the existing linked list.
### **[Reference1](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)**
### **[Reference2](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)**
### **[Reference3](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)**
