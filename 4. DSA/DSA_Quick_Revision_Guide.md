# DSA Quick Revision Guide - BPSC Computer Teacher Exam

> **Purpose:** Last-minute revision covering all important concepts, formulas, and key points.

---

## 📊 TIME & SPACE COMPLEXITY CHEAT SHEET

### Common Complexities (Fastest to Slowest)
```
O(1) < O(log log n) < O(log n) < O(√n) < O(n) < O(n log n) < O(n²) < O(n³) < O(2ⁿ) < O(n!)
```

### Growth Rate Comparison (n = 1000)
| Complexity | Operations | Name |
|------------|------------|------|
| O(1) | 1 | Constant |
| O(log n) | ~10 | Logarithmic |
| O(n) | 1,000 | Linear |
| O(n log n) | ~10,000 | Linearithmic |
| O(n²) | 1,000,000 | Quadratic |
| O(2ⁿ) | 10³⁰⁰ | Exponential |

### Asymptotic Notations Summary
| Notation | Meaning | Use Case |
|----------|---------|----------|
| **O (Big-O)** | Upper bound | Worst-case |
| **Ω (Omega)** | Lower bound | Best-case |
| **Θ (Theta)** | Tight bound | Average/Exact |
| **o (little-o)** | Strict upper bound | Grows slower |
| **ω (little-omega)** | Strict lower bound | Grows faster |

### Master Theorem Quick Reference
**For T(n) = aT(n/b) + f(n)**

| Case | Condition | Result |
|------|-----------|--------|
| 1 | f(n) = O(n^c), c < log_b(a) | Θ(n^(log_b(a))) |
| 2 | f(n) = Θ(n^c log^k n), c = log_b(a) | Θ(n^c log^(k+1) n) |
| 3 | f(n) = Ω(n^c), c > log_b(a) + regularity | Θ(f(n)) |

### Common Recurrences
| Recurrence | Complexity | Example |
|------------|------------|---------|
| T(n) = T(n-1) + O(1) | O(n) | Linear recursion |
| T(n) = T(n-1) + O(n) | O(n²) | Insertion sort |
| T(n) = 2T(n/2) + O(1) | O(n) | Binary tree height |
| T(n) = 2T(n/2) + O(n) | O(n log n) | Merge sort |
| T(n) = T(n-1) + T(n-2) | O(2ⁿ) | Fibonacci |

---

## 🗂️ DATA STRUCTURES COMPARISON

### Linear Data Structures

| Data Structure | Access | Search | Insert | Delete | Space | Notes |
|----------------|--------|--------|--------|--------|-------|-------|
| **Array** | O(1) | O(n) | O(n) | O(n) | O(n) | Fixed size, contiguous |
| **Dynamic Array** | O(1) | O(n) | O(1)* | O(n) | O(n) | *Amortized |
| **Singly Linked List** | O(n) | O(n) | O(1)** | O(1)** | O(n) | **At head |
| **Doubly Linked List** | O(n) | O(n) | O(1) | O(1)*** | O(n) | ***With node pointer |
| **Stack** | - | - | O(1) | O(1) | O(n) | LIFO |
| **Queue** | - | - | O(1) | O(1) | O(n) | FIFO |

### Non-Linear Data Structures

| Data Structure | Search | Insert | Delete | Notes |
|----------------|--------|--------|--------|-------|
| **Binary Search Tree** | O(h) | O(h) | O(h) | h = height, worst O(n) |
| **AVL Tree** | O(log n) | O(log n) | O(log n) | Balanced BST |
| **Red-Black Tree** | O(log n) | O(log n) | O(log n) | Balanced BST |
| **B-Tree** | O(log n) | O(log n) | O(log n) | Multi-way tree |
| **Heap (Binary)** | O(n) | O(log n) | O(log n) | Complete binary tree |
| **Hash Table** | O(1)* | O(1)* | O(1)* | *Average case |
| **Graph (Adj List)** | O(V+E) | O(1) | O(E) | Space: O(V+E) |
| **Graph (Adj Matrix)** | O(1) | O(1) | O(1) | Space: O(V²) |

---

## 🔍 SEARCHING ALGORITHMS

