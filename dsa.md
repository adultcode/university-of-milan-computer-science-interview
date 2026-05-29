<!-- # 🚀 UNIMI Computer Science MSc Interview — Expanded Crash Guide -->
# 🚀 Data Structures and Algorithms (DSA)

> Use this as a quick review map before interviews.
> Try to explain each topic in **60–90 seconds**.

---

# 📚 Core Goal

* Explain simple algorithms clearly
* Write basic pseudocode
* Discuss time complexity confidently

### Most Common Interview Tasks

* Matrix multiplication
* Fisher–Yates shuffle
* Binary search
* Stack / Queue / Array questions
* Big-O analysis

---

# 🧠 Variables, Data Types & Control Flow

Variables store data, data types define what kind of data is stored, and control flow determines which instructions execute.

Although interviewers may not ask directly about these basics, you need them to explain code clearly.

## ✅ Interview Answer

> A program uses variables to store values and control structures like if-statements and loops to decide execution flow.


---

# 📦 Arrays

An array stores elements in contiguous memory and allows direct access using an index.

* Access by index → **O(1)**
* Insert/Delete in middle → usually **O(n)**

Because elements may need to shift after insertion or deletion.

## ✅ Interview Answer

> An array is good when we need fast index-based access and know the size or can use a dynamic array.


---

# 🔗 Linked Lists

A linked list stores data as nodes where each node points to the next one.

### Advantages

* Fast insertion/deletion when node is known

### Disadvantages

* Random access is slow → **O(n)**

Because traversal starts from the head node.

## ✅ Interview Answer

> A linked list is more flexible for insertion and deletion, but slower than arrays for direct access.


---

# 📚 Stacks & Queues

## Stack → LIFO

**Last In, First Out**

Example:

* Undo operations
* Function call stack

## Queue → FIFO

**First In, First Out**

Example:

* Scheduling
* Buffering
* Task processing

## ✅ Interview Answer

> A stack removes the most recently added element, while a queue removes the oldest added element.


---

# 🗂️ Hash Tables

A hash table maps keys to values using a hash function.

### Average Complexity

| Operation | Complexity |
| --------- | ---------- |
| Lookup    | O(1)       |
| Insert    | O(1)       |
| Delete    | O(1)       |

### Important Concept

Collisions happen when multiple keys map to the same location.

Common solutions:

* Chaining
* Open Addressing

## ✅ Interview Answer

> A hash table is useful when we need fast key-based lookup, such as checking whether an item exists.


---

# 🔄 Sorting

Sorting arranges data in a specific order.

## Common Complexities

| Algorithm           | Complexity |
| ------------------- | ---------- |
| Bubble Sort         | O(n²)      |
| Merge Sort          | O(n log n) |
| Quicksort (average) | O(n log n) |

Sorting is often used before:

* Searching
* Grouping
* Data processing

## ✅ Interview Answer

> Sorting is often used before searching or grouping data, but it has a cost, typically O(n log n) for efficient general-purpose sorting.


---

# 🔍 Binary Search

Binary search only works on **sorted data**.

At each step:

1. Compare target with middle element
2. Discard half of the search space

Time complexity:

[
O(\log n)
]

## ✅ Interview Answer

> Because the input is sorted, I can use binary search and reduce the search space by half each time.


---

# 🔁 Recursion

Recursion happens when a function calls itself to solve smaller versions of the same problem.

A recursive solution needs:

* Base case → stops recursion
* Recursive case → continues recursion

Examples:

* Factorial
* Tree traversal
* DFS

## ✅ Interview Answer

> Recursion is useful when a problem can naturally be divided into smaller similar subproblems, like trees or factorial.


---

# 📈 Big-O Time Complexity

Big-O describes how runtime grows as input size increases.

It focuses on scalability rather than exact execution time.

## Common Complexities

