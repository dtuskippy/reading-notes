## Data Structures and Algorithms Reading Notes
<p>A massive read (and watch) about the ultra-important topic of data structures and algoritms.</p>

### Basic Recursion

* Recursion is when a function calls itself, and is used to make a function more clear (i.e. easier to understand), despite often times providing no performance benefits.
* Recursion is split into 2 cases to avoid the possibility of spiraling into an infinite loop:
    * Base Case: When the function doesn't call itself again, so it doesn't go into an infinite loop.
    * Recursive Case: When the function calls itself.
* When a recursive spirals into an infinite loop, control+C will kill it.

### Data Structures in 15 Minutes

* Compound data: data items grouped together (multiple price points for a stock price), and this is stored in a data structure.
* Big O Notation: how a data structured is measured at doing a specific thing efficiently -- basically a measure of how well an operation scales. 
* Linked list
    * Node: atomic unit of a link list, and contains:
        * Value: e.g. an integer
        * Pointer: Points you to next node in chain
    * Head: first node in list
    * Tail: last node in list (no pointer)
    * Pros: adding and deleting new items (can change where next pointer is pointing)
    * Cons: retrieval or searching (each node is only aware of the node next to it)
* Arrays
    * A continuous block of cells in computer memory, which allows itself to be great indexing data
    * Pros: makes it easy to retrieve items
    * Cons: as an array increases in size, may have to me be moved in memory because it starts to 'collide' with other items in memory
        * In lower level languages (aside from JS, Python), this is why you must declare the size of an array in advance
* Hash table
    * Holds key-value pairs -- an object in JS; dictionary in Python
    * Hashing function: under the hood, works a lot like an array -- key gets run through a hashing function that spits out a memory location
    * Pros: good at retrieving and add / remove; different than array in that memory locations (spit out by hashing function) do NOT have to be next to each otherj
    * Cons: 'collisions' can occur, where hashing functions maps 2 different keys to same location in memory
* Stack and Queue
    * Both built on top of arrays, with different features
    * Stack: LIFO data structure (think cafeteria trays)
        * Push: adding
        * Pop: removing
        * Call stack: keeps track of all activity
        * DFS (Depth-First Search): algorithm stack used with
    * Queue (FIFO -- just like standing in line)
        * Enqueue: adding item to end.
        * Dequeue: removing item from front.
        * BFS (Breadth-First Search): algorithm queue used with
    * Pros: add and remove
    * Cons: limited use cases