| Algorithm | Time (Best) | Time (Avg) | Time (Worst) | Space | Requirement |
|-----------|-------------|------------|--------------|-------|-------------|
| **Linear Search** | O(1) | O(n) | O(n) | O(1) | None |
| **Binary Search** | O(1) | O(log n) | O(log n) | O(1) | Sorted array |
| **Jump Search** | O(1) | O(√n) | O(√n) | O(1) | Sorted array |
| **Interpolation Search** | O(1) | O(log log n) | O(n) | O(1) | Sorted + uniform |
| **Exponential Search** | O(1) | O(log n) | O(log n) | O(1) | Sorted + unbounded |

### Key Points
- **Binary Search:** Requires sorted array, divides search space by 2 each time
- **Jump Search:** Optimal jump size = √n
- **Interpolation Search:** Best for uniformly distributed data
- **Exponential Search:** Good for unbounded/infinite arrays

---

## 📊 SORTING ALGORITHMS - COMPLETE TABLE

### Comparison-Based Sorting

| Algorithm | Best | Average | Worst | Space | Stable | In-place | Notes |
|-----------|------|---------|-------|-------|--------|----------|-------|
| **Bubble Sort** | O(n) | O(n²) | O(n²) | O(1) | Yes | Yes | Simple, adaptive |
| **Selection Sort** | O(n²) | O(n²) | O(n²) | O(1) | No* | Yes | Minimum swaps |
| **Insertion Sort** | O(n) | O(n²) | O(n²) | O(1) | Yes | Yes | Good for nearly sorted |
| **Merge Sort** | O(n log n) | O(n log n) | O(n log n) | O(n) | Yes | No | Guaranteed O(n log n) |
| **Quick Sort** | O(n log n) | O(n log n) | O(n²) | O(log n) | No | Yes | Average case fast |
| **Heap Sort** | O(n log n) | O(n log n) | O(n log n) | O(1) | No | Yes | No best/worst variation |
| **Shell Sort** | O(n log n) | O(n^1.25) | O(n²) | O(1) | No | Yes | Gap sequence dependent |
| **Tim Sort** | O(n) | O(n log n) | O(n log n) | O(n) | Yes | No | Python/Java default |

*Can be made stable with extra space

### Non-Comparison-Based Sorting

| Algorithm | Time | Space | Range | Stable | Notes |
|-----------|------|-------|-------|--------|-------|
| **Counting Sort** | O(n+k) | O(n+k) | k = range | Yes | For integers, small range |
| **Radix Sort** | O(d(n+k)) | O(n+k) | d = digits | Yes | For integers, uses counting |
| **Bucket Sort** | O(n+k) | O(n+k) | - | Yes | For uniformly distributed |

### Sorting - Key Facts to Remember

**Stable Sorting:**
- Maintains relative order of equal elements
- Stable: Bubble, Insertion, Merge, Tim, Counting, Radix, Bucket
- Unstable: Selection, Quick, Heap, Shell

**In-place Sorting:**
- Uses O(1) extra space (excluding recursion stack)
- In-place: Bubble, Selection, Insertion, Quick, Heap, Shell
- Not in-place: Merge, Tim, Counting, Radix, Bucket

**Best General-Purpose:**
- **Small arrays (n < 10):** Insertion Sort
- **Nearly sorted:** Insertion Sort or Tim Sort
- **Large arrays:** Quick Sort (average), Merge Sort (guaranteed)
- **Memory constrained:** Heap Sort or Quick Sort

**Theoretical Lower Bound:** Any comparison-based sorting requires Ω(n log n) comparisons in worst case.

---

## 🌳 TREE ALGORITHMS

### Tree Traversals

| Traversal | Order | Use Case | Implementation |
|-----------|-------|----------|----------------|
| **Preorder** | Root-Left-Right | Copy tree, prefix expression | DFS/Stack |
| **Inorder** | Left-Root-Right | BST → sorted order | DFS/Stack |
| **Postorder** | Left-Right-Root | Delete tree, postfix expression | DFS/Stack |
| **Level Order** | Level by level | BFS, shortest path | Queue |

### Binary Search Tree (BST)
- **Property:** left < root < right for all nodes
- **Inorder traversal:** Gives sorted sequence
- **Search/Insert/Delete:** O(h) where h = height
- **Worst case:** O(n) for skewed tree
- **Best case:** O(log n) for balanced tree

### Balanced Trees Comparison

