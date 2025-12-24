# Data Structures & Algorithms (DSA) — BPSC Computer Teacher Exam Notes (Detailed & Comprehensive)

**Format:** Theory (concepts + exam points + formulas) → Section MCQs (A–D) → Correct Option → Explanation

---

## 1) Introduction & Complexity Analysis

### What is a Data Structure?
- A way to **organize and store data** so operations (search, insert, delete, update) can be done efficiently.
- **Linear DS:** Array, Linked List, Stack, Queue.
- **Non-linear DS:** Trees, Graphs.

### What is an Algorithm?
- A **finite set of steps** to solve a problem correctly.
- Quality measured by **time complexity** and **space complexity**.

### Asymptotic Notations (Most asked)
- **Big-O (O):** Upper bound (worst-case growth).
- **Big-Ω (Ω):** Lower bound (best-case growth).
- **Big-Θ (Θ):** Tight bound (exact growth class).

### Common Growth Rates (increasing order)
- O(1) < O(log n) < O(n) < O(n log n) < O(n^2) < O(2^n) < O(n!)

### Rules (Quick)
- Drop constants: 3n + 10 → O(n)
- Dominant term: n^2 + n → O(n^2)
- Loop patterns:
  - Single loop to n → O(n)
  - Nested loops n×n → O(n^2)
  - Halving each step → O(log n)

---

### MCQs (Section 1)

## Q1. The notation that gives the **upper bound** of time complexity is:
A. Ω (Big-Omega)
B. Θ (Big-Theta)
C. O (Big-O)
D. π (Pi)

> **Correct Option: C**
> **Explanation:** Big-O describes an upper bound and is commonly used to express worst-case growth.

## Q2. If an algorithm runs in time 5n + 20, its Big-O is:
A. O(n^2)
B. O(n)
C. O(log n)
D. O(1)

> **Correct Option: B**
> **Explanation:** Drop constants and lower-order terms; 5n+20 grows linearly.

## Q3. A loop where the variable is divided by 2 each iteration has complexity:
A. O(n)
B. O(n^2)
C. O(log n)
D. O(1)

> **Correct Option: C**
> **Explanation:** Repeated halving leads to logarithmic number of iterations.

---

## 2) Arrays

### Key Points
- **Contiguous memory** structure, supports O(1) random access using index.
- **Insertion/deletion** in middle requires shifting: O(n).
- **2D array** stored in memory as 1D using row-major/column-major order.

### Advantages
- Fast access, cache-friendly.

### Disadvantages
- Fixed size (static arrays), expensive insert/delete in middle.

### Dynamic Arrays (Vectors)
- Dynamically resize when capacity exceeded.
- Amortized O(1) insertion at end.

---

### MCQs (Section 2)

## Q4. Random access in arrays is:
A. O(1)
B. O(log n)
C. O(n)
D. O(n log n)

> **Correct Option: A**
> **Explanation:** Direct indexing gives constant time access.

## Q5. Inserting an element at the beginning of an array of size n takes:
A. O(1)
B. O(log n)
C. O(n)
D. O(n^2)

> **Correct Option: C**
> **Explanation:** All elements must be shifted right by one.

---

## 3) Linked Lists

### Types
- **Singly LL:** node = (data, next)
- **Doubly LL:** (prev, data, next)
- **Circular LL:** last node points to first.

### Operations (Typical)
- Insert/delete at head: **O(1)**
- Search by value: **O(n)**

### Pros/Cons
- **Pros:** dynamic size, insert/delete easier than arrays (no shifting).
- **Cons:** extra memory for pointers; no random access.

---

### MCQs (Section 3)

## Q6. Which structure supports dynamic size and no contiguous memory requirement?
A. Array
B. Linked list
C. Stack
D. Heap sort

> **Correct Option: B**
> **Explanation:** Linked lists allocate nodes dynamically and do not require contiguous memory.

## Q7. Accessing the k-th element in a singly linked list is:
A. O(1)
B. O(log n)
C. O(k)
D. O(n^2)