* Graphs and Trees
    * Graph: entire field in CompSci called Graph Theory; similar to a linked list, where there are nodes pointing to other nodes, except that in this case, the pointers are called edges
        * Edges: can also have weights assigned to them (gave example of NY and Boston, road between them is edge, and distance in miles between them is the weight of that edge)
        * Very big in social media - 'social graph'
    * Trees: special kind of hierarchical graph in which the data expands out in one direction
        * Can be used to represent a family tree, with parent child relationships
        * HTML tree with nested elements
    * Binary Search Tree: specific type of tree with very specific rules that allow for searching really efficiently
        * Each node can have max 2 children left and right
            * Left has to be < Node
            * Right has to be > Node
        * So if you had a node of 5, and looking for 7, would know it is to the right or not in the tree at all (i.e. wouldn't do unnecessary searching)
        * Pros: efficient search
        * Cons: if you add elements in a weird order (e.g. too many to the left or right), and can get unbalanced, all the advantages are wiped out

### Big O Explained
* Big O: 
    * Basically, algorithmic efficiency.
    * An equation that describes how the runtime scales with respect to some input variables
* O(1): constant time respect to the size of the input, e.g. the pigeon in her South Africa example carrying a USB stick, i.e. doesn't take longer with more input.
* O(n): scales linearly with respect to to the size of the input, e.g. the actual internet connection between offices in her South Africa example, i.e. twice the amount of data will roughly take twice the amount of time to deliver.
* Example 1: function that checks for an element in the array => O(n), where n is the is the size of the array.
* Example 2: function that checks for all pairs of values in the array => O(n)^2 where n is the size of the array.
* Example 3: mow grass in a SQUARE plot of land 
    Option 1: O(a), where a is the area of grass  [*Note: can use a as a variable, n is just a variable name]
    Option 2: O(s^2), where is length of a side of the plot of land
* 4 Rules:
    1. Different steps in your algorithm get added up, e.g. 2 steps: O(a) + O(b)
    2. Drop constants, e.g. two different functions looking for MinMax in an array would not be O(2n), would be O(n), where n is the size of the array
    3. Different inputs => different variables, e.g. function looking for intersection of elements between arrayA and arrayB would not be O(n^2), would be O(a*b), where a and b represent the length of the respective arrays
    4. Drop non-dominant terms, e.g. function where both O(n) and O(n^2) are run, would NOT be O(n + n^2), would be O(n^2)
        

### Basic Data Structures
8 commonly used data structures every programmer must know:
1. Arrays
    * An array is a structure of fixed-size, which can hold items of the same data type. 
    * It can be an array of integers, an array of floating-point numbers, an array of strings or even an array of arrays (such as 2-dimensional arrays). 
    * Arrays are indexed, meaning that random access is possible.
    * Array operations
       * Traverse: Go through the elements and print them.
       * Search: Search for an element in the array. You can search the element by its value or its index
       * Update: Update the value of an existing element at a given index
    * Applications
       * Used as the building blocks to build other data structures such as array lists, heaps, hash tables, vectors and matrices.
       * Used for different sorting algorithms such as insertion sort, quick sort, bubble sort and merge sort.
2. Linked Lists
    * A linked list is a sequential structure that consists of a sequence of items in linear order which are linked to each other. 
    * Hence, you have to access data sequentially and random access is not possible. 
    * Linked lists provide a simple and flexible representation of dynamic sets.
    * Key terms:
        * Elements in a linked list are known as nodes.
        * Each node contains a key and a pointer to its successor node, known as next.
        * The attribute named head points to the first element of the linked list.
        * The last element of the linked list is known as the tail.
    * Linked List types:
        * Singly linked list — Traversal of items can be done in the forward direction only.
        * Doubly linked list — Traversal of items can be done in both forward and backward directions. Nodes consist of an additional pointer known as prev, pointing to the previous node.
        * Circular linked lists — Linked lists where the prev pointer of the head points to the tail and the next pointer of the tail points to the head.
    * Linked list operations
        * Search: Find the first element with the key k in the given linked list by a simple linear search and returns a pointer to this element
        * Insert: Insert a key to the linked list. An insertion can be done in 3 different ways; insert at the beginning of the list, insert at the end of the list and insert in the middle of the list.
        * Delete: Removes an element x from a given linked list. You cannot delete a node by a single step. A deletion can be done in 3 different ways; delete from the beginning of the list, delete from the end of the list and delete from the middle of the list.
    * Applications of linked lists
        * Used for symbol table management in compiler design.
        * Used in switching between programs using Alt + Tab (implemented using Circular Linked List).
3. Stacks
    * A stack is a LIFO (Last In First Out — the element placed at last can be accessed at first) structure which can be commonly found in many programming languages. 
    * This structure is named as “stack” because it resembles a real-world stack — a stack of plates.
    * Stack operations
        * Push: Insert an element on to the top of the stack.
        * Pop: Delete the topmost element and return it.
    * Furthermore, the following additional functions are provided for a stack in order to check its status.
        * Peek: Return the top element of the stack without deleting it.
        * isEmpty: Check if the stack is empty.
        * isFull: Check if the stack is full.
    * Applications of stacks
        * Used for expression evaluation (e.g.: shunting-yard algorithm for parsing and evaluating mathematical expressions).
        * Used to implement function calls in recursion programming.
4. Queues
    * A queue is a FIFO (First In First Out — the element placed at first can be accessed at first) structure which can be commonly found in many programming languages. This structure is named as “queue” because it resembles a real-world queue — people waiting in a queue.
    * Queue operations
        * Enqueue: Insert an element to the end of the queue.
        * Dequeue: Delete the element from the beginning of the queue.
    * Applications of queues
        * Used to manage threads in multithreading.
        * Used to implement queuing systems (e.g.: priority queues).
5. Hash Tables
    * A Hash Table is a data structure that stores values which have keys associated with each of them.
        * Furthermore, it supports lookup efficiently if we know the key associated with the value.
        * Hence it is very efficient in inserting and searching, irrespective of the size of the data.
    * Direct Addressing uses the one-to-one mapping between the values and keys when storing in a table.
        * However, there is a problem with this approach when there is a large number of key-value pairs.
        * The table will be huge with so many records and may be impractical or even impossible to be stored, given the memory available on a typical computer. To avoid this issue we use hash tables.
    * Hash Functions are used to overcome the aforementioned problem in direct addressing.
        * In direct accessing, a value with key k is stored in the slot k.
        * Using the hash function, we calculate the index of the table (slot) to which each value goes.
        * The value calculated using the hash function for a given key is called the hash value which indicates the index of the table to which the value is mapped.
        * Collision can arise when the hash function generates the same index for more than one key. We can resolve collisions by selecting a suitable hash function and use techniques such as chaining and open addressing.
    * Applications of hash tables
        * Used to implement database indexes.
        * Used to implement associative arrays.
        * Used to implement the “set” data structure.
6. Trees
    * A tree is a hierarchical structure where data is organized hierarchically and are linked together. This structure is different from a linked list whereas, in a linked list, items are linked in a linear order.
    * Binary Search Trees, is a binary tree where data is organized in a hierarchical structure. This data structure stores values in sorted order -- Every node in a binary search tree comprises the following attributes:
        * key: The value stored in the node.
        * left: The pointer to the left child.
        * right: The pointer to the right child.
        * p: The pointer to the parent node.
    * A binary search tree exhibits a unique property that distinguishes it from other trees. This property is known as the binary-search-tree property.
        * Let x be a node in a binary search tree.
        * If y is a node in the left subtree of x, then y.key ≤ x.key
        * If y is a node in the right subtree of x, then y.key ≥ x.key
    * Applications of trees
        * Binary Trees: Used to implement expression parsers and expression solvers.
        * Binary Search Tree: used in many search applications where data are constantly entering and leaving.
        * Heaps: used by JVM (Java Virtual Machine) to store Java objects.
        * Treaps: used in wireless networking.
7. Heaps
    * A Heap is a special case of a binary tree where the parent nodes are compared to their children with their values and are arranged accordingly.
    * Heaps can be of 2 types.
        * Min Heap — the key of the parent is less than or equal to those of its children. This is called the min-heap property. The root will contain the minimum value of the heap.
        * Max Heap — the key of the parent is greater than or equal to those of its children. This is called the max-heap property. The root will contain the maximum value of the heap.
    * Applications of heaps
        * Used in heapsort algorithm.
        * Used to implement priority queues as the priority values can be ordered according to the heap property where the heap can  be implemented using an array.
        * Queue functions can be implemented using heaps within O(log n) time.
        Used to find the kᵗʰ smallest (or largest) value in a given array.
8. Graphs
    * A graph consists of a finite set of vertices or nodes and a set of edges connecting these vertices.
        * The order of a graph is the number of vertices in the graph. The size of a graph is the number of edges in the graph.
        * Two nodes are said to be adjacent if they are connected to each other by the same edge.
    * Directed graphs
        * A graph G is said to be a directed graph if all its edges have a direction indicating what is the start vertex and what is the end vertex.
        * We say that (u, v) is incident from or leaves vertex u and is incident to or enters vertex v.
        * Self-loops: Edges from a vertex to itself.
    * Undirected graphs
        * A graph G is said to be an undirected graph if all its edges have no direction. It can go in both ways between the two vertices.
        * If a vertex is not connected to any other node in the graph, it is said to be isolated.
    * Applications of graphs
        * Used to represent social media networks. Each user is a vertex, and when users connect they create an edge.
        * Used to represent web pages and links by search engines. Web pages on the internet are linked to each other by hyperlinks. Each page is a vertex and the hyperlink between two pages is an edge. Used for Page Ranking in Google.
        * Used to represent locations and routes in GPS. Locations are vertices and the routes connecting locations are edges. Used to calculate the shortest route between two locations.


### Why Big O
* Big-O is just the name of the notation used to describe how efficient an algorithm is, and it's whole point is to measure the efficienty of algorithms, because with algorithms, efficiency is literally THE point.
* For example, a function returns the first carrot it finds in a list of vegetables:
    * In the worst case, the code might need to check every single vegetable in the list before it finds a carrot. 
    * Another way of saying the same thing is “the time complexity of this function is O(n).” 
    * The letter “O” can just be thought of as shorthand for the rough “order” of magnitude of operations it takes to run the function, while “n” represents the possible number of vegetables passed in each time. 
    * So O(n) is just a math-style way of describing roughly how long (in the worst case) a function will take in terms of the number of inputs passed in.

### Discussion Questions

1. What is 1 of the more important things you should consider when deciding which data structure is best suited to solve a particular problem?
    * Understanding basic requirements of the application, like the expected inputs and outputs, scale and performance expectations.
2. How can we ensure that we’ll avoid an infinite recursive call stack?
    * To prevent infinite recursion, you need at least one branch (i.e. of an if/else statement) that does not make a recursive call. Branches without recursive calls are called base cases; branches with recursive calls are called recursive cases.

### Things I want to know more about

1. This is a massive intake of information, that clearly needs a lot more time and experience to digest properly - i.e. things I want to know more about: all of it. 
