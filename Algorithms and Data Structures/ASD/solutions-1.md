### 1. Ranks, asymptotic notation
a. Asymptotic notations:
- $n\log n + n^{3/2} = \Theta(n^{3/2})$
- $n^2 + n = \Theta(n^2)$
- $n^{1/2} + 4 = \Theta(n^{1/2})$
- $\log_2(2^n) = \Theta(n)$
- $n\log n + n = \Theta(n\log n)$
- $3\log n + 1 = \Theta(\log n)$

b. Order of Growth:
- $\log n, n^{1/2}, n, n\log n, n^{3/2}, n^2$

### 2. Binary search 
a. Compared to: `7, 12, 15, 13`
b. Return value: `-1`

### 3. SelectionSort 
a. Transformation steps:
```plaintext
0: 6 3 1 0 2 5 4 7
1: 0 3 1 6 2 5 4 7
2: 0 1 3 6 2 5 4 7
3: 0 1 2 6 3 5 4 7
4: 0 1 2 3 6 5 4 7
5: 0 1 2 3 4 5 6 7
6: 0 1 2 3 4 5 6 7
7: 0 1 2 3 4 5 6 7
```

b. Total comparisons: `28`

### 4. InsertionSort 
a. Transformation steps :
```plaintext
0: 6 3 1 0 2 5 4 7
1: 3 6 1 0 2 5 4 7 (1)
2: 1 3 6 0 2 5 4 7 (2)
3: 0 1 3 6 2 5 4 7 (3)
4: 0 1 2 3 6 5 4 7 (3)
5: 0 1 2 3 5 6 4 7 (2)
6: 0 1 2 3 4 5 6 7 (3)
7: 0 1 2 3 4 5 6 7 (1)
```

b. Total comparisons: `15`

### 5. MergeSort 
a. Tree of subsequences:
```plaintext
6 3 1 0 2 5 4 7
6 3 1 0 | 2 5 4 7
6 3 | 1 0 | 2 5 | 4 7
6 | 3 | 1 | 0 | 2 | 5 | 4 | 7
```
```plaintext
3 6 | 0 1 | 2 5 | 4 7 (4)
0 1 3 6 | 2 4 5 7 (5)
0 1 2 3 4 5 6 7 (7)
```

b. Total comparisons: `16`

### 6. Partitioning function 
a. Final array: `[0 3 1 2 4 6 9 8]`

b. Return value: `5`

### 7. CountSort
a. Final helper (counts) array:
`[0 0 2 5 6 8 10 10 10 10 10 10]`

### 8. RadixSort 
a. Order after each phase of sorting:
```plaintext
501, 201, 125, 521, 321, 105, 211, 325
501, 201, 521, 321, 211, 123, 105, 325
501, 201, 105, 211, 521, 321, 123, 325
105, 123, 201, 211, 321, 325, 501, 521
```