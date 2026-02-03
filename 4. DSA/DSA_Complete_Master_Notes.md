# [MCQ Practice Sheet](DSA_BPSC_MCQ_320_With_Explanations.md)
# [Back to Study Guide](../README.md)

# 📖 COMPREHENSIVE DATA STRUCTURES & ALGORITHMS (DSA) LECTURE NOTES

> **How to use:**
> 1. Read this theory file first for concepts and explanations.
> 2. After finishing, attempt the linked MCQ sheet for practice.
> 3. Use the README for the recommended study order.

**Target Exams:** BPSC TRE (Computer Science) | UPPSC Polytechnic Lecturer | STET  
**Author:** Senior Computer Science Faculty  
**Level:** Advanced/Graduate Level for Competitive Teaching Exams  
**Format:** Point-wise, Diagrams, Tables, Examples, MCQs with Explanations

---

# 📚 TABLE OF CONTENTS
1. Module 1: Complexity Analysis & Asymptotic Notations
2. Module 2: Arrays & Strings
3. Module 3: Linked Lists (All Variants)
4. Module 4: Stack & Queue (Linear Data Structures)
5. Module 5: Recursion & Backtracking
6. Module 6: Trees (Binary Trees, BST, AVL, B-Trees)
7. Module 7: Heaps & Priority Queues
8. Module 8: Hashing & Hash Tables
9. Module 9: Graphs (Representation & Traversals)
10. Module 10: Graph Algorithms (Shortest Path & MST)
11. Module 11: Searching Algorithms
12. Module 12: Sorting Algorithms (Detailed Analysis)
13. Module 13: Algorithm Design Paradigms
14. Module 14: Dynamic Programming (Classic Problems)
15. Module 15: Greedy Algorithms
16. Module 16: String Algorithms
17. Module 17: Advanced Data Structures
18. Module 18: Revision & Quick Reference

---

# 🎯 MODULE 1: COMPLEXITY ANALYSIS & ASYMPTOTIC NOTATIONS

## 1.1 Why Algorithm Analysis?

### The Need for Analysis
* **Machine Independence:** Compare algorithms without running them on specific hardware.
* **Language Independence:** Compare algorithms without implementing them in specific programming languages.
* **Input Size Scaling:** Understand how performance changes as input grows.

### Two Main Measures
1. **Time Complexity:** How much time does an algorithm take?
2. **Space Complexity:** How much memory does an algorithm use?

---

## 1.2 Types of Analysis

### 1. Best-Case Analysis (Ω - Omega Notation)
* **Definition:** Minimum time/space required for any input of size n.
* **Real-world Analogy:** The optimistic scenario.
* **Example:** In Linear Search, best case is O(1) when element is at first position.

### 2. Average-Case Analysis (Θ - Theta Notation)
* **Definition:** Expected time/space over all possible inputs of size n.
* **Calculation:** Sum of all cases × their probabilities.
* **Example:** Linear Search average case is O(n/2) = O(n).

### 3. Worst-Case Analysis (O - Big O Notation)
* **Definition:** Maximum time/space required for any input of size n.
* **Real-world Analogy:** The pessimistic scenario.
* **Most Used:** In practice, we analyze worst-case because:
  - Gives guaranteed upper bound.
  - For some algorithms (sorting, searching), worst case occurs often.
  - Average case is often difficult to calculate.

---

## 1.3 Asymptotic Notations (The Language of Complexity)

### 1. Big-O Notation (O) - Upper Bound

**Mathematical Definition:**
```
f(n) = O(g(n)) if there exist positive constants c and n₀ such that:
0 ≤ f(n) ≤ c·g(n) for all n ≥ n₀
```

**In Simple Terms:** f(n) grows no faster than g(n) (ignoring constant factors and lower-order terms).

**Examples:**
* 5n² + 3n + 10 = O(n²)
  - For c = 6 and n₀ = 10, 5n² + 3n + 10 ≤ 6n²
* 100n + 50 = O(n)
* log(n) + 5 = O(log n)

**Graph Representation:**
```
     |        f(n)
     |       /
     |      /___c·g(n)
     |     /   /
     |    /   /
     |___/___/________
        n₀
```

### 2. Big-Ω Notation (Ω) - Lower Bound

**Mathematical Definition:**
```
f(n) = Ω(g(n)) if there exist positive constants c and n₀ such that:
0 ≤ c·g(n) ≤ f(n) for all n ≥ n₀
```

**In Simple Terms:** f(n) grows at least as fast as g(n).

**Examples:**
* 5n² + 3n = Ω(n²)
* n log n + 100n = Ω(n log n)

### 3. Big-Θ Notation (Θ) - Tight Bound

**Mathematical Definition:**
```
f(n) = Θ(g(n)) if there exist positive constants c₁, c₂ and n₀ such that:
0 ≤ c₁·g(n) ≤ f(n) ≤ c₂·g(n) for all n ≥ n₀
```

**In Simple Terms:** f(n) grows exactly as fast as g(n).

**Relationship:** f(n) = Θ(g(n)) ⟺ f(n) = O(g(n)) AND f(n) = Ω(g(n))

**Examples:**
* 5n² + 3n = Θ(n²)
* n/2 + 100 = Θ(n)

### 4. Little-o Notation (o) - Strict Upper Bound

**Mathematical Definition:**
```
f(n) = o(g(n)) if for ALL c > 0, there exists n₀ such that:
0 ≤ f(n) < c·g(n) for all n ≥ n₀
```

**In Simple Terms:** f(n) grows strictly slower than g(n).

**Examples:**
* n = o(n²)
* log n = o(n)

### 5. Little-ω Notation (ω) - Strict Lower Bound

**Mathematical Definition:**
```
f(n) = ω(g(n)) if for ALL c > 0, there exists n₀ such that:
0 ≤ c·g(n) < f(n) for all n ≥ n₀
```

**In Simple Terms:** f(n) grows strictly faster than g(n).

---

## 1.4 Common Growth Rates (Increasing Order)

| Complexity | Name | Example Algorithm | Notes |
|------------|------|-------------------|-------|
| **O(1)** | Constant | Array access, Hash table lookup | Independent of input size |
| **O(log log n)** | Double Logarithmic | Interpolation search (uniform data) | Very rare |
| **O(log n)** | Logarithmic | Binary search, AVL operations | Halving problem size |
| **O(√n)** | Square root | Prime checking (trial division) | Square root of input |
| **O(n)** | Linear | Linear search, Array traversal | Proportional to input |
| **O(n log n)** | Linearithmic | Merge sort, Heap sort, Quick sort (avg) | Optimal comparison sorting |
| **O(n²)** | Quadratic | Bubble sort, Selection sort, Insertion sort | Nested loops |
| **O(n³)** | Cubic | Floyd-Warshall, Matrix multiplication | Triple nested loops |
| **O(2ⁿ)** | Exponential | Subset generation, Fibonacci (naive) | Doubles with each input |
| **O(n!)** | Factorial | Permutation generation, TSP brute force | Grows extremely fast |

### Visual Comparison (for n = 20)
```
O(1):        1 operation
O(log n):    ~5 operations
O(n):        20 operations
O(n log n):  ~86 operations
O(n²):       400 operations
O(2ⁿ):       1,048,576 operations
O(n!):       2.43 × 10¹⁸ operations
```

---

## 1.5 Rules for Asymptotic Analysis

### Rule 1: Drop Constants
* **Before:** 3n² + 5n + 100
* **After:** O(n²)
* **Reason:** Constants don't affect growth rate for large n.

### Rule 2: Drop Lower-Order Terms
* **Before:** n³ + n² + n + 1
* **After:** O(n³)
* **Reason:** Higher-order term dominates for large n.

### Rule 3: Multiplication of Complexities
* **Sequential Statements:** Add complexities
  ```
  Statement 1: O(n)
  Statement 2: O(n²)
  Total: O(n) + O(n²) = O(n²)
  ```
* **Nested Statements:** Multiply complexities
  ```
  for (i = 0; i < n; i++)        // O(n)
      for (j = 0; j < n; j++)    // O(n)
          statement;              // O(1)
  Total: O(n) × O(n) × O(1) = O(n²)
  ```

### Rule 4: Logarithmic Loops
* **Halving:** Loop variable divided by constant → O(log n)
  ```
  for (i = n; i > 0; i = i/2)    // O(log n)
  ```