| Complexity | Meaning           |
| ---------- | ----------------- |
| O(1)       | Constant          |
| O(log n)   | Logarithmic       |
| O(n)       | Linear            |
| O(n log n) | Efficient sorting |
| O(n²)      | Nested loops      |

## ✅ Interview Answer

> Time complexity tells us how an algorithm scales when the input becomes larger.


---

# 🧮 Matrix Multiplication

To multiply:

* Matrix A → size `n × m`
* Matrix B → size `m × p`

Result matrix size:

[
n \times p
]

Each output cell is the dot product of:

* One row from A
* One column from B

The basic algorithm uses **three nested loops**.

## ✅ Interview Answer

> For square matrices, the simple matrix multiplication algorithm is O(n³).


---

# 🎲 Fisher–Yates Shuffle

Fisher–Yates is the standard unbiased algorithm for shuffling an array.

## Algorithm

Starting from the end:

1. Pick a random index from `0` to `i`
2. Swap elements

Time complexity:

[
O(n)
]

## ✅ Interview Answer

> If the random generator is fair, Fisher–Yates gives every permutation equal probability.


---

# 🎯 Likely Interview Questions

Practice these answers aloud. Do not memorize word-for-word; memorize the structure and key points.


## 1. How do you multiply two matrices?

To multiply two matrices, the number of columns in the first matrix must be equal to the number of rows in the second
matrix. If A is n x m and B is m x p, the result C will be n x p.

For each cell C[i][j], I compute the dot product of row i from A and column j from B. 
The simple algorithm uses three
nested loops. Its time complexity is O(n*m*p), and for square matrices it is O(n^3).

```
for i from 0 to n-1:
for j from 0 to p-1:
C[i][j] = 0
for k from 0 to m-1:
C[i][j] += A[i][k] * B[k][j]
```
---
## 2. How do you shuffle an array?

I would use the Fisher-Yates shuffle. Starting from the last index, I choose a random index between 0 and the current
index and swap the two elements.

This method is unbiased if the random number generator is fair, because every permutation has the same probability.
The time complexity is O(n), and it shuffles in place with O(1) extra memory.

```
for i from n-1 down to 1:
j = random integer between 0 and i
swap arr[i] and arr[j]
```
---
## 3. What is binary search?

Binary search is a search algorithm for sorted data. 
It repeatedly checks the middle element and removes half of the
remaining search space. It is much faster than linear search for large sorted arrays, with O(log n) time complexity.

 The main condition is that the data must be sorted

---

## 4. What is the difference between an array and a linked list?

An array stores elements in contiguous memory and allows O(1) access by index, but insertion or deletion in the middle
can be O(n). A linked list stores nodes connected by pointers. 

It is better for insertion and deletion when the position is known, but random access is O(n) because we must traverse node by node.

---

## 5. What is the difference between a stack and a queue?
A stack follows LIFO: last in, first out. The last element added is the first one removed. A queue follows FIFO: first in, first
out. The first element added is the first one removed. Stacks are useful for recursion and undo operations; queues are
useful for scheduling, buffering, and breadth-first search

---

## 6. What is recursion?

Recursion is a technique where a function calls itself to solve smaller versions of the same problem. Every recursive
function needs a base case to stop and a recursive case to continue. For example, factorial(n) can be defined as n *
factorial(n-1), with factorial(0) = 1.

---

## 7. What's hashing? How it works?


## 8. Write a function that checks if a string is palindrome. 
---

# 🎯 Final Interview Tips

* Speak clearly and confidently
* Always mention time complexity
* Explain trade-offs between data structures
* Use small examples while explaining
* If you forget syntax, explain the logic

---

# ⚡ Quick Revision Checklist

* [ ] Arrays vs Linked Lists
* [ ] Stack vs Queue
* [ ] Hash Tables
* [ ] Binary Search
* [ ] Sorting Complexity
* [ ] Recursion
* [ ] Big-O
* [ ] Matrix Multiplication
* [ ] Fisher–Yates Shuffle

---

Good luck with your interview 🚀
