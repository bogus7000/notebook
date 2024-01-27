*Based on course materials by Marcin Sydow - Algorithms and Data Structures*

- [Correctness of an Algorithm](#correctness-of-an-algorithm)
  - [What Does Algorithm Mean?](#what-does-algorithm-mean)
  - [Pseudocode](#pseudocode)
  - [Algorithm Design](#algorithm-design)
  - [Algorithm Specification](#algorithm-specification)
  - [Total Correctness of an Algorithm](#total-correctness-of-an-algorithm)
  - [Partial Correctness of an Algorithm](#partial-correctness-of-an-algorithm)
  - [The Stop Property](#the-stop-property)
  - [Proving Partial Correctness - Invariants](#proving-partial-correctness---invariants)
  - [Example Task in Algorithmics](#example-task-in-algorithmics)
- [Complexity of an Algorithm](#complexity-of-an-algorithm)
  - [Desired Properties of a Good Algorithm](#desired-properties-of-a-good-algorithm)
    - [1) Correctness of the Algorithm](#1-correctness-of-the-algorithm)
    - [2) Complexity of the Algorithm](#2-complexity-of-the-algorithm)
  - [Example: The Search Problem](#example-the-search-problem)
    - [The Speed of the Algorithm](#the-speed-of-the-algorithm)
      - [Dominating Operations](#dominating-operations)
      - [Example: Determining Dominating Operations](#example-determining-dominating-operations)
      - [Example: Determining the Data Size](#example-determining-the-data-size)
    - [Time Complexity of Algorithm](#time-complexity-of-algorithm)
      - [Example: Time Complexity](#example-time-complexity)
    - [Pessimistic Time Complexity](#pessimistic-time-complexity)
    - [Average Time Complexity of Algorithm](#average-time-complexity-of-algorithm)
    - [Space Complexity of Algorithm](#space-complexity-of-algorithm)
    - [Asymptotic Notation - Big O](#asymptotic-notation---big-o)
    - [Asymptotic Notation - Big Theta](#asymptotic-notation---big-theta)
      - [Other Flavours of Asymptotic Notation](#other-flavours-of-asymptotic-notation)
    - [Remarks on Using Asymptotic Notation](#remarks-on-using-asymptotic-notation)
    - [Comparing Ranks of Functions](#comparing-ranks-of-functions)
    - [Most Common Ranks of Functions](#most-common-ranks-of-functions)
      - [Examples](#examples)
    - [Questions/Problems](#questionsproblems)
- [Searching](#searching)
  - [Divide and Conquer](#divide-and-conquer)
  - [The Searching Problem](#the-searching-problem)
  - [Searching Continued](#searching-continued)
  - [More Effective Searching](#more-effective-searching)
  - [Searching in a Sorted Sequence](#searching-in-a-sorted-sequence)
  - [Skipping Algorithm](#skipping-algorithm)
  - [Divide and Conquer in Searching](#divide-and-conquer-in-searching)
  - [Binary Search Algorithm (Code)](#binary-search-algorithm-code)
  - [Analysis of the Binary Search Algorithm](#analysis-of-the-binary-search-algorithm)
  - [Positional Statistics](#positional-statistics)
  - [Searching the 2nd Smallest Element](#searching-the-2nd-smallest-element)
  - [The Tournament Algorithm](#the-tournament-algorithm)
  - [K-th Positional Statistics - Hoare's Algorithm](#k-th-positional-statistics---hoares-algorithm)
  - [The Partition Procedure](#the-partition-procedure)
  - [Analysis of Partition](#analysis-of-partition)
  - [Hoare's Algorithm - Overview](#hoares-algorithm---overview)
  - [Review Topics](#review-topics)
- [Sorting Part 1](#sorting-part-1)
  - [Introduction](#introduction)
    - [Input](#input)
    - [Output](#output)
    - [Note](#note)
  - [The Importance of Sorting](#the-importance-of-sorting)
    - [Applications of Sorting](#applications-of-sorting)
  - [Selection Sort](#selection-sort)
    - [Concept](#concept)
    - [Pseudo-Code](#pseudo-code)
      - [Functions](#functions)
      - [Invariant](#invariant)
  - [Selection Sort - Analysis](#selection-sort---analysis)
    - [Dominating Operation](#dominating-operation)
    - [Data Size](#data-size)
    - [Complexity](#complexity)
  - [Insertion Sort](#insertion-sort)
    - [Pseudo-Code](#pseudo-code-1)
      - [Invariant](#invariant-1)
  - [Insertion Sort - Analysis](#insertion-sort---analysis)
    - [Pessimistic Case](#pessimistic-case)
  - [Average Time Complexity Analysis](#average-time-complexity-analysis)
    - [Assumption](#assumption)
    - [Calculation](#calculation)
  - [Analysis Continued](#analysis-continued)
    - [Observations](#observations)
  - [Insertion-Sort with Binary Search](#insertion-sort-with-binary-search)
    - [Idea](#idea)
    - [Complexity](#complexity-1)
  - [Divide and Conquer Sorting: Merge Sort](#divide-and-conquer-sorting-merge-sort)
    - [Process](#process)
    - [Merge Sort Scheme](#merge-sort-scheme)
      - [Merge Function](#merge-function)
  - [Merge Function Analysis](#merge-function-analysis)
    - [Dominating Operation](#dominating-operation-1)
    - [Data Size](#data-size-1)
    - [Time Complexity](#time-complexity)
    - [Space Complexity](#space-complexity)
  - [Time Complexity Analysis of Merge-sort](#time-complexity-analysis-of-merge-sort)
    - [Complexity](#complexity-2)
  - [Short Summary: Selection Sort (SS), Insertion Sort (IS), and Merge Sort (MS)](#short-summary-selection-sort-ss-insertion-sort-is-and-merge-sort-ms)
    - [Square vs Linear-Logarithmic Complexity](#square-vs-linear-logarithmic-complexity)
  - [Linked Lists](#linked-lists)
    - [Purpose](#purpose)
    - [Types](#types)
    - [Linked Lists vs Arrays](#linked-lists-vs-arrays)
    - [Application in MergeSort](#application-in-mergesort)
  - [Questions/Problems](#questionsproblems-1)
    - [Topics Covered](#topics-covered)
- [Sorting Part 2](#sorting-part-2)
- [Lists and arrays](#lists-and-arrays)
- [Priority queue](#priority-queue)
- [Dictionary](#dictionary)


# Correctness of an Algorithm

## What Does Algorithm Mean?
An algorithm is a recipe for performing a list of actions. The term is derived from the Arabic version of the name al-Khwarizmi, a Persian mathematician (A.D. 780-850). Algorithmics is fundamental to computer science, gaining more importance with the growth of data, the Internet, search engines, etc.

## Pseudocode
Pseudocode is an abstract representation of an algorithm:
- It is similar to popular programming languages like Java, C/C++, and Pascal.
- It plays an informative role rather than a formal one, with relaxed syntax.
- Includes literals (numbers, strings, null), variables (must be initialized, no declarations), and arrays (indexed from 0 using the [] operator).
- Uses operators such as assignment (=), comparison (e.g., ==), arithmetic (e.g., +, ++, +=), and logic (e.g., !).
- Allows for functions (including recursion), return instructions, conditional statements (IF), and loops (FOR, WHILE).

## Algorithm Design
Algorithm design involves creating a solution to a computational task before its implementation in a programming language. It is a necessary step before programming.

## Algorithm Specification
Specification outlines the task to be accomplished:
- May include the algorithm's name and a list of its arguments.
- Initial condition specifies the correct input data.
- Final condition specifies the desired result of the algorithm.
The conditions should be expressed precisely, often in words.

Example Task: "Compute the sum of numbers in an array given its length."
Specification:
- Name: sum(Arr, len)
- Input (Initial Condition): Algorithm receives two arguments:
  1. Arr - an array of integer numbers.
  2. len - the length of Arr (a natural number).
- Output (Final Condition): Algorithm returns the sum of the first len numbers in Arr (an integer).

## Total Correctness of an Algorithm
An algorithm is totally correct if, for any correct input data, it:
1. Stops.
2. Returns correct output.

## Partial Correctness of an Algorithm
Partial correctness involves:
1. Checking whether the algorithm stops.
2. Ensuring that if the algorithm stops with correct input data, its result is correct.

Note: Partial correctness does not guarantee that the algorithm will stop.

## The Stop Property
Proof of total correctness assumes:
1. The algorithm always stops for correct input data.
2. The algorithm is partially correct.

Example in Pseudocode:
```c
sum(array, len) {
    sum = 0;
    i = 0;
    while (i < len) {
        sum += array[i];
        i++;
    }
    return sum;
}
```
To prove the stop property, observe that:
1. The algorithm stops when i ≥ len.
2. len is a constant, finite natural number.
3. i increases by 1 in each iteration, ensuring termination after a finite number of iterations.

## Proving Partial Correctness - Invariants
Invariants help prove the partial correctness of algorithms, especially useful for `WHILE` loops.

Definition:
- A loop invariant is a logical predicate that remains true before and after each loop iteration.

## Example Task in Algorithmics

Analyze the following algorithm:

```c
algor1(Arr, len) {
    i = 1;
    x = Arr[0];
    while (i < len) {
        if (Arr[i] > x) {
            x = Arr[i];
        }
        i++;
    }
    return x;
}
```
To prove correctness, show:
1. The stop property.
2. Partial correctness using a loop invariant.

We aim to prove that `x` is the maximum in `Arr`:

- Target: `(∀0 ≤ j < len x ≥ Arr[j]) ∧ (∃0 ≤ j < len(x == Arr[j]))`
- Loop invariant: `∀0 ≤ j < i x ≥ Arr[j] ∧ (∃0 ≤ j < len(x == Arr[j]))`
- Stop condition: `i == len`
- Proof: `((∀0 ≤ j < i x ≥ Arr[j]) ∧ (i == len)) => (∀0 ≤ j < len x ≥ Arr[j])`

# Complexity of an Algorithm

## Desired Properties of a Good Algorithm
A good algorithm should satisfy two main conditions:
1. Compute the correct (desired) output for the given problem.
2. Be effective (fast).

### 1) Correctness of the Algorithm
Ensures that the algorithm produces the desired output.

### 2) Complexity of the Algorithm
Complexity measures the algorithm's time efficiency (how fast it is) and space efficiency (amount of memory used).

## Example: The Search Problem
- **Problem Definition**: Searching a key in an array.
- **Specification**: 
  - **Input**: `arr` (an array of integers), `len` (its length), `key` (an integer to be found).
  - **Output**: An integer `0 ≤ i < len` being the index in `arr` where the key is stored, or `-1` if the key is not in the first `len` positions of the array.
- **Code**: 
  ```cpp
  find(arr, len, key) {
    i = 0;
    while (i < len) {
      if (arr[i] == key)
        return i;
      i++;
    }
    return -1;
  }
  ```

### The Speed of the Algorithm
- **How to Measure**: Count the basic operations, ensuring independence from any programming language and specific input data.

#### Dominating Operations
- **Approach**: Identify representative operations that cover the amount of work proportional to the total work of the algorithm.
- **Steps**:
  1. Determine the set of dominating operations.
  2. Observe the influence of input on the number of dominating operations.

#### Example: Determining Dominating Operations
- **Algorithm**: The search algorithm above.
- **Considerations**:
  - Assignment `i = 0`: No.
  - Comparison `i < len`: Yes.
  - Comparison `arr[i] == key`: Yes.
  - Return statement `return i`: No.
  - Index increment `i++`: Yes.

#### Example: Determining the Data Size
- **Data Size**: Length of the array `arr`.

### Time Complexity of Algorithm
- **Definition**: The number of dominating operations executed as a function of data size.

#### Example: Time Complexity
- **Considerations**: 
  - Dominating operation: Comparison `arr[i] == key`.
  - Data size: Length of array, denoted as `n`.
- **Variability**: Number of operations ranges from 1 (key found at the first index) to `n` (key absent or at the last index).

### Pessimistic Time Complexity
- **Definition**: The worst-case number of dominating operations for input data of size `n`.
- **Formula**: `W(n) = n`, representing the worst-case scenario.

### Average Time Complexity of Algorithm
- **Definition**: The expected value of the random variable representing the number of dominating operations.
- `n`: Data size
- `Dn`: The set of all possible input datasets of size `n`
- `t(d)`: The number of dominating operations for dataset `d (of size n) (d ∈ Dn)`
- `Xn`: Random variable, its value is `t(d) for d ∈ Dn`
- `Pnk`: The probability distribution of the random variable `Xn` (i.e. the probability that for input data of size n the algorithm will execute `k dominating operations (k ≥ 0)`)

- Algorithm:
$$
% Average time complexity algorithm
A(n) = \sum_{k \geq 0} p_{nk} \cdot k = \sum P(X_n = k) \cdot k
$$

`(A(n) Average)`

- **Consideration**: Assumes a probabilistic model of input data.
- **Example**: With a uniform distribution of the key (the key to be found occurs exactly once in array and with the same probability on each index), `A(n) = (n + 1) / 2`.

- Uniform distribution:
$$
% Uniform distribution
\forall_{0 \leq k < n} P(X_n = k) = \frac{1}{n}
$$

- Average time complexity of `find()`:
$$
% Average time complexity of find()
A(n) = \sum_{k \geq 0} P(X_n = k) \cdot k = \sum_{0 \leq k < n} \frac{1}{n} \cdot k = \frac{n+1}{2}
$$

### Space Complexity of Algorithm
- **Definition**: The number of memory units used as a function of data size.
- **Example**: For the search algorithm, space complexity is constant (`S(n) = const`), as it consumes memory for a single variable and a fixed number of additional temporary variables.

### Asymptotic Notation - Big O
- **Purpose**: Expresses the upper bound of the complexity function, allowing to neglect unimportant details.
- **Definition**: `f(n) = O(g(n))` if there exist constants `c > 0` and `n0` such that for all `n ≥ n0`, `f(n) ≤ c·g(n)`.

The Big O notation `O()` intuitively corresponds to the `≤`` symbol (in terms of ranks of orders of functions).

For example, the fact that $W(n)$ of our exemplary algorithm has an upper bound of the linear rank can be noted as:
$W(n) = \frac{n+1}{2} = O(n)$.
The constant space complexity $S(n)$ of that algorithm can be expressed with the following special notation: $S(n) = O(1)$.


### Asymptotic Notation - Big Theta
- **Definition**: `f(n) = Θ(g(n))` if `f(n) = O(g(n))` and `g(n) = O(f(n))`. Represents the same rank of order.

Another important flavor of asymptotic notation is "big Theta":

The function $f(n)$ has the same rank of order as the function $g(n): f(n) = \Theta(g(n))$ if and only if $f(n) = O(g(n))$ and $g(n) = O(f(n))$.

The $\Theta$ notation intuitively corresponds to the "=" symbol (in terms of ranks of orders of functions).

Notice that $\Theta$ is defined with the use of $O()$, similarly as "=" symbol can be defined with the use of "≤" symbol.

E.g., the expression: $f(n) = n^2 + n - 3 = \Theta(n^2)$
reads as "the $n^2 + n - 3$ function" is of square rank of order.


#### Other Flavours of Asymptotic Notation
1. **Θ**: Equals $=$.
2. **O**: Less than or equal to $\leq$.
3. **Ω**: Greater than or equal to $\geq$.
4. **o**: Less than $<$.
5. **ω**: Greater than $>$.

$W(n)=o(n)$ means: "the rank of function W(n) is lower than linear"

### Remarks on Using Asymptotic Notation
- **Usage**: Often used on the right-hand side of the `=` symbol, as in `f(n) = g(n) + O(h(n))`.

### Comparing Ranks of Functions
- **Method**: Compute the limit of `f(n) / g(n)` as `n` approaches infinity.
- **Outcomes**: The limit can be ∞ (f has a higher rank), a positive constant (same ranks), or zero (g has a higher rank).

### Most Common Ranks of Functions

#### Examples
- **constant** (e.g. $S(n) = 3 = \Theta(1)$)
- **logarithmic** (e.g. $W(n) = 2 + \log_2{n} = \Theta(\log(n))$)
- **linear** (e.g. $A(n) = 2n + 1 = \Theta(n)$)
- **linear-logarithmic** (e.g. $A(n) = 1.44 \cdot n \log(n) = \Theta(n \log(n))$)
- **square** (e.g. $W(n) = n^2 + 4 = \Theta(n^2)$)
- **cubic** (e.g. $A(n) = \Theta(n^3)$)
- **sub-exponential** (e.g. $A(n) = \Theta(n^{\log_2(n)})$)
- **exponential** (e.g. $A(n) = \Theta(2^n)$)
- **factorial** (e.g. $W(n) = \Theta(n!)$)

In simplification: in practice, an _over-polynomial_ rank of time complexity is considered as "unacceptably high".

In case of space complexity, even linear rank is considered as _very high_.


### Questions/Problems
- How to measure the speed of an algorithm?
- What are the two key considerations before assessing time complexity?
- What is a dominating operation?
- Define Time and Space Complexity of an Algorithm.
- Define Pessimistic and Average Time Complexity.
- Determine time complexity for simple algorithms.
- Purpose and interpretation of the O() notation and other asymptotic notations.

# Searching 

## Divide and Conquer
- **Concept**: A principal method in algorithm design, where a problem is divided into smaller sub-problems. The solutions of these sub-problems are then combined to solve the original problem.
- **Implementation**: Often executed using recursion, where a function calls itself with a subset of the problem.
- **Historical Origin**: The strategy has roots in politics. The term "Divide et Impera" (Latin for Divide and Conquer) is attributed to Philip II of Macedonia (382-336 BC) during his governance over the Greeks. [Source: Wikipedia]

## The Searching Problem
- **Function Prototype**: `search(S, len, key)`
- **Inputs**:
  - `S`: A sequence of integers, indexed from 0 to `len-1`.
  - `len`: The length of the sequence.
  - `key`: The integer number to be found.
- **Output**: Returns an index (a natural number less than `len`), where `S[index] == key`, or `-1` if the key is not present in the sequence.
- **Example**:
  - For `S = (3,5,8,2,1,8,4,2,9)`, `search(S, 9, 2)` should return 3, and `search(S, 9, 7)` should return -1.

## Searching Continued
- **Dominating Operation**: The comparison operation is a significant factor in standard algorithms solving the searching problem, with the data size usually being the length of the sequence (`len`).
- **Sequential Search Algorithm**: Previously discussed with linear time complexity $W(\text{len}) = \Theta(\text{len})$. The multiplicative factor is 1 (i.e., $W(\text{len}) = \text{len}$), and this can't be improved due to the problem's nature.

## More Effective Searching
- **Improvement Strategy**: To search more efficiently, one beneficial property would be sorting the input sequence.

## Searching in a Sorted Sequence
- **Different Problem**: This is considered a different problem due to the altered input condition (sorted sequence).
- **Input**: `S` - a sequence of non-decreasingly sorted integers, `len` - a natural number indicating the length of the sequence, and `key` - the integer number to be found.
- **Output**: Similar to the unsorted case, but the additional assumption of sorted data allows for more efficient problem solving.

## Skipping Algorithm
- **Approach**: In a sorted input sequence, it is feasible to check every $k$-th cell (skipping $k-1$ elements each time). Upon finding the first number higher than the key, only the last $k-1$ elements are checked.
- **Performance**: Asymptotically, this method is $k$ times faster than normal sequential search for unordered input sequences ($W(\text{len}) = 1/k * \Theta(\text{len})$), but it still has linear complexity.
- **Optimal $k$**: The optimal choice for $k$, in terms of pessimistic complexity, is $k = \sqrt{\text{len}}$.

## Divide and Conquer in Searching
- **Function Prototype**: `search(S, len, key)`, input is sorted
- **Binary Search Algorithm**: A classic application of the Divide and Conquer approach for a sorted input sequence.
  1. While the length of the sequence is positive:
  2. Check the middle element of the current sequence.
  3. If it equals the key, return the result.
  4. If higher than the key, restrict searching to the left sub-sequence.
  5. If less than the key, restrict searching to the right sub-sequence.
  6. Repeat from step 1.
  7. Return `-1` if the key isn't found.

## Binary Search Algorithm (Code)
- **Pseudocode**:
  ```c
  search(S, len, key) {
      l = 0
      r = len - 1
      while (l <= r) {
          m = (l + r) / 2
          if (S[m] == key) return m
          else if (S[m] > key) r = m - 1
          else l = m + 1
      }
      return -1
  }
  ```
- **Requirement**: Random access to the $m$-th element `S[m]` of the sequence demands that the sequence is stored in RAM for efficiency.

## Analysis of the Binary Search Algorithm
- **Data Size**: The length of the sequence - `len`.
- **Dominating Operation**: Comparison (`S[m] == key`), assuming the sequence is in RAM.
- **Time Complexity**: $W(\text{len}) = \Theta(\log_2(\text{len}))$.
- **Space Complexity**: $S(\text{len}) = O(1)$.
- **Limitation**: If data does not fit into RAM, this analysis is inadequate, as `S[m] == key` cannot be considered an atomic operation.

## Positional Statistics
- **Concept**: The k-th positional statistic in a sequence of orderable elements is the k-th smallest (or largest) element.
- **Example**: Finding the minimum is equivalent to finding the 1st positional statistic. In a sorted sequence, this task is trivial.

## Searching the 2nd Smallest Element
- **Function**: `second(S, len)`, no assumption that the sequence is sorted
- **Input**: An unsorted sequence `S` and its length `len`.
- **Output**: The second smallest element in `S`.
- **Simple Solution**: Find the minimum, exclude it, and repeat. This needs $2 \times \text{len}$ comparisons.
- **Efficiency Question**: Can this be achieved more effectively?

## The Tournament Algorithm
- **Idea**: Use the divide and conquer method in a tournament-style process. In each round, the sequence is divided into pairs, and the smaller element in each pair advances to the next round. The process continues until only the smallest element remains.
- **Locating the Second Smallest**: It is among the direct competitors of the smallest element.
- **Efficiency**: Requires $\text{len} - 1$ comparisons for the tournament, plus an additional $O(\log_2(\text{len}))$ comparisons to find the second smallest.

## K-th Positional Statistics - Hoare's Algorithm
- **Function**: `kthSmallest(S, len, k)`, no assumption of order of the input sequence
- **Input**: A sequence `S`, its length `len`, and the positional statistic `k`.
- **Output**: The k-th smallest element in `S`.
- **Method**: A divide and conquer approach utilizing a partition procedure.

## The Partition Procedure
- **Function**: `partition(S, l, r)`
- **Purpose**: Selects an element `M` and reorganizes the sequence such that elements on the left of `M` are not greater than `M`, and those on the right are not less.
- **Output**: The final position of the median element `M`.

## Analysis of Partition
- **Property**: If the index returned by `partition` equals `k`, then the element at this index is the k-th positional statistic.
- **Complexity**: $W(n) = n + O(1)$ and $S(n) = O(1)$

## Hoare's Algorithm - Overview
- **Procedure**:
  1. Call `partition` on the sequence.
  2. If the returned index equals `k`, return `S[k]`.
  3. Else, continue on the appropriate sub-sequence, considering abandoned elements.
- **Time Complexity**: Linear, often faster than the repeated minimum method.
- **Inventor**: J.R. Hoare.

## Review Topics
1. Sequential search algorithm.
2. Searching in a sorted sequence (skipping elements).
3. Binary Search Algorithm (analysis and code).
4. Positional Statistics.
5. The Tournament Algorithm.
6. The Partition Procedure (specification).
7. Hoare's Algorithm (concept).

# Sorting Part 1

## Introduction

### Input
- **S:** A sequence of elements that can be ordered according to a binary total-order relation $R \subseteq S \times S$.
- **len:** The length of the sequence (a natural number).

### Output
- **S':** A non-decreasingly sorted sequence consisting of elements of the multi-set of the input sequence `S`.
    - For example, $\forall_{0<i<len} \, (S[i − 1], S[i]) \in R$.

### Note
- For simplicity, this course assumes sorting of natural numbers, but all discussed algorithms can be easily adapted to sort any other ordered universe.

---

## The Importance of Sorting

Sorting is a crucial operation in data processing within computer science, intensively studied since the mid-20th century.

### Applications of Sorting
- Acceleration of searching.
- Acceleration of operations on relations by key (e.g., in databases).
- Data visualization.
- Computing statistical characteristics.
- Many others.

---

## Selection Sort

### Concept
Identify the minimum `len` times, excluding it from further processing and placing it in the correct position in the output sequence.

### Pseudo-Code
```c
selectionSort(S, len){
  i=0
  while(i < len){
    mini = indexOfMin(S, i, len)
    swap(S, i, mini)
    i++
  }
}

```

#### Functions
- `indexOfMin(S, i, len)`: Returns index of minimum among the elements `S[j]`, where $i \leq j < len$.
- `swap(S, i, mini)`: Swaps the positions of `S[i]` and `S[mini]`.

#### Invariant
- The invariant of the above loop is to be determined.

---

## Selection Sort - Analysis

### Dominating Operation
- Comparing two elements in an array.

### Data Size
- Length of the sequence (`len`).

### Complexity
- The external loop iterates `len − 1` times.
- In each `i`-th iteration, it seeks the minimum in a sequence of `(len-i)` elements
- The complexity is: $W(\text{len})=\sum_{i=1}^{len-1} i = \frac{len(len-1)}{2} = \Theta(len^2)$ comparisons.
- Complexity: $\Theta(len^2)$ for both worst and average cases (square).

---

## Insertion Sort

### Pseudo-Code
```python
def insertionSort(arr, len):
    for next in range(1, len):
        curr = next
        temp = arr[next]
        while curr > 0 and temp < arr[curr - 1]:
            arr[curr] = arr[curr - 1]
            curr -= 1
        arr[curr] = temp
```

#### Invariant
- The invariant of the external loop is to be determined.

---

## Insertion Sort - Analysis

### Pessimistic Case
- When the data is inversely sorted.
- Complexity: $W(n) = \frac{n(n-1)}{2} = \frac{1}{2}n^2 + \Theta(n) = \Theta(n^2)$.
- Adapts to the degree of sortedness of input data.

---

## Average Time Complexity Analysis

### Assumption
- Each permutation of input elements is equally likely.

### Calculation
- For the `i`-th iteration of the external loop, the algorithm needs on average $\frac{1}{2} \sum_{j=1}^{i} j$ comparisons.
- Thus, $A(n) = \Theta(n^2)$.

Let's assume a simple model of input data - each permutation of input elements is equally likely. Then, for the $i-th$ iteration of the external loop the algorithm will need (on average):

$\frac{1}{i} \sum_{j=1}^{i} j = \frac{1}{i} \frac{(i+1)i}{2} = \frac{i+1}{2}$

comparisons. Thus, we obtain:

$A(n) = \sum_{i=1}^{n-1} \frac{i+1}{2} = \frac{1}{2} \sum_{k=2}^{n} k = \frac{1}{4} n^2 + \Theta(n) = \Theta(n^2)$


---

## Analysis Continued

### Observations
- On average, the algorithm is twice as fast as Selection Sort.
- Square complexity is too high for large data.

---

## Insertion-Sort with Binary Search

### Idea
- Use binary search to find the correct position in the already sorted subsequence.
- Retains the same number of comparisons for each input data.

### Complexity
- Comparisons: $\Theta(n \log n)$.
- The insert operation in an array implementation costs a linear number of assignments, leading to square complexity overall.

---

## Divide and Conquer Sorting: Merge Sort

### Process
1. Divide the sequence into 2 halves.
2. Sort each half separately.
3. Merge the sorted halves.

### Merge Sort Scheme
```python
def mergeSort(S, len):
    if len <= 1:
        return S[0:len]
    m = len // 2
    return merge(mergeSort(S[0:m], m), mergeSort(S[m:len], len-m))
```

#### Merge Function
- Merges two sorted sequences into one sorted sequence.

---

## Merge Function Analysis

### Dominating Operation
- Comparing two elements or indexes.

### Data Size
- Total length of

 two subsequences to be merged (`n = len1 + len2`).

### Time Complexity
- $W(n) = A(n) = \Theta(n)$.

### Space Complexity
- High if sequences are represented as arrays: $S(n) = \Theta(n)$.
- Reduced with linked lists.

---

## Time Complexity Analysis of Merge-sort

### Complexity
- $W(len) = A(len) = \Theta(len \cdot \log len)$.
- Linear-logarithmic complexity.

---

## Short Summary: Selection Sort (SS), Insertion Sort (IS), and Merge Sort (MS)

- **Selection and Insertion Sort:**
    - Square time complexity $\Theta(n^2)$.
- **Merge Sort:**
    - Faster with linear-logarithmic complexity $\Theta(n \log n)$.
    - Requires more memory if implemented with arrays.

### Square vs Linear-Logarithmic Complexity
- Significant speed difference, especially for large datasets.

---

## Linked Lists

### Purpose
- To save memory and avoid unnecessary copying in merge sort.

### Types
- Uni-directional.
- Bi-directional.
- Cyclic.

### Linked Lists vs Arrays
- Arrays: fast random access, less memory consumption.
- Linked lists: efficient for modifications, slower access.

### Application in MergeSort
- Using uni-directional lists improves space complexity to $O(1)$, assuming recursion implementation issue is neglected.

---

## Questions/Problems

### Topics Covered
- Sorting
- Selection Sort
- Insertion Sort
- Merge Sort
- Linked Lists

# Sorting Part 2

# Lists and arrays

# Priority queue

# Dictionary 

*Edited and formatted with the help of ChatGPT*