* **Multiplying:** Loop variable multiplied by constant → O(log n)
  ```
  for (i = 1; i < n; i = i*2)    // O(log n)
  ```

---

## 1.6 Master Theorem (For Divide and Conquer Recurrences)

### Standard Form
```
T(n) = aT(n/b) + f(n)
where:
- a ≥ 1: number of subproblems
- b > 1: factor by which problem size is reduced
- f(n): cost of divide and combine steps
```

### Three Cases

**Case 1: Work at leaves dominates**
```
If f(n) = O(n^c) where c < log_b(a)
Then T(n) = Θ(n^(log_b(a)))
```
**Example:** T(n) = 2T(n/2) + O(1)
* a = 2, b = 2, c = 0
* log₂(2) = 1 > 0
* **Result:** T(n) = Θ(n)

**Case 2: Work equally distributed**
```
If f(n) = Θ(n^c·log^k(n)) where c = log_b(a) and k ≥ 0
Then T(n) = Θ(n^c·log^(k+1)(n))
```
**Example:** T(n) = 2T(n/2) + O(n) [Merge Sort]
* a = 2, b = 2, c = 1
* log₂(2) = 1 = c
* **Result:** T(n) = Θ(n log n)

**Case 3: Work at root dominates**
```
If f(n) = Ω(n^c) where c > log_b(a)
AND af(n/b) ≤ kf(n) for some k < 1 (regularity condition)
Then T(n) = Θ(f(n))
```
**Example:** T(n) = 2T(n/2) + O(n²)
* a = 2, b = 2, c = 2
* log₂(2) = 1 < 2
* **Result:** T(n) = Θ(n²)

### Common Recurrences Table

| Recurrence | Algorithm | Complexity |
|------------|-----------|------------|
| T(n) = T(n-1) + O(1) | Linear recursion | O(n) |
| T(n) = T(n-1) + O(n) | Insertion sort | O(n²) |
| T(n) = 2T(n-1) + O(1) | Binary tree recursion | O(2ⁿ) |
| T(n) = T(n/2) + O(1) | Binary search | O(log n) |
| T(n) = 2T(n/2) + O(n) | Merge sort | O(n log n) |
| T(n) = 2T(n/2) + O(1) | Binary tree height | O(n) |
| T(n) = T(n-1) + T(n-2) | Fibonacci (naive) | O(2ⁿ) |

---

## 1.7 Space Complexity Analysis

### Components of Space Complexity
1. **Fixed Part (Constant Space):**
   - Code space (instructions)
   - Simple variables, constants
   - Fixed-size component space

2. **Variable Part (Depends on Input):**
   - Dynamically allocated memory
   - Recursion stack space
   - Input-dependent data structures

### Total Space = Fixed Part + Variable Part

### Examples

**Example 1: Simple Function**
```cpp
int sum(int a, int b) {
    return a + b;
}
```
* Space: O(1) - only two integers

**Example 2: Array Sum**
```cpp
int arraySum(int arr[], int n) {
    int sum = 0;
    for (int i = 0; i < n; i++) {
        sum += arr[i];
    }
    return sum;
}
```
* Input array: O(n)
* Variables (sum, i): O(1)
* **Total Auxiliary Space:** O(1) (not counting input)

**Example 3: Recursive Factorial**
```cpp
int factorial(int n) {
    if (n == 0) return 1;
    return n * factorial(n-1);
}
```
* Each recursive call takes O(1) space
* Maximum depth: n
* **Stack Space:** O(n)

**Example 4: Merge Sort**
```cpp
void mergeSort(int arr[], int n) {
    // Creates temporary arrays
}
```
* Temporary array: O(n)
* Recursion stack: O(log n)
* **Total Auxiliary Space:** O(n)

---

## 1.8 Amortized Analysis

### Definition
**Amortized Analysis** gives the average performance of each operation in the worst case over a sequence of operations.

### Difference from Average-Case
* **Average-case:** Average over all possible inputs
* **Amortized:** Average over sequence of operations in worst case

### Example: Dynamic Array (Vector)
```
Operations: Insert n elements into initially empty dynamic array

Single insertion:
- If array not full: O(1)
- If array full: O(n) (copy all elements to larger array)

Sequence of n insertions:
- Total cost: n + (1 + 2 + 4 + 8 + ... + n/2) ≈ 3n
- Amortized cost per insertion: 3n/n = O(1)
```

### Three Methods
1. **Aggregate Method:** Total cost / Number of operations
2. **Accounting Method:** Charge each operation, use saved credit for expensive operations
3. **Potential Method:** Use potential function to analyze

---

## 1.9 Practice Problems with Detailed Solutions

### Problem 1: Find the complexity
```cpp
for (int i = 0; i < n; i++) {
    for (int j = i; j < n; j++) {
        cout << i << " " << j << endl;
    }
}
```
**Solution:**
* Outer loop: i from 0 to n-1
* Inner loop: j from i to n-1
* Iterations: n + (n-1) + (n-2) + ... + 1 = n(n+1)/2
* **Complexity:** O(n²)

### Problem 2: Find the complexity
```cpp
for (int i = 1; i < n; i = i * 2) {
    for (int j = 0; j < i; j++) {
        cout << i << " " << j << endl;
    }
}
```
**Solution:**
* Outer loop: i = 1, 2, 4, 8, ..., < n → O(log n) iterations
* When i = 2^k, inner loop runs 2^k times
* Total: 1 + 2 + 4 + 8 + ... + n/2 = n - 1
* **Complexity:** O(n)

### Problem 3: Find the complexity
```cpp
int fibonacci(int n) {
    if (n <= 1) return n;
    return fibonacci(n-1) + fibonacci(n-2);
}
```
**Solution:**
* Recurrence: T(n) = T(n-1) + T(n-2) + O(1)
* This grows like Fibonacci numbers ≈ φⁿ where φ = (1+√5)/2 ≈ 1.618
* **Complexity:** O(2ⁿ) (upper bound), Ω(1.5ⁿ) (lower bound)

---

## 📝 MCQs for Module 1

### Q1. What does Big-O notation represent?
A. Best-case complexity  
B. Average-case complexity  
C. Worst-case upper bound  
D. Exact complexity

> **Answer: C**  
> **Explanation:** Big-O provides an asymptotic upper bound, typically used for worst-case analysis.

### Q2. The complexity of binary search is:
A. O(n)  
B. O(log n)  
C. O(n log n)  
D. O(1)

> **Answer: B**  
> **Explanation:** Binary search halves the search space in each step, leading to O(log n) complexity.

### Q3. For T(n) = 2T(n/2) + O(n), using Master theorem:
A. O(n)  
B. O(log n)  
C. O(n log n)  
D. O(n²)

> **Answer: C**  
> **Explanation:** This is Case 2 of Master theorem where a=2, b=2, and f(n)=O(n). Result is Θ(n log n).

### Q4. Which of the following grows the fastest?
A. O(n²)  
B. O(n log n)  
C. O(2ⁿ)  
D. O(n³)

> **Answer: C**  
> **Explanation:** Exponential growth O(2ⁿ) is faster than polynomial growth O(n³), O(n²), or O(n log n).

### Q5. The space complexity of recursive factorial is:
A. O(1)  
B. O(log n)  
C. O(n)  
D. O(n²)

> **Answer: C**  
> **Explanation:** Each recursive call uses stack space, and maximum recursion depth is n.

---

# 🗂️ MODULE 2: ARRAYS & STRINGS

## 2.1 Arrays - The Foundation

### What is an Array?
* **Definition:** A collection of elements of the same type stored in contiguous memory locations.
* **Key Property:** Random access in O(1) time using index.

### Memory Layout
```
Array: arr[5] = {10, 20, 30, 40, 50}

Memory Address:
[1000] → 10
[1004] → 20   (assuming 4 bytes per integer)
[1008] → 30
[1012] → 40
[1016] → 50

Access arr[3]: address = base_address + (index × size_of_element)
             = 1000 + (3 × 4) = 1012
```

### Characteristics
* **Fixed Size:** Size determined at declaration (for static arrays)
* **Homogeneous:** All elements of same data type
* **Contiguous:** Elements stored in consecutive memory locations
* **Index-based:** Access using zero-based indexing

---

