# Data Structures & Algorithms (DSA) — BPSC Computer Teacher Notes (Ultra Detailed)

**Format:** Detailed theory + exam tables + formulas → Topic-wise MCQs (A–D) → Correct Option → Explanation

---

## 1) Complexity & Asymptotic Analysis

### Why Complexity?
- Complexity estimates help compare algorithms independent of machine and language.
- Two main measures:
- **Time complexity:** number of primitive operations.
- **Space complexity:** extra memory used.

### Asymptotic Notations
| Notation | Meaning | Typical use |
|---|---|---|
| **O(g(n))** | Upper bound | Worst-case growth |
| **Ω(g(n))** | Lower bound | Best-case growth |
| **Θ(g(n))** | Tight bound | Exact growth class |

### Common Growth Order
| Complexity | Name | Example |
|---|---|---|
| O(1) | Constant | Array index access |
| O(log n) | Logarithmic | Binary search |
| O(n) | Linear | Linear search |
| O(n log n) | Linearithmic | Merge/Heap sort |
| O(n^2) | Quadratic | Bubble/Selection sort |
| O(2^n) | Exponential | Subset enumeration |
| O(n!) | Factorial | Permutations brute-force |

### Handy Rules
- Drop constants: 7n + 100 → O(n)
- Keep dominant term: n^2 + n → O(n^2)
- Nested loops multiply: (n)(n) → O(n^2)
- Repeated halving: n, n/2, n/4… → O(log n)

### Master Theorem (Quick Table)
For recurrences of form: **T(n) = aT(n/b) + f(n)**
| Case | Condition | Result |
|---|---|---|
| 1 | f(n) = O(n^(log_b a − ε)) | T(n)=Θ(n^(log_b a)) |
| 2 | f(n)=Θ(n^(log_b a) log^k n) | T(n)=Θ(n^(log_b a) log^(k+1) n) |
| 3 | f(n)=Ω(n^(log_b a + ε)) and regularity | T(n)=Θ(f(n)) |

---

### MCQs (Section 1)

## Q1. Big-O notation represents:
A. Lower bound
B. Upper bound
C. Exact bound only
D. No bound

> **Correct Option: B**
> **Explanation:** Big-O gives an asymptotic upper bound (commonly worst-case).

## Q2. For T(n)=2T(n/2)+n, the time complexity is:
A. O(n)
B. O(n log n)
C. O(n^2)
D. O(log n)

> **Correct Option: B**
> **Explanation:** This is the merge sort recurrence; by Master theorem case 2 → Θ(n log n).

## Q3. If a loop repeatedly divides n by 2 until it becomes 1, number of iterations is:
A. n
B. log n
C. n log n
D. n^2

> **Correct Option: B**
> **Explanation:** Repeated halving leads to logarithmic iterations.

---

## 2) Arrays

### Key Points
- Stored in **contiguous memory**.
- **Random access:** A[i] in O(1).
- Insert/delete at arbitrary position needs shifting → O(n).

### Operations Complexity (Array)
| Operation | Time |
|---|---|
| Access A[i] | O(1) |
| Search (unsorted) | O(n) |
| Insert at end (static) | O(1) if space else not possible |
| Insert at middle | O(n) |
| Delete at middle | O(n) |

### Dynamic Array (Vector/ArrayList)
- If capacity full, resize (often double) and copy.
- **Amortized** insertion at end: O(1).

---

### MCQs (Section 2)

## Q4. Random access in arrays is:
A. O(1)
B. O(log n)
C. O(n)
D. O(n log n)

> **Correct Option: A**
> **Explanation:** Direct index-to-address computation gives constant time access.

## Q5. Deleting the first element in an array of size n requires:
A. No shifting
B. Shifting n−1 elements
C. Shifting 1 element
D. Only swapping

> **Correct Option: B**
> **Explanation:** All remaining elements shift left by one.

---

## 3) Linked Lists

### Types
- **Singly:** (data, next)
- **Doubly:** (prev, data, next)
- **Circular:** last node points to head

### Operations Complexity (Linked List)
| Operation | Singly LL | Doubly LL |
|---|---:|---:|
| Insert at head | O(1) | O(1) |
| Delete at head | O(1) | O(1) |
| Insert at tail | O(n) (if no tail pointer) | O(1) (with tail) |
| Search | O(n) | O(n) |
| Random access | Not supported | Not supported |

### When to Use
- Frequent insert/delete in middle (after traversal).
- Unknown size at compile time.

---

### MCQs (Section 3)

## Q6. Linked list is preferred over array when:
A. Random access is required
B. Frequent insertion/deletion in middle is required
C. Memory must be contiguous
D. Only sorting is needed

> **Correct Option: B**
> **Explanation:** Linked list avoids shifting cost; insert/delete is pointer updates after reaching position.

## Q7. In a singly linked list, accessing the k-th node takes:
A. O(1)
B. O(log k)
C. O(k)
D. O(k log k)