> **Correct Option: C**
> **Explanation:** Must traverse from head to the k-th node.

---

## 4) Stack

### Definition
- Linear DS following **LIFO** (Last In First Out).

### Operations
- push, pop, peek/top.
- Implemented using **array** or **linked list**.

### Applications
- Function calls/recursion stack, expression evaluation, parentheses checking, undo operations.

### Time Complexities
- Push: O(1)
- Pop: O(1)
- Peek: O(1)

---

### MCQs (Section 4)

## Q8. Stack follows:
A. FIFO
B. LIFO
C. Random access
D. Priority order

> **Correct Option: B**
> **Explanation:** Last inserted element is removed first.

## Q9. Which is a common application of stack?
A. BFS traversal
B. Parentheses matching
C. CPU scheduling (Round Robin)
D. Hashing

> **Correct Option: B**
> **Explanation:** Stack is used to match opening and closing brackets.

---

## 5) Queue & Deque

### Queue
- Linear DS following **FIFO** (First In First Out).
- Operations: enqueue, dequeue, front/rear.
- Time: O(1) each.

### Circular Queue
- Solves wasted space problem in linear queue (array implementation).

### Deque
- Double-ended queue: insert/delete at both ends.
- Time: O(1) for all operations.

### Applications
- Scheduling, buffering, BFS in graphs, print queue.

---

### MCQs (Section 5)

## Q10. Queue follows:
A. LIFO
B. FIFO
C. FILO
D. LILO

> **Correct Option: B**
> **Explanation:** First inserted element is removed first.

## Q11. BFS traversal uses:
A. Stack
B. Queue
C. Heap
D. Hash table

> **Correct Option: B**
> **Explanation:** BFS explores level by level using a queue.

---

## 6) Recursion

### Concept
- Function calls itself with smaller input until a base condition.

### Notes
- Recursion uses **call stack**.
- Can be converted to iteration using an explicit stack.

### Common Recurrence Relations
- T(n) = T(n-1) + 1 → O(n) (linear recursion)
- T(n) = 2T(n/2) + n → O(n log n) (Merge sort, divide and conquer)
- T(n) = T(n-1) + T(n-2) → O(2^n) (Fibonacci, exponential)

---

### MCQs (Section 6)

## Q12. Recursion internally uses:
A. Queue
B. Stack
C. Heap
D. Hash table

> **Correct Option: B**
> **Explanation:** Recursive calls are stored in the call stack.

---

## 7) Trees (Basics)

### Terms
- Node, edge, root, parent/child, siblings, leaf, degree.
- **Height:** number of edges in longest path root→leaf.
- **Depth:** number of edges from root to node.

### Binary Tree
- Each node has at most two children.
- Maximum nodes at level k: 2^k.

### Traversals
- **Preorder:** Root–Left–Right (depth-first)
- **Inorder:** Left–Root–Right (depth-first)
- **Postorder:** Left–Right–Root (depth-first)
- **Level order:** BFS (breadth-first, uses queue)

---

### MCQs (Section 7)

## Q13. Inorder traversal order is:
A. Root–Left–Right
B. Left–Root–Right
C. Left–Right–Root
D. Root–Right–Left

> **Correct Option: B**
> **Explanation:** Inorder visits left subtree, then root, then right subtree.

## Q14. Level order traversal is also called:
A. Depth-first
B. Breadth-first
C. In-order
D. Pre-order

> **Correct Option: B**
> **Explanation:** Level order explores all nodes at depth k before k+1 (breadth-first).

---

## 8) Binary Search Tree (BST)

### Property
- For each node: left subtree keys < node key < right subtree keys.
- No duplicate keys (typically).

### Operations (Average)
- Search/Insert/Delete: O(log n) average, O(n) worst (skewed tree).

### Worst Case
- Skewed tree (like a linked list) gives O(n) for all operations.

---

### MCQs (Section 8)

## Q15. In a BST, the inorder traversal gives:
A. Random order
B. Descending order
C. Sorted (ascending) order
D. Level order