## 2.2 Array Operations and Complexities

| Operation | Description | Time Complexity | Space Complexity |
|-----------|-------------|-----------------|------------------|
| **Access** | arr[i] | O(1) | O(1) |
| **Search (Unsorted)** | Linear scan | O(n) | O(1) |
| **Search (Sorted)** | Binary search | O(log n) | O(1) |
| **Insert at End** | Add element (if space available) | O(1) | O(1) |
| **Insert at Beginning** | Shift all elements right | O(n) | O(1) |
| **Insert at Position i** | Shift elements from i onwards | O(n) | O(1) |
| **Delete at End** | Remove last element | O(1) | O(1) |
| **Delete at Beginning** | Shift all elements left | O(n) | O(1) |
| **Delete at Position i** | Shift elements after i | O(n) | O(1) |

### Why Insert/Delete at Beginning/Middle is O(n)?
```
Original: [10, 20, 30, 40, 50]
Insert 5 at beginning:

Step 1: Shift all elements right
[10, 10, 20, 30, 40, 50]  // Copy 10
[10, 10, 20, 20, 30, 40, 50]  // Copy 20
... (n shifts)

Step 2: Insert at index 0
[5, 10, 20, 30, 40, 50]

Total operations: n shifts + 1 insert = O(n)
```

---

## 2.3 Types of Arrays

### 1. One-Dimensional Array
```cpp
int arr[5] = {1, 2, 3, 4, 5};
```

### 2. Multi-Dimensional Array (2D Array)
```cpp
int matrix[3][4] = {
    {1,  2,  3,  4},
    {5,  6,  7,  8},
    {9, 10, 11, 12}
};
```

#### Memory Storage of 2D Arrays

**Row-Major Order (C, C++, Python):**
```
matrix[3][4] stored as:
[1][2][3][4][5][6][7][8][9][10][11][12]
 Row 0      Row 1      Row 2
```

**Address Calculation (Row-Major):**
```
Address of matrix[i][j] = Base + [(i × n_cols + j) × size]
where n_cols = number of columns
```

**Column-Major Order (Fortran, MATLAB):**
```
matrix[3][4] stored as:
[1][5][9][2][6][10][3][7][11][4][8][12]
 Col 0    Col 1     Col 2     Col 3
```

### 3. Dynamic Arrays (Vectors/ArrayLists)

**Problem with Static Arrays:** Fixed size determined at compile time.

**Solution:** Dynamic Arrays
* **Resize when needed:** When full, allocate larger array and copy elements.
* **Typical Strategy:** Double the capacity.
* **Amortized O(1) insertion:** Although occasional resize is O(n), amortized cost is O(1).

**Example: Vector in C++**
```cpp
vector<int> v;
v.push_back(10);  // Amortized O(1)
v.push_back(20);
v.push_back(30);
```

**Resizing Process:**
```
Initial capacity: 1
After 1 insert: [10]

After 2 inserts: Capacity doubled to 2
[10, 20]

After 3 inserts: Capacity doubled to 4
[10, 20, 30, _]

After 5 inserts: Capacity doubled to 8
[10, 20, 30, 40, 50, _, _, _]
```

**Cost Analysis:**
* Insertions: 1, 1, 2, 1, 4, 1, 1, 1, 8, ...
* Total for n insertions: n + (1 + 2 + 4 + 8 + ... + n/2) < 3n
* **Amortized cost per insertion:** O(1)

---

## 2.4 Common Array Algorithms

### 1. Reversal
```cpp
void reverse(int arr[], int n) {
    int left = 0, right = n-1;
    while (left < right) {
        swap(arr[left], arr[right]);
        left++;
        right--;
    }
}
```
* **Time:** O(n)
* **Space:** O(1)

### 2. Rotation (Left Rotate by d positions)
```cpp
// Method 1: Using Reversal (Space-efficient)
void leftRotate(int arr[], int n, int d) {
    reverse(arr, 0, d-1);        // Reverse first d elements
    reverse(arr, d, n-1);        // Reverse remaining elements
    reverse(arr, 0, n-1);        // Reverse entire array
}
```
* **Time:** O(n)
* **Space:** O(1)

**Example:**
```
arr = [1, 2, 3, 4, 5, 6, 7], d = 2

Step 1: Reverse first 2 elements
[2, 1, 3, 4, 5, 6, 7]

Step 2: Reverse remaining elements
[2, 1, 7, 6, 5, 4, 3]

Step 3: Reverse entire array
[3, 4, 5, 6, 7, 1, 2]
```

### 3. Kadane's Algorithm (Maximum Subarray Sum)
```cpp
int maxSubarraySum(int arr[], int n) {
    int maxSoFar = arr[0];
    int maxEndingHere = arr[0];
    
    for (int i = 1; i < n; i++) {
        maxEndingHere = max(arr[i], maxEndingHere + arr[i]);
        maxSoFar = max(maxSoFar, maxEndingHere);
    }
    
    return maxSoFar;
}
```
* **Time:** O(n)
* **Space:** O(1)

**Example:**
```
arr = [-2, 1, -3, 4, -1, 2, 1, -5, 4]

Iteration by iteration:
i=1: maxEndingHere = max(1, -2+1) = 1, maxSoFar = 1
i=2: maxEndingHere = max(-3, 1-3) = -2, maxSoFar = 1
i=3: maxEndingHere = max(4, -2+4) = 4, maxSoFar = 4
i=4: maxEndingHere = max(-1, 4-1) = 3, maxSoFar = 4
i=5: maxEndingHere = max(2, 3+2) = 5, maxSoFar = 5
i=6: maxEndingHere = max(1, 5+1) = 6, maxSoFar = 6
...

Maximum subarray sum = 6 (subarray [4, -1, 2, 1])
```

### 4. Two Pointer Technique
```cpp
// Find pair with sum = target in sorted array
bool findPair(int arr[], int n, int target) {
    int left = 0, right = n-1;
    
    while (left < right) {
        int sum = arr[left] + arr[right];
        if (sum == target) return true;
        else if (sum < target) left++;
        else right--;
    }
    
    return false;
}
```
* **Time:** O(n)
* **Space:** O(1)

### 5. Sliding Window Technique
```cpp
// Maximum sum of k consecutive elements
int maxSumSubarray(int arr[], int n, int k) {
    int maxSum = 0, windowSum = 0;
    
    // Calculate sum of first window
    for (int i = 0; i < k; i++) {
        windowSum += arr[i];
    }
    maxSum = windowSum;
    
    // Slide window
    for (int i = k; i < n; i++) {
        windowSum = windowSum - arr[i-k] + arr[i];
        maxSum = max(maxSum, windowSum);
    }
    
    return maxSum;
}
```
* **Time:** O(n)
* **Space:** O(1)

---

## 2.5 Strings

### String Basics
* **Definition:** Array of characters terminated by '\0' (in C/C++).
* **Immutable in some languages:** Java, Python (new string object created on modification).
* **Mutable in others:** C, C++ (can modify in-place).

### String Operations Complexity

| Operation | Description | Time Complexity |
|-----------|-------------|-----------------|
| **Access** | s[i] | O(1) |
| **Length** | strlen(s) | O(n) in C, O(1) in many languages |
| **Concatenation** | s1 + s2 | O(n+m) |
| **Substring** | s.substr(i, len) | O(len) |
| **Search** | Find substring | O(n×m) naive, O(n+m) KMP |
| **Comparison** | s1 == s2 | O(min(len(s1), len(s2))) |

### Common String Algorithms

#### 1. Palindrome Check
```cpp
bool isPalindrome(string s) {
    int left = 0, right = s.length() - 1;
    
    while (left < right) {
        if (s[left] != s[right]) return false;
        left++;
        right--;
    }
    
    return true;
}
```
* **Time:** O(n)
* **Space:** O(1)

#### 2. Anagram Check
```cpp
bool areAnagrams(string s1, string s2) {
    if (s1.length() != s2.length()) return false;
    
    int count[256] = {0};
    
    for (int i = 0; i < s1.length(); i++) {
        count[s1[i]]++;
        count[s2[i]]--;
    }
    
    for (int i = 0; i < 256; i++) {
        if (count[i] != 0) return false;
    }
    
    return true;
}
```
* **Time:** O(n)
* **Space:** O(1) - fixed size array