> **Correct Option: C**
> **Explanation:** Traversal from head is required.

---

## 4) Stack

### Definition
- LIFO: Last-In First-Out.

### Implementations
- **Array stack:** fast; fixed capacity unless dynamic.
- **Linked-list stack:** dynamic; extra pointer overhead.

### Common Uses
- Function calls/recursion
- Expression evaluation (infix → postfix)
- Parenthesis matching
- Undo operations

### Operations
| Operation | Meaning | Time |
|---|---|---:|
| push(x) | insert at top | O(1) |
| pop() | remove from top | O(1) |
| peek() | top element without removing | O(1) |

---

### MCQs (Section 4)

## Q8. Stack follows:
A. FIFO
B. LIFO
C. Priority-based
D. Round-robin

> **Correct Option: B**
> **Explanation:** Stack removes the most recently inserted element first.

---

## 5) Queue, Circular Queue, Deque

### Queue
- FIFO: First-In First-Out.

### Circular Queue (Array)
- Solves wasted-space issue of linear queue.
- Uses modulo indexing.

### Deque
- Insert/delete at both ends.

### Operations
| Structure | Enqueue | Dequeue | Notes |
|---|---:|---:|---|
| Queue | O(1) | O(1) | FIFO |
| Circular Queue | O(1) | O(1) | uses wrap-around |
| Deque | O(1) | O(1) | both ends |

---

### MCQs (Section 5)

## Q9. BFS traversal uses:
A. Stack
B. Queue
C. Recursion only
D. Hash table

> **Correct Option: B**
> **Explanation:** BFS explores level-by-level using a queue.

---

## 6) Recursion & Backtracking

### Recursion
- A function calling itself with smaller inputs.
- Needs **base condition** to stop.

### Backtracking
- A systematic trial approach: choose → explore → un-choose.
- Used in: N-Queens, permutations, Sudoku.

### Recurrence Examples
| Recurrence | Typical complexity |
|---|---|
| T(n)=T(n−1)+1 | Θ(n) |
| T(n)=2T(n/2)+n | Θ(n log n) |
| T(n)=T(n−1)+T(n−2) | Θ(2^n) |

---

### MCQs (Section 6)

## Q10. Recursion primarily uses:
A. Queue
B. Stack
C. Heap
D. Hashing

> **Correct Option: B**
> **Explanation:** Function call frames are pushed onto the call stack.

---

## 7) Trees Fundamentals

### Basic Terms
- Node, edge, root, parent, child, leaf, level, degree.
- **Height:** longest root→leaf path (edges count).

### Tree Types (Quick Comparison)
| Type | Key property | Search time |
|---|---|---|
| Binary Tree | ≤2 children | depends |
| BST | left < root < right | O(h) |
| AVL | balanced BST | O(log n) |
| Heap | complete + heap-order | O(log n) insert/delete |

### Traversals
| Traversal | Order |
|---|---|
| Preorder | Root–Left–Right |
| Inorder | Left–Root–Right |
| Postorder | Left–Right–Root |
| Level order | BFS (Queue) |

---

### MCQs (Section 7)

## Q11. Inorder traversal of a BST produces:
A. Random order
B. Sorted order
C. Reverse postorder
D. Level order only

> **Correct Option: B**
> **Explanation:** Inorder visits keys in increasing order in a BST.

---

## 8) BST, AVL Trees

### BST
- Property: left keys < node < right keys.
- Average operations: O(log n) if balanced; worst-case O(n) when skewed.

### AVL Tree
- Self-balancing BST.
- Balance factor BF = height(left) − height(right).
- AVL constraint: |BF| ≤ 1.
- Uses rotations: LL, RR, LR, RL.

---

### MCQs (Section 8)

## Q12. AVL tree ensures:
A. All leaves at same level
B. |Balance factor| ≤ 1
C. Heap order property
D. Graph acyclicity

> **Correct Option: B**
> **Explanation:** AVL maintains height balance using rotations.

---

## 9) Heap & Priority Queue

### Heap Basics
- **Complete binary tree**.
- **Min-heap:** root is minimum.
- **Max-heap:** root is maximum.

### Heap Operations
| Operation | Time |
|---|---:|
| Find-min/max | O(1) |
| Insert | O(log n) |
| Delete-min/max | O(log n) |
| Build-heap (heapify n elements) | O(n) |

---

### MCQs (Section 9)

## Q13. Heap is best described as:
A. Balanced BST
B. Complete binary tree with heap-order property
C. Full binary tree always
D. Graph with cycles

> **Correct Option: B**
> **Explanation:** Heap requires completeness plus heap-order property.

---

## 10) Hashing

### Hash Table
- Maps key → index using hash function.

### Collisions
- Two distinct keys map to same index.