> **Correct Option: C**
> **Explanation:** Inorder traversal of BST yields sorted sequence.

## Q16. Worst-case time for BST search is:
A. O(log n)
B. O(1)
C. O(n)
D. O(n log n)

> **Correct Option: C**
> **Explanation:** Skewed BST can degenerate to a chain.

---

## 9) AVL Trees

### Balance Factor
- BF = Height(left) - Height(right)
- For AVL: |BF| ≤ 1 for all nodes.

### Rotations
- Single right rotation, Single left rotation, Left-Right, Right-Left.

### Operations
- Search/Insert/Delete: O(log n) guaranteed.

---

### MCQs (Section 9)

## Q17. AVL tree maintains:
A. Balance factor ≤ 0
B. |Balance factor| ≤ 1
C. All nodes have equal height
D. No rotations needed

> **Correct Option: B**
> **Explanation:** AVL ensures |BF| ≤ 1 to maintain balance.

---

## 10) Heap & Priority Queue

### Binary Heap
- **Complete binary tree** stored often in an array.
- **Max-heap:** parent ≥ children
- **Min-heap:** parent ≤ children

### Priority Queue
- Often implemented using heap.

### Complexities
- Insert: O(log n)
- Delete-max/min: O(log n)
- Find-max/min: O(1)
- Heapify: O(n) for n elements.

---

### MCQs (Section 10)

## Q18. A binary heap is a:
A. Perfect binary tree
B. Complete binary tree
C. Full binary tree always
D. Skewed tree

> **Correct Option: B**
> **Explanation:** Heap structure requires completeness; heap-order property defines min/max.

## Q19. Inserting an element into a min-heap takes:
A. O(1)
B. O(log n)
C. O(n)
D. O(n log n)

> **Correct Option: B**
> **Explanation:** Insert at leaf and percolate up (at most log n swaps).

---

## 11) Hashing

### Hash Table
- Uses **hash function** to map keys to table indices.

### Collisions
- Two keys map to same index.

### Collision Resolution
1. **Chaining:** linked list at each slot.
2. **Open addressing:** linear probing, quadratic probing, double hashing.

### Load Factor
- α = number_of_elements / table_size
- Rehash when α exceeds threshold (typically 0.75).

---

### MCQs (Section 11)

## Q20. Collision in hashing means:
A. Key not found
B. Two keys map to same index
C. Table is full
D. Hash function is constant

> **Correct Option: B**
> **Explanation:** Collision occurs when multiple keys produce the same hash index.

---

## 12) Searching Algorithms

### Linear Search
- Works on unsorted data.
- Time: O(n) worst, O(1) best.

### Binary Search
- Requires sorted array.
- Time: O(log n).

### Interpolation Search
- For uniformly distributed data.
- Time: O(log log n) average.

---

### MCQs (Section 12)

## Q21. Binary search requires:
A. Unsorted array
B. Sorted array
C. Linked list only
D. Hash table

> **Correct Option: B**
> **Explanation:** Binary search repeatedly halves search space; needs sorted order.

---

## 13) Sorting Algorithms (Very Important)

### Comparison-based Sorting
- **Bubble Sort:** O(n^2), stable, in-place. Swaps adjacent elements.
- **Selection Sort:** O(n^2), in-place, not stable generally. Finds min repeatedly.
- **Insertion Sort:** O(n^2) worst, O(n) best (nearly sorted), stable. Inserts into sorted portion.
- **Merge Sort:** O(n log n), stable, needs O(n) extra space. Divide-and-conquer.
- **Quick Sort:** O(n log n) average, O(n^2) worst, in-place (partition in-place). Divide-and-conquer.
- **Heap Sort:** O(n log n), in-place, not stable. Uses heap structure.

### Non-Comparison Sorting
- **Counting Sort:** O(n+k) where k = range, not in-place.
- **Radix Sort:** O(d(n+k)) where d = digits, k = base.
- **Bucket Sort:** O(n+k) average, depends on input distribution.