#### 3. String Reversal
```cpp
void reverseString(string &s) {
    int left = 0, right = s.length() - 1;
    
    while (left < right) {
        swap(s[left], s[right]);
        left++;
        right--;
    }
}
```
* **Time:** O(n)
* **Space:** O(1)

---

## 📝 MCQs for Module 2

### Q1. What is the time complexity of accessing an element in an array by index?
A. O(n)  
B. O(log n)  
C. O(1)  
D. O(n²)

> **Answer: C**  
> **Explanation:** Arrays provide direct access to elements using index calculation: base_address + (index × size).

### Q2. The address of matrix[i][j] in row-major order (with base address B, and n columns) is:
A. B + i × j  
B. B + (i + j)  
C. B + (i × n + j) × size  
D. B + j × n + i

> **Answer: C**  
> **Explanation:** In row-major order, we skip i complete rows (each with n elements) and then j elements.

### Q3. The amortized time complexity of push_back() operation in dynamic array (vector) is:
A. O(1)  
B. O(log n)  
C. O(n)  
D. O(n log n)

> **Answer: A**  
> **Explanation:** Although occasional resizing takes O(n), the amortized cost over n operations is O(1).

### Q4. Kadane's algorithm is used for:
A. Sorting an array  
B. Finding maximum subarray sum  
C. Searching in array  
D. Reversing an array

> **Answer: B**  
> **Explanation:** Kadane's algorithm finds the maximum sum of contiguous subarray in O(n) time.

### Q5. The time complexity of checking if two strings are anagrams is:
A. O(n log n)  
B. O(n²)  
C. O(n)  
D. O(1)

> **Answer: C**  
> **Explanation:** Using a frequency array, we can count characters in O(n) time.

---

# 🔗 MODULE 3: LINKED LISTS (ALL VARIANTS)

## 3.1 Linked List Basics

### What is a Linked List?
* **Definition:** A linear data structure where elements (nodes) are stored in non-contiguous memory locations.
* **Each Node Contains:**
  1. Data field
  2. Pointer(s) to next/previous node(s)

### Why Linked Lists?

**Advantages over Arrays:**
* Dynamic size (grow/shrink at runtime)
* Efficient insertion/deletion (no shifting required)
* No wasted memory (allocate only what you need)

**Disadvantages:**
* No random access (must traverse from head)
* Extra memory for pointers
* Cache-unfriendly (non-contiguous memory)
* More complex to implement

---

## 3.2 Types of Linked Lists

### 1. Singly Linked List

**Structure:**
```cpp
struct Node {
    int data;
    Node* next;
};
```

**Visual Representation:**
```
HEAD → [10|●] → [20|●] → [30|●] → [40|NULL]
```

**Operations Complexity:**

| Operation | Time | Space |
|-----------|------|-------|
| Insert at beginning | O(1) | O(1) |
| Insert at end | O(n) without tail, O(1) with tail | O(1) |
| Insert at position | O(n) | O(1) |
| Delete from beginning | O(1) | O(1) |
| Delete from end | O(n) | O(1) |
| Delete specific node | O(n) | O(1) |
| Search | O(n) | O(1) |
| Traverse | O(n) | O(1) |

**Basic Operations:**

```cpp
// Insert at beginning
void insertAtBeginning(Node** head, int data) {
    Node* newNode = new Node();
    newNode->data = data;
    newNode->next = *head;
    *head = newNode;
}

// Insert at end
void insertAtEnd(Node** head, int data) {
    Node* newNode = new Node();
    newNode->data = data;
    newNode->next = NULL;
    
    if (*head == NULL) {
        *head = newNode;
        return;
    }
    
    Node* temp = *head;
    while (temp->next != NULL) {
        temp = temp->next;
    }
    temp->next = newNode;
}

// Delete node with given key
void deleteNode(Node** head, int key) {
    Node* temp = *head;
    Node* prev = NULL;
    
    // If head node holds the key
    if (temp != NULL && temp->data == key) {
        *head = temp->next;
        delete temp;
        return;
    }
    
    // Search for the key
    while (temp != NULL && temp->data != key) {
        prev = temp;
        temp = temp->next;
    }
    
    // Key not found
    if (temp == NULL) return;
    
    // Unlink the node
    prev->next = temp->next;
    delete temp;
}

// Search for a key
bool search(Node* head, int key) {
    Node* temp = head;
    while (temp != NULL) {
        if (temp->data == key) return true;
        temp = temp->next;
    }
    return false;
}
```

---

### 2. Doubly Linked List

**Structure:**
```cpp
struct Node {
    int data;
    Node* prev;
    Node* next;
};
```

**Visual Representation:**
```
NULL ← [10] ↔ [20] ↔ [30] ↔ [40] → NULL
       ↑
      HEAD
```

**Advantages over Singly Linked List:**
* Can traverse in both directions
* Delete a node in O(1) if node pointer is given
* Can insert before a given node efficiently

**Disadvantages:**
* Extra memory for prev pointer
* More complex implementation

**Basic Operations:**

```cpp
// Insert at beginning
void insertAtBeginning(Node** head, int data) {
    Node* newNode = new Node();
    newNode->data = data;
    newNode->next = *head;
    newNode->prev = NULL;
    
    if (*head != NULL) {
        (*head)->prev = newNode;
    }
    
    *head = newNode;
}

// Delete a node (given pointer to node)
void deleteNode(Node** head, Node* del) {
    if (*head == NULL || del == NULL) return;
    
    // If node to be deleted is head
    if (*head == del) {
        *head = del->next;
    }
    
    // Change next only if not last node
    if (del->next != NULL) {
        del->next->prev = del->prev;
    }
    
    // Change prev only if not first node
    if (del->prev != NULL) {
        del->prev->next = del->next;
    }
    
    delete del;
}

// Reverse a doubly linked list
void reverse(Node** head) {
    Node* temp = NULL;
    Node* current = *head;
    
    while (current != NULL) {
        // Swap next and prev for current node
        temp = current->prev;
        current->prev = current->next;
        current->next = temp;
        current = current->prev;
    }
    
    // Change head
    if (temp != NULL) {
        *head = temp->prev;
    }
}
```

---

### 3. Circular Linked List

**Structure:** Last node points back to the first node (or head).

**Singly Circular:**
```
      ┌──────────────────┐
      ↓                  |
HEAD → [10] → [20] → [30] → [40] ─┘
```

**Doubly Circular:**
```
      ┌──────────────────────────┐
      ↓                          |
     [10] ↔ [20] ↔ [30] ↔ [40] ──┘
      ↑                    ↓
      └────────────────────┘
```

**Applications:**
* Round-robin scheduling
* Circular buffers
* Undo functionality in applications
* Music/video playlist

**Basic Operations:**

```cpp
// Insert at beginning of circular linked list
void insertAtBeginning(Node** head, int data) {
    Node* newNode = new Node();
    newNode->data = data;
    
    if (*head == NULL) {
        newNode->next = newNode;  // Points to itself
        *head = newNode;
        return;
    }
    
    Node* temp = *head;
    while (temp->next != *head) {
        temp = temp->next;
    }
    
    temp->next = newNode;
    newNode->next = *head;
    *head = newNode;
}

// Delete a node from circular linked list
void deleteNode(Node** head, int key) {
    if (*head == NULL) return;
    
    Node* curr = *head;
    Node* prev = NULL;
    
    // If head is to be deleted
    if (curr->data == key) {
        // Find last node
        while (curr->next != *head) {
            curr = curr->next;
        }
        
        // If only one node
        if (curr == *head) {
            delete *head;
            *head = NULL;
            return;
        }
        
        curr->next = (*head)->next;
        delete *head;
        *head = curr->next;
        return;
    }
    
    // Search for node to delete
    do {
        prev = curr;
        curr = curr->next;
    } while (curr != *head && curr->data != key);
    
    if (curr->data == key) {
        prev->next = curr->next;
        delete curr;
    }
}
```

---

## 3.3 Common Linked List Problems

### 1. Reverse a Linked List

**Iterative Approach:**
```cpp
Node* reverse(Node* head) {
    Node* prev = NULL;
    Node* current = head;
    Node* next = NULL;
    
    while (current != NULL) {
        next = current->next;  // Store next
        current->next = prev;  // Reverse link
        prev = current;        // Move prev forward
        current = next;        // Move current forward
    }
    
    return prev;  // New head
}
```
* **Time:** O(n)
* **Space:** O(1)