| Tree Type | Height | Rotation | Search | Insert | Delete | Use Case |
|-----------|--------|----------|--------|--------|--------|----------|
| **AVL Tree** | Strictly O(log n) | Strict | O(log n) | O(log n) | O(log n) | Frequent searches |
| **Red-Black Tree** | ~O(log n) | Relaxed | O(log n) | O(log n) | O(log n) | Frequent insertions |
| **B-Tree** | O(log n) | - | O(log n) | O(log n) | O(log n) | Databases, file systems |

### AVL Tree
- **Balance Factor (BF):** Height(left) - Height(right)
- **AVL Property:** |BF| ≤ 1 for all nodes
- **Rotations:** LL (right), RR (left), LR (left-right), RL (right-left)

### B-Tree (Order m)
- Each node has at most m children
- Each non-root node has at least ⌈m/2⌉ children
- All leaves at same level
- Used in databases and file systems

---

## 📈 HEAP DATA STRUCTURE

### Binary Heap Properties
- **Complete Binary Tree:** All levels filled except possibly last (filled left to right)
- **Heap Order:**
  - **Max-Heap:** Parent ≥ Children
  - **Min-Heap:** Parent ≤ Children

### Heap Operations

| Operation | Time Complexity | Description |
|-----------|----------------|-------------|
| **Find Min/Max** | O(1) | Root element |
| **Insert** | O(log n) | Insert at end, bubble up |
| **Delete Min/Max** | O(log n) | Remove root, bubble down |
| **Heapify** | O(n) | Build heap from array |
| **Heap Sort** | O(n log n) | Extract all elements |

### Array Representation
- **Parent of i:** ⌊(i-1)/2⌋
- **Left child of i:** 2i + 1
- **Right child of i:** 2i + 2

### Heapify Algorithm
**Bottom-up (O(n)):**
```
Start from last non-leaf node: ⌊n/2⌋ - 1
For each node from right to left:
    Percolate down to maintain heap property
```

### Priority Queue Implementation
- Best implemented using Binary Heap
- Operations: enqueue O(log n), dequeue O(log n), peek O(1)

---

## 🔗 GRAPH ALGORITHMS

### Graph Representations

| Representation | Space | Add Vertex | Add Edge | Remove Edge | Query Edge |
|----------------|-------|------------|----------|-------------|------------|
| **Adjacency Matrix** | O(V²) | O(V²) | O(1) | O(1) | O(1) |
| **Adjacency List** | O(V+E) | O(1) | O(1) | O(E) | O(deg(V)) |

**Use Adjacency List for:** Sparse graphs (E << V²)  
**Use Adjacency Matrix for:** Dense graphs, frequent edge queries

### Graph Traversal Algorithms

| Algorithm | Time | Space | Data Structure | Use Cases |
|-----------|------|-------|----------------|-----------|
| **BFS** | O(V+E) | O(V) | Queue | Shortest path (unweighted), level-order |
| **DFS** | O(V+E) | O(V) | Stack/Recursion | Cycle detection, topological sort, connectivity |

### Shortest Path Algorithms

| Algorithm | Type | Time | Space | Works With | Notes |
|-----------|------|------|-------|------------|-------|
| **Dijkstra** | Single-source | O((V+E) log V) | O(V) | Non-negative weights | Uses min-heap |
| **Bellman-Ford** | Single-source | O(VE) | O(V) | Negative weights | Detects negative cycles |
| **Floyd-Warshall** | All-pairs | O(V³) | O(V²) | Negative weights | DP approach |
| **BFS** | Single-source | O(V+E) | O(V) | Unweighted | Queue-based |

### Minimum Spanning Tree (MST)

| Algorithm | Time | Space | Approach | Notes |
|-----------|------|-------|----------|-------|
| **Kruskal's** | O(E log E) | O(V) | Greedy (edges) | Sort edges, use Union-Find |
| **Prim's** | O((V+E) log V) | O(V) | Greedy (vertices) | Uses min-heap |

**MST Properties:**
- Has V-1 edges for V vertices
- No cycles
- Connects all vertices
- Minimum total edge weight

### Other Important Graph Algorithms

| Algorithm | Time | Purpose |
|-----------|------|---------|
| **Topological Sort** | O(V+E) | Linear ordering of DAG |
| **Strongly Connected Components (Kosaraju)** | O(V+E) | Find SCCs in directed graph |
| **Articulation Points** | O(V+E) | Find critical vertices |
| **Bridges** | O(V+E) | Find critical edges |
| **Cycle Detection (Undirected)** | O(V+E) | Uses DFS |
| **Cycle Detection (Directed)** | O(V+E) | Uses DFS + recursion stack |