### Collision Handling
| Technique | Idea | Notes |
|---|---|---|
| Chaining | store list at each slot | easy; extra memory |
| Linear probing | next free slot sequentially | primary clustering |
| Quadratic probing | probe i^2 steps | reduces clustering |
| Double hashing | second hash decides jump | best dispersion |

### Load Factor
- α = n/m (n items, m table size).
- Higher α → more collisions.

---

### MCQs (Section 10)

## Q14. Chaining resolves collisions using:
A. Linked lists
B. Stacks
C. Trees only
D. Sorting

> **Correct Option: A**
> **Explanation:** Each hash slot holds a linked list of keys mapping there.

---

## 11) Searching

### Comparison
| Search | Requirement | Time |
|---|---|---|
| Linear search | none | O(n) |
| Binary search | sorted data | O(log n) |

---

### MCQs (Section 11)

## Q15. Binary search requires:
A. Unsorted data
B. Sorted data
C. Hash table only
D. Graph only

> **Correct Option: B**
> **Explanation:** Binary search halves the search interval, requiring sorted order.

---

## 12) Sorting (Most Important)

### Sorting Comparison Table
| Algorithm | Best | Average | Worst | Space | Stable | In-place |
|---|---:|---:|---:|---:|---:|---:|
| Bubble | O(n) | O(n^2) | O(n^2) | O(1) | Yes | Yes |
| Selection | O(n^2) | O(n^2) | O(n^2) | O(1) | No (generally) | Yes |
| Insertion | O(n) | O(n^2) | O(n^2) | O(1) | Yes | Yes |
| Merge | O(n log n) | O(n log n) | O(n log n) | O(n) | Yes | No |
| Quick | O(n log n) | O(n log n) | O(n^2) | O(log n) stack | No (generally) | Yes |
| Heap | O(n log n) | O(n log n) | O(n log n) | O(1) | No | Yes |
| Counting | O(n+k) | O(n+k) | O(n+k) | O(n+k) | Yes | No |

### Notes (Exam points)
- **Stable sort:** equal keys keep relative order.
- **In-place:** uses O(1) extra memory (ignoring recursion stack).

---

### MCQs (Section 12)

## Q16. Which sorting algorithm is stable with guaranteed O(n log n) worst-case?
A. Quick sort
B. Merge sort
C. Heap sort
D. Selection sort

> **Correct Option: B**
> **Explanation:** Merge sort is stable and always O(n log n).

## Q17. Worst-case of quick sort is:
A. O(n)
B. O(n log n)
C. O(n^2)
D. O(log n)

> **Correct Option: C**
> **Explanation:** Worst pivot partitions can create skewed recursion.

---

## 13) Graphs

### Representation
| Representation | Space | Edge lookup | Best for |
|---|---:|---:|---|
| Adjacency Matrix | O(V^2) | O(1) | Dense graphs |
| Adjacency List | O(V+E) | O(deg(v)) | Sparse graphs |

### Traversals
- **BFS:** queue; shortest path in unweighted graphs.
- **DFS:** stack/recursion; topological sort, cycle detection.

### High-yield Algorithms
- **Topological sort:** only for DAG.
- **Dijkstra:** non-negative weights.

---

### MCQs (Section 13)

## Q18. Adjacency list is preferred for:
A. Dense graphs
B. Sparse graphs
C. Only trees
D. Only directed graphs

> **Correct Option: B**
> **Explanation:** Adjacency list uses O(V+E) space which is efficient for sparse graphs.

## Q19. Topological sorting is possible only in:
A. Tree
B. Undirected graph
C. DAG
D. Complete graph

> **Correct Option: C**
> **Explanation:** Topological ordering requires directed acyclic graph.

---

## 14) Algorithm Design Techniques

### Comparison Table
| Technique | Key idea | Typical examples |
|---|---|---|
| Divide & Conquer | split → solve → combine | Merge sort, Quick sort, Binary search |
| Greedy | locally best choice | Activity selection, Huffman, Kruskal/Prim |
| Dynamic Programming | store subproblem results | LCS, Knapsack, Matrix chain |
| Backtracking | try & undo choices | N-Queens, Sudoku |

---

### MCQs (Section 14)

## Q20. DP is most suitable when the problem has:
A. No recursion
B. Overlapping subproblems
C. Only sorting
D. Only hashing

> **Correct Option: B**
> **Explanation:** DP avoids recomputation by storing overlapping subproblem solutions.

---

## 15) String Algorithms

### Pattern Matching
| Algorithm | Time | Key idea |
|---|---:|---|
| Naive | O(nm) | check at every shift |
| KMP | O(n+m) | LPS avoids rechecking |

---

### MCQs (Section 15)

## Q21. KMP algorithm uses:
A. Heap
B. LPS array
C. Queue
D. Hash chaining

> **Correct Option: B**
> **Explanation:** LPS (Longest Proper Prefix also Suffix) enables skipping comparisons.

---

## End of Notes