**Recursive Approach:**
```cpp
Node* reverse(Node* head) {
    if (head == NULL || head->next == NULL) {
        return head;
    }
    
    Node* rest = reverse(head->next);
    head->next->next = head;
    head->next = NULL;
    
    return rest;
}
```
* **Time:** O(n)
* **Space:** O(n) - recursion stack

---

### 2. Detect Cycle (Floyd's Cycle Detection Algorithm)

**Problem:** Determine if a linked list has a cycle.

**Floyd's Tortoise and Hare Algorithm:**
```cpp
bool hasCycle(Node* head) {
    if (head == NULL) return false;
    
    Node* slow = head;
    Node* fast = head;
    
    while (fast != NULL && fast->next != NULL) {
        slow = slow->next;          // Move 1 step
        fast = fast->next->next;    // Move 2 steps
        
        if (slow == fast) return true;  // Cycle detected
    }
    
    return false;  // No cycle
}
```
* **Time:** O(n)
* **Space:** O(1)

**Why it works:**
* If there's a cycle, fast pointer will eventually catch up with slow pointer.
* In a cycle of length L, they meet in at most L iterations after both enter the cycle.

**Finding Cycle Start:**
```cpp
Node* detectCycleStart(Node* head) {
    Node* slow = head;
    Node* fast = head;
    
    // Detect cycle
    while (fast != NULL && fast->next != NULL) {
        slow = slow->next;
        fast = fast->next->next;
        
        if (slow == fast) break;
    }
    
    if (fast == NULL || fast->next == NULL) return NULL;  // No cycle
    
    // Find start of cycle
    slow = head;
    while (slow != fast) {
        slow = slow->next;
        fast = fast->next;
    }
    
    return slow;  // Start of cycle
}
```

---

### 3. Find Middle Element

**Method 1: Two Pointers (Slow and Fast)**
```cpp
Node* findMiddle(Node* head) {
    if (head == NULL) return NULL;
    
    Node* slow = head;
    Node* fast = head;
    
    while (fast != NULL && fast->next != NULL) {
        slow = slow->next;
        fast = fast->next->next;
    }
    
    return slow;  // Middle node
}
```
* **Time:** O(n)
* **Space:** O(1)

**Note:** If even number of nodes, this returns the second middle node.

---

### 4. Remove N-th Node from End

**Method: Two Pointers with Gap**
```cpp
Node* removeNthFromEnd(Node* head, int n) {
    Node* dummy = new Node();
    dummy->next = head;
    
    Node* first = dummy;
    Node* second = dummy;
    
    // Move first n+1 steps ahead
    for (int i = 0; i <= n; i++) {
        first = first->next;
    }
    
    // Move both pointers
    while (first != NULL) {
        first = first->next;
        second = second->next;
    }
    
    // Remove n-th node from end
    Node* temp = second->next;
    second->next = second->next->next;
    delete temp;
    
    Node* newHead = dummy->next;
    delete dummy;
    return newHead;
}
```
* **Time:** O(n)
* **Space:** O(1)

---

### 5. Merge Two Sorted Linked Lists

```cpp
Node* mergeSortedLists(Node* l1, Node* l2) {
    Node* dummy = new Node();
    Node* tail = dummy;
    
    while (l1 != NULL && l2 != NULL) {
        if (l1->data <= l2->data) {
            tail->next = l1;
            l1 = l1->next;
        } else {
            tail->next = l2;
            l2 = l2->next;
        }
        tail = tail->next;
    }
    
    // Attach remaining nodes
    tail->next = (l1 != NULL) ? l1 : l2;
    
    Node* mergedHead = dummy->next;
    delete dummy;
    return mergedHead;
}
```
* **Time:** O(m + n)
* **Space:** O(1)

---

### 6. Check if Linked List is Palindrome

**Method: Reverse Second Half**
```cpp
bool isPalindrome(Node* head) {
    if (head == NULL || head->next == NULL) return true;
    
    // Find middle
    Node* slow = head;
    Node* fast = head;
    while (fast != NULL && fast->next != NULL) {
        slow = slow->next;
        fast = fast->next->next;
    }
    
    // Reverse second half
    Node* secondHalf = reverse(slow);
    
    // Compare first and second half
    Node* firstHalf = head;
    while (secondHalf != NULL) {
        if (firstHalf->data != secondHalf->data) return false;
        firstHalf = firstHalf->next;
        secondHalf = secondHalf->next;
    }
    
    return true;
}
```
* **Time:** O(n)
* **Space:** O(1)

---

### 7. Intersection Point of Two Linked Lists

**Method: Length Difference**
```cpp
Node* getIntersectionNode(Node* headA, Node* headB) {
    int lenA = getLength(headA);
    int lenB = getLength(headB);
    
    // Advance the longer list by difference
    while (lenA > lenB) {
        headA = headA->next;
        lenA--;
    }
    while (lenB > lenA) {
        headB = headB->next;
        lenB--;
    }
    
    // Move both pointers until they meet
    while (headA != headB) {
        headA = headA->next;
        headB = headB->next;
    }
    
    return headA;  // Intersection point or NULL
}

int getLength(Node* head) {
    int length = 0;
    while (head != NULL) {
        length++;
        head = head->next;
    }
    return length;
}
```
* **Time:** O(m + n)
* **Space:** O(1)

---

## 3.4 Comparison: Array vs. Linked List

| Feature | Array | Linked List |
|---------|-------|-------------|
| **Memory** | Contiguous | Non-contiguous |
| **Size** | Fixed (static) | Dynamic |
| **Access Time** | O(1) | O(n) |
| **Insert at Beginning** | O(n) | O(1) |
| **Insert at End** | O(1) amortized | O(n) or O(1) with tail |
| **Delete at Beginning** | O(n) | O(1) |
| **Memory Overhead** | None | Pointer(s) per node |
| **Cache Performance** | Good (locality) | Poor (scattered) |
| **Random Access** | Yes | No |

---

## 📝 MCQs for Module 3

### Q1. The time complexity of inserting a node at the beginning of a singly linked list is:
A. O(n)  
B. O(log n)  
C. O(1)  
D. O(n log n)

> **Answer: C**  
> **Explanation:** Insertion at beginning requires only updating the new node's next pointer and the head pointer, which is O(1).

### Q2. Floyd's cycle detection algorithm uses:
A. One pointer  
B. Two pointers moving at different speeds  
C. Three pointers  
D. Stack

> **Answer: B**  
> **Explanation:** Floyd's algorithm uses two pointers - slow (moves 1 step) and fast (moves 2 steps). If there's a cycle, they eventually meet.

### Q3. In a doubly linked list, deleting a node (given pointer to the node) takes:
A. O(n)  
B. O(log n)  
C. O(1)  
D. O(n²)

> **Answer: C**  
> **Explanation:** With node pointer, we can directly access prev and next pointers to unlink the node in O(1) time.

### Q4. The space complexity of reversing a linked list iteratively is:
A. O(n)  
B. O(log n)  
C. O(1)  
D. O(n²)

> **Answer: C**  
> **Explanation:** Iterative reversal only uses a fixed number of pointers (prev, current, next), hence O(1) space.

### Q5. Circular linked lists are commonly used in:
A. Stack implementation  
B. Binary search  
C. Round-robin scheduling  
D. Sorting

> **Answer: C**  
> **Explanation:** Circular linked lists are perfect for round-robin scheduling where we need to cycle through items repeatedly.

---


# 📚 MODULE 4: STACK & QUEUE (LINEAR DATA STRUCTURES)

## 4.1 Stack - LIFO Data Structure

### Definition
* **Stack:** A linear data structure that follows the **Last-In-First-Out (LIFO)** principle.
* **Real-world Analogy:** Stack of plates, stack of books.

### Basic Operations

| Operation | Description | Time Complexity |
|-----------|-------------|-----------------|
| **push(x)** | Insert element x at top | O(1) |
| **pop()** | Remove and return top element | O(1) |
| **peek() / top()** | Return top element without removing | O(1) |
| **isEmpty()** | Check if stack is empty | O(1) |
| **size()** | Return number of elements | O(1) |

---

### Implementation Methods

