# Data Structures and Algorithms (DSA) Notes

## 1. Arrays

Arrays are fundamental data structures that store elements of the same type in contiguous memory locations.

### Key Characteristics:
- **Access Time**: O(1) for element retrieval by index
- **Memory Allocation**: 
  - Dynamic in languages like Python and JavaScript
  - Static in languages like C

### Comparison with Linked Lists:
- Arrays require contiguous memory allocation
- Linked Lists are dynamic and can grow as needed

### Common Issues:
- **Array Index Out of Bounds Exception**: Occurs when accessing an element at an invalid index (negative or beyond array size)

### Techniques:
- **In-place Array Reversal**: 
  - Use two pointers (start and end)
  - Swap elements until pointers meet in the middle
  - Time Complexity: O(n), Space Complexity: O(1)

### Advantages and Disadvantages:
- **Advantages**: 
  - Constant time access
  - Simple implementation
  - Efficient storage for contiguous data
- **Disadvantages**: 
  - Fixed size (in some languages)
  - Inefficient for insertions and deletions, especially in the middle

### Additional Array Operations:
- **Searching**: Linear search O(n), Binary search O(log n) for sorted arrays
- **Sorting**: Various algorithms like QuickSort, MergeSort, etc.
- **Rotation**: Shifting elements by a certain number of positions

## 2. Linked Lists

A linear data structure where elements are stored in nodes, each pointing to the next node in the sequence.

### Types:
1. Singly Linked List: Each node points to the next node
2. Doubly Linked List: Each node points to both next and previous nodes
3. Circular Linked List: Last node points back to the first node

### Advantages:
- Dynamic memory allocation
- Efficient insertion and deletion
- Can represent complex data structures
- Useful for implementing queues and stacks
- Applicable in memory management and caching
- Facilitates garbage collection

### Time Complexity:
- **Insertion**:
  - At beginning: O(1)
  - At end: O(n) for singly, O(1) for doubly if tail is maintained
  - At specific position: O(n)
- **Deletion**:
  - At beginning: O(1)
  - At end: O(n) for singly, O(1) for doubly if tail is maintained
  - At specific position: O(n)
- **Search**: O(n)
- **Traversal**: O(n)

### Comparison with Dynamic Arrays:

#### Dynamic Arrays:
- **Advantages**:
  - Fast random access: O(1)
  - Efficient for large data sets
  - Contiguous memory allocation
- **Disadvantages**:
  - Slow insertion/deletion in middle: O(n)
  - Fixed size, potential memory waste or reallocation

#### Linked Lists:
- **Advantages**:
  - Efficient insertion/deletion in middle: O(1)
  - Dynamic growth and shrinkage
  - Flexible for complex data structures
- **Disadvantages**:
  - Slow random access: O(n)
  - Higher memory overhead due to pointers
  - Less cache-friendly