---

### MCQs (Section 13)

## Q22. Which sorting algorithm is stable and guaranteed O(n log n)?
A. Quick sort
B. Merge sort
C. Heap sort
D. Selection sort

> **Correct Option: B**
> **Explanation:** Merge sort is stable and has worst-case O(n log n).

## Q23. Worst-case time of quicksort is:
A. O(n log n)
B. O(log n)
C. O(n^2)
D. O(n)

> **Correct Option: C**
> **Explanation:** Bad pivot choices can produce skewed partitions leading to O(n^2).

---

## 14) Graphs

### Graph Types
- **Directed/Undirected**, **Weighted/Unweighted**.
- Representation:
  - **Adjacency matrix:** O(V^2) space, fast edge lookup.
  - **Adjacency list:** O(V+E) space, good for sparse graphs.

### Traversals
- **BFS:** uses queue; shortest path in unweighted graph.
- **DFS:** uses stack/recursion; cycle detection, topological sorting.

### Key Algorithms
- **Dijkstra:** Single-source shortest path (non-negative weights). O((V+E) log V) with min-heap.
- **Floyd-Warshall:** All-pairs shortest path. O(V^3).
- **Kruskal:** Minimum spanning tree. O(E log E).
- **Prim:** Minimum spanning tree. O(V^2) or O((V+E) log V).
- **Topological Sort:** For DAG. O(V+E).

---

### MCQs (Section 14)

## Q24. Adjacency list is preferred for:
A. Dense graphs
B. Sparse graphs
C. Only directed graphs
D. Only trees

> **Correct Option: B**
> **Explanation:** For sparse graphs, adjacency list uses O(V+E) space efficiently.

## Q25. DFS is most useful for:
A. Shortest path in unweighted graph
B. Topological sorting
C. Minimum spanning tree
D. Single-source shortest path

> **Correct Option: B**
> **Explanation:** DFS finds topological order in DAG.

---

## 15) Algorithm Design Techniques (BPSC-level)

### Divide and Conquer
- Break problem into subproblems, solve recursively, combine.
- Examples: Merge sort, Quick sort, Binary search.

### Greedy
- Make locally optimal choices hoping for global optimum.
- Examples: Activity selection, Huffman coding, Dijkstra (non-negative edges), Prim/Kruskal (MST).

### Dynamic Programming (DP)
- Overlapping subproblems + optimal substructure.
- Use memoization (top-down) or tabulation (bottom-up).
- Examples: Fibonacci, 0/1 Knapsack, Longest Common Subsequence (LCS), Coin change, Matrix chain multiplication.

### Backtracking
- Explore search space, undo decisions when dead-end.
- Examples: N-Queens, Sudoku, Permutations/Combinations.

---

### MCQs (Section 15)

## Q26. Dynamic programming is best suited when a problem has:
A. Only one solution
B. Overlapping subproblems
C. No recursion
D. Only sorting

> **Correct Option: B**
> **Explanation:** DP stores solutions of overlapping subproblems to avoid recomputation.

## Q27. Greedy algorithms work optimally for:
A. All problems
B. Problems with optimal substructure and greedy choice property
C. Only sorting problems
D. All graph problems

> **Correct Option: B**
> **Explanation:** Greedy works when local optimum leads to global optimum (problem-dependent).

---

## 16) String Algorithms

### Pattern Matching
- **Naive:** O(n·m)
- **KMP (Knuth-Morris-Pratt):** O(n+m) using LPS array.
- **Boyer-Moore:** O(n/m) average, good for large alphabets.

### Longest Common Subsequence (LCS)
- DP solution: O(m·n) time, O(m·n) space.

---

### MCQs (Section 16)

## Q28. KMP algorithm improves pattern matching by:
A. Using multiple threads
B. Avoiding recomputation using LPS array
C. Sorting the pattern
D. Only checking first character

> **Correct Option: B**
> **Explanation:** LPS array avoids rechecking characters.

---

## End of DSA Comprehensive Notes
---