#### 1. Array-based Stack
```cpp
class Stack {
private:
    int* arr;
    int top;
    int capacity;
    
public:
    Stack(int size) {
        arr = new int[size];
        capacity = size;
        top = -1;
    }
    
    void push(int x) {
        if (top == capacity - 1) {
            cout << "Stack Overflow" << endl;
            return;
        }
        arr[++top] = x;
    }
    
    int pop() {
        if (top == -1) {
            cout << "Stack Underflow" << endl;
            return -1;
        }
        return arr[top--];
    }
    
    int peek() {
        if (top == -1) {
            cout << "Stack is empty" << endl;
            return -1;
        }
        return arr[top];
    }
    
    bool isEmpty() {
        return top == -1;
    }
};
```

**Pros:** Fast access, cache-friendly  
**Cons:** Fixed size, potential overflow

#### 2. Linked List-based Stack
```cpp
class Stack {
private:
    struct Node {
        int data;
        Node* next;
    };
    Node* top;
    
public:
    Stack() {
        top = NULL;
    }
    
    void push(int x) {
        Node* newNode = new Node();
        newNode->data = x;
        newNode->next = top;
        top = newNode;
    }
    
    int pop() {
        if (top == NULL) {
            cout << "Stack Underflow" << endl;
            return -1;
        }
        int value = top->data;
        Node* temp = top;
        top = top->next;
        delete temp;
        return value;
    }
    
    int peek() {
        if (top == NULL) {
            cout << "Stack is empty" << endl;
            return -1;
        }
        return top->data;
    }
    
    bool isEmpty() {
        return top == NULL;
    }
};
```

**Pros:** Dynamic size, no overflow  
**Cons:** Extra memory for pointers

---

### Applications of Stack

#### 1. Function Call Management (Call Stack)
* When a function is called, its activation record is pushed onto the call stack.
* When function returns, its record is popped.
* Recursion uses this mechanism.

#### 2. Expression Evaluation

**Infix to Postfix Conversion:**
```
Infix: A + B * C
Postfix: A B C * +

Infix: (A + B) * C
Postfix: A B + C *
```

**Algorithm:**
```cpp
string infixToPostfix(string infix) {
    stack<char> s;
    string postfix = "";
    
    for (char c : infix) {
        // If operand, add to output
        if (isalnum(c)) {
            postfix += c;
        }
        // If '(', push to stack
        else if (c == '(') {
            s.push(c);
        }
        // If ')', pop until '('
        else if (c == ')') {
            while (!s.empty() && s.top() != '(') {
                postfix += s.top();
                s.pop();
            }
            s.pop();  // Remove '('
        }
        // If operator
        else {
            while (!s.empty() && precedence(s.top()) >= precedence(c)) {
                postfix += s.top();
                s.pop();
            }
            s.push(c);
        }
    }
    
    // Pop remaining operators
    while (!s.empty()) {
        postfix += s.top();
        s.pop();
    }
    
    return postfix;
}

int precedence(char op) {
    if (op == '^') return 3;
    if (op == '*' || op == '/') return 2;
    if (op == '+' || op == '-') return 1;
    return 0;
}
```

**Postfix Evaluation:**
```cpp
int evaluatePostfix(string postfix) {
    stack<int> s;
    
    for (char c : postfix) {
        // If operand, push to stack
        if (isdigit(c)) {
            s.push(c - '0');
        }
        // If operator, pop two operands and apply operator
        else {
            int op2 = s.top(); s.pop();
            int op1 = s.top(); s.pop();
            
            switch(c) {
                case '+': s.push(op1 + op2); break;
                case '-': s.push(op1 - op2); break;
                case '*': s.push(op1 * op2); break;
                case '/': s.push(op1 / op2); break;
            }
        }
    }
    
    return s.top();
}
```

#### 3. Parentheses Matching
```cpp
bool isBalanced(string expr) {
    stack<char> s;
    
    for (char c : expr) {
        if (c == '(' || c == '[' || c == '{') {
            s.push(c);
        }
        else if (c == ')' || c == ']' || c == '}') {
            if (s.empty()) return false;
            
            char top = s.top();
            if ((c == ')' && top == '(') ||
                (c == ']' && top == '[') ||
                (c == '}' && top == '{')) {
                s.pop();
            } else {
                return false;
            }
        }
    }
    
    return s.empty();
}
```

#### 4. Backtracking
* DFS (Depth-First Search)
* Undo operations in editors
* Browser history (back button)

#### 5. Stock Span Problem
```cpp
// Find number of consecutive days before current day
// where stock price was less than or equal to current price
vector<int> calculateSpan(vector<int>& prices) {
    int n = prices.size();
    vector<int> span(n);
    stack<int> s;  // Store indices
    
    for (int i = 0; i < n; i++) {
        // Pop elements while stack is not empty and
        // top of stack is smaller than or equal to prices[i]
        while (!s.empty() && prices[s.top()] <= prices[i]) {
            s.pop();
        }
        
        // If stack is empty, span is i+1
        // Otherwise, span is i - index of top element
        span[i] = s.empty() ? (i + 1) : (i - s.top());
        
        s.push(i);
    }
    
    return span;
}
```
* **Time:** O(n)
* **Space:** O(n)

---

## 4.2 Queue - FIFO Data Structure

### Definition
* **Queue:** A linear data structure that follows the **First-In-First-Out (FIFO)** principle.
* **Real-world Analogy:** Line at ticket counter, printer queue.

### Basic Operations

| Operation | Description | Time Complexity |
|-----------|-------------|-----------------|
| **enqueue(x)** | Insert element x at rear | O(1) |
| **dequeue()** | Remove and return front element | O(1) |
| **front()** | Return front element without removing | O(1) |
| **rear()** | Return rear element without removing | O(1) |
| **isEmpty()** | Check if queue is empty | O(1) |
| **size()** | Return number of elements | O(1) |

---

### Types of Queues

#### 1. Simple Queue (Linear Queue)

**Array-based Implementation:**
```cpp
class Queue {
private:
    int* arr;
    int front, rear, capacity, count;
    
public:
    Queue(int size) {
        arr = new int[size];
        capacity = size;
        front = 0;
        rear = -1;
        count = 0;
    }
    
    void enqueue(int x) {
        if (count == capacity) {
            cout << "Queue Overflow" << endl;
            return;
        }
        rear = (rear + 1) % capacity;
        arr[rear] = x;
        count++;
    }
    
    int dequeue() {
        if (count == 0) {
            cout << "Queue Underflow" << endl;
            return -1;
        }
        int value = arr[front];
        front = (front + 1) % capacity;
        count--;
        return value;
    }
    
    int getFront() {
        if (count == 0) {
            cout << "Queue is empty" << endl;
            return -1;
        }
        return arr[front];
    }
    
    bool isEmpty() {
        return count == 0;
    }
};
```

#### 2. Circular Queue

**Why Circular Queue?**
* In linear queue implementation, when rear reaches end, we cannot add more elements even if there's space at the beginning.
* Circular queue solves this by wrapping around using modulo operation.

**Visualization:**
```
Initial: [_, _, _, _]  front=0, rear=-1

After enqueue(10): [10, _, _, _]  front=0, rear=0
After enqueue(20): [10, 20, _, _]  front=0, rear=1
After enqueue(30): [10, 20, 30, _]  front=0, rear=2
After dequeue(): [_, 20, 30, _]  front=1, rear=2
After enqueue(40): [_, 20, 30, 40]  front=1, rear=3
After enqueue(50): [50, 20, 30, 40]  front=1, rear=0 (wrapped around)
```

**Key Operations:**
* `rear = (rear + 1) % capacity` - wrap around at end
* `front = (front + 1) % capacity` - wrap around at end

#### 3. Deque (Double-Ended Queue)

**Definition:** Queue where insertion and deletion can happen at both ends.