### Common Linked List Operations:
- Reversing a linked list
- Detecting cycles (Floyd's Cycle-Finding Algorithm)
- Finding the middle element
- Merging two sorted linked lists

## 3. Stack

A linear data structure following the Last-In-First-Out (LIFO) principle.

### Operations:
- Push: Insert an element
- Pop: Remove the top element
- Peek: View the top element

### Implementation:
- Can be implemented using arrays or linked lists

### Time Complexity:
- Push, Pop, Peek: O(1)

### Applications:
- Function calls and recursion
- Expression evaluation
- Parsing
- Undo mechanisms in software
- Depth-First Search (DFS) in graph algorithms
- Backtracking algorithms

### Common Issues:
- Stack Overflow: Exceeding allocated memory
- Stack Underflow: Attempting to pop from an empty stack

### Related Concepts:
- Postfix Expression: Operator follows operands
- Infix to Postfix conversion
- Balancing parentheses in expressions

## 4. Queue

A linear data structure following the First-In-First-Out (FIFO) principle.

### Operations:
- Enqueue: Add an element to the rear
- Dequeue: Remove an element from the front

### Implementation:
- Array-based: Use front and rear pointers
- Linked List-based: Use head and tail pointers
- Circular Queue: Efficient use of fixed-size array

### Time Complexity:
- Enqueue: O(1)
- Dequeue: O(1) for simple and circular queues, O(log n) for priority queues

### Applications:
- Task scheduling
- Message passing
- Simulation of real-world scenarios
- Breadth-First Search (BFS) in graph algorithms
- Cache implementation

### Variations:
- Priority Queue: Elements dequeued based on priority
- Double-ended Queue (Deque): Insertions and deletions allowed at both ends

### Advanced Queue Concepts:
- Queue using Stacks: Implement a queue using two stacks
- Circular Buffer: Fixed-size queue with wraparound

## 5. Heap

A complete binary tree satisfying the heap property.

### Types:
- Max-heap: Root node has the maximum value
- Min-heap: Root node has the minimum value

### Operations:
- Insertion (Heapify-up)
- Deletion (Heapify-down)
- Peek (Get max/min element)

### Time Complexity:
- Insertion: O(log n)
- Deletion: O(log n)
- Finding min/max element: O(1)
- Building a heap from an array: O(n)

### Applications:
- Heap Sort
- Priority Queues
- Finding kth largest/smallest element
- Median maintenance

### Implementation:
- Usually implemented using arrays
- Parent and child relationships can be calculated using indices

## 6. Hash Data Structure

Stores key-value pairs, using hashed keys to determine value locations.

### Key Concepts:
- Hash Function: Converts keys into array indices
- Hash Collision: When two different keys hash to the same value
- Load Factor: Ratio of occupied slots to total slots

### Collision Resolution:
- Chaining: Each array slot contains a linked list of elements
- Open Addressing: Probing for next available slot (Linear, Quadratic, Double Hashing)

### Time Complexity:
- Average case: O(1) for insertion, deletion, and search
- Worst case: O(n) when many collisions occur

### Applications:
- Implementing associative arrays
- Database indexing
- Caching
- Symbol tables in compilers

## 7. Tree

A non-linear data structure with nodes connected by edges.

### Types:
- Binary Tree: Each node has at most two children
- Binary Search Tree (BST): Left subtree contains smaller values, right subtree larger values
- AVL Tree: Self-balancing BST
- Red-Black Tree: Self-balancing BST with good worst-case guarantees
- B-Tree: Self-balancing tree data structure that maintains sorted data and allows searches, sequential access, insertions, and deletions in logarithmic time

### Basic Operations:
- Insertion
- Deletion
- Traversal (preorder, inorder, postorder, level-order)
- Searching

### When to Use:
- Ideal for hierarchical data
- Efficient for ordered searching
- Representing file systems, organization structures

### Traversal Methods:
- Preorder: Root, Left, Right
- Inorder: Left, Root, Right
- Postorder: Left, Right, Root
- Level-order: Breadth-first traversal

### Special Applications:
- Converting Binary Search Tree to Sorted Array: Use inorder traversal
- Lowest Common Ancestor (LCA) problem
- Balancing a BST

### Advanced Tree Concepts:
- Trie (Prefix Tree): Efficient for string search and prefix matching
- Segment Tree: Used for range queries and updates
- Fenwick Tree (Binary Indexed Tree): Efficient for range sum queries and updates

## 8. Graph

A non-linear data structure consisting of vertices and edges.

### Representations:
- Adjacency Matrix
- Adjacency List

### Types:
- Directed vs Undirected
- Weighted vs Unweighted
- Cyclic vs Acyclic

### Basic Algorithms:
- Depth-First Search (DFS)
- Breadth-First Search (BFS)
- Topological Sorting

### Advanced Algorithms:
- Dijkstra's Algorithm: Shortest path in weighted graphs
- Bellman-Ford Algorithm: Shortest path with negative weights
- Kruskal's and Prim's Algorithms: Minimum Spanning Tree
- Floyd-Warshall Algorithm: All pairs shortest path

### Applications:
- Social Networks
- Maps and Navigation
- Recommendation Systems
- Network Flow Problems

## 9. Dynamic Programming

An algorithmic paradigm that solves complex problems by breaking them down into simpler subproblems.

### Key Concepts:
- Optimal Substructure
- Overlapping Subproblems

### Approaches:
- Top-down (Memoization)
- Bottom-up (Tabulation)

### Classic Problems:
- Fibonacci Sequence
- Knapsack Problem
- Longest Common Subsequence
- Matrix Chain Multiplication

### Applications:
- Resource Allocation
- Sequence Alignment in Bioinformatics
- Optimal Binary Search Trees

## 10. Greedy Algorithms

Algorithmic paradigm that makes the locally optimal choice at each step.

### Characteristics:
- Makes the best immediate choice
- May not always lead to global optimum

### Classic Problems:
- Activity Selection
- Huffman Coding
- Fractional Knapsack

### Applications:
- Scheduling Problems
- Data Compression
- Minimum Spanning Trees (Kruskal's, Prim's)