### Key Graph Concepts

**Graph Types:**
- **Directed/Undirected:** Edges have/don't have direction
- **Weighted/Unweighted:** Edges have/don't have weights
- **Connected:** Path exists between every pair of vertices
- **Complete:** Edge exists between every pair of vertices
- **Cyclic/Acyclic:** Contains/doesn't contain cycles
- **DAG:** Directed Acyclic Graph

**Special Graphs:**
- **Tree:** Connected acyclic graph with V-1 edges
- **Forest:** Collection of trees
- **Bipartite:** Vertices can be divided into 2 sets (no edge within set)
- **Complete Graph (Kn):** Every pair connected, E = V(V-1)/2

---

## 🧮 HASHING

### Hash Table Basics
- **Load Factor (α):** n/m (n = elements, m = table size)
- **Collision:** Two keys map to same index
- **Good Hash Function:** Uniform distribution, fast to compute

### Collision Resolution Techniques

| Technique | Description | Search (Avg) | Search (Worst) | Notes |
|-----------|-------------|--------------|----------------|-------|
| **Chaining** | Linked list at each slot | O(1+α) | O(n) | Simple, no clustering |
| **Linear Probing** | h(k,i) = (h(k)+i) mod m | O(1) | O(n) | Primary clustering |
| **Quadratic Probing** | h(k,i) = (h(k)+i²) mod m | O(1) | O(n) | Reduces clustering |
| **Double Hashing** | h(k,i) = (h1(k)+i·h2(k)) mod m | O(1) | O(n) | Best distribution |

### Common Hash Functions
1. **Division Method:** h(k) = k mod m (m should be prime)
2. **Multiplication Method:** h(k) = ⌊m(kA mod 1)⌋ (A ≈ 0.618)
3. **Universal Hashing:** Randomly select from family of hash functions

### When to Rehash
- When load factor exceeds threshold (typically 0.75)
- Create new table (typically 2× size)
- Reinsert all elements

---

## 🎯 ALGORITHM DESIGN PARADIGMS

### 1. Divide and Conquer
**Strategy:** Divide problem → Solve subproblems → Combine solutions

**Template:**
```
function divideAndConquer(problem):
    if problem is small enough:
        solve directly
    divide problem into subproblems
    solve each subproblem recursively
    combine solutions
```

**Examples:**
- Merge Sort: T(n) = 2T(n/2) + O(n) = O(n log n)
- Quick Sort: T(n) = T(k) + T(n-k-1) + O(n) = O(n log n) avg
- Binary Search: T(n) = T(n/2) + O(1) = O(log n)
- Strassen's Matrix Multiplication: O(n^2.807)

### 2. Dynamic Programming (DP)
**When to Use:**
- Overlapping subproblems
- Optimal substructure

**Approaches:**
1. **Memoization (Top-Down):** Recursion + caching
2. **Tabulation (Bottom-Up):** Iterative + table

**Classic Problems:**

| Problem | Recurrence | Complexity | Space |
|---------|------------|------------|-------|
| **Fibonacci** | F(n) = F(n-1) + F(n-2) | O(n) | O(n) or O(1) |
| **0/1 Knapsack** | dp[i][w] = max(take, skip) | O(nW) | O(nW) |
| **LCS** | dp[i][j] = dp[i-1][j-1]+1 or max | O(mn) | O(mn) |
| **LIS** | dp[i] = max(dp[j]+1) | O(n²) | O(n) |
| **Coin Change** | dp[i] = min(dp[i-coin]+1) | O(n×m) | O(n) |
| **Edit Distance** | dp[i][j] = min(insert,delete,replace) | O(mn) | O(mn) |
| **Matrix Chain Multiplication** | dp[i][j] = min(dp[i][k]+dp[k+1][j]+cost) | O(n³) | O(n²) |

### 3. Greedy Algorithms
**When to Use:**
- Optimal substructure
- Greedy choice property (local optimum → global optimum)

**Classic Problems:**

| Problem | Strategy | Complexity | Correctness |
|---------|----------|------------|-------------|
| **Activity Selection** | Sort by end time | O(n log n) | Provably optimal |
| **Fractional Knapsack** | Sort by value/weight ratio | O(n log n) | Provably optimal |
| **Huffman Coding** | Build tree from frequencies | O(n log n) | Provably optimal |
| **Dijkstra's Algorithm** | Choose min distance vertex | O((V+E) log V) | Non-negative weights |
| **Prim's/Kruskal's MST** | Choose min weight edge | O(E log E) | Provably optimal |