```cpp
class Deque {
private:
    int* arr;
    int front, rear, size, capacity;
    
public:
    Deque(int cap) {
        capacity = cap;
        arr = new int[capacity];
        front = -1;
        rear = 0;
        size = 0;
    }
    
    void insertFront(int x) {
        if (size == capacity) {
            cout << "Overflow" << endl;
            return;
        }
        if (front == -1) {
            front = 0;
            rear = 0;
        } else {
            front = (front - 1 + capacity) % capacity;
        }
        arr[front] = x;
        size++;
    }
    
    void insertRear(int x) {
        if (size == capacity) {
            cout << "Overflow" << endl;
            return;
        }
        if (front == -1) {
            front = 0;
            rear = 0;
        } else {
            rear = (rear + 1) % capacity;
        }
        arr[rear] = x;
        size++;
    }
    
    int deleteFront() {
        if (size == 0) {
            cout << "Underflow" << endl;
            return -1;
        }
        int value = arr[front];
        if (size == 1) {
            front = -1;
            rear = -1;
        } else {
            front = (front + 1) % capacity;
        }
        size--;
        return value;
    }
    
    int deleteRear() {
        if (size == 0) {
            cout << "Underflow" << endl;
            return -1;
        }
        int value = arr[rear];
        if (size == 1) {
            front = -1;
            rear = -1;
        } else {
            rear = (rear - 1 + capacity) % capacity;
        }
        size--;
        return value;
    }
};
```

**Applications:**
* Storing history for undo/redo operations
* Sliding window problems
* A-Steal job scheduling algorithm

#### 4. Priority Queue

**Definition:** Queue where each element has a priority, and element with highest priority is dequeued first.

**Common Implementations:**
1. **Unsorted Array:** Enqueue O(1), Dequeue O(n)
2. **Sorted Array:** Enqueue O(n), Dequeue O(1)
3. **Heap:** Enqueue O(log n), Dequeue O(log n) ✓ **Best**

*(Detailed coverage in Module 7: Heaps)*

---

### Applications of Queue

#### 1. CPU Scheduling
* Process scheduling in operating systems
* Round-robin scheduling

#### 2. BFS (Breadth-First Search)
```cpp
void BFS(Graph g, int start) {
    bool visited[MAX];
    memset(visited, false, sizeof(visited));
    
    queue<int> q;
    visited[start] = true;
    q.push(start);
    
    while (!q.empty()) {
        int vertex = q.front();
        q.pop();
        cout << vertex << " ";
        
        for (int adjacent : g.adj[vertex]) {
            if (!visited[adjacent]) {
                visited[adjacent] = true;
                q.push(adjacent);
            }
        }
    }
}
```

#### 3. Printer Queue
* Jobs are processed in FIFO order

#### 4. Handling Requests
* Web server request handling
* Handling requests in call centers

#### 5. Generate Binary Numbers
```cpp
// Generate binary numbers from 1 to n
void generateBinaryNumbers(int n) {
    queue<string> q;
    q.push("1");
    
    for (int i = 0; i < n; i++) {
        string s = q.front();
        q.pop();
        cout << s << endl;
        
        q.push(s + "0");
        q.push(s + "1");
    }
}
```
**Output for n=5:** 1, 10, 11, 100, 101

---

## 📝 MCQs for Module 4

### Q1. Stack follows which principle?
A. FIFO  
B. LIFO  
C. Priority-based  
D. Random access

> **Answer: B**  
> **Explanation:** Stack is Last-In-First-Out - the last element inserted is the first to be removed.

### Q2. The time complexity of push and pop operations in a stack is:
A. O(n)  
B. O(log n)  
C. O(1)  
D. O(n log n)

> **Answer: C**  
> **Explanation:** Both push and pop operations work at the top of the stack and take constant time.

### Q3. Infix expression A + B * C in postfix notation is:
A. ABC*+  
B. AB+C*  
C. A+BC*  
D. ABC+*

> **Answer: A**  
> **Explanation:** Following operator precedence, * has higher precedence than +, so: A B C * +

### Q4. Queue follows which principle?
A. LIFO  
B. FIFO  
C. Priority-based  
D. None of these

> **Answer: B**  
> **Explanation:** Queue is First-In-First-Out - the first element inserted is the first to be removed.

### Q5. Circular queue is used to overcome the limitation of:
A. Linked list  
B. Stack  
C. Linear queue  
D. Binary tree

> **Answer: C**  
> **Explanation:** Circular queue solves the problem of wasted space in linear queue by wrapping around.

### Q6. Which data structure is used in BFS traversal?
A. Stack  
B. Queue  
C. Heap  
D. Hash table

> **Answer: B**  
> **Explanation:** BFS uses a queue to explore nodes level by level.

---

# 🌳 MODULE 5: RECURSION & BACKTRACKING

## 5.1 Recursion Fundamentals

### Definition
**Recursion:** A function that calls itself with a smaller/simpler input until a base condition is reached.

### Components of Recursion
1. **Base Case:** Condition that stops recursion
2. **Recursive Case:** Function calls itself with modified parameters
3. **Progress Toward Base Case:** Each recursive call must move toward the base case

### How Recursion Works Internally
* **Call Stack:** Each function call is pushed onto the call stack
* **Stack Frame:** Contains local variables, parameters, return address
* **Unwinding:** When base case is reached, stack frames are popped

---

### Simple Example: Factorial
```cpp
int factorial(int n) {
    // Base case
    if (n == 0 || n == 1) {
        return 1;
    }
    
    // Recursive case
    return n * factorial(n - 1);
}
```

**Execution Trace for factorial(4):**
```
factorial(4)
  = 4 * factorial(3)
  = 4 * (3 * factorial(2))
  = 4 * (3 * (2 * factorial(1)))
  = 4 * (3 * (2 * 1))
  = 4 * (3 * 2)
  = 4 * 6
  = 24
```

**Call Stack Visualization:**
```
factorial(4) calls factorial(3)
factorial(3) calls factorial(2)
factorial(2) calls factorial(1)
factorial(1) returns 1
factorial(2) returns 2
factorial(3) returns 6
factorial(4) returns 24
```

---

### Types of Recursion

#### 1. Linear Recursion
**Definition:** Function calls itself at most once.

**Example:** Factorial, Sum of n numbers
```cpp
int sum(int n) {
    if (n == 0) return 0;
    return n + sum(n - 1);
}
```
* **Time:** O(n)
* **Space:** O(n) - call stack

#### 2. Binary Recursion (Tree Recursion)
**Definition:** Function calls itself twice.

**Example:** Fibonacci
```cpp
int fibonacci(int n) {
    if (n <= 1) return n;
    return fibonacci(n - 1) + fibonacci(n - 2);
}
```
* **Time:** O(2ⁿ) - exponential
* **Space:** O(n) - maximum depth of recursion tree

**Recursion Tree for fibonacci(5):**
```
                     fib(5)
                    /      \
               fib(4)        fib(3)
              /     \        /     \
         fib(3)   fib(2)  fib(2) fib(1)
         /   \     /   \   /   \
    fib(2) fib(1) f(1) f(0) f(1) f(0)
    /   \
  f(1) f(0)
```

**Problem:** Many repeated calculations (fib(2), fib(3) computed multiple times)

**Solution:** Dynamic Programming (memoization)

#### 3. Tail Recursion
**Definition:** Recursive call is the last operation in the function.

**Example:**
```cpp
// Non-tail recursive
int factorial(int n) {
    if (n == 1) return 1;
    return n * factorial(n - 1);  // Multiplication after recursive call
}

// Tail recursive
int factorialTail(int n, int acc = 1) {
    if (n == 1) return acc;
    return factorialTail(n - 1, n * acc);  // Recursive call is last operation
}
```

**Advantage:** Tail recursion can be optimized by compiler to iterative form (tail call optimization).

#### 4. Indirect Recursion
**Definition:** Function A calls function B, which calls function A.

**Example:**
```cpp
void functionA(int n) {
    if (n > 0) {
        cout << n << " ";
        functionB(n - 1);
    }
}

void functionB(int n) {
    if (n > 0) {
        cout << n << " ";
        functionA(n - 1);
    }
}
```

---

## 5.2 Recursion vs Iteration

| Aspect | Recursion | Iteration |
|--------|-----------|-----------|
| **Definition** | Function calls itself | Repeating using loops |
| **Termination** | Base case | Loop condition |
| **Memory** | Uses call stack (more memory) | Uses loop variables (less memory) |
| **Speed** | Slower (function call overhead) | Faster |
| **Code** | Often more intuitive and elegant | Can be verbose |
| **Stack Overflow** | Possible with deep recursion | No risk |
| **Best For** | Tree/graph traversal, divide & conquer | Simple loops, better performance critical code |

### Converting Recursion to Iteration

