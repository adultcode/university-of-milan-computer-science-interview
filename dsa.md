# 🚀 UNIMI Computer Science MSc Interview — Expanded Crash Guide

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