**Note:** Greedy doesn't always work (e.g., 0/1 Knapsack needs DP)

### 4. Backtracking
**Strategy:** Try all possibilities, abandon invalid paths

**Template:**
```
function backtrack(choices, current_solution):
    if is_solution(current_solution):
        add to results
        return
    for choice in choices:
        if is_valid(choice):
            make_choice()
            backtrack(remaining_choices, updated_solution)
            undo_choice()
```

**Classic Problems:**
- N-Queens: O(N!)
- Sudoku Solver: O(9^(n²))
- Subset Sum: O(2ⁿ)
- Graph Coloring: O(m^V)
- Hamiltonian Path: O(N!)

---

## 📝 STRING ALGORITHMS

### Pattern Matching Algorithms

| Algorithm | Preprocessing | Matching | Total | Space | Best For |
|-----------|---------------|----------|-------|-------|----------|
| **Naive** | - | O(nm) | O(nm) | O(1) | Small strings |
| **Rabin-Karp** | O(m) | O(n+m) avg, O(nm) worst | O(n+m) | O(1) | Multiple pattern search |
| **KMP** | O(m) | O(n) | O(n+m) | O(m) | Single pattern |
| **Boyer-Moore** | O(m+σ) | O(n/m) best, O(nm) worst | O(n+m) | O(m+σ) | Large alphabet |

**Notes:**
- n = text length, m = pattern length, σ = alphabet size
- KMP uses LPS (Longest Proper Prefix which is also Suffix) array
- Boyer-Moore uses bad character and good suffix heuristics

### Other String Algorithms

| Algorithm/Problem | Complexity | Use Case |
|-------------------|------------|----------|
| **Longest Common Subsequence (LCS)** | O(mn) | Diff tools, DNA sequence |
| **Longest Common Substring** | O(mn) | Plagiarism detection |
| **Longest Palindromic Substring** | O(n²) DP, O(n) Manacher's | Palindrome problems |
| **Edit Distance (Levenshtein)** | O(mn) | Spell checker, DNA alignment |
| **Trie Insert/Search** | O(m) | Autocomplete, spell checker |
| **Suffix Array Construction** | O(n log² n) | Pattern matching, data compression |

---

## 🔬 ADVANCED DATA STRUCTURES (Quick Overview)

### Segment Tree
- **Purpose:** Range queries (sum, min, max) with updates
- **Build:** O(n)
- **Query:** O(log n)
- **Update:** O(log n)
- **Space:** O(4n) ≈ O(n)

### Fenwick Tree (Binary Indexed Tree)
- **Purpose:** Prefix sums with updates
- **Build:** O(n log n) or O(n)
- **Query:** O(log n)
- **Update:** O(log n)
- **Space:** O(n)
- **Simpler than Segment Tree but less versatile**

### Disjoint Set Union (Union-Find)
- **Purpose:** Track disjoint sets, connectivity
- **Find:** O(α(n)) ≈ O(1) with path compression
- **Union:** O(α(n)) ≈ O(1) with union by rank
- **Applications:** Kruskal's MST, detect cycles, dynamic connectivity

### Trie (Prefix Tree)
- **Purpose:** Efficient string storage and retrieval
- **Insert/Search:** O(m) where m = string length
- **Space:** O(ALPHABET_SIZE × N × M) worst case
- **Applications:** Autocomplete, spell checker, IP routing

---

## 💡 PROBLEM-SOLVING PATTERNS

### Two Pointers
**Use when:** Array/string problems with pairs, triplets, or subarrays
**Examples:** Two sum (sorted), remove duplicates, container with most water

### Sliding Window
**Use when:** Subarray/substring problems with contiguous elements
**Types:**
- **Fixed Size:** Max sum of k elements
- **Variable Size:** Longest substring with k distinct characters

### Fast & Slow Pointers
**Use when:** Linked list cycle detection, finding middle element
**Examples:** Detect cycle, find cycle start, palindrome linked list

### Merge Intervals
**Use when:** Overlapping intervals
**Examples:** Merge intervals, insert interval, meeting rooms

### Binary Search Variations
**Use when:** Sorted array or search space that can be divided
**Examples:** Search in rotated array, find peak element, sqrt(x)