**Recursive Factorial:**
```cpp
int factorial(int n) {
    if (n <= 1) return 1;
    return n * factorial(n - 1);
}
```

**Iterative Factorial:**
```cpp
int factorial(int n) {
    int result = 1;
    for (int i = 2; i <= n; i++) {
        result *= i;
    }
    return result;
}
```

---

## 5.3 Classic Recursion Problems

### 1. Tower of Hanoi
**Problem:** Move n disks from source rod to destination rod using auxiliary rod, following:
* Only one disk can be moved at a time
* Only smaller disk can be placed on top of larger disk

**Solution:**
```cpp
void towerOfHanoi(int n, char source, char dest, char aux) {
    if (n == 1) {
        cout << "Move disk 1 from " << source << " to " << dest << endl;
        return;
    }
    
    // Move n-1 disks from source to auxiliary using destination
    towerOfHanoi(n - 1, source, aux, dest);
    
    // Move nth disk from source to destination
    cout << "Move disk " << n << " from " << source << " to " << dest << endl;
    
    // Move n-1 disks from auxiliary to destination using source
    towerOfHanoi(n - 1, aux, dest, source);
}
```
* **Recurrence:** T(n) = 2T(n-1) + 1
* **Time:** O(2ⁿ)
* **Space:** O(n) - recursion depth

**Number of moves:** 2ⁿ - 1

### 2. Generate All Subsets (Power Set)
```cpp
void generateSubsets(string s, int index, string current) {
    if (index == s.length()) {
        cout << "{" << current << "}" << endl;
        return;
    }
    
    // Exclude current character
    generateSubsets(s, index + 1, current);
    
    // Include current character
    generateSubsets(s, index + 1, current + s[index]);
}
```
* **Time:** O(2ⁿ)
* **Space:** O(n) - recursion depth

**Example:** For s="ABC", generates: {}, {C}, {B}, {BC}, {A}, {AC}, {AB}, {ABC}

### 3. Generate All Permutations
```cpp
void permute(string s, int left, int right) {
    if (left == right) {
        cout << s << endl;
        return;
    }
    
    for (int i = left; i <= right; i++) {
        // Swap
        swap(s[left], s[i]);
        
        // Recurse
        permute(s, left + 1, right);
        
        // Backtrack (undo swap)
        swap(s[left], s[i]);
    }
}
```
* **Time:** O(n × n!)
* **Space:** O(n) - recursion depth

### 4. Print All Paths in Binary Tree
```cpp
void printPaths(TreeNode* root, vector<int>& path) {
    if (root == NULL) return;
    
    path.push_back(root->data);
    
    // If leaf node, print path
    if (root->left == NULL && root->right == NULL) {
        for (int val : path) {
            cout << val << " ";
        }
        cout << endl;
    } else {
        printPaths(root->left, path);
        printPaths(root->right, path);
    }
    
    path.pop_back();  // Backtrack
}
```

---

## 5.4 Backtracking

### Definition
**Backtracking:** A systematic way to search for solutions by trying partial solutions and abandoning them ("backtracking") if they don't lead to a valid solution.

### Template
```cpp
void backtrack(parameters) {
    if (isValidSolution(parameters)) {
        addToResult(parameters);
        return;
    }
    
    for (each possible choice) {
        // Make choice
        choose();
        
        // Explore
        backtrack(modified_parameters);
        
        // Undo choice (backtrack)
        unchoose();
    }
}
```

---

### Classic Backtracking Problems

#### 1. N-Queens Problem
**Problem:** Place N queens on N×N chessboard such that no two queens attack each other.

```cpp
bool isSafe(vector<vector<int>>& board, int row, int col, int n) {
    // Check column
    for (int i = 0; i < row; i++) {
        if (board[i][col] == 1) return false;
    }
    
    // Check upper left diagonal
    for (int i = row, j = col; i >= 0 && j >= 0; i--, j--) {
        if (board[i][j] == 1) return false;
    }
    
    // Check upper right diagonal
    for (int i = row, j = col; i >= 0 && j < n; i--, j++) {
        if (board[i][j] == 1) return false;
    }
    
    return true;
}

void solveNQueens(vector<vector<int>>& board, int row, int n) {
    if (row == n) {
        printBoard(board, n);
        return;
    }
    
    for (int col = 0; col < n; col++) {
        if (isSafe(board, row, col, n)) {
            // Place queen
            board[row][col] = 1;
            
            // Recurse
            solveNQueens(board, row + 1, n);
            
            // Backtrack
            board[row][col] = 0;
        }
    }
}
```
* **Time:** O(N!)
* **Space:** O(N²)

#### 2. Sudoku Solver
```cpp
bool isSafe(int board[9][9], int row, int col, int num) {
    // Check row
    for (int x = 0; x < 9; x++) {
        if (board[row][x] == num) return false;
    }
    
    // Check column
    for (int x = 0; x < 9; x++) {
        if (board[x][col] == num) return false;
    }
    
    // Check 3x3 box
    int startRow = row - row % 3;
    int startCol = col - col % 3;
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            if (board[i + startRow][j + startCol] == num) return false;
        }
    }
    
    return true;
}

bool solveSudoku(int board[9][9], int row, int col) {
    // If reached end of board
    if (row == 9) return true;
    
    // Move to next row if end of current row
    if (col == 9) return solveSudoku(board, row + 1, 0);
    
    // Skip filled cells
    if (board[row][col] != 0) return solveSudoku(board, row, col + 1);
    
    // Try placing digits 1-9
    for (int num = 1; num <= 9; num++) {
        if (isSafe(board, row, col, num)) {
            // Place number
            board[row][col] = num;
            
            // Recurse
            if (solveSudoku(board, row, col + 1)) return true;
            
            // Backtrack
            board[row][col] = 0;
        }
    }
    
    return false;  // No solution found
}
```

#### 3. Rat in a Maze
**Problem:** Find path from (0,0) to (n-1,n-1) in a maze where 1 represents valid cell and 0 represents blocked.

```cpp
bool isSafe(int maze[4][4], int x, int y, int n) {
    return (x >= 0 && x < n && y >= 0 && y < n && maze[x][y] == 1);
}

bool solveMaze(int maze[4][4], int x, int y, int sol[4][4], int n) {
    // Reached destination
    if (x == n-1 && y == n-1) {
        sol[x][y] = 1;
        return true;
    }
    
    // Check if current cell is valid
    if (isSafe(maze, x, y, n)) {
        // Mark current cell as part of solution
        sol[x][y] = 1;
        
        // Move right
        if (solveMaze(maze, x + 1, y, sol, n)) return true;
        
        // Move down
        if (solveMaze(maze, x, y + 1, sol, n)) return true;
        
        // Backtrack
        sol[x][y] = 0;
        return false;
    }
    
    return false;
}
```

---

## 📝 MCQs for Module 5

### Q1. The space complexity of a recursive function is determined by:
A. Number of recursive calls  
B. Maximum depth of recursion  
C. Size of input  
D. Number of variables

> **Answer: B**  
> **Explanation:** Space complexity depends on the maximum depth of recursion, which determines the call stack size.

### Q2. The time complexity of naive Fibonacci recursion is:
A. O(n)  
B. O(log n)  
C. O(2ⁿ)  
D. O(n²)

> **Answer: C**  
> **Explanation:** Fibonacci makes two recursive calls for each n, leading to exponential time O(2ⁿ).

### Q3. Tower of Hanoi with n disks requires minimum moves:
A. n  
B. 2ⁿ  
C. 2ⁿ - 1  
D. n²

> **Answer: C**  
> **Explanation:** The recurrence T(n) = 2T(n-1) + 1 gives total moves = 2ⁿ - 1.

### Q4. Tail recursion can be optimized to:
A. Reduce time complexity  
B. Eliminate recursion by converting to iteration  
C. Increase space complexity  
D. Add more recursive calls

> **Answer: B**  
> **Explanation:** Tail call optimization converts tail-recursive functions to iterative form, eliminating recursion overhead.

### Q5. Backtracking is commonly used in:
A. Sorting algorithms  
B. Finding all possible solutions  
C. Binary search  
D. Hashing

> **Answer: B**  
> **Explanation:** Backtracking systematically explores all possible solutions (e.g., N-Queens, Sudoku).

---


# Additional modules will be added...
