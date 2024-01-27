*Based on course materials by Marcin Sydow - Algorithms and Data Structures*

- [Correctness of an Algorithm](#correctness-of-an-algorithm)
	- [Introduction to Correctness](#introduction-to-correctness)
	- [Specification](#specification)
	- [Total vs. Partial Correctness](#total-vs-partial-correctness)
	- [Stop Property](#stop-property)
	- [Invariants](#invariants)
	- [Proving Correctness](#proving-correctness)
	- [Practical Application](#practical-application)
- [Complexity of an Algorithm](#complexity-of-an-algorithm)
	- [Understanding Complexity](#understanding-complexity)
	- [Dominating Operations](#dominating-operations)
	- [Time Complexity](#time-complexity)
	- [Space Complexity](#space-complexity)
	- [Asymptotic Notation](#asymptotic-notation)
	- [Practical Application](#practical-application-1)
	- [Advanced Concepts](#advanced-concepts)
- [Searching](#searching)
	- [Basic Concepts](#basic-concepts)
	- [Sequential and Skipping Algorithms](#sequential-and-skipping-algorithms)
	- [Binary Search](#binary-search)
	- [Positional Statistics](#positional-statistics)
	- [Tournament Algorithm](#tournament-algorithm)
	- [Partitioning and Hoare's Algorithm](#partitioning-and-hoares-algorithm)
	- [Practical Applications](#practical-applications)
	- [Advanced Concepts](#advanced-concepts-1)
- [Sorting Part 1](#sorting-part-1)
	- [General Understanding](#general-understanding)
	- [Selection Sort](#selection-sort)
	- [Insertion Sort](#insertion-sort)
	- [Merge Sort](#merge-sort)
	- [Algorithm Analysis](#algorithm-analysis)
	- [Practical Considerations](#practical-considerations)
	- [Advanced Topics](#advanced-topics)
- [Sorting Part 2](#sorting-part-2)
	- [QuickSort](#quicksort)
	- [CountSort](#countsort)
	- [RadixSort](#radixsort)
	- [Stability in Sorting](#stability-in-sorting)
	- [Lower Bound for Comparison-Based Sorting](#lower-bound-for-comparison-based-sorting)
	- [Comparative Analysis](#comparative-analysis)
	- [Practical Considerations](#practical-considerations-1)
- [Lists and arrays](#lists-and-arrays)
	- [Linked Lists](#linked-lists)
	- [Abstract Data Structures](#abstract-data-structures)
	- [Amortised Analysis](#amortised-analysis)
	- [Unbounded Arrays](#unbounded-arrays)
	- [Operations and Implementations](#operations-and-implementations)
	- [Dynamic Arrays](#dynamic-arrays)
	- [Comparison Between Data Structures](#comparison-between-data-structures)
- [Priority queue](#priority-queue)
	- [Priority Queue Basics](#priority-queue-basics)
	- [Naive Implementations](#naive-implementations)
	- [Binary Heap](#binary-heap)
	- [Binary Heap Operations](#binary-heap-operations)
	- [Heapify and Constructing a Binary Heap](#heapify-and-constructing-a-binary-heap)
	- [Binomial Heap](#binomial-heap)
	- [Binomial Heap Operations](#binomial-heap-operations)
	- [Advanced Topics](#advanced-topics-1)
	- [Practical Applications](#practical-applications-1)
- [Dictionary](#dictionary)
	- [Fundamental Concepts](#fundamental-concepts)
	- [Hash Tables](#hash-tables)
	- [Hash Functions](#hash-functions)
	- [Binary Search Trees (BST)](#binary-search-trees-bst)
	- [AVL Trees](#avl-trees)
	- [Self-organizing Trees](#self-organizing-trees)
	- [Ordered Dynamic Set Operations](#ordered-dynamic-set-operations)
	- [Advanced Topics](#advanced-topics-2)


# Correctness of an Algorithm        

## Introduction to Correctness
- What is the definition of the correctness of an algorithm?
- How does the concept of correctness relate to the input and output specifications of an algorithm?

## Specification
- What components make up a specification for an algorithm?
- Can you explain the difference between initial conditions and final conditions in an algorithm's specification?

## Total vs. Partial Correctness
- What is the difference between total correctness and partial correctness of an algorithm?
- Provide an example of an algorithm that is partially correct but not totally correct.

## Stop Property
- Define the stop property of an algorithm. Why is it important?
- How can you prove that an algorithm possesses the stop property?

## Invariants
- What is an invariant in the context of algorithms, and how is it used to prove correctness?
- Can you give an example of a loop invariant and explain how it helps in proving an algorithm's correctness?

## Proving Correctness
- What are the steps involved in proving the total correctness of an algorithm?
- How does proving the stop property differ from proving partial correctness?

## Practical Application
- Given a simple algorithm, can you identify its specification, prove its stop property, and establish its partial correctness?
- How would you approach finding a suitable loop invariant for a given algorithm?

# Complexity of an Algorithm

## Understanding Complexity
- What is meant by the 'complexity' of an algorithm?
- Distinguish between time complexity and space complexity.

## Dominating Operations
- Define 'dominating operations' in the context of algorithm complexity.
- How do you determine the dominating operations of an algorithm?

## Time Complexity
- What does time complexity measure in an algorithm?
- Explain the terms 'pessimistic time complexity' and 'average time complexity'.

## Space Complexity
- How is space complexity defined, and what does it measure?
- Why is space complexity considered platform-dependent?

## Asymptotic Notation
- What is asymptotic notation, and why is it used in algorithm analysis?
- Define the Big O notation and provide an example of its use.
- What does Big Theta (Θ) notation signify, and how does it differ from Big O?

## Practical Application
- Given a simple algorithm, how would you identify its dominating operations and determine its time complexity?
- For a provided function, express its complexity using Big O notation.

## Advanced Concepts
- Describe other flavors of asymptotic notation such as little o, Big Omega (Ω), and little omega (ω), and explain when each is used.
- Discuss the relevance of considering the limit of a function's growth rate to compare the ranks of functions.

These questions are designed to deepen your understanding of key concepts related to algorithm complexity, including how to measure and express the efficiency of algorithms in terms of time and space usage.

# Searching 

## Basic Concepts
- What is the divide and conquer strategy in algorithm design?
- Define the searching problem and its general specifications.

## Sequential and Skipping Algorithms
- Describe the sequential search algorithm and its time complexity.
- How does the skipping algorithm improve upon sequential search, and what is its limitation?

## Binary Search
- Explain the binary search algorithm. How does it utilize the divide and conquer approach?
- Discuss the time complexity and space requirements of binary search.

## Positional Statistics
- What is meant by 'k-th positional statistic' in a sequence?
- How does sorting affect the efficiency of searching for positional statistics?

## Tournament Algorithm
- Describe the tournament algorithm for finding the second smallest element. How does it work?
- Analyze the complexity of the tournament algorithm. Why is it considered efficient?

## Partitioning and Hoare's Algorithm
- What is the partition procedure, and how is it used in searching algorithms?
- Explain Hoare's algorithm for finding the k-th smallest element. What makes it efficient?

## Practical Applications
- How would you apply the partitioning technique to sort an array?
- Compare and contrast the efficiency of Hoare's algorithm to the tournament algorithm for finding the second smallest element.

## Advanced Concepts
- Discuss the implications of data not fitting into RAM for the binary search algorithm.
- How can the divide and conquer method be applied to improve the search for positional statistics beyond the k-th smallest element?

# Sorting Part 1 

## General Understanding
- What is the purpose of sorting in computer science, and why is it considered a fundamental operation?
- Describe the general input and output of a sorting algorithm.

## Selection Sort
- Explain the basic principle behind the Selection Sort algorithm.
- What is the time complexity of Selection Sort, and why?

## Insertion Sort
- Describe how the Insertion Sort algorithm works.
- Discuss the best, average, and worst-case time complexities of Insertion Sort. What factors influence these complexities?

## Merge Sort
- Summarize the divide and conquer strategy as applied in Merge Sort.
- How does the Merge Sort algorithm achieve its efficiency, and what is its time complexity?

## Algorithm Analysis
- Compare and contrast the time complexities of Selection Sort, Insertion Sort, and Merge Sort.
- What is the space complexity of Merge Sort when arrays are used, and how does it change with linked lists?

## Practical Considerations
- For a given list of elements, determine which sorting algorithm (among Selection, Insertion, or Merge Sort) would be most efficient considering the list's characteristics.
- How does the choice of data structure (array vs. linked list) affect the implementation and efficiency of sorting algorithms?

## Advanced Topics
- Discuss how the insertion sort algorithm can be optimized using binary search.
- What are the limitations of simple sorting algorithms like Selection and Insertion Sort when dealing with large datasets?

# Sorting Part 2

## QuickSort
- Explain the divide and conquer strategy used in QuickSort.
- How does the choice of pivot affect the efficiency of QuickSort?
- What is the best, average, and worst-case time complexity of QuickSort, and under what conditions do these cases occur?

## CountSort
- Describe how CountSort works without using comparisons.
- What are the main advantages and disadvantages of CountSort in terms of time and space complexity?

## RadixSort
- Explain the principle behind RadixSort and how it differs from other sorting algorithms.
- In what scenarios is RadixSort particularly efficient, and why?

## Stability in Sorting
- What does it mean for a sorting algorithm to be stable?
- Why is stability important in certain applications?

## Lower Bound for Comparison-Based Sorting
- What is the lower bound for the time complexity of any comparison-based sorting algorithm?
- Explain how the decision tree model proves this lower bound.

## Comparative Analysis
- Compare the time and space complexities of QuickSort, CountSort, and RadixSort.
- Discuss the trade-offs between these algorithms in terms of speed and resource utilization.

## Practical Considerations
- Given a specific type of data or application, how would you choose the most appropriate sorting algorithm?
- How do non-comparison-based algorithms like CountSort and RadixSort achieve lower time complexity, and what limitations do they have?

# Lists and arrays

## Linked Lists
- What are the differences between singly linked lists, doubly linked lists, and cyclic lists?
- How do operations on linked lists like insertion or deletion differ in terms of complexity between singly and doubly linked lists?

## Abstract Data Structures
- Define an Abstract Data Structure (ADS) and how it differs from concrete data structures like arrays or linked lists.
- Provide examples of operations for Stack, Queue, and Deque, and explain their use cases.

## Amortised Analysis
- Explain the concept of amortised analysis and why it's important in data structure operation analysis.
- Describe the potential function method and how it's used to compute amortised costs.

## Unbounded Arrays
- What is an unbounded array, and how does it differ from a standard array?
- Discuss the amortised cost of operations like pushBack and indexing in unbounded arrays.

## Operations and Implementations
- How can common list operations like `isEmpty`, `insertAfter`, and `removeBefore` be implemented efficiently in linked lists?
- Discuss the implementation and complexity of the `splice` operation in the context of doubly linked lists.

## Dynamic Arrays
- Describe the process and complexity of dynamically growing and shrinking an array.
- How does the amortised analysis apply to operations on dynamically resizing arrays?

## Comparison Between Data Structures
- Compare the complexities of sequence operations (like insert, remove, pushBack) across different data structures: singly linked lists (SList), doubly linked lists (DList), unbounded arrays (UArray), and cyclic arrays (CArray).
- Discuss the trade-offs in choosing between linked lists and arrays for specific applications.

# Priority queue

## Priority Queue Basics
- What is a priority queue and how does it differ from a regular queue?
- Describe the primary operations of a priority queue.

## Naive Implementations
- Compare the time complexities of `insert`, `findMin`, and `deleteMin` operations in unsorted and sorted sequence implementations of priority queues.

## Binary Heap
- Explain the heap-order property in a binary heap.
- How is a binary heap represented in an array, and why is this representation efficient?

## Binary Heap Operations
- Describe the process and complexity of the `insert` operation in a binary heap.
- Explain how `findMin` and `deleteMin` operations are performed in a binary heap and their complexities.

## Heapify and Constructing a Binary Heap
- What is the heapify operation, and how does it contribute to constructing a binary heap from an arbitrary array?

## Binomial Heap
- Define a binomial heap and explain how it is constructed from binomial trees.
- Discuss the advantages of binomial heaps in terms of merge operation.

## Binomial Heap Operations
- Describe the complexities of `findMin`, `merge`, `insert`, `deleteMin`, `decreaseKey`, and `delete` operations in a binomial heap.

## Advanced Topics
- How do binomial heaps facilitate the merge operation, and what is the complexity?
- Compare the efficiency of binary and binomial heaps in terms of various operations.

## Practical Applications
- Provide examples of real-world applications where priority queues are essential.
- Discuss how HeapSort utilizes a priority queue to sort an array.

# Dictionary 

## Fundamental Concepts
- What is a dictionary in data structures and what are its key operations?
- How does direct addressing work, and what are its limitations?

## Hash Tables
- Describe the principle of a hash table. How does it handle collisions?
- Explain the difference between open hashing and the chaining method.

## Hash Functions
- What are the desirable properties of a hash function?
- How does universal hashing help in minimizing collisions?

## Binary Search Trees (BST)
- What defines the structure of a BST, and how are the `insert`, `search`, and `delete` operations performed?
- Discuss the average and worst-case time complexities of operations in a BST.

## AVL Trees
- How does an AVL tree ensure that the tree remains balanced?
- What are the rotations used in AVL trees, and why are they necessary?

## Self-organizing Trees
- Explain the concept of splay trees and how they achieve amortized logarithmic time complexity.
- Compare the performance and use cases of splay trees with AVL trees.

## Ordered Dynamic Set Operations
- Discuss how BSTs support ordered dynamic set operations like `minimum`, `maximum`, `predecessor`, and `successor`.
- Why are hash tables not efficient for ordered dynamic set operations?

## Advanced Topics
- What is perfect hashing, and under what circumstances is it used?
- Explain how B-trees and their variants are designed for efficient on-disk storage and retrieval.

*Edited and formatted with the help of ChatGPT*