### Top K Elements
**Use when:** Finding largest/smallest K elements
**Approach:** Use heap (O(n log k)) or quickselect (O(n) average)

### Tree DFS
**Use when:** Tree traversal, path problems
**Examples:** Path sum, diameter, lowest common ancestor

### Tree BFS
**Use when:** Level-order traversal, shortest path in tree
**Examples:** Level order traversal, right view, zigzag traversal

### Graph DFS
**Use when:** Cycle detection, path finding, connectivity
**Examples:** Number of islands, clone graph, course schedule

### Graph BFS
**Use when:** Shortest path (unweighted), level-wise processing
**Examples:** Shortest path, word ladder, rotting oranges

---

## 🎓 COMMON MISTAKES TO AVOID

### 1. Off-by-One Errors
- Array indexing (0-based vs 1-based)
- Loop bounds (< n vs ≤ n)
- Empty arrays/lists

### 2. Integer Overflow
- Use long long for large computations
- Check before multiplying large numbers
- Modulo arithmetic: (a+b)%m = ((a%m)+(b%m))%m

### 3. Null/None Checks
- Always check if pointer/reference is null
- Especially in linked lists and trees

### 4. Edge Cases
- Empty input
- Single element
- All elements same
- Negative numbers
- Very large numbers

### 5. Time Complexity
- Nested loops often O(n²)
- Be careful with string concatenation in loops (can be O(n²))
- Hidden complexities in library functions

### 6. Space Complexity
- Recursion uses stack space O(depth)
- Creating new arrays/strings uses space
- In-place modification may be required

---

## 📚 IMPORTANT FORMULAS & FACTS

### Mathematical Formulas
```
Sum of first n natural numbers: n(n+1)/2
Sum of squares: n(n+1)(2n+1)/6
Sum of cubes: [n(n+1)/2]²
Sum of GP: a(r^n - 1)/(r-1)
Number of subsets of size n: 2^n
Number of permutations: n!
Number of combinations: C(n,r) = n!/(r!(n-r)!)
```

### Tree Properties
```
Binary Tree:
- Max nodes at level l: 2^l
- Max nodes in tree of height h: 2^(h+1) - 1
- Min height with n nodes: ⌈log₂(n+1)⌉

Complete Binary Tree:
- Height: ⌊log₂ n⌋
- Internal nodes: ⌊n/2⌋

Full Binary Tree:
- If n leaf nodes, total nodes = 2n - 1
```

### Graph Properties
```
Complete Graph (Kn):
- Edges: n(n-1)/2
- Each vertex degree: n-1

Tree:
- Edges = Vertices - 1
- Exactly one path between any two vertices

DAG:
- Must have at least one vertex with in-degree 0
- Must have at least one vertex with out-degree 0
```

---

## 🎯 EXAM-SPECIFIC TIPS

### High-Weightage Topics
1. **Sorting Algorithms** - Time/space complexity, stability
2. **Tree Traversals** - All types with examples
3. **Graph Algorithms** - BFS, DFS, Dijkstra, MST
4. **Hashing** - Collision resolution techniques
5. **Dynamic Programming** - Classic problems
6. **Complexity Analysis** - Asymptotic notations, recurrence relations
7. **BST Operations** - Search, insert, delete
8. **Stack & Queue Applications**

### Quick Memorization Tips
1. **Stable Sorts:** "BIM-TCR" (Bubble, Insertion, Merge, Tim, Counting, Radix)
2. **O(n log n) Sorts:** "MHQ" (Merge, Heap, Quick-average)
3. **Tree Traversals:** "PIL" (Preorder-Inorder-Postorder) + Level order
4. **MST Algorithms:** "KP" (Kruskal, Prim)
5. **Shortest Path:** "DBF" (Dijkstra, Bellman-Ford, Floyd-Warshall)

### Common Trick Questions
1. **BST inorder traversal?** → Sorted sequence
2. **Quick sort worst case?** → O(n²) (poor pivot selection)
3. **Heap is what type of tree?** → Complete binary tree
4. **DFS uses?** → Stack (or recursion)
5. **BFS uses?** → Queue
6. **AVL balance factor?** → Height(left) - Height(right), |BF| ≤ 1
7. **Stable but O(n log n)?** → Merge sort
8. **In-place O(n log n)?** → Heap sort, Quick sort (average)

---

## 🔢 NUMERIC EXAMPLES FOR PRACTICE

### Example 1: Time Complexity
```
for (i = 0; i < n; i++)
    for (j = i; j < n; j++)
        for (k = 0; k < j; k++)
            statement;

Answer: O(n³)
Outer loop: n times
Middle loop: ~n/2 times (average)
Inner loop: ~n/2 times (average)
Total: n × n/2 × n/2 = n³/4 = O(n³)
```

### Example 2: Recurrence
```
T(n) = 3T(n/4) + n²

Using Master Theorem:
a = 3, b = 4
f(n) = n²
log_b(a) = log₄(3) ≈ 0.79

f(n) = n² = Ω(n^(0.79 + ε)) for ε > 0
This is Case 3
Therefore: T(n) = Θ(n²)
```

### Example 3: Heap Operations
```
Build max-heap from: [4, 10, 3, 5, 1]

Step 1: Start from last non-leaf = ⌊5/2⌋ - 1 = 1 (index)
Array: [4, 10, 3, 5, 1]

Step 2: Heapify at index 1 (element 10)
10 > max(5, 1), no change

Step 3: Heapify at index 0 (element 4)
max(10, 3) = 10, swap 4 and 10
Array: [10, 4, 3, 5, 1]

Heapify at index 1 (element 4)
max(5, 1) = 5, swap 4 and 5
Array: [10, 5, 3, 4, 1]

Final Max-Heap: [10, 5, 3, 4, 1]
```

---

## ✅ LAST-MINUTE CHECKLIST

### Must Know Before Exam
- [ ] Time complexities of all sorting algorithms
- [ ] Difference between stable and unstable sorting
- [ ] Tree traversal orders (pre, in, post, level)
- [ ] BST property and inorder traversal result
- [ ] AVL tree balance factor and range
- [ ] Heap property (min-heap vs max-heap)
- [ ] Hash collision resolution methods
- [ ] BFS vs DFS (uses, data structures)
- [ ] Dijkstra's algorithm (works with non-negative weights)
- [ ] MST algorithms (Kruskal vs Prim)
- [ ] Stack LIFO, Queue FIFO
- [ ] Big-O, Omega, Theta notations
- [ ] Master theorem cases
- [ ] DP vs Greedy (when to use which)
- [ ] Linked list cycle detection (Floyd's algorithm)

---

## 🎯 FINAL TIPS

1. **Practice MCQs:** Solve previous year papers
2. **Focus on Concepts:** Don't just memorize, understand why
3. **Trace Algorithms:** Practice tracing with small examples
4. **Time Management:** Don't spend too much time on one question
5. **Elimination:** If confused, eliminate obviously wrong options
6. **Complexity Analysis:** Often tested, practice identifying patterns
7. **Edge Cases:** Questions often have tricky edge cases
8. **Formula Sheet:** Create your own for quick revision
9. **Mock Tests:** Take timed tests before exam
10. **Stay Calm:** If stuck, move on and come back later

---

## 📖 QUICK REFERENCE INDEXES

### When to Use What Data Structure

| Need | Use |
|------|-----|
| Fast access by index | Array |
| Frequent insert/delete at ends | Linked List |
| LIFO operations | Stack |
| FIFO operations | Queue |
| Priority-based processing | Priority Queue (Heap) |
| Fast search/insert/delete | Hash Table |
| Sorted data with operations | BST/AVL |
| Range queries | Segment Tree |
| Prefix sums | Fenwick Tree |
| String prefix matching | Trie |
| Disjoint sets | Union-Find |

### When to Use What Algorithm

| Need | Use |
|------|-----|
| Sort small array | Insertion Sort |
| Sort large array (average) | Quick Sort |
| Sort with guarantee | Merge Sort or Heap Sort |
| Sort integers (small range) | Counting Sort |
| Search in sorted array | Binary Search |
| Shortest path (unweighted) | BFS |
| Shortest path (weighted, non-negative) | Dijkstra |
| Shortest path (negative weights) | Bellman-Ford |
| All-pairs shortest path | Floyd-Warshall |
| Minimum spanning tree | Kruskal or Prim |
| Detect cycle | DFS (+ recursion stack for directed) |
| Topological sort | DFS or Kahn's algorithm |
| Pattern matching | KMP or Boyer-Moore |
| Optimization with subproblems | Dynamic Programming |
| Optimization with greedy choice | Greedy Algorithm |

---

**Best of luck with your BPSC Computer Teacher Exam!** 🎓

*Remember: Understanding > Memorization*
