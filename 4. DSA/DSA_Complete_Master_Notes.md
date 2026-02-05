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



# 🌳 MODULE 6: TREES (BINARY TREES, BST, AVL, B-TREES)

## 6.1 Introduction to Trees

### What is a Tree?
* **Definition:** A hierarchical data structure consisting of nodes connected by edges, with no cycles.
* **Key Properties:**
  - One node is designated as the **root**
  - Every node (except root) has exactly one parent
  - There is a unique path from root to every node

### Basic Tree Terminology

```
          A (Root)
         / \
        B   C
       / \   \
      D   E   F
     /
    G
```

| Term | Definition | Example |
|------|------------|---------|
| **Root** | Topmost node with no parent | A |
| **Parent** | Node with child(ren) | A is parent of B and C |
| **Child** | Node descended from another | B and C are children of A |
| **Siblings** | Nodes with same parent | B and C are siblings |
| **Leaf** | Node with no children | E, F, G are leaves |
| **Internal Node** | Node with at least one child | A, B, C, D |
| **Ancestor** | Nodes on path from root to node | A, B, D are ancestors of G |
| **Descendant** | Nodes in subtree below node | D, E, G are descendants of B |
| **Degree** | Number of children of a node | Degree(A)=2, Degree(D)=1 |
| **Height** | Longest path from node to leaf | Height(A)=3, Height(B)=2 |
| **Depth/Level** | Distance from root to node | Depth(D)=2, Depth(G)=3 |
| **Subtree** | Tree formed by node and descendants | Subtree of B includes D, E, G |

### Properties
* **Number of edges in tree with n nodes:** n - 1
* **Maximum nodes at level L:** 2^L (for binary tree)
* **Maximum nodes in tree of height h:** 2^(h+1) - 1

---

## 6.2 Binary Trees

### Definition
A tree where each node has **at most 2 children** (left child and right child).

### Types of Binary Trees

#### 1. Full Binary Tree
* **Definition:** Every node has either 0 or 2 children (no node has exactly 1 child).
```
      A
     / \
    B   C
   / \
  D   E
```
* **Property:** If full binary tree has L leaves, internal nodes = L - 1

#### 2. Complete Binary Tree
* **Definition:** All levels completely filled except possibly the last, which is filled from left to right.
```
      A
     / \
    B   C
   / \  /
  D  E F
```
* **Used in:** Heap implementation
* **Property:** If there are n nodes, height = ⌊log₂ n⌋

#### 3. Perfect Binary Tree
* **Definition:** All internal nodes have 2 children, and all leaves are at same level.
```
      A
     / \
    B   C
   / \ / \
  D  E F  G
```
* **Nodes at level L:** 2^L
* **Total nodes:** 2^(h+1) - 1 where h is height
* **Leaves:** 2^h

#### 4. Balanced Binary Tree
* **Definition:** Height of left and right subtrees of every node differ by at most 1.
* **Examples:** AVL trees, Red-Black trees
* **Height:** O(log n)

#### 5. Degenerate (Skewed) Tree
* **Definition:** Each parent has only one child (essentially a linked list).
```
    A
     \
      B
       \
        C
         \
          D
```
* **Height:** O(n) - worst case

---

## 6.3 Binary Tree Representation

### 1. Array Representation (for Complete Binary Trees)
```
Tree:      A
          / \
         B   C
        / \ /
       D  E F

Array: [A, B, C, D, E, F]
Index:  0  1  2  3  4  5
```

**Index Relationships:**
* **Left child of node at i:** 2i + 1
* **Right child of node at i:** 2i + 2
* **Parent of node at i:** ⌊(i-1)/2⌋

### 2. Linked Representation
```cpp
struct Node {
    int data;
    Node* left;
    Node* right;
    
    Node(int val) {
        data = val;
        left = NULL;
        right = NULL;
    }
};
```

---

## 6.4 Binary Tree Traversals

### 1. Depth-First Traversals

#### A. Inorder (Left-Root-Right)
```cpp
void inorder(Node* root) {
    if (root == NULL) return;
    
    inorder(root->left);      // Visit left subtree
    cout << root->data << " "; // Visit root
    inorder(root->right);     // Visit right subtree
}
```
**Example:**
```
Tree:     4
         / \
        2   6
       / \ / \
      1  3 5  7

Inorder: 1 2 3 4 5 6 7 (Sorted order for BST!)
```

#### B. Preorder (Root-Left-Right)
```cpp
void preorder(Node* root) {
    if (root == NULL) return;
    
    cout << root->data << " "; // Visit root
    preorder(root->left);      // Visit left subtree
    preorder(root->right);     // Visit right subtree
}
```
**Example:** `4 2 1 3 6 5 7`
**Use:** Tree construction, prefix expression evaluation

#### C. Postorder (Left-Right-Root)
```cpp
void postorder(Node* root) {
    if (root == NULL) return;
    
    postorder(root->left);     // Visit left subtree
    postorder(root->right);    // Visit right subtree
    cout << root->data << " "; // Visit root
}
```
**Example:** `1 3 2 5 7 6 4`
**Use:** Tree deletion, postfix expression evaluation

### 2. Breadth-First Traversal

#### Level Order Traversal
```cpp
void levelOrder(Node* root) {
    if (root == NULL) return;
    
    queue<Node*> q;
    q.push(root);
    
    while (!q.empty()) {
        Node* current = q.front();
        q.pop();
        
        cout << current->data << " ";
        
        if (current->left != NULL)
            q.push(current->left);
        if (current->right != NULL)
            q.push(current->right);
    }
}
```
**Example:** `4 2 6 1 3 5 7`

### Traversal Complexities
| Traversal | Time Complexity | Space Complexity |
|-----------|-----------------|------------------|
| Inorder | O(n) | O(h) - recursion stack |
| Preorder | O(n) | O(h) - recursion stack |
| Postorder | O(n) | O(h) - recursion stack |
| Level Order | O(n) | O(w) - queue, w=max width |

---

## 6.5 Binary Search Tree (BST)

### Definition
A binary tree where for every node:
* All nodes in **left subtree ≤ node value**
* All nodes in **right subtree > node value**
* Both left and right subtrees are also BSTs

```
Valid BST:      8
               / \
              3   10
             / \    \
            1   6    14
               / \   /
              4   7 13
```

### BST Operations

#### 1. Search
```cpp
Node* search(Node* root, int key) {
    if (root == NULL || root->data == key)
        return root;
    
    if (key < root->data)
        return search(root->left, key);
    else
        return search(root->right, key);
}
```
* **Time:** O(h) where h is height
  - Best/Average: O(log n) for balanced BST
  - Worst: O(n) for skewed BST

#### 2. Insertion
```cpp
Node* insert(Node* root, int key) {
    if (root == NULL)
        return new Node(key);
    
    if (key < root->data)
        root->left = insert(root->left, key);
    else if (key > root->data)
        root->right = insert(root->right, key);
    
    return root;
}
```

#### 3. Deletion (Three Cases)

```cpp
Node* deleteNode(Node* root, int key) {
    if (root == NULL) return root;
    
    if (key < root->data)
        root->left = deleteNode(root->left, key);
    else if (key > root->data)
        root->right = deleteNode(root->right, key);
    else {
        // Case 1: Leaf node
        if (root->left == NULL && root->right == NULL) {
            delete root;
            return NULL;
        }
        // Case 2: One child
        else if (root->left == NULL) {
            Node* temp = root->right;
            delete root;
            return temp;
        }
        else if (root->right == NULL) {
            Node* temp = root->left;
            delete root;
            return temp;
        }
        // Case 3: Two children
        else {
            Node* temp = findMin(root->right);  // Inorder successor
            root->data = temp->data;
            root->right = deleteNode(root->right, temp->data);
        }
    }
    return root;
}

Node* findMin(Node* root) {
    while (root->left != NULL)
        root = root->left;
    return root;
}
```

**Deletion Cases:**
```
Case 1 - Leaf:      Delete directly
   20                  20
  /  \                /  \
 10  30       →      10  30
    /
   25 (delete)

Case 2 - One child: Replace with child
   20                  20
  /  \                /  \
 10  30       →      10  25
      \
      25
   (delete 30)

Case 3 - Two children: Replace with inorder successor/predecessor
   20                  25
  /  \                /  \
 10  30       →      10  30
    /  \                   \
   25  35                  35
   (delete 20)
```

### BST Applications
1. **Database indexing**
2. **Symbol tables in compilers**
3. **Autocomplete features**
4. **Priority queues (inefficient compared to heaps)**

---

## 6.6 AVL Trees (Self-Balancing BST)

### Definition
* **AVL Tree:** BST where height difference between left and right subtrees (balance factor) of every node is ≤ 1.
* **Balance Factor (BF):** height(left subtree) - height(right subtree)
* **Valid BF values:** -1, 0, 1

### Why AVL Trees?
* BST operations are O(h)
* Skewed BST has h = O(n) → operations become O(n)
* AVL maintains h = O(log n) → operations remain O(log n)

### Node Structure
```cpp
struct AVLNode {
    int data;
    AVLNode* left;
    AVLNode* right;
    int height;
    
    AVLNode(int val) {
        data = val;
        left = NULL;
        right = NULL;
        height = 1;
    }
};
```

### Rotations to Maintain Balance

#### 1. Left Rotation (LL Case)
```
   y                    x
  / \                  / \
 T1  x       →        y   T3
    / \              / \
   T2 T3            T1 T2
```
```cpp
AVLNode* leftRotate(AVLNode* y) {
    AVLNode* x = y->right;
    AVLNode* T2 = x->left;
    
    x->left = y;
    y->right = T2;
    
    y->height = max(height(y->left), height(y->right)) + 1;
    x->height = max(height(x->left), height(x->right)) + 1;
    
    return x;
}
```

#### 2. Right Rotation (RR Case)
```
     y                  x
    / \                / \
   x   T3      →      T1  y
  / \                    / \
 T1 T2                  T2 T3
```

#### 3. Left-Right Rotation (LR Case)
```
   z                z              x
  / \              / \            / \
 y   T4    →      x   T4   →     y   z
/ \              / \             / \ / \
T1  x           y  T3           T1 T2 T3 T4
   / \         / \
  T2 T3       T1 T2

Step 1: Left rotate y    Step 2: Right rotate z
```

#### 4. Right-Left Rotation (RL Case)
```
Similar to LR but mirrored
```

### AVL Insertion
```cpp
AVLNode* insert(AVLNode* node, int key) {
    // 1. Normal BST insertion
    if (node == NULL)
        return new AVLNode(key);
    
    if (key < node->data)
        node->left = insert(node->left, key);
    else if (key > node->data)
        node->right = insert(node->right, key);
    else
        return node;  // Duplicate keys not allowed
    
    // 2. Update height
    node->height = 1 + max(height(node->left), height(node->right));
    
    // 3. Get balance factor
    int balance = getBalance(node);
    
    // 4. Balance the tree (4 cases)
    
    // Left Left Case
    if (balance > 1 && key < node->left->data)
        return rightRotate(node);
    
    // Right Right Case
    if (balance < -1 && key > node->right->data)
        return leftRotate(node);
    
    // Left Right Case
    if (balance > 1 && key > node->left->data) {
        node->left = leftRotate(node->left);
        return rightRotate(node);
    }
    
    // Right Left Case
    if (balance < -1 && key < node->right->data) {
        node->right = rightRotate(node->right);
        return leftRotate(node);
    }
    
    return node;
}

int height(AVLNode* node) {
    if (node == NULL) return 0;
    return node->height;
}

int getBalance(AVLNode* node) {
    if (node == NULL) return 0;
    return height(node->left) - height(node->right);
}
```

### AVL vs BST Comparison

| Operation | BST (Average) | BST (Worst) | AVL Tree |
|-----------|---------------|-------------|----------|
| Search | O(log n) | O(n) | O(log n) |
| Insert | O(log n) | O(n) | O(log n) |
| Delete | O(log n) | O(n) | O(log n) |
| Space | O(n) | O(n) | O(n) |

---

## 6.7 B-Trees (Multiway Search Trees)

### Definition
* **B-Tree:** Self-balancing tree optimized for systems that read/write large blocks of data (databases, file systems).
* **Properties of B-Tree of order m:**
  1. Every node has at most m children
  2. Every internal node (except root) has at least ⌈m/2⌉ children
  3. Root has at least 2 children (unless it's a leaf)
  4. All leaves are at the same level
  5. A non-leaf node with k children contains k-1 keys

### B-Tree of Order 3 (2-3 Tree)
```
Example B-Tree:
          [30]
         /    \
    [10,20]  [40,50]
    /  |  \   /  |  \
  [5][15][25][35][45][55]
```

### Why B-Trees?

#### Problem with Binary Trees for Disk Storage:
* Binary trees: Each node access = 1 disk read
* For large data, height can be large → many disk reads
* **Example:** 1 million keys, binary tree height ≈ 20

#### Solution: B-Trees:
* Each node stores multiple keys → more branching
* Height significantly reduced
* **Example:** 1 million keys, B-tree of order 100, height ≈ 3
* **Fewer disk accesses = Better performance**

### B-Tree Operations

#### 1. Search
```cpp
// Pseudocode for B-Tree search
Node* search(Node* node, int key) {
    int i = 0;
    // Find first key greater than or equal to search key
    while (i < node->n && key > node->keys[i])
        i++;
    
    // Key found
    if (i < node->n && key == node->keys[i])
        return node;
    
    // Key not found and node is leaf
    if (node->leaf)
        return NULL;
    
    // Recurse to appropriate child
    return search(node->children[i], key);
}
```
* **Time:** O(log n) - base is m (order)

#### 2. Insertion
**Rules:**
1. Always insert into a leaf node
2. If leaf is full, split it and promote middle key to parent
3. If parent is full, split parent recursively

**Example:** Insert 32 into:
```
Before:        [30]
              /    \
         [10,20]  [40,50]

After:         [30,40]
              /   |   \
         [10,20] [32] [50]
```

#### 3. Deletion
**Three Cases:**
1. **Key in leaf:** Simply delete
2. **Key in internal node:** Replace with predecessor/successor
3. **Underflow:** Borrow from sibling or merge nodes

### B-Tree vs B+ Tree

| Feature | B-Tree | B+ Tree |
|---------|--------|---------|
| **Data location** | Internal + leaf nodes | Only leaf nodes |
| **Leaf connection** | Not connected | Leaves form linked list |
| **Search** | Can end at internal node | Always ends at leaf |
| **Range queries** | Inefficient | Efficient (traverse leaves) |
| **Usage** | File systems | Databases |

### Applications
1. **Database indexing** (MySQL InnoDB uses B+ trees)
2. **File systems** (NTFS, ext4)
3. **Multilevel indexing**

---

## 6.8 Common Tree Algorithms

### 1. Height of Binary Tree
```cpp
int height(Node* root) {
    if (root == NULL) return 0;
    return 1 + max(height(root->left), height(root->right));
}
```
**Time:** O(n), **Space:** O(h)

### 2. Diameter of Binary Tree
**Definition:** Longest path between any two nodes (may or may not pass through root).

```cpp
int diameter(Node* root, int& height) {
    if (root == NULL) {
        height = 0;
        return 0;
    }
    
    int leftHeight = 0, rightHeight = 0;
    int leftDiameter = diameter(root->left, leftHeight);
    int rightDiameter = diameter(root->right, rightHeight);
    
    height = 1 + max(leftHeight, rightHeight);
    
    // Diameter is max of:
    // 1. Left subtree diameter
    // 2. Right subtree diameter
    // 3. Path through root (leftHeight + rightHeight + 1)
    return max({leftDiameter, rightDiameter, leftHeight + rightHeight + 1});
}
```

### 3. Lowest Common Ancestor (LCA) in BST
```cpp
Node* LCA(Node* root, int n1, int n2) {
    if (root == NULL) return NULL;
    
    // If both n1 and n2 are smaller, LCA is in left subtree
    if (root->data > n1 && root->data > n2)
        return LCA(root->left, n1, n2);
    
    // If both n1 and n2 are greater, LCA is in right subtree
    if (root->data < n1 && root->data < n2)
        return LCA(root->right, n1, n2);
    
    // Otherwise, root is LCA
    return root;
}
```

### 4. Check if Binary Tree is BST
```cpp
bool isBST(Node* root, int min, int max) {
    if (root == NULL) return true;
    
    if (root->data <= min || root->data >= max)
        return false;
    
    return isBST(root->left, min, root->data) &&
           isBST(root->right, root->data, max);
}

// Call: isBST(root, INT_MIN, INT_MAX)
```

### 5. Print All Root-to-Leaf Paths
```cpp
void printPaths(Node* root, vector<int>& path) {
    if (root == NULL) return;
    
    path.push_back(root->data);
    
    // If leaf node, print path
    if (root->left == NULL && root->right == NULL) {
        for (int val : path)
            cout << val << " ";
        cout << endl;
    }
    
    printPaths(root->left, path);
    printPaths(root->right, path);
    
    path.pop_back();  // Backtrack
}
```

---

## 📝 MCQs for Module 6

### Q1. In a complete binary tree with n nodes, what is the height?
A. O(n)  
B. O(log n)  
C. O(n²)  
D. O(√n)

> **Answer: B**  
> **Explanation:** Complete binary trees are balanced with all levels filled except possibly the last. Height = ⌊log₂ n⌋ = O(log n).

### Q2. Inorder traversal of a BST gives:
A. Random order  
B. Sorted order (ascending)  
C. Sorted order (descending)  
D. Level order

> **Answer: B**  
> **Explanation:** Inorder traversal (Left-Root-Right) of BST visits nodes in ascending sorted order.

### Q3. In AVL tree, balance factor of a node can be:
A. Any integer  
B. Only 0  
C. -1, 0, or 1  
D. -2, -1, 0, 1, 2

> **Answer: C**  
> **Explanation:** AVL tree maintains balance by ensuring balance factor (height difference) is only -1, 0, or 1.

### Q4. B-Tree is primarily used for:
A. In-memory sorting  
B. Disk-based database indexing  
C. Network routing  
D. String matching

> **Answer: B**  
> **Explanation:** B-Trees minimize disk accesses by storing multiple keys per node, making them ideal for database indexing.

### Q5. Time complexity to search in a balanced BST with n nodes:
A. O(1)  
B. O(log n)  
C. O(n)  
D. O(n log n)

> **Answer: B**  
> **Explanation:** In balanced BST, height is O(log n), and search follows one path from root to leaf.

### Q6. Which rotation is needed when AVL tree is left-heavy and left child is right-heavy?
A. Single right rotation  
B. Single left rotation  
C. Left-Right rotation  
D. Right-Left rotation

> **Answer: C**  
> **Explanation:** LR case requires left rotation on left child followed by right rotation on root.

### Q7. Maximum number of nodes in a binary tree of height h:
A. 2^h  
B. 2^h - 1  
C. 2^(h+1) - 1  
D. h²

> **Answer: C**  
> **Explanation:** Perfect binary tree has 1+2+4+...+2^h = 2^(h+1) - 1 nodes.

### Q8. Deletion of node with two children in BST is replaced by:
A. Left child  
B. Right child  
C. Inorder successor or predecessor  
D. Parent node

> **Answer: C**  
> **Explanation:** Node is replaced with inorder successor (smallest in right subtree) or predecessor (largest in left subtree).

---


# 🔺 MODULE 7: HEAPS & PRIORITY QUEUES

## 7.1 Introduction to Heaps

### What is a Heap?
* **Definition:** A complete binary tree that satisfies the heap property.
* **Complete Binary Tree:** All levels filled except possibly the last, which is filled from left to right.

### Heap Property

#### Max Heap
* **Property:** Value of each node ≥ values of its children
* **Root:** Contains maximum element

```
Max Heap:      90
              /  \
            80   70
           / \   /
          50 40 60
```

#### Min Heap
* **Property:** Value of each node ≤ values of its children
* **Root:** Contains minimum element

```
Min Heap:      10
              /  \
            20   30
           / \   /
          50 40 60
```

### Why Heaps?
* **Priority Queue implementation:** Efficient insertion and extraction of min/max
* **Heap Sort:** Sorts in O(n log n)
* **Graph algorithms:** Dijkstra, Prim (using min heap)
* **Finding kth largest/smallest element**

---

## 7.2 Heap Representation

### Array Representation
Heaps are stored in arrays using level-order traversal.

```
Heap:          10
              /  \
            20   30
           / \   /
          50 40 60

Array: [10, 20, 30, 50, 40, 60]
Index:  0   1   2   3   4   5
```

**Index Relationships:**
* **Left child of node at i:** 2i + 1
* **Right child of node at i:** 2i + 2
* **Parent of node at i:** ⌊(i-1)/2⌋

**Advantages:**
* No pointers needed
* Cache-friendly (contiguous memory)
* Easy to calculate parent/child indices

---

## 7.3 Heap Operations

### 1. Heapify (Maintain Heap Property)

#### Heapify Down (for Max Heap)
Used after deleting root or building heap.

```cpp
void heapifyDown(int arr[], int n, int i) {
    int largest = i;
    int left = 2 * i + 1;
    int right = 2 * i + 2;
    
    // If left child is larger
    if (left < n && arr[left] > arr[largest])
        largest = left;
    
    // If right child is larger
    if (right < n && arr[right] > arr[largest])
        largest = right;
    
    // If largest is not root
    if (largest != i) {
        swap(arr[i], arr[largest]);
        heapifyDown(arr, n, largest);  // Recursively heapify
    }
}
```
**Time:** O(log n) - moves down height of tree

#### Heapify Up
Used after inserting new element.

```cpp
void heapifyUp(int arr[], int i) {
    int parent = (i - 1) / 2;
    
    // If current node is greater than parent, swap
    if (i > 0 && arr[i] > arr[parent]) {
        swap(arr[i], arr[parent]);
        heapifyUp(arr, parent);  // Recursively heapify up
    }
}
```
**Time:** O(log n)

### 2. Insert

```cpp
void insert(vector<int>& heap, int key) {
    // Add new element at end
    heap.push_back(key);
    
    // Heapify up to maintain heap property
    int i = heap.size() - 1;
    
    while (i > 0 && heap[(i-1)/2] < heap[i]) {
        swap(heap[i], heap[(i-1)/2]);
        i = (i - 1) / 2;
    }
}
```
**Time:** O(log n)

**Example:**
```
Insert 35 into max heap:

Step 1: Add at end
[90, 80, 70, 50, 40, 60, 35]

Step 2: Heapify up
          90
         /  \
       80    70
      / \    / \
     50 40  60  35

No swaps needed (35 < 70)
Result: [90, 80, 70, 50, 40, 60, 35]
```

### 3. Extract Max/Min

```cpp
int extractMax(vector<int>& heap) {
    if (heap.empty()) {
        cout << "Heap is empty" << endl;
        return -1;
    }
    
    // Store max value
    int maxVal = heap[0];
    
    // Move last element to root
    heap[0] = heap.back();
    heap.pop_back();
    
    // Heapify down from root
    int i = 0, n = heap.size();
    while (true) {
        int largest = i;
        int left = 2 * i + 1;
        int right = 2 * i + 2;
        
        if (left < n && heap[left] > heap[largest])
            largest = left;
        if (right < n && heap[right] > heap[largest])
            largest = right;
        
        if (largest == i) break;
        
        swap(heap[i], heap[largest]);
        i = largest;
    }
    
    return maxVal;
}
```
**Time:** O(log n)

**Example:**
```
Extract max from [90, 80, 70, 50, 40, 60]:

Step 1: Remove root, move last to root
[60, 80, 70, 50, 40]

Step 2: Heapify down
          60              80
         /  \            /  \
       80    70    →   60   70
      / \             / \
     50 40           50 40

Step 3: Continue heapifying
          80
         /  \
       50    70
      / \
     60 40

Final: [80, 50, 70, 60, 40]
Extracted: 90
```

### 4. Build Heap

```cpp
void buildHeap(int arr[], int n) {
    // Start from last non-leaf node and heapify down
    for (int i = n/2 - 1; i >= 0; i--) {
        heapifyDown(arr, n, i);
    }
}
```
**Time:** O(n) - not O(n log n)!

**Proof:**
* Leaves (n/2 nodes): 0 swaps
* Nodes at height 1 (n/4 nodes): 1 swap each
* Nodes at height 2 (n/8 nodes): 2 swaps each
* ...
* Total: n/4 × 1 + n/8 × 2 + n/16 × 3 + ... ≈ O(n)

---

## 7.4 Heap Sort

### Algorithm
```cpp
void heapSort(int arr[], int n) {
    // 1. Build max heap
    buildHeap(arr, n);
    
    // 2. Extract elements one by one
    for (int i = n - 1; i > 0; i--) {
        // Move current root to end
        swap(arr[0], arr[i]);
        
        // Heapify reduced heap
        heapifyDown(arr, i, 0);
    }
}
```

### Complexity Analysis
* **Build Heap:** O(n)
* **Extract n times:** n × O(log n) = O(n log n)
* **Total Time:** O(n log n)
* **Space:** O(1) - in-place sorting
* **Stable:** No

### Example
```
Array: [4, 10, 3, 5, 1]

Step 1: Build max heap
[10, 5, 3, 4, 1]

Step 2: Extract max (10), move to end
[1, 5, 3, 4 | 10]
Heapify: [5, 4, 3, 1 | 10]

Step 3: Extract max (5), move to end
[1, 4, 3 | 5, 10]
Heapify: [4, 1, 3 | 5, 10]

Step 4: Extract max (4), move to end
[3, 1 | 4, 5, 10]
Heapify: [3, 1 | 4, 5, 10]

Step 5: Extract max (3), move to end
[1 | 3, 4, 5, 10]

Sorted: [1, 3, 4, 5, 10]
```

---

## 7.5 Priority Queue

### Definition
* **Priority Queue:** Abstract data type where each element has a priority.
* **Operations:**
  - `insert(x, priority)`: Add element with priority
  - `extractMax()`/`extractMin()`: Remove and return highest/lowest priority element
  - `peek()`: Return highest/lowest priority element without removing

### Implementation Comparison

| Implementation | Insert | Extract Max/Min | Find Max/Min |
|----------------|--------|-----------------|--------------|
| **Unsorted Array** | O(1) | O(n) | O(n) |
| **Sorted Array** | O(n) | O(1) | O(1) |
| **Unsorted Linked List** | O(1) | O(n) | O(n) |
| **Sorted Linked List** | O(n) | O(1) | O(1) |
| **Binary Heap** | **O(log n)** | **O(log n)** | **O(1)** ✓ |
| **BST** | O(log n) | O(log n) | O(log n) |

**Winner:** Binary Heap provides best balance!

### C++ STL Priority Queue
```cpp
#include <queue>

// Max Heap (default)
priority_queue<int> maxHeap;
maxHeap.push(10);
maxHeap.push(30);
maxHeap.push(20);
cout << maxHeap.top();  // 30
maxHeap.pop();          // Remove 30

// Min Heap (using greater comparator)
priority_queue<int, vector<int>, greater<int>> minHeap;
minHeap.push(10);
minHeap.push(30);
minHeap.push(20);
cout << minHeap.top();  // 10
minHeap.pop();          // Remove 10
```

---

## 7.6 Applications of Heaps

### 1. Find Kth Largest Element
```cpp
int findKthLargest(vector<int>& nums, int k) {
    // Use min heap of size k
    priority_queue<int, vector<int>, greater<int>> minHeap;
    
    for (int num : nums) {
        minHeap.push(num);
        if (minHeap.size() > k)
            minHeap.pop();
    }
    
    return minHeap.top();
}
```
**Time:** O(n log k), **Space:** O(k)

### 2. Merge K Sorted Arrays
```cpp
vector<int> mergeKSortedArrays(vector<vector<int>>& arrays) {
    // Min heap to store {value, array_index, element_index}
    priority_queue<tuple<int, int, int>, 
                   vector<tuple<int, int, int>>,
                   greater<tuple<int, int, int>>> minHeap;
    
    // Add first element of each array
    for (int i = 0; i < arrays.size(); i++) {
        if (!arrays[i].empty())
            minHeap.push({arrays[i][0], i, 0});
    }
    
    vector<int> result;
    
    while (!minHeap.empty()) {
        auto [val, arrIdx, elemIdx] = minHeap.top();
        minHeap.pop();
        result.push_back(val);
        
        // Add next element from same array
        if (elemIdx + 1 < arrays[arrIdx].size()) {
            minHeap.push({arrays[arrIdx][elemIdx + 1], 
                         arrIdx, 
                         elemIdx + 1});
        }
    }
    
    return result;
}
```
**Time:** O(n log k) where n = total elements, k = number of arrays

### 3. Top K Frequent Elements
```cpp
vector<int> topKFrequent(vector<int>& nums, int k) {
    // Count frequencies
    unordered_map<int, int> freq;
    for (int num : nums)
        freq[num]++;
    
    // Min heap of size k
    priority_queue<pair<int, int>, 
                   vector<pair<int, int>>,
                   greater<pair<int, int>>> minHeap;
    
    for (auto [num, count] : freq) {
        minHeap.push({count, num});
        if (minHeap.size() > k)
            minHeap.pop();
    }
    
    vector<int> result;
    while (!minHeap.empty()) {
        result.push_back(minHeap.top().second);
        minHeap.pop();
    }
    
    return result;
}
```

### 4. Median of Stream
```cpp
class MedianFinder {
    priority_queue<int> maxHeap;  // Left half
    priority_queue<int, vector<int>, greater<int>> minHeap;  // Right half
    
public:
    void addNum(int num) {
        if (maxHeap.empty() || num <= maxHeap.top())
            maxHeap.push(num);
        else
            minHeap.push(num);
        
        // Balance heaps
        if (maxHeap.size() > minHeap.size() + 1) {
            minHeap.push(maxHeap.top());
            maxHeap.pop();
        } else if (minHeap.size() > maxHeap.size()) {
            maxHeap.push(minHeap.top());
            minHeap.pop();
        }
    }
    
    double findMedian() {
        if (maxHeap.size() == minHeap.size())
            return (maxHeap.top() + minHeap.top()) / 2.0;
        return maxHeap.top();
    }
};
```
**Time:** addNum O(log n), findMedian O(1)

---

## 7.7 Heap vs BST

| Feature | Binary Heap | BST |
|---------|-------------|-----|
| **Structure** | Complete binary tree | Not necessarily complete |
| **Ordering** | Parent vs children only | Left < Parent < Right |
| **Find Min/Max** | O(1) | O(log n) in balanced, O(n) worst |
| **Insert** | O(log n) | O(log n) avg, O(n) worst |
| **Delete Min/Max** | O(log n) | O(log n) avg, O(n) worst |
| **Search arbitrary** | O(n) | O(log n) avg, O(n) worst |
| **Array representation** | Efficient | Not practical |
| **Use case** | Priority queue | Searching, ordered data |

---

## 📝 MCQs for Module 7

### Q1. In a max heap, which property must hold?
A. Parent < Both children  
B. Parent > Both children  
C. Parent = Both children  
D. Left child > Right child

> **Answer: B**  
> **Explanation:** In max heap, parent node is always greater than or equal to its children.

### Q2. Time complexity to build a heap from n elements:
A. O(log n)  
B. O(n)  
C. O(n log n)  
D. O(n²)

> **Answer: B**  
> **Explanation:** Build heap uses heapify-down from bottom up, resulting in O(n) time, not O(n log n).

### Q3. Heap sort has time complexity:
A. O(n)  
B. O(n log n)  
C. O(n²)  
D. O(log n)

> **Answer: B**  
> **Explanation:** Building heap is O(n), then extracting n elements each taking O(log n) = O(n log n) total.

### Q4. In array representation of heap, left child of node at index i is at:
A. i/2  
B. 2i  
C. 2i + 1  
D. i + 1

> **Answer: C**  
> **Explanation:** Using 0-based indexing, left child of node at i is at 2i + 1.

### Q5. Which data structure is best for implementing priority queue?
A. Array  
B. Linked List  
C. Binary Heap  
D. Stack

> **Answer: C**  
> **Explanation:** Binary heap provides O(log n) for insert and extract operations, optimal for priority queue.

### Q6. Extract max operation in max heap takes:
A. O(1)  
B. O(log n)  
C. O(n)  
D. O(n log n)

> **Answer: B**  
> **Explanation:** After removing root, we need to heapify down which takes O(log n) time.

### Q7. Is heap sort a stable sorting algorithm?
A. Yes, always  
B. No, never  
C. Depends on implementation  
D. Only for ascending order

> **Answer: B**  
> **Explanation:** Heap sort is not stable as it can change relative order of equal elements.

### Q8. To find median of a stream efficiently, we use:
A. One max heap  
B. One min heap  
C. Two heaps (one max, one min)  
D. Binary search tree

> **Answer: C**  
> **Explanation:** Use max heap for smaller half and min heap for larger half to find median in O(1).

---


# 🔑 MODULE 8: HASHING & HASH TABLES

## 8.1 Introduction to Hashing

### What is Hashing?
* **Hashing:** Technique to map data of arbitrary size to fixed-size values (hash values/codes).
* **Hash Function:** Function that converts input (key) into an index in hash table.
* **Hash Table:** Data structure that stores key-value pairs with O(1) average-case access.

### Why Hashing?
**Problem with Arrays/Lists:**
* Search: O(n)
* Need better performance for large datasets

**Problem with BST:**
* Search: O(log n) average, O(n) worst
* Still not constant time

**Solution: Hash Table**
* Search: O(1) average
* Insert: O(1) average
* Delete: O(1) average

---

## 8.2 Hash Functions

### Properties of Good Hash Function
1. **Deterministic:** Same key always produces same hash value
2. **Uniform Distribution:** Minimizes collisions
3. **Fast to compute:** O(1) complexity
4. **Minimize collisions:** Different keys should produce different hash values

### Common Hash Functions

#### 1. Division Method
```
h(key) = key % tableSize
```
**Best when:** tableSize is prime (reduces collisions)

**Example:**
```
key = 45, tableSize = 11
h(45) = 45 % 11 = 1
```

#### 2. Multiplication Method
```
h(key) = ⌊tableSize × (key × A mod 1)⌋
where A is constant (0 < A < 1), Knuth suggests A ≈ 0.618
```

#### 3. Mid-Square Method
```
1. Square the key
2. Extract middle digits
3. Take mod tableSize
```
**Example:**
```
key = 60
60² = 3600
Extract middle: 60
h(60) = 60 % 100 = 60
```

#### 4. Folding Method
```
1. Divide key into parts
2. Add parts
3. Take mod tableSize
```
**Example:**
```
key = 123456789
123 + 456 + 789 = 1368
h(key) = 1368 % 100 = 68
```

#### 5. String Hashing (Polynomial Rolling Hash)
```cpp
int hashString(string s) {
    int hash = 0;
    int p = 31;  // Prime number
    int m = 1e9 + 9;  // Large prime
    
    long long power = 1;
    for (char c : s) {
        hash = (hash + (c - 'a' + 1) * power) % m;
        power = (power * p) % m;
    }
    
    return hash;
}
```

---

## 8.3 Collisions and Collision Resolution

### What is a Collision?
When two different keys hash to the same index.

```
Example:
h(key) = key % 10
h(15) = 5
h(25) = 5  ← Collision!
```

### Collision Resolution Techniques

---

## 8.4 Open Addressing

**Principle:** All elements stored in hash table itself. When collision occurs, probe for next available slot.

### 1. Linear Probing
**Formula:** h'(key, i) = (h(key) + i) % tableSize

```cpp
int linearProbe(int key, int i, int tableSize) {
    return (hash(key) + i) % tableSize;
}
```

**Example:**
```
Insert: 50, 70, 76, 85, 93
Hash function: h(key) = key % 10
Table size: 10

Insert 50: h(50) = 0 → [50, _, _, _, _, _, _, _, _, _]
Insert 70: h(70) = 0 (collision) → try index 1 → [50, 70, _, _, _, _, _, _, _, _]
Insert 76: h(76) = 6 → [50, 70, _, _, _, _, 76, _, _, _]
Insert 85: h(85) = 5 → [50, 70, _, _, _, 85, 76, _, _, _]
Insert 93: h(93) = 3 → [50, 70, _, 93, _, 85, 76, _, _, _]
```

**Advantages:**
* Simple implementation
* Good cache performance

**Disadvantages:**
* **Primary Clustering:** Consecutive blocks of occupied slots
* Degrades performance as table fills

### 2. Quadratic Probing
**Formula:** h'(key, i) = (h(key) + c₁×i + c₂×i²) % tableSize

```cpp
int quadraticProbe(int key, int i, int tableSize) {
    return (hash(key) + i * i) % tableSize;
}
```

**Example:**
```
h(key) = key % 10

Insert 50: index = (0 + 0²) % 10 = 0
Insert 70: collision at 0
  Try i=1: (0 + 1²) % 10 = 1
  Insert at index 1
Insert 80: collision at 0
  Try i=1: (0 + 1²) % 10 = 1 (occupied)
  Try i=2: (0 + 2²) % 10 = 4
  Insert at index 4
```

**Advantages:**
* Reduces primary clustering

**Disadvantages:**
* **Secondary Clustering:** Keys with same hash still probe same sequence
* May not probe all slots

### 3. Double Hashing
**Formula:** h'(key, i) = (h₁(key) + i × h₂(key)) % tableSize

```cpp
int doubleHash(int key, int i, int tableSize) {
    int h1 = key % tableSize;
    int h2 = 1 + (key % (tableSize - 1));
    return (h1 + i * h2) % tableSize;
}
```

**Example:**
```
h₁(key) = key % 11
h₂(key) = 1 + (key % 10)

Insert 76: h₁(76) = 10 → [_, _, _, _, _, _, _, _, _, _, 76]
Insert 93: h₁(93) = 5 → [_, _, _, _, _, 93, _, _, _, _, 76]
Insert 20: h₁(20) = 9 → [_, _, _, _, _, 93, _, _, _, 20, 76]
Insert 31: h₁(31) = 9 (collision)
  h₂(31) = 1 + (31 % 10) = 2
  Try (9 + 1×2) % 11 = 0
  Insert at index 0 → [31, _, _, _, _, 93, _, _, _, 20, 76]
```

**Advantages:**
* Best collision resolution among open addressing methods
* Uniform probing

**Disadvantages:**
* More complex computation
* h₂(key) should never be 0

---

## 8.5 Separate Chaining

**Principle:** Each hash table slot contains a linked list (or other structure) of all elements that hash to that slot.

```cpp
class HashTable {
private:
    vector<list<pair<int, int>>> table;  // list of (key, value) pairs
    int size;
    
    int hash(int key) {
        return key % size;
    }
    
public:
    HashTable(int s) : size(s) {
        table.resize(size);
    }
    
    void insert(int key, int value) {
        int index = hash(key);
        
        // Check if key already exists, update value
        for (auto& kv : table[index]) {
            if (kv.first == key) {
                kv.second = value;
                return;
            }
        }
        
        // Insert new key-value pair
        table[index].push_back({key, value});
    }
    
    bool search(int key, int& value) {
        int index = hash(key);
        
        for (auto& kv : table[index]) {
            if (kv.first == key) {
                value = kv.second;
                return true;
            }
        }
        
        return false;
    }
    
    void remove(int key) {
        int index = hash(key);
        
        table[index].remove_if([key](pair<int, int> kv) {
            return kv.first == key;
        });
    }
};
```

**Visualization:**
```
Insert: 50, 70, 76, 85, 93
Hash function: h(key) = key % 10

Index 0: 50 → 70 → NULL
Index 3: 93 → NULL
Index 5: 85 → NULL
Index 6: 76 → NULL
...
```

**Advantages:**
* Simple implementation
* Hash table never fills up
* Less sensitive to hash function

**Disadvantages:**
* Extra memory for pointers
* Poor cache performance
* If chains grow long, becomes O(n)

---

## 8.6 Load Factor and Rehashing

### Load Factor (α)
```
α = n / m
where n = number of keys inserted
      m = table size
```

**Impact:**
* **Open Addressing:** Performance degrades when α > 0.7
* **Separate Chaining:** Can handle α > 1, but longer chains

### Rehashing
When load factor exceeds threshold, resize and rehash.

```cpp
void rehash() {
    vector<list<pair<int, int>>> oldTable = table;
    size = size * 2;  // Double the size
    table.clear();
    table.resize(size);
    
    // Reinsert all elements
    for (auto& chain : oldTable) {
        for (auto& kv : chain) {
            insert(kv.first, kv.second);
        }
    }
}
```

**Time Complexity:**
* Rehashing: O(n)
* Amortized insert: O(1) (if done rarely)

---

## 8.7 Time Complexity Analysis

### Average Case (with good hash function)
| Operation | Chaining | Open Addressing |
|-----------|----------|-----------------|
| **Search** | O(1 + α) | O(1 / (1-α)) |
| **Insert** | O(1) | O(1 / (1-α)) |
| **Delete** | O(1 + α) | O(1 / (1-α)) |

where α = load factor

### Worst Case
* **All operations:** O(n) - when all keys collide

**Assumptions for O(1):**
* Good hash function (uniform distribution)
* Load factor kept reasonable (α < 0.7 for open addressing)
* Table size is large enough

---

## 8.8 Applications of Hashing

### 1. Detect Duplicates
```cpp
bool hasDuplicate(vector<int>& arr) {
    unordered_set<int> seen;
    
    for (int num : arr) {
        if (seen.count(num))
            return true;
        seen.insert(num);
    }
    
    return false;
}
```
**Time:** O(n), **Space:** O(n)

### 2. Two Sum Problem
```cpp
vector<int> twoSum(vector<int>& nums, int target) {
    unordered_map<int, int> map;  // value → index
    
    for (int i = 0; i < nums.size(); i++) {
        int complement = target - nums[i];
        
        if (map.count(complement))
            return {map[complement], i};
        
        map[nums[i]] = i;
    }
    
    return {};
}
```
**Time:** O(n), **Space:** O(n)

### 3. Frequency Count
```cpp
void printFrequencies(vector<int>& arr) {
    unordered_map<int, int> freq;
    
    for (int num : arr)
        freq[num]++;
    
    for (auto& [num, count] : freq)
        cout << num << ": " << count << endl;
}
```

### 4. Group Anagrams
```cpp
vector<vector<string>> groupAnagrams(vector<string>& strs) {
    unordered_map<string, vector<string>> map;
    
    for (string& s : strs) {
        string key = s;
        sort(key.begin(), key.end());
        map[key].push_back(s);
    }
    
    vector<vector<string>> result;
    for (auto& [key, group] : map)
        result.push_back(group);
    
    return result;
}
```

### 5. Longest Consecutive Sequence
```cpp
int longestConsecutive(vector<int>& nums) {
    unordered_set<int> numSet(nums.begin(), nums.end());
    int longest = 0;
    
    for (int num : numSet) {
        // Check if start of sequence
        if (!numSet.count(num - 1)) {
            int current = num;
            int currentLength = 1;
            
            while (numSet.count(current + 1)) {
                current++;
                currentLength++;
            }
            
            longest = max(longest, currentLength);
        }
    }
    
    return longest;
}
```
**Time:** O(n), **Space:** O(n)

---

## 8.9 Hash Table vs Other Data Structures

| Operation | Array | Linked List | BST | Hash Table |
|-----------|-------|-------------|-----|------------|
| **Search** | O(n) | O(n) | O(log n) | O(1) avg |
| **Insert** | O(n) | O(1) | O(log n) | O(1) avg |
| **Delete** | O(n) | O(n) | O(log n) | O(1) avg |
| **Ordered traversal** | ✓ | ✗ | ✓ | ✗ |
| **Range queries** | ✓ | ✗ | ✓ | ✗ |
| **Min/Max** | O(n) | O(n) | O(log n) | O(n) |

**When to use Hash Table:**
* Need fast lookup/insert/delete
* Don't need ordered data
* Don't need range queries

**When NOT to use Hash Table:**
* Need ordered traversal
* Need range queries
* Need min/max efficiently
* Memory is very limited

---

## 8.10 C++ STL Hash Containers

### 1. unordered_set
```cpp
#include <unordered_set>

unordered_set<int> s;
s.insert(10);
s.insert(20);
s.erase(10);
if (s.count(20))  // Returns 0 or 1
    cout << "Found";
```

### 2. unordered_map
```cpp
#include <unordered_map>

unordered_map<string, int> map;
map["Alice"] = 90;
map["Bob"] = 85;
map["Alice"] = 95;  // Updates value

if (map.find("Alice") != map.end())
    cout << map["Alice"];  // 95
```

### 3. unordered_multiset & unordered_multimap
Allow duplicate keys.

```cpp
unordered_multiset<int> ms;
ms.insert(10);
ms.insert(10);  // Duplicate allowed
ms.count(10);   // Returns 2

unordered_multimap<string, int> mm;
mm.insert({"Alice", 90});
mm.insert({"Alice", 95});  // Duplicate key allowed
```

---

## 📝 MCQs for Module 8

### Q1. Average time complexity of search in hash table:
A. O(1)  
B. O(log n)  
C. O(n)  
D. O(n²)

> **Answer: A**  
> **Explanation:** With good hash function and reasonable load factor, hash table provides O(1) average search time.

### Q2. Which collision resolution method uses linked lists?
A. Linear probing  
B. Quadratic probing  
C. Double hashing  
D. Separate chaining

> **Answer: D**  
> **Explanation:** Separate chaining stores colliding elements in linked lists at each hash table slot.

### Q3. Primary clustering is a problem in:
A. Separate chaining  
B. Linear probing  
C. Double hashing  
D. All methods equally

> **Answer: B**  
> **Explanation:** Linear probing creates consecutive blocks of occupied slots (primary clustering).

### Q4. If hash table size is 10 and load factor is 0.8, how many elements are stored?
A. 8  
B. 10  
C. 12  
D. 80

> **Answer: A**  
> **Explanation:** Load factor = n/m, so 0.8 = n/10, therefore n = 8.

### Q5. Which is NOT a property of a good hash function?
A. Deterministic  
B. Uniform distribution  
C. Slow computation  
D. Minimize collisions

> **Answer: C**  
> **Explanation:** Good hash function should be fast to compute, not slow.

### Q6. In double hashing, h₂(key) should never be:
A. 1  
B. 0  
C. Prime number  
D. Odd number

> **Answer: B**  
> **Explanation:** If h₂(key) = 0, probe sequence won't advance, causing infinite loop.

### Q7. Rehashing is done when:
A. First collision occurs  
B. Load factor exceeds threshold  
C. Table is half full  
D. After every deletion

> **Answer: B**  
> **Explanation:** Rehashing resizes table when load factor exceeds threshold (typically 0.7-0.75).

### Q8. Hash tables are NOT suitable for:
A. Fast lookups  
B. Duplicate detection  
C. Range queries  
D. Frequency counting

> **Answer: C**  
> **Explanation:** Hash tables don't maintain order, making range queries inefficient. Use BST or sorted array instead.

---


# 🕸️ MODULE 9: GRAPHS (REPRESENTATION & TRAVERSALS)

## 9.1 Introduction to Graphs

### What is a Graph?
* **Definition:** Non-linear data structure consisting of **vertices (nodes)** and **edges** connecting them.
* **G = (V, E)** where V = set of vertices, E = set of edges

### Graph Terminology

```
Example Graph:
    A --- B
    |     |
    C --- D --- E
```

| Term | Definition | Example |
|------|------------|---------|
| **Vertex/Node** | Fundamental unit | A, B, C, D, E |
| **Edge** | Connection between two vertices | (A,B), (A,C), etc. |
| **Adjacent** | Two vertices connected by edge | A and B are adjacent |
| **Degree** | Number of edges incident to vertex | Degree(D) = 3 |
| **Path** | Sequence of vertices connected by edges | A→C→D→E |
| **Cycle** | Path that starts and ends at same vertex | A→B→D→C→A |
| **Connected Graph** | Path exists between every pair of vertices | Above graph is connected |
| **Disconnected** | Some vertices unreachable from others | - |
| **Complete Graph** | Edge between every pair of vertices | K₅ (5 vertices, 10 edges) |

---

## 9.2 Types of Graphs

### 1. Directed Graph (Digraph)
* **Edges have direction:** (A → B) ≠ (B → A)
* **Represented by:** Arrows

```
    A → B
    ↓   ↓
    C ← D
```

**Applications:** Web pages (hyperlinks), Social media (followers), Task scheduling

### 2. Undirected Graph
* **Edges have no direction:** (A, B) = (B, A)
* **Represented by:** Lines

```
    A --- B
    |     |
    C --- D
```

**Applications:** Social networks (friendships), Road networks

### 3. Weighted Graph
* **Edges have weights/costs**

```
    A --5-- B
    |       |
    3       2
    |       |
    C --7-- D
```

**Applications:** Road networks (distances), Network routing (latency)

### 4. Unweighted Graph
* **All edges have equal weight (typically 1)**

### 5. Cyclic Graph
* **Contains at least one cycle**

### 6. Acyclic Graph
* **No cycles**
* **DAG (Directed Acyclic Graph):** Important in many applications

```
DAG Example:
    A → B
    ↓   ↓
    C → D
```

**Applications:** Task scheduling, Course prerequisites, Build systems

### 7. Connected vs Disconnected

**Connected:**
```
    A --- B
    |     |
    C --- D
```

**Disconnected:**
```
    A --- B     E --- F
    |
    C
```

---

## 9.3 Graph Representation

### 1. Adjacency Matrix

**Definition:** 2D array where matrix[i][j] = 1 if edge exists from i to j, else 0.

#### Undirected Graph Example
```
Graph:      0 --- 1
            |     |
            2 --- 3

Adjacency Matrix:
    0  1  2  3
0 [ 0  1  1  0 ]
1 [ 1  0  0  1 ]
2 [ 1  0  0  1 ]
3 [ 0  1  1  0 ]
```

#### Directed Graph Example
```
Graph:      0 → 1
            ↑   ↓
            2 ← 3

Adjacency Matrix:
    0  1  2  3
0 [ 0  1  0  0 ]
1 [ 0  0  0  1 ]
2 [ 1  0  0  0 ]
3 [ 0  0  1  0 ]
```

#### Weighted Graph
```
Graph:      0 --5-- 1
            |       |
            3       2
            |       |
            2 --7-- 3

Matrix:
    0  1  2  3
0 [ 0  5  3  0 ]
1 [ 5  0  0  2 ]
2 [ 3  0  0  7 ]
3 [ 0  2  7  0 ]
```

#### Implementation
```cpp
class Graph {
private:
    int V;  // Number of vertices
    vector<vector<int>> adjMatrix;
    
public:
    Graph(int vertices) {
        V = vertices;
        adjMatrix.resize(V, vector<int>(V, 0));
    }
    
    void addEdge(int u, int v, int weight = 1) {
        adjMatrix[u][v] = weight;
        adjMatrix[v][u] = weight;  // For undirected graph
    }
    
    void removeEdge(int u, int v) {
        adjMatrix[u][v] = 0;
        adjMatrix[v][u] = 0;
    }
    
    bool hasEdge(int u, int v) {
        return adjMatrix[u][v] != 0;
    }
    
    void printGraph() {
        for (int i = 0; i < V; i++) {
            for (int j = 0; j < V; j++) {
                cout << adjMatrix[i][j] << " ";
            }
            cout << endl;
        }
    }
};
```

#### Complexity
| Operation | Time | Space |
|-----------|------|-------|
| **Add Edge** | O(1) | O(V²) |
| **Remove Edge** | O(1) | O(V²) |
| **Check Edge** | O(1) | O(V²) |
| **Get All Adjacent** | O(V) | O(V²) |

**Pros:**
* Edge queries in O(1)
* Simple representation
* Good for dense graphs

**Cons:**
* O(V²) space even for sparse graphs
* Iterating over all edges: O(V²)

---

### 2. Adjacency List

**Definition:** Array of lists. Each vertex has a list of its adjacent vertices.

#### Example
```
Graph:      0 --- 1
            |     |
            2 --- 3

Adjacency List:
0 → [1, 2]
1 → [0, 3]
2 → [0, 3]
3 → [1, 2]
```

#### Implementation
```cpp
class Graph {
private:
    int V;
    vector<list<int>> adjList;
    
public:
    Graph(int vertices) {
        V = vertices;
        adjList.resize(V);
    }
    
    void addEdge(int u, int v) {
        adjList[u].push_back(v);
        adjList[v].push_back(u);  // For undirected
    }
    
    void removeEdge(int u, int v) {
        adjList[u].remove(v);
        adjList[v].remove(u);
    }
    
    void printGraph() {
        for (int i = 0; i < V; i++) {
            cout << i << " → ";
            for (int neighbor : adjList[i])
                cout << neighbor << " ";
            cout << endl;
        }
    }
};
```

#### For Weighted Graphs
```cpp
class WeightedGraph {
private:
    int V;
    vector<list<pair<int, int>>> adjList;  // {neighbor, weight}
    
public:
    WeightedGraph(int vertices) {
        V = vertices;
        adjList.resize(V);
    }
    
    void addEdge(int u, int v, int weight) {
        adjList[u].push_back({v, weight});
        adjList[v].push_back({u, weight});  // For undirected
    }
};
```

#### Complexity
| Operation | Time | Space |
|-----------|------|-------|
| **Add Edge** | O(1) | O(V + E) |
| **Remove Edge** | O(V) | O(V + E) |
| **Check Edge** | O(V) | O(V + E) |
| **Get All Adjacent** | O(1) | O(V + E) |

**Pros:**
* Space-efficient for sparse graphs
* Iterating over adjacent vertices is fast

**Cons:**
* Checking if edge exists: O(V)
* Slightly complex implementation

---

### 3. Edge List

**Definition:** List of all edges, each represented as a pair (or triple for weighted).

```cpp
vector<pair<int, int>> edges;  // {u, v}
// For weighted: vector<tuple<int, int, int>> edges;  // {u, v, weight}
```

**Example:**
```
Graph edges: [(0,1), (0,2), (1,3), (2,3)]
```

**Usage:** Kruskal's MST algorithm, sorting edges

---

### Comparison of Representations

| Representation | Space | Add Edge | Check Edge | Iterate Adjacent |
|----------------|-------|----------|------------|------------------|
| **Adjacency Matrix** | O(V²) | O(1) | O(1) | O(V) |
| **Adjacency List** | O(V+E) | O(1) | O(degree) | O(degree) |
| **Edge List** | O(E) | O(1) | O(E) | O(E) |

**Rules of Thumb:**
* **Dense graph (E ≈ V²):** Use adjacency matrix
* **Sparse graph (E << V²):** Use adjacency list
* **Need to process all edges:** Edge list

---

## 9.4 Graph Traversals

### 1. Breadth-First Search (BFS)

#### Algorithm
* **Strategy:** Visit all neighbors before going deeper
* **Data Structure:** Queue (FIFO)
* **Applications:** Shortest path in unweighted graph, level-order traversal

#### Implementation
```cpp
void BFS(int start) {
    vector<bool> visited(V, false);
    queue<int> q;
    
    visited[start] = true;
    q.push(start);
    
    while (!q.empty()) {
        int vertex = q.front();
        q.pop();
        cout << vertex << " ";
        
        // Visit all adjacent vertices
        for (int neighbor : adjList[vertex]) {
            if (!visited[neighbor]) {
                visited[neighbor] = true;
                q.push(neighbor);
            }
        }
    }
}
```

#### Example
```
Graph:      0 --- 1
            |     |
            2 --- 3 --- 4

BFS from 0:
Step 1: Visit 0, enqueue 1, 2       Output: 0
Step 2: Visit 1, enqueue 3          Output: 0 1
Step 3: Visit 2 (already visited 0) Output: 0 1 2
Step 4: Visit 3, enqueue 4          Output: 0 1 2 3
Step 5: Visit 4                     Output: 0 1 2 3 4
```

#### BFS for Shortest Path (Unweighted)
```cpp
void BFS_ShortestPath(int start, int end) {
    vector<bool> visited(V, false);
    vector<int> parent(V, -1);
    queue<int> q;
    
    visited[start] = true;
    q.push(start);
    
    while (!q.empty()) {
        int vertex = q.front();
        q.pop();
        
        if (vertex == end) break;
        
        for (int neighbor : adjList[vertex]) {
            if (!visited[neighbor]) {
                visited[neighbor] = true;
                parent[neighbor] = vertex;
                q.push(neighbor);
            }
        }
    }
    
    // Reconstruct path
    if (!visited[end]) {
        cout << "No path exists" << endl;
        return;
    }
    
    vector<int> path;
    int current = end;
    while (current != -1) {
        path.push_back(current);
        current = parent[current];
    }
    
    reverse(path.begin(), path.end());
    for (int v : path)
        cout << v << " ";
}
```

#### Complexity
* **Time:** O(V + E)
* **Space:** O(V) for queue and visited array

---

### 2. Depth-First Search (DFS)

#### Algorithm
* **Strategy:** Go as deep as possible before backtracking
* **Data Structure:** Stack (or recursion)
* **Applications:** Cycle detection, topological sort, connectivity

#### Recursive Implementation
```cpp
void DFS(int vertex, vector<bool>& visited) {
    visited[vertex] = true;
    cout << vertex << " ";
    
    for (int neighbor : adjList[vertex]) {
        if (!visited[neighbor]) {
            DFS(neighbor, visited);
        }
    }
}

// Call function
void startDFS(int start) {
    vector<bool> visited(V, false);
    DFS(start, visited);
}
```

#### Iterative Implementation
```cpp
void DFS_Iterative(int start) {
    vector<bool> visited(V, false);
    stack<int> s;
    
    s.push(start);
    
    while (!s.empty()) {
        int vertex = s.top();
        s.pop();
        
        if (!visited[vertex]) {
            visited[vertex] = true;
            cout << vertex << " ";
            
            // Push all adjacent vertices
            for (int neighbor : adjList[vertex]) {
                if (!visited[neighbor]) {
                    s.push(neighbor);
                }
            }
        }
    }
}
```

#### Example
```
Graph:      0 --- 1
            |     |
            2 --- 3 --- 4

DFS from 0:
Step 1: Visit 0, explore 1          Output: 0
Step 2: Visit 1, explore 3          Output: 0 1
Step 3: Visit 3, explore 2          Output: 0 1 3
Step 4: Visit 2 (already visited 0) Output: 0 1 3 2
Step 5: Visit 4                     Output: 0 1 3 2 4
```

#### Complexity
* **Time:** O(V + E)
* **Space:** O(V) for recursion stack/explicit stack

---

### BFS vs DFS Comparison

| Feature | BFS | DFS |
|---------|-----|-----|
| **Data Structure** | Queue | Stack/Recursion |
| **Traversal** | Level by level | Deep then backtrack |
| **Shortest Path** | ✓ (unweighted) | ✗ |
| **Space** | O(V) - can be more | O(V) - recursion depth |
| **Completeness** | ✓ | ✓ (if graph is finite) |
| **Cycle Detection** | Possible | Easier |
| **Use Cases** | Shortest path, level order | Topological sort, strongly connected components |

---

## 9.5 Applications of Graph Traversals

### 1. Check if Graph is Connected
```cpp
bool isConnected() {
    vector<bool> visited(V, false);
    DFS(0, visited);
    
    for (bool v : visited) {
        if (!v) return false;
    }
    return true;
}
```

### 2. Count Connected Components
```cpp
int countConnectedComponents() {
    vector<bool> visited(V, false);
    int count = 0;
    
    for (int i = 0; i < V; i++) {
        if (!visited[i]) {
            DFS(i, visited);
            count++;
        }
    }
    
    return count;
}
```

### 3. Detect Cycle in Undirected Graph (using DFS)
```cpp
bool hasCycleDFS(int vertex, vector<bool>& visited, int parent) {
    visited[vertex] = true;
    
    for (int neighbor : adjList[vertex]) {
        if (!visited[neighbor]) {
            if (hasCycleDFS(neighbor, visited, vertex))
                return true;
        }
        // If neighbor is visited and not parent, cycle exists
        else if (neighbor != parent) {
            return true;
        }
    }
    
    return false;
}

bool hasCycle() {
    vector<bool> visited(V, false);
    
    for (int i = 0; i < V; i++) {
        if (!visited[i]) {
            if (hasCycleDFS(i, visited, -1))
                return true;
        }
    }
    
    return false;
}
```

### 4. Detect Cycle in Directed Graph
```cpp
bool hasCycleDirected(int vertex, vector<int>& color) {
    // color: 0 = white (unvisited), 1 = gray (in progress), 2 = black (done)
    color[vertex] = 1;  // Mark as in progress
    
    for (int neighbor : adjList[vertex]) {
        if (color[neighbor] == 1) {
            // Back edge found → cycle
            return true;
        }
        if (color[neighbor] == 0) {
            if (hasCycleDirected(neighbor, color))
                return true;
        }
    }
    
    color[vertex] = 2;  // Mark as done
    return false;
}

bool hasCycle() {
    vector<int> color(V, 0);
    
    for (int i = 0; i < V; i++) {
        if (color[i] == 0) {
            if (hasCycleDirected(i, color))
                return true;
        }
    }
    
    return false;
}
```

### 5. Topological Sort (for DAG)
```cpp
void topologicalSortUtil(int vertex, vector<bool>& visited, stack<int>& s) {
    visited[vertex] = true;
    
    for (int neighbor : adjList[vertex]) {
        if (!visited[neighbor])
            topologicalSortUtil(neighbor, visited, s);
    }
    
    s.push(vertex);  // Push after visiting all descendants
}

void topologicalSort() {
    vector<bool> visited(V, false);
    stack<int> s;
    
    for (int i = 0; i < V; i++) {
        if (!visited[i])
            topologicalSortUtil(i, visited, s);
    }
    
    while (!s.empty()) {
        cout << s.top() << " ";
        s.pop();
    }
}
```

**Example:**
```
DAG:    0 → 1 → 3
        ↓   ↓
        2 → 4

Topological Order: 0 2 1 4 3 (or other valid orderings)
```

---

## 📝 MCQs for Module 9

### Q1. Time complexity of BFS and DFS in adjacency list representation:
A. O(V)  
B. O(E)  
C. O(V + E)  
D. O(V × E)

> **Answer: C**  
> **Explanation:** Both BFS and DFS visit each vertex once and explore each edge once, giving O(V + E).

### Q2. Which traversal uses a queue?
A. DFS  
B. BFS  
C. Both  
D. Neither

> **Answer: B**  
> **Explanation:** BFS uses queue (FIFO) to process vertices level by level.

### Q3. Best representation for a dense graph:
A. Adjacency list  
B. Edge list  
C. Adjacency matrix  
D. All are equally good

> **Answer: C**  
> **Explanation:** For dense graphs (E ≈ V²), adjacency matrix is space-efficient and provides O(1) edge lookup.

### Q4. Topological sorting is possible only on:
A. Undirected graphs  
B. Directed Acyclic Graphs  
C. Connected graphs  
D. Complete graphs

> **Answer: B**  
> **Explanation:** Topological sort is only defined for DAGs (directed graphs with no cycles).

### Q5. Space complexity of adjacency list representation:
A. O(V)  
B. O(E)  
C. O(V + E)  
D. O(V²)

> **Answer: C**  
> **Explanation:** Need O(V) for vertex array and O(E) for storing all edges.

### Q6. BFS can find shortest path in:
A. Unweighted graphs  
B. Weighted graphs  
C. Both  
D. Neither

> **Answer: A**  
> **Explanation:** BFS finds shortest path (minimum edges) only in unweighted graphs. For weighted, use Dijkstra.

### Q7. In directed graph, if DFS finds a back edge, the graph has:
A. Multiple components  
B. A cycle  
C. No path  
D. Euler circuit

> **Answer: B**  
> **Explanation:** Back edge in DFS indicates a cycle in the graph.

### Q8. Maximum number of edges in an undirected graph with V vertices:
A. V  
B. V²  
C. V(V-1)/2  
D. V(V-1)

> **Answer: C**  
> **Explanation:** Complete undirected graph has V vertices choose 2 = V(V-1)/2 edges.

---


# 🛤️ MODULE 10: GRAPH ALGORITHMS (SHORTEST PATH & MST)

## 10.1 Shortest Path Algorithms

### Problem Statement
Given a weighted graph and a source vertex, find the shortest path from source to all other vertices.

---

## 10.2 Dijkstra's Algorithm (Single-Source Shortest Path)

### Prerequisites
* **Works on:** Weighted graphs with **non-negative** edge weights
* **Fails on:** Negative edge weights

### Algorithm
**Greedy approach:** Always pick the minimum distance unvisited vertex.

```cpp
vector<int> dijkstra(int source, vector<vector<pair<int, int>>>& graph, int V) {
    // graph[u] = {(v, weight), ...}
    vector<int> dist(V, INT_MAX);
    dist[source] = 0;
    
    // Min heap: {distance, vertex}
    priority_queue<pair<int, int>, 
                   vector<pair<int, int>>,
                   greater<pair<int, int>>> pq;
    pq.push({0, source});
    
    while (!pq.empty()) {
        int u = pq.top().second;
        int d = pq.top().first;
        pq.pop();
        
        // Skip if we already found a better path
        if (d > dist[u]) continue;
        
        // Check all neighbors
        for (auto [v, weight] : graph[u]) {
            if (dist[u] + weight < dist[v]) {
                dist[v] = dist[u] + weight;
                pq.push({dist[v], v});
            }
        }
    }
    
    return dist;
}
```

### Example
```
Graph:      0 --4-- 1
            |       |
            2       3
            |       |
            2 --1-- 3

Source: 0

Initial: dist = [0, ∞, ∞, ∞]

Step 1: Process 0
  Update dist[1] = 4, dist[2] = 2
  dist = [0, 4, 2, ∞]

Step 2: Process 2 (minimum unvisited)
  Update dist[3] = 3
  dist = [0, 4, 2, 3]

Step 3: Process 3
  Update dist[1] = min(4, 3+3) = 4
  dist = [0, 4, 2, 3]

Step 4: Process 1
  No updates

Final shortest distances from 0: [0, 4, 2, 3]
```

### Time Complexity
| Implementation | Time Complexity |
|----------------|-----------------|
| **Array** | O(V²) |
| **Binary Heap** | O((V + E) log V) |
| **Fibonacci Heap** | O(E + V log V) |

### Space Complexity
* O(V) for distance array
* O(V) for priority queue

### With Path Reconstruction
```cpp
void dijkstraWithPath(int source, int destination) {
    vector<int> dist(V, INT_MAX);
    vector<int> parent(V, -1);
    dist[source] = 0;
    
    priority_queue<pair<int, int>, 
                   vector<pair<int, int>>,
                   greater<pair<int, int>>> pq;
    pq.push({0, source});
    
    while (!pq.empty()) {
        int u = pq.top().second;
        int d = pq.top().first;
        pq.pop();
        
        if (d > dist[u]) continue;
        
        for (auto [v, weight] : adjList[u]) {
            if (dist[u] + weight < dist[v]) {
                dist[v] = dist[u] + weight;
                parent[v] = u;
                pq.push({dist[v], v});
            }
        }
    }
    
    // Reconstruct path
    vector<int> path;
    int current = destination;
    while (current != -1) {
        path.push_back(current);
        current = parent[current];
    }
    reverse(path.begin(), path.end());
    
    cout << "Distance: " << dist[destination] << endl;
    cout << "Path: ";
    for (int v : path)
        cout << v << " ";
}
```

---

## 10.3 Bellman-Ford Algorithm

### Prerequisites
* **Works on:** Weighted graphs with negative edge weights
* **Detects:** Negative weight cycles
* **Slower than Dijkstra** but more versatile

### Algorithm
**Dynamic Programming:** Relax all edges V-1 times.

```cpp
bool bellmanFord(int source, vector<tuple<int, int, int>>& edges, int V) {
    // edges = {(u, v, weight)}
    vector<int> dist(V, INT_MAX);
    dist[source] = 0;
    
    // Relax all edges V-1 times
    for (int i = 0; i < V - 1; i++) {
        for (auto [u, v, weight] : edges) {
            if (dist[u] != INT_MAX && dist[u] + weight < dist[v]) {
                dist[v] = dist[u] + weight;
            }
        }
    }
    
    // Check for negative weight cycles
    for (auto [u, v, weight] : edges) {
        if (dist[u] != INT_MAX && dist[u] + weight < dist[v]) {
            cout << "Negative weight cycle detected" << endl;
            return false;
        }
    }
    
    // Print distances
    cout << "Vertex\tDistance from Source" << endl;
    for (int i = 0; i < V; i++)
        cout << i << "\t" << dist[i] << endl;
    
    return true;
}
```

### Example
```
Graph with negative weight:
    0 --4-- 1
    |       |
   -2       3
    |       |
    2 ---1- 3

Edges: {(0,1,4), (0,2,-2), (1,3,3), (2,3,1)}

Iteration 1:
  dist = [0, 4, -2, ∞]

Iteration 2:
  dist = [0, 4, -2, -1]

Iteration 3:
  No changes

Check for negative cycle: None found
Final: [0, 4, -2, -1]
```

### Time Complexity
* **Time:** O(V × E)
* **Space:** O(V)

### When to Use?
* **Dijkstra:** No negative weights, need faster algorithm
* **Bellman-Ford:** Has negative weights, need to detect negative cycles

---

## 10.4 Floyd-Warshall Algorithm (All-Pairs Shortest Path)

### Prerequisites
* **Finds:** Shortest paths between **all pairs** of vertices
* **Works on:** Negative weights (but no negative cycles)

### Algorithm
**Dynamic Programming:** Consider all intermediate vertices.

```cpp
void floydWarshall(vector<vector<int>>& graph, int V) {
    vector<vector<int>> dist = graph;
    
    // Initialize: dist[i][i] = 0
    for (int i = 0; i < V; i++)
        dist[i][i] = 0;
    
    // For each intermediate vertex k
    for (int k = 0; k < V; k++) {
        // For each source vertex i
        for (int i = 0; i < V; i++) {
            // For each destination vertex j
            for (int j = 0; j < V; j++) {
                if (dist[i][k] != INT_MAX && 
                    dist[k][j] != INT_MAX &&
                    dist[i][k] + dist[k][j] < dist[i][j]) {
                    dist[i][j] = dist[i][k] + dist[k][j];
                }
            }
        }
    }
    
    // Check for negative cycle
    for (int i = 0; i < V; i++) {
        if (dist[i][i] < 0) {
            cout << "Negative weight cycle detected" << endl;
            return;
        }
    }
    
    // Print distance matrix
    cout << "Shortest distances between every pair:" << endl;
    for (int i = 0; i < V; i++) {
        for (int j = 0; j < V; j++) {
            if (dist[i][j] == INT_MAX)
                cout << "INF ";
            else
                cout << dist[i][j] << " ";
        }
        cout << endl;
    }
}
```

### Example
```
Graph:      0 --5-- 1
            |       |
            10      3
            |       |
            2 --1-- 3

Initial Matrix:
    0   1   2   3
0 [ 0   5  10  INF]
1 [ INF 0  INF  3 ]
2 [INF INF  0   1 ]
3 [INF INF INF  0 ]

After k=0:
    0   1   2   3
0 [ 0   5  10  INF]
1 [INF  0  INF  3 ]
2 [INF INF  0   1 ]
3 [INF INF INF  0 ]

After k=1:
    0   1   2   3
0 [ 0   5  10  8  ]
1 [INF  0  INF  3 ]
2 [INF INF  0   1 ]
3 [INF INF INF  0 ]

After k=2:
    0   1   2   3
0 [ 0   5  10  8  ]
1 [INF  0  INF  3 ]
2 [INF INF  0   1 ]
3 [INF INF INF  0 ]

After k=3:
    0   1   2   3
0 [ 0   5  10  8  ]
1 [INF  0  INF  3 ]
2 [INF INF  0   1 ]
3 [INF INF INF  0 ]
```

### Time Complexity
* **Time:** O(V³)
* **Space:** O(V²)

### Use Cases
* Dense graphs where all-pairs needed
* Transitive closure
* Network diameter calculation

---

## 10.5 Minimum Spanning Tree (MST)

### Definition
* **Spanning Tree:** Subgraph that is a tree and connects all vertices
* **MST:** Spanning tree with minimum total edge weight

```
Graph:          MST:
  A --4-- B       A --4-- B
  |  \    |       |       |
  3   2   1       3       1
  |    \  |       |       |
  C --5-- D       C       D
  
Total weight: 8 (minimum possible)
```

### Properties
* **Edges in MST:** V - 1 (where V = number of vertices)
* **No cycles**
* **Connects all vertices**
* **May not be unique** (multiple MSTs can exist)

---

## 10.6 Prim's Algorithm

### Algorithm
**Greedy:** Start from any vertex, repeatedly add minimum weight edge that connects tree to a new vertex.

```cpp
int primMST(vector<vector<pair<int, int>>>& graph, int V) {
    // graph[u] = {(v, weight), ...}
    vector<int> key(V, INT_MAX);     // Minimum weight to include vertex
    vector<bool> inMST(V, false);    // Vertex included in MST
    vector<int> parent(V, -1);       // Store MST edges
    
    // Min heap: {weight, vertex}
    priority_queue<pair<int, int>,
                   vector<pair<int, int>>,
                   greater<pair<int, int>>> pq;
    
    // Start from vertex 0
    key[0] = 0;
    pq.push({0, 0});
    
    int mstWeight = 0;
    
    while (!pq.empty()) {
        int u = pq.top().second;
        int weight = pq.top().first;
        pq.pop();
        
        if (inMST[u]) continue;
        
        inMST[u] = true;
        mstWeight += weight;
        
        // Check all adjacent vertices
        for (auto [v, w] : graph[u]) {
            if (!inMST[v] && w < key[v]) {
                key[v] = w;
                parent[v] = u;
                pq.push({w, v});
            }
        }
    }
    
    // Print MST edges
    cout << "MST Edges:" << endl;
    for (int i = 1; i < V; i++) {
        cout << parent[i] << " - " << i << " : " << key[i] << endl;
    }
    
    return mstWeight;
}
```

### Example
```
Graph:
    A --2-- B
    |  \    |
    3   6   1
    |    \  |
    C --5-- D

Step 1: Start with A
  Add A to MST
  Update key: B=2, C=3, D=6

Step 2: Process B (minimum key)
  Add edge A-B (weight 2)
  Update key: D=1

Step 3: Process D (minimum key)
  Add edge B-D (weight 1)

Step 4: Process C (minimum key)
  Add edge A-C (weight 3)

MST edges: A-B (2), B-D (1), A-C (3)
Total weight: 6
```

### Time Complexity
| Implementation | Time Complexity |
|----------------|-----------------|
| **Adjacency Matrix** | O(V²) |
| **Binary Heap** | O((V + E) log V) |
| **Fibonacci Heap** | O(E + V log V) |

---

## 10.7 Kruskal's Algorithm

### Algorithm
**Greedy:** Sort all edges, add edges one by one if they don't form a cycle.

```cpp
struct Edge {
    int u, v, weight;
    bool operator<(const Edge& other) const {
        return weight < other.weight;
    }
};

class UnionFind {
private:
    vector<int> parent, rank;
    
public:
    UnionFind(int n) {
        parent.resize(n);
        rank.resize(n, 0);
        for (int i = 0; i < n; i++)
            parent[i] = i;
    }
    
    int find(int x) {
        if (parent[x] != x)
            parent[x] = find(parent[x]);  // Path compression
        return parent[x];
    }
    
    bool unite(int x, int y) {
        int px = find(x);
        int py = find(y);
        
        if (px == py) return false;  // Already in same set
        
        // Union by rank
        if (rank[px] < rank[py]) {
            parent[px] = py;
        } else if (rank[px] > rank[py]) {
            parent[py] = px;
        } else {
            parent[py] = px;
            rank[px]++;
        }
        return true;
    }
};

int kruskalMST(vector<Edge>& edges, int V) {
    // Sort edges by weight
    sort(edges.begin(), edges.end());
    
    UnionFind uf(V);
    int mstWeight = 0;
    vector<Edge> mstEdges;
    
    for (Edge& e : edges) {
        // If adding edge doesn't create cycle
        if (uf.unite(e.u, e.v)) {
            mstEdges.push_back(e);
            mstWeight += e.weight;
            
            // Stop if MST is complete
            if (mstEdges.size() == V - 1)
                break;
        }
    }
    
    // Print MST
    cout << "MST Edges:" << endl;
    for (Edge& e : mstEdges) {
        cout << e.u << " - " << e.v << " : " << e.weight << endl;
    }
    
    return mstWeight;
}
```

### Example
```
Edges (sorted by weight):
(B,D,1), (A,B,2), (A,C,3), (C,D,5), (A,D,6)

Step 1: Add B-D (1), no cycle
Step 2: Add A-B (2), no cycle
Step 3: Add A-C (3), no cycle
Step 4: Skip C-D (5), would create cycle
Step 5: Skip A-D (6), would create cycle

MST: B-D (1), A-B (2), A-C (3)
Total: 6
```

### Time Complexity
* **Time:** O(E log E) or O(E log V)
  - Sorting edges: O(E log E)
  - Union-Find operations: O(E α(V)) where α is inverse Ackermann
* **Space:** O(V + E)

---

## 10.8 Prim vs Kruskal

| Feature | Prim's | Kruskal's |
|---------|--------|-----------|
| **Approach** | Grow tree from single vertex | Add edges in increasing weight order |
| **Data Structure** | Priority queue | Sorting + Union-Find |
| **Time (dense)** | O(V²) with array | O(E log E) |
| **Time (sparse)** | O((V+E) log V) with heap | O(E log E) |
| **Best for** | Dense graphs | Sparse graphs |
| **Edge list needed** | No | Yes |
| **Implementation** | Slightly easier | Requires Union-Find |

---

## 10.9 Applications

### Dijkstra's Algorithm
1. **GPS navigation** - shortest route
2. **Network routing** - OSPF protocol
3. **Social networks** - degrees of separation

### Bellman-Ford
1. **Routing with cost changes** - BGP protocol
2. **Arbitrage detection** - currency exchange (negative cycles)

### Floyd-Warshall
1. **All-pairs shortest paths** - routing tables
2. **Transitive closure** - reachability matrix
3. **Graph diameter** calculation

### MST Applications
1. **Network design** - minimize cable length
2. **Cluster analysis** - single linkage clustering
3. **Image segmentation**
4. **Approximation algorithms** - TSP, Steiner tree

---

## 📝 MCQs for Module 10

### Q1. Dijkstra's algorithm fails when graph has:
A. Cycles  
B. Negative edge weights  
C. Multiple edges  
D. Disconnected components

> **Answer: B**  
> **Explanation:** Dijkstra assumes non-negative weights. For negative weights, use Bellman-Ford.

### Q2. Time complexity of Floyd-Warshall algorithm:
A. O(V²)  
B. O(V³)  
C. O(V × E)  
D. O(E log V)

> **Answer: B**  
> **Explanation:** Floyd-Warshall uses three nested loops over all vertices, giving O(V³).

### Q3. Number of edges in MST of graph with V vertices:
A. V  
B. V - 1  
C. V + 1  
D. 2V

> **Answer: B**  
> **Explanation:** MST is a tree connecting all vertices, so it has exactly V - 1 edges.

### Q4. Kruskal's algorithm uses which data structure?
A. Queue  
B. Stack  
C. Union-Find  
D. Heap only

> **Answer: C**  
> **Explanation:** Kruskal uses Union-Find (Disjoint Set) to detect cycles when adding edges.

### Q5. Which algorithm finds shortest path from single source?
A. Prim's  
B. Kruskal's  
C. Dijkstra's  
D. Floyd-Warshall

> **Answer: C**  
> **Explanation:** Dijkstra finds shortest paths from single source to all vertices.

### Q6. Bellman-Ford can detect:
A. Bipartite graphs  
B. Negative weight cycles  
C. Euler circuits  
D. Hamiltonian paths

> **Answer: B**  
> **Explanation:** Bellman-Ford relaxes edges V-1 times; any further relaxation indicates negative cycle.

### Q7. Prim's algorithm is best for:
A. Sparse graphs  
B. Dense graphs  
C. Directed graphs only  
D. Unweighted graphs

> **Answer: B**  
> **Explanation:** Prim's O(V²) implementation is efficient for dense graphs.

### Q8. Floyd-Warshall finds shortest paths between:
A. Single source to all vertices  
B. All pairs of vertices  
C. Source to destination  
D. Adjacent vertices only

> **Answer: B**  
> **Explanation:** Floyd-Warshall computes shortest paths between all pairs of vertices.

---


# 🔍 MODULE 11: SEARCHING ALGORITHMS

## 11.1 Linear Search

### Algorithm
Search for element by checking each element sequentially.

```cpp
int linearSearch(int arr[], int n, int key) {
    for (int i = 0; i < n; i++) {
        if (arr[i] == key)
            return i;  // Return index
    }
    return -1;  // Not found
}
```

### Complexity
* **Time:**
  - Best case: O(1) - element at first position
  - Average case: O(n/2) = O(n)
  - Worst case: O(n) - element at last position or not present
* **Space:** O(1)

### Characteristics
* **Works on:** Sorted and unsorted arrays
* **Stable:** Yes
* **In-place:** Yes
* **Use when:** Small arrays, unsorted data

---

## 11.2 Binary Search

### Prerequisites
* **Array must be sorted**

### Algorithm
Repeatedly divide search space in half.

```cpp
// Iterative
int binarySearch(int arr[], int n, int key) {
    int left = 0, right = n - 1;
    
    while (left <= right) {
        int mid = left + (right - left) / 2;  // Avoid overflow
        
        if (arr[mid] == key)
            return mid;
        else if (arr[mid] < key)
            left = mid + 1;
        else
            right = mid - 1;
    }
    
    return -1;  // Not found
}

// Recursive
int binarySearchRecursive(int arr[], int left, int right, int key) {
    if (left > right)
        return -1;
    
    int mid = left + (right - left) / 2;
    
    if (arr[mid] == key)
        return mid;
    else if (arr[mid] < key)
        return binarySearchRecursive(arr, mid + 1, right, key);
    else
        return binarySearchRecursive(arr, left, mid - 1, key);
}
```

### Example
```
arr = [2, 5, 8, 12, 16, 23, 38, 45, 56, 67, 78]
key = 23

Iteration 1: left=0, right=10, mid=5
  arr[5] = 23, found at index 5

key = 45

Iteration 1: left=0, right=10, mid=5
  arr[5] = 23 < 45, search right half
  left=6, right=10

Iteration 2: left=6, right=10, mid=8
  arr[8] = 56 > 45, search left half
  left=6, right=7

Iteration 3: left=6, right=7, mid=6
  arr[6] = 38 < 45, search right half
  left=7, right=7

Iteration 4: left=7, right=7, mid=7
  arr[7] = 45, found at index 7
```

### Complexity
* **Time:**
  - Best case: O(1) - element at middle
  - Average/Worst case: O(log n)
* **Space:**
  - Iterative: O(1)
  - Recursive: O(log n) - recursion stack

### Proof of O(log n)
```
After 1st comparison: n/2 elements remain
After 2nd comparison: n/4 elements remain
After kth comparison: n/2^k elements remain

When n/2^k = 1:
  2^k = n
  k = log₂ n
```

---

## 11.3 Binary Search Variants

### 1. Find First Occurrence
```cpp
int findFirst(int arr[], int n, int key) {
    int left = 0, right = n - 1;
    int result = -1;
    
    while (left <= right) {
        int mid = left + (right - left) / 2;
        
        if (arr[mid] == key) {
            result = mid;
            right = mid - 1;  // Continue searching left
        } else if (arr[mid] < key) {
            left = mid + 1;
        } else {
            right = mid - 1;
        }
    }
    
    return result;
}
```

### 2. Find Last Occurrence
```cpp
int findLast(int arr[], int n, int key) {
    int left = 0, right = n - 1;
    int result = -1;
    
    while (left <= right) {
        int mid = left + (right - left) / 2;
        
        if (arr[mid] == key) {
            result = mid;
            left = mid + 1;  // Continue searching right
        } else if (arr[mid] < key) {
            left = mid + 1;
        } else {
            right = mid - 1;
        }
    }
    
    return result;
}
```

### 3. Count Occurrences
```cpp
int countOccurrences(int arr[], int n, int key) {
    int first = findFirst(arr, n, key);
    if (first == -1) return 0;
    
    int last = findLast(arr, n, key);
    return last - first + 1;
}
```

### 4. Find Floor (Largest element ≤ key)
```cpp
int findFloor(int arr[], int n, int key) {
    int left = 0, right = n - 1;
    int result = -1;
    
    while (left <= right) {
        int mid = left + (right - left) / 2;
        
        if (arr[mid] <= key) {
            result = mid;
            left = mid + 1;
        } else {
            right = mid - 1;
        }
    }
    
    return result;
}
```

### 5. Find Ceiling (Smallest element ≥ key)
```cpp
int findCeiling(int arr[], int n, int key) {
    int left = 0, right = n - 1;
    int result = -1;
    
    while (left <= right) {
        int mid = left + (right - left) / 2;
        
        if (arr[mid] >= key) {
            result = mid;
            right = mid - 1;
        } else {
            left = mid + 1;
        }
    }
    
    return result;
}
```

---

## 11.4 Jump Search

### Algorithm
Jump ahead by fixed steps, then do linear search in block.

```cpp
int jumpSearch(int arr[], int n, int key) {
    int step = sqrt(n);  // Optimal jump size
    int prev = 0;
    
    // Jump to find block
    while (arr[min(step, n) - 1] < key) {
        prev = step;
        step += sqrt(n);
        if (prev >= n)
            return -1;
    }
    
    // Linear search in block
    while (arr[prev] < key) {
        prev++;
        if (prev == min(step, n))
            return -1;
    }
    
    if (arr[prev] == key)
        return prev;
    
    return -1;
}
```

### Complexity
* **Time:** O(√n)
* **Space:** O(1)
* **Prerequisite:** Sorted array

### Optimal Jump Size
* Jump size = √n minimizes jumps + linear search
* **Total operations:** (n/√n) jumps + √n comparisons = 2√n = O(√n)

---

## 11.5 Interpolation Search

### Algorithm
Estimate position based on value (like looking up in phone book).

```cpp
int interpolationSearch(int arr[], int n, int key) {
    int left = 0, right = n - 1;
    
    while (left <= right && key >= arr[left] && key <= arr[right]) {
        if (left == right) {
            if (arr[left] == key) return left;
            return -1;
        }
        
        // Estimate position
        int pos = left + ((key - arr[left]) * (right - left)) / 
                         (arr[right] - arr[left]);
        
        if (arr[pos] == key)
            return pos;
        else if (arr[pos] < key)
            left = pos + 1;
        else
            right = pos - 1;
    }
    
    return -1;
}
```

### Complexity
* **Time:**
  - Best/Average (uniform distribution): O(log log n)
  - Worst (non-uniform distribution): O(n)
* **Space:** O(1)
* **Prerequisites:** Sorted array, uniformly distributed values

### When to Use?
* **Best for:** Large sorted arrays with uniform distribution
* **Example:** Searching in dictionary, phone book

---

## 11.6 Exponential Search

### Algorithm
Find range by exponential jumps, then binary search.

```cpp
int exponentialSearch(int arr[], int n, int key) {
    if (arr[0] == key)
        return 0;
    
    // Find range for binary search
    int i = 1;
    while (i < n && arr[i] <= key)
        i *= 2;
    
    // Binary search in range [i/2, min(i, n-1)]
    return binarySearch(arr, i/2, min(i, n-1), key);
}

int binarySearch(int arr[], int left, int right, int key) {
    while (left <= right) {
        int mid = left + (right - left) / 2;
        
        if (arr[mid] == key)
            return mid;
        else if (arr[mid] < key)
            left = mid + 1;
        else
            right = mid - 1;
    }
    return -1;
}
```

### Complexity
* **Time:** O(log n)
* **Space:** O(1)

### Advantages
* **Better than binary search** when element is near beginning
* **Useful for** unbounded/infinite arrays

---

## 11.7 Ternary Search

### Algorithm
Divide array into three parts.

```cpp
int ternarySearch(int arr[], int left, int right, int key) {
    if (left > right)
        return -1;
    
    int mid1 = left + (right - left) / 3;
    int mid2 = right - (right - left) / 3;
    
    if (arr[mid1] == key)
        return mid1;
    if (arr[mid2] == key)
        return mid2;
    
    if (key < arr[mid1])
        return ternarySearch(arr, left, mid1 - 1, key);
    else if (key > arr[mid2])
        return ternarySearch(arr, mid2 + 1, right, key);
    else
        return ternarySearch(arr, mid1 + 1, mid2 - 1, key);
}
```

### Complexity
* **Time:** O(log₃ n) ≈ O(log n)
* **Space:** O(log n) - recursion

### Binary vs Ternary Search
* **Binary:** One comparison per iteration, log₂ n iterations
* **Ternary:** Two comparisons per iteration, log₃ n iterations
* **Total comparisons:**
  - Binary: log₂ n
  - Ternary: 2 × log₃ n ≈ 1.26 × log₂ n
* **Binary search is more efficient!**

---

## 11.8 Special Search Problems

### 1. Search in Rotated Sorted Array
```cpp
int searchRotated(int arr[], int n, int key) {
    int left = 0, right = n - 1;
    
    while (left <= right) {
        int mid = left + (right - left) / 2;
        
        if (arr[mid] == key)
            return mid;
        
        // Left half is sorted
        if (arr[left] <= arr[mid]) {
            if (key >= arr[left] && key < arr[mid])
                right = mid - 1;
            else
                left = mid + 1;
        }
        // Right half is sorted
        else {
            if (key > arr[mid] && key <= arr[right])
                left = mid + 1;
            else
                right = mid - 1;
        }
    }
    
    return -1;
}
```
**Example:** `[4, 5, 6, 7, 0, 1, 2]` - rotated at index 4

### 2. Find Peak Element
```cpp
int findPeak(int arr[], int n) {
    int left = 0, right = n - 1;
    
    while (left < right) {
        int mid = left + (right - left) / 2;
        
        if (arr[mid] < arr[mid + 1])
            left = mid + 1;  // Peak is on right
        else
            right = mid;      // Peak is on left or at mid
    }
    
    return left;
}
```

### 3. Search in 2D Sorted Matrix
```cpp
bool searchMatrix(vector<vector<int>>& matrix, int target) {
    if (matrix.empty()) return false;
    
    int m = matrix.size(), n = matrix[0].size();
    int left = 0, right = m * n - 1;
    
    while (left <= right) {
        int mid = left + (right - left) / 2;
        int midValue = matrix[mid / n][mid % n];
        
        if (midValue == target)
            return true;
        else if (midValue < target)
            left = mid + 1;
        else
            right = mid - 1;
    }
    
    return false;
}
```
**Time:** O(log(m×n))

### 4. Find Minimum in Rotated Sorted Array
```cpp
int findMin(int arr[], int n) {
    int left = 0, right = n - 1;
    
    while (left < right) {
        int mid = left + (right - left) / 2;
        
        if (arr[mid] > arr[right])
            left = mid + 1;  // Min is in right half
        else
            right = mid;      // Min is in left half or at mid
    }
    
    return arr[left];
}
```

---

## 11.9 Comparison of Search Algorithms

| Algorithm | Time (Best) | Time (Avg) | Time (Worst) | Space | Prerequisites |
|-----------|-------------|------------|--------------|-------|---------------|
| **Linear Search** | O(1) | O(n) | O(n) | O(1) | None |
| **Binary Search** | O(1) | O(log n) | O(log n) | O(1) | Sorted |
| **Jump Search** | O(1) | O(√n) | O(√n) | O(1) | Sorted |
| **Interpolation** | O(1) | O(log log n) | O(n) | O(1) | Sorted + Uniform |
| **Exponential** | O(1) | O(log n) | O(log n) | O(1) | Sorted |
| **Ternary** | O(1) | O(log n) | O(log n) | O(log n) | Sorted |

---

## 11.10 When to Use Which Search?

### Linear Search
* **Small arrays** (n < 100)
* **Unsorted data**
* **Single search operation**

### Binary Search
* **Sorted array**
* **Multiple searches** (amortize sorting cost)
* **General purpose** - most common choice

### Jump Search
* **Large sorted array**
* **Better cache performance** than binary search
* **Bounded jumps** useful in some systems

### Interpolation Search
* **Uniformly distributed sorted data**
* **Large datasets** (phone books, dictionaries)
* **Position can be estimated**

### Exponential Search
* **Unbounded/infinite arrays**
* **Element likely near beginning**
* **Useful in streaming data**

---

## 📝 MCQs for Module 11

### Q1. Time complexity of binary search:
A. O(n)  
B. O(log n)  
C. O(n log n)  
D. O(√n)

> **Answer: B**  
> **Explanation:** Binary search divides search space in half each iteration, taking log₂ n steps.

### Q2. Which search algorithm does NOT require sorted array?
A. Binary Search  
B. Jump Search  
C. Linear Search  
D. Interpolation Search

> **Answer: C**  
> **Explanation:** Linear search checks each element sequentially and works on unsorted data.

### Q3. Optimal jump size in jump search for array of size n:
A. n/2  
B. √n  
C. log n  
D. n

> **Answer: B**  
> **Explanation:** √n minimizes total comparisons: (n/√n) jumps + √n linear search = 2√n.

### Q4. Best case time complexity of interpolation search:
A. O(1)  
B. O(log n)  
C. O(log log n)  
D. O(n)

> **Answer: C**  
> **Explanation:** With uniform distribution, interpolation search can narrow down position very quickly.

### Q5. For searching in rotated sorted array, time complexity is:
A. O(n)  
B. O(log n)  
C. O(√n)  
D. O(n log n)

> **Answer: B**  
> **Explanation:** Modified binary search identifies which half is sorted and searches accordingly.

### Q6. Which is faster: binary search or ternary search?
A. Binary search  
B. Ternary search  
C. Both same  
D. Depends on data

> **Answer: A**  
> **Explanation:** Binary search makes 1 comparison per iteration, ternary makes 2. Binary is more efficient overall.

### Q7. Space complexity of recursive binary search:
A. O(1)  
B. O(log n)  
C. O(n)  
D. O(n log n)

> **Answer: B**  
> **Explanation:** Recursion stack depth equals number of recursive calls = O(log n).

### Q8. Exponential search is particularly useful for:
A. Small arrays  
B. Unsorted arrays  
C. Unbounded/infinite arrays  
D. Duplicate elements

> **Answer: C**  
> **Explanation:** Exponential search finds range exponentially then uses binary search, ideal for unbounded arrays.

---


# 🔀 MODULE 12: SORTING ALGORITHMS (DETAILED ANALYSIS)

## 12.1 Classification of Sorting Algorithms

### Based on Memory Usage
* **Internal Sorting:** All data fits in RAM (most algorithms)
* **External Sorting:** Data too large, uses disk (merge sort variant)

### Based on Stability
* **Stable:** Preserves relative order of equal elements
  - Examples: Merge Sort, Insertion Sort, Bubble Sort
* **Unstable:** May change relative order of equal elements
  - Examples: Quick Sort, Heap Sort, Selection Sort

### Based on Adaptivity
* **Adaptive:** Performance improves for partially sorted data
  - Examples: Insertion Sort, Bubble Sort
* **Non-adaptive:** Same performance regardless of input
  - Examples: Selection Sort, Heap Sort

---

## 12.2 Bubble Sort

### Algorithm
```cpp
void bubbleSort(int arr[], int n) {
    for (int i = 0; i < n - 1; i++) {
        bool swapped = false;
        
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                swap(arr[j], arr[j + 1]);
                swapped = true;
            }
        }
        
        // Optimization: if no swap, array is sorted
        if (!swapped) break;
    }
}
```

### Complexity
* **Time:**
  - Best: O(n) - already sorted
  - Average: O(n²)
  - Worst: O(n²)
* **Space:** O(1)
* **Stable:** Yes
* **Adaptive:** Yes (with optimization)

---

## 12.3 Selection Sort

### Algorithm
```cpp
void selectionSort(int arr[], int n) {
    for (int i = 0; i < n - 1; i++) {
        int minIdx = i;
        
        // Find minimum in unsorted part
        for (int j = i + 1; j < n; j++) {
            if (arr[j] < arr[minIdx])
                minIdx = j;
        }
        
        swap(arr[i], arr[minIdx]);
    }
}
```

### Complexity
* **Time:** O(n²) in all cases
* **Space:** O(1)
* **Stable:** No
* **Adaptive:** No

### Key Points
* Minimum number of swaps: n-1
* Good when write operations are costly

---

## 12.4 Insertion Sort

### Algorithm
```cpp
void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;
        
        // Shift elements greater than key
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j--;
        }
        
        arr[j + 1] = key;
    }
}
```

### Complexity
* **Time:**
  - Best: O(n) - already sorted
  - Average: O(n²)
  - Worst: O(n²) - reverse sorted
* **Space:** O(1)
* **Stable:** Yes
* **Adaptive:** Yes

### Use Cases
* Small arrays (< 50 elements)
* Nearly sorted arrays
* Online algorithm (sorts as it receives data)

---

## 12.5 Merge Sort

### Algorithm
```cpp
void merge(int arr[], int left, int mid, int right) {
    int n1 = mid - left + 1;
    int n2 = right - mid;
    
    int L[n1], R[n2];
    
    for (int i = 0; i < n1; i++)
        L[i] = arr[left + i];
    for (int j = 0; j < n2; j++)
        R[j] = arr[mid + 1 + j];
    
    int i = 0, j = 0, k = left;
    
    while (i < n1 && j < n2) {
        if (L[i] <= R[j])
            arr[k++] = L[i++];
        else
            arr[k++] = R[j++];
    }
    
    while (i < n1)
        arr[k++] = L[i++];
    while (j < n2)
        arr[k++] = R[j++];
}

void mergeSort(int arr[], int left, int right) {
    if (left < right) {
        int mid = left + (right - left) / 2;
        
        mergeSort(arr, left, mid);
        mergeSort(arr, mid + 1, right);
        merge(arr, left, mid, right);
    }
}
```

### Complexity
* **Time:** O(n log n) in all cases
* **Space:** O(n) - temporary arrays
* **Stable:** Yes
* **Adaptive:** No

### Recurrence Relation
```
T(n) = 2T(n/2) + O(n)
Using Master Theorem: Case 2
T(n) = O(n log n)
```

---

## 12.6 Quick Sort

### Algorithm
```cpp
int partition(int arr[], int low, int high) {
    int pivot = arr[high];
    int i = low - 1;
    
    for (int j = low; j < high; j++) {
        if (arr[j] < pivot) {
            i++;
            swap(arr[i], arr[j]);
        }
    }
    
    swap(arr[i + 1], arr[high]);
    return i + 1;
}

void quickSort(int arr[], int low, int high) {
    if (low < high) {
        int pi = partition(arr, low, high);
        
        quickSort(arr, low, pi - 1);
        quickSort(arr, pi + 1, high);
    }
}
```

### Complexity
* **Time:**
  - Best/Average: O(n log n)
  - Worst: O(n²) - already sorted with bad pivot
* **Space:** O(log n) - recursion stack
* **Stable:** No
* **Adaptive:** No

### Pivot Selection Strategies
1. **First/Last element:** Simple but worst for sorted data
2. **Random element:** Better average performance
3. **Median-of-three:** Better pivot selection
4. **Median-of-medians:** Guarantees O(n log n) but overhead

### Randomized Quick Sort
```cpp
int randomPartition(int arr[], int low, int high) {
    int random = low + rand() % (high - low + 1);
    swap(arr[random], arr[high]);
    return partition(arr, low, high);
}
```

---

## 12.7 Heap Sort

### Algorithm
```cpp
void heapify(int arr[], int n, int i) {
    int largest = i;
    int left = 2 * i + 1;
    int right = 2 * i + 2;
    
    if (left < n && arr[left] > arr[largest])
        largest = left;
    if (right < n && arr[right] > arr[largest])
        largest = right;
    
    if (largest != i) {
        swap(arr[i], arr[largest]);
        heapify(arr, n, largest);
    }
}

void heapSort(int arr[], int n) {
    // Build max heap
    for (int i = n / 2 - 1; i >= 0; i--)
        heapify(arr, n, i);
    
    // Extract elements one by one
    for (int i = n - 1; i > 0; i--) {
        swap(arr[0], arr[i]);
        heapify(arr, i, 0);
    }
}
```

### Complexity
* **Time:** O(n log n) in all cases
* **Space:** O(1)
* **Stable:** No
* **Adaptive:** No

---

## 12.8 Counting Sort

### Algorithm
```cpp
void countingSort(int arr[], int n) {
    int maxVal = *max_element(arr, arr + n);
    int minVal = *min_element(arr, arr + n);
    int range = maxVal - minVal + 1;
    
    vector<int> count(range, 0);
    vector<int> output(n);
    
    // Count occurrences
    for (int i = 0; i < n; i++)
        count[arr[i] - minVal]++;
    
    // Cumulative count
    for (int i = 1; i < range; i++)
        count[i] += count[i - 1];
    
    // Build output array
    for (int i = n - 1; i >= 0; i--) {
        output[count[arr[i] - minVal] - 1] = arr[i];
        count[arr[i] - minVal]--;
    }
    
    // Copy to original array
    for (int i = 0; i < n; i++)
        arr[i] = output[i];
}
```

### Complexity
* **Time:** O(n + k) where k is range
* **Space:** O(n + k)
* **Stable:** Yes
* **Use when:** Small range of integers

---

## 12.9 Radix Sort

### Algorithm
```cpp
void countingSortByDigit(int arr[], int n, int exp) {
    vector<int> output(n);
    vector<int> count(10, 0);
    
    for (int i = 0; i < n; i++)
        count[(arr[i] / exp) % 10]++;
    
    for (int i = 1; i < 10; i++)
        count[i] += count[i - 1];
    
    for (int i = n - 1; i >= 0; i--) {
        output[count[(arr[i] / exp) % 10] - 1] = arr[i];
        count[(arr[i] / exp) % 10]--;
    }
    
    for (int i = 0; i < n; i++)
        arr[i] = output[i];
}

void radixSort(int arr[], int n) {
    int maxVal = *max_element(arr, arr + n);
    
    for (int exp = 1; maxVal / exp > 0; exp *= 10)
        countingSortByDigit(arr, n, exp);
}
```

### Complexity
* **Time:** O(d × (n + k)) where d is number of digits
* **Space:** O(n + k)
* **Stable:** Yes
* **Use when:** Fixed-length integer keys

---

## 12.10 Bucket Sort

### Algorithm
```cpp
void bucketSort(float arr[], int n) {
    vector<vector<float>> buckets(n);
    
    // Put elements in buckets
    for (int i = 0; i < n; i++) {
        int bucketIdx = n * arr[i];
        buckets[bucketIdx].push_back(arr[i]);
    }
    
    // Sort individual buckets
    for (int i = 0; i < n; i++)
        sort(buckets[i].begin(), buckets[i].end());
    
    // Concatenate all buckets
    int index = 0;
    for (int i = 0; i < n; i++) {
        for (float val : buckets[i])
            arr[index++] = val;
    }
}
```

### Complexity
* **Time:**
  - Average: O(n + k) where k is number of buckets
  - Worst: O(n²) - all elements in one bucket
* **Space:** O(n + k)
* **Use when:** Uniform distribution

---

## 12.11 Sorting Algorithm Comparison

| Algorithm | Best | Average | Worst | Space | Stable | Adaptive |
|-----------|------|---------|-------|-------|--------|----------|
| **Bubble** | O(n) | O(n²) | O(n²) | O(1) | Yes | Yes |
| **Selection** | O(n²) | O(n²) | O(n²) | O(1) | No | No |
| **Insertion** | O(n) | O(n²) | O(n²) | O(1) | Yes | Yes |
| **Merge** | O(n log n) | O(n log n) | O(n log n) | O(n) | Yes | No |
| **Quick** | O(n log n) | O(n log n) | O(n²) | O(log n) | No | No |
| **Heap** | O(n log n) | O(n log n) | O(n log n) | O(1) | No | No |
| **Counting** | O(n+k) | O(n+k) | O(n+k) | O(k) | Yes | No |
| **Radix** | O(d(n+k)) | O(d(n+k)) | O(d(n+k)) | O(n+k) | Yes | No |
| **Bucket** | O(n+k) | O(n+k) | O(n²) | O(n) | Yes | No |

---

## 📝 MCQs for Module 12

### Q1. Which sorting algorithm has best worst-case time complexity?
A. Quick Sort  
B. Merge Sort  
C. Bubble Sort  
D. Selection Sort

> **Answer: B**  
> **Explanation:** Merge sort has O(n log n) worst-case, while quick sort has O(n²) worst-case.

### Q2. Which sorting algorithm is NOT stable?
A. Merge Sort  
B. Insertion Sort  
C. Quick Sort  
D. Bubble Sort

> **Answer: C**  
> **Explanation:** Quick sort doesn't preserve relative order of equal elements (unstable).

### Q3. Time complexity of counting sort is:
A. O(n log n)  
B. O(n + k)  
C. O(n²)  
D. O(n log k)

> **Answer: B**  
> **Explanation:** Counting sort is O(n + k) where k is the range of input values.

### Q4. Which sort is best for nearly sorted arrays?
A. Merge Sort  
B. Quick Sort  
C. Insertion Sort  
D. Heap Sort

> **Answer: C**  
> **Explanation:** Insertion sort is adaptive with O(n) best-case for nearly sorted data.

### Q5. Heap sort space complexity is:
A. O(1)  
B. O(log n)  
C. O(n)  
D. O(n log n)

> **Answer: A**  
> **Explanation:** Heap sort is in-place sorting with O(1) auxiliary space.

---

# 🎨 MODULE 13: ALGORITHM DESIGN PARADIGMS

## 13.1 Divide and Conquer

### Principle
1. **Divide:** Break problem into smaller subproblems
2. **Conquer:** Solve subproblems recursively
3. **Combine:** Merge solutions of subproblems

### Examples

#### 1. Binary Search
```cpp
int binarySearch(int arr[], int left, int right, int key) {
    if (left <= right) {
        int mid = left + (right - left) / 2;
        
        if (arr[mid] == key)
            return mid;
        if (arr[mid] > key)
            return binarySearch(arr, left, mid - 1, key);
        return binarySearch(arr, mid + 1, right, key);
    }
    return -1;
}
```

#### 2. Maximum Subarray Sum
```cpp
int maxCrossingSum(int arr[], int left, int mid, int right) {
    int sum = 0, leftSum = INT_MIN;
    for (int i = mid; i >= left; i--) {
        sum += arr[i];
        leftSum = max(leftSum, sum);
    }
    
    sum = 0;
    int rightSum = INT_MIN;
    for (int i = mid + 1; i <= right; i++) {
        sum += arr[i];
        rightSum = max(rightSum, sum);
    }
    
    return leftSum + rightSum;
}

int maxSubarraySum(int arr[], int left, int right) {
    if (left == right)
        return arr[left];
    
    int mid = (left + right) / 2;
    
    return max({maxSubarraySum(arr, left, mid),
                maxSubarraySum(arr, mid + 1, right),
                maxCrossingSum(arr, left, mid, right)});
}
```

#### 3. Closest Pair of Points
**Time:** O(n log n)

### Characteristics
* **Recursion-based**
* **Independent subproblems**
* **Examples:** Merge sort, quick sort, binary search
* **Time complexity:** Often O(n log n)

---

## 13.2 Dynamic Programming (DP)

### Principle
* Solve problems by breaking into **overlapping subproblems**
* **Store results** of subproblems (memoization/tabulation)
* **Reuse** stored results instead of recomputing

### Properties Required
1. **Optimal Substructure:** Optimal solution contains optimal solutions of subproblems
2. **Overlapping Subproblems:** Same subproblems solved multiple times

### Approaches

#### 1. Memoization (Top-Down)
```cpp
int fibonacci(int n, vector<int>& memo) {
    if (n <= 1) return n;
    
    if (memo[n] != -1)
        return memo[n];
    
    memo[n] = fibonacci(n-1, memo) + fibonacci(n-2, memo);
    return memo[n];
}
```

#### 2. Tabulation (Bottom-Up)
```cpp
int fibonacci(int n) {
    vector<int> dp(n + 1);
    dp[0] = 0;
    dp[1] = 1;
    
    for (int i = 2; i <= n; i++)
        dp[i] = dp[i-1] + dp[i-2];
    
    return dp[n];
}
```

### Examples
* Fibonacci, LCS, LIS, Knapsack, Matrix Chain Multiplication
* *Detailed coverage in Module 14*

---

## 13.3 Greedy Algorithms

### Principle
* Make **locally optimal choice** at each step
* Hope that local optimum leads to global optimum

### When Greedy Works?
* **Greedy Choice Property:** Local optimal choice leads to global optimal
* **Optimal Substructure:** Optimal solution contains optimal subproblems

### Examples

#### 1. Activity Selection
```cpp
struct Activity {
    int start, finish;
};

bool compare(Activity a, Activity b) {
    return a.finish < b.finish;
}

int activitySelection(Activity arr[], int n) {
    sort(arr, arr + n, compare);
    
    int count = 1;
    int lastFinish = arr[0].finish;
    
    for (int i = 1; i < n; i++) {
        if (arr[i].start >= lastFinish) {
            count++;
            lastFinish = arr[i].finish;
        }
    }
    
    return count;
}
```

#### 2. Fractional Knapsack
```cpp
struct Item {
    int value, weight;
    double ratio;
};

double fractionalKnapsack(Item arr[], int n, int capacity) {
    sort(arr, arr + n, [](Item a, Item b) {
        return a.ratio > b.ratio;
    });
    
    double totalValue = 0;
    
    for (int i = 0; i < n; i++) {
        if (capacity >= arr[i].weight) {
            totalValue += arr[i].value;
            capacity -= arr[i].weight;
        } else {
            totalValue += arr[i].ratio * capacity;
            break;
        }
    }
    
    return totalValue;
}
```

### Greedy vs DP
* **Greedy:** Makes choice once, never reconsider
* **DP:** Examines all choices, stores results

---

## 13.4 Backtracking

### Principle
* **Try all possibilities** systematically
* **Prune** branches that can't lead to solution
* **Backtrack** when dead end reached

### Template
```cpp
void backtrack(state, result) {
    if (isSolution(state)) {
        addToResult(state, result);
        return;
    }
    
    for (choice in allChoices) {
        if (isValid(choice, state)) {
            makeChoice(choice, state);
            backtrack(state, result);
            undoChoice(choice, state);  // Backtrack
        }
    }
}
```

### Examples

#### 1. N-Queens
```cpp
bool isSafe(vector<vector<int>>& board, int row, int col, int n) {
    // Check column
    for (int i = 0; i < row; i++)
        if (board[i][col] == 1)
            return false;
    
    // Check upper left diagonal
    for (int i = row, j = col; i >= 0 && j >= 0; i--, j--)
        if (board[i][j] == 1)
            return false;
    
    // Check upper right diagonal
    for (int i = row, j = col; i >= 0 && j < n; i--, j++)
        if (board[i][j] == 1)
            return false;
    
    return true;
}

bool solveNQueens(vector<vector<int>>& board, int row, int n) {
    if (row >= n)
        return true;
    
    for (int col = 0; col < n; col++) {
        if (isSafe(board, row, col, n)) {
            board[row][col] = 1;
            
            if (solveNQueens(board, row + 1, n))
                return true;
            
            board[row][col] = 0;  // Backtrack
        }
    }
    
    return false;
}
```

---

## 13.5 Branch and Bound

### Principle
* Systematic enumeration with **pruning using bounds**
* Uses **cost function** to decide which branch to explore
* Often uses **priority queue** (best-first search)

### Example: 0/1 Knapsack
```cpp
struct Node {
    int level, profit, weight;
    double bound;
};

double calculateBound(Node u, int n, int W, Item arr[]) {
    if (u.weight >= W) return 0;
    
    double bound = u.profit;
    int j = u.level + 1;
    int totalWeight = u.weight;
    
    while (j < n && totalWeight + arr[j].weight <= W) {
        totalWeight += arr[j].weight;
        bound += arr[j].value;
        j++;
    }
    
    if (j < n)
        bound += (W - totalWeight) * arr[j].ratio;
    
    return bound;
}
```

---

## 📝 MCQs for Module 13

### Q1. Which paradigm is used in merge sort?
A. Greedy  
B. Divide and Conquer  
C. Dynamic Programming  
D. Backtracking

> **Answer: B**  
> **Explanation:** Merge sort divides array, recursively sorts, then merges - classic divide and conquer.

### Q2. Dynamic programming is applicable when problem has:
A. Overlapping subproblems only  
B. Optimal substructure only  
C. Both overlapping subproblems and optimal substructure  
D. Neither property

> **Answer: C**  
> **Explanation:** DP requires both overlapping subproblems (for memoization benefit) and optimal substructure.

### Q3. Greedy approach is optimal for:
A. 0/1 Knapsack  
B. Fractional Knapsack  
C. Longest Common Subsequence  
D. Matrix Chain Multiplication

> **Answer: B**  
> **Explanation:** Fractional knapsack has greedy choice property, while 0/1 knapsack needs DP.

### Q4. Backtracking is used in:
A. Binary Search  
B. Merge Sort  
C. N-Queens Problem  
D. Dijkstra's Algorithm

> **Answer: C**  
> **Explanation:** N-Queens requires trying all possibilities with backtracking when solution not feasible.

### Q5. Difference between backtracking and branch & bound:
A. Branch & bound uses bounding function  
B. Backtracking uses bounding function  
C. Both are same  
D. Neither uses bounding

> **Answer: A**  
> **Explanation:** Branch & bound prunes branches using bound calculations, backtracking tries all valid options.

---

# 💎 MODULE 14: DYNAMIC PROGRAMMING (CLASSIC PROBLEMS)

## 14.1 Fibonacci Number

### Recursive (Exponential)
```cpp
int fib(int n) {
    if (n <= 1) return n;
    return fib(n-1) + fib(n-2);
}
```
**Time:** O(2ⁿ)

### Memoization (Top-Down DP)
```cpp
int fibMemo(int n, vector<int>& memo) {
    if (n <= 1) return n;
    if (memo[n] != -1) return memo[n];
    
    memo[n] = fibMemo(n-1, memo) + fibMemo(n-2, memo);
    return memo[n];
}
```
**Time:** O(n), **Space:** O(n)

### Tabulation (Bottom-Up DP)
```cpp
int fibTab(int n) {
    if (n <= 1) return n;
    
    vector<int> dp(n + 1);
    dp[0] = 0;
    dp[1] = 1;
    
    for (int i = 2; i <= n; i++)
        dp[i] = dp[i-1] + dp[i-2];
    
    return dp[n];
}
```

### Space Optimized
```cpp
int fibOptimized(int n) {
    if (n <= 1) return n;
    
    int prev2 = 0, prev1 = 1;
    
    for (int i = 2; i <= n; i++) {
        int current = prev1 + prev2;
        prev2 = prev1;
        prev1 = current;
    }
    
    return prev1;
}
```
**Time:** O(n), **Space:** O(1)

---

## 14.2 Longest Common Subsequence (LCS)

### Problem
Find length of longest subsequence common to both strings.

### Recursive
```cpp
int lcs(string s1, string s2, int m, int n) {
    if (m == 0 || n == 0)
        return 0;
    
    if (s1[m-1] == s2[n-1])
        return 1 + lcs(s1, s2, m-1, n-1);
    
    return max(lcs(s1, s2, m-1, n), lcs(s1, s2, m, n-1));
}
```
**Time:** O(2^(m+n))

### DP Solution
```cpp
int lcsDP(string s1, string s2) {
    int m = s1.length(), n = s2.length();
    vector<vector<int>> dp(m + 1, vector<int>(n + 1, 0));
    
    for (int i = 1; i <= m; i++) {
        for (int j = 1; j <= n; j++) {
            if (s1[i-1] == s2[j-1])
                dp[i][j] = 1 + dp[i-1][j-1];
            else
                dp[i][j] = max(dp[i-1][j], dp[i][j-1]);
        }
    }
    
    return dp[m][n];
}
```
**Time:** O(m × n), **Space:** O(m × n)

### Print LCS
```cpp
string printLCS(string s1, string s2, vector<vector<int>>& dp) {
    int i = s1.length(), j = s2.length();
    string lcs = "";
    
    while (i > 0 && j > 0) {
        if (s1[i-1] == s2[j-1]) {
            lcs = s1[i-1] + lcs;
            i--;
            j--;
        } else if (dp[i-1][j] > dp[i][j-1]) {
            i--;
        } else {
            j--;
        }
    }
    
    return lcs;
}
```

---

## 14.3 Longest Increasing Subsequence (LIS)

### Problem
Find length of longest subsequence where elements are in increasing order.

### DP Solution O(n²)
```cpp
int lisDP(int arr[], int n) {
    vector<int> dp(n, 1);
    
    for (int i = 1; i < n; i++) {
        for (int j = 0; j < i; j++) {
            if (arr[j] < arr[i])
                dp[i] = max(dp[i], dp[j] + 1);
        }
    }
    
    return *max_element(dp.begin(), dp.end());
}
```

### Binary Search O(n log n)
```cpp
int lisOptimized(int arr[], int n) {
    vector<int> tail;
    
    for (int i = 0; i < n; i++) {
        auto it = lower_bound(tail.begin(), tail.end(), arr[i]);
        
        if (it == tail.end())
            tail.push_back(arr[i]);
        else
            *it = arr[i];
    }
    
    return tail.size();
}
```

---

## 14.4 0/1 Knapsack

### Problem
Given weights and values of n items, find maximum value that can be obtained with weight limit W.

### Recursive
```cpp
int knapsack(int W, int wt[], int val[], int n) {
    if (n == 0 || W == 0)
        return 0;
    
    if (wt[n-1] > W)
        return knapsack(W, wt, val, n-1);
    
    return max(val[n-1] + knapsack(W - wt[n-1], wt, val, n-1),
               knapsack(W, wt, val, n-1));
}
```

### DP Solution
```cpp
int knapsackDP(int W, int wt[], int val[], int n) {
    vector<vector<int>> dp(n + 1, vector<int>(W + 1, 0));
    
    for (int i = 1; i <= n; i++) {
        for (int w = 1; w <= W; w++) {
            if (wt[i-1] <= w)
                dp[i][w] = max(val[i-1] + dp[i-1][w - wt[i-1]],
                              dp[i-1][w]);
            else
                dp[i][w] = dp[i-1][w];
        }
    }
    
    return dp[n][W];
}
```
**Time:** O(n × W), **Space:** O(n × W)

---

## 14.5 Coin Change Problem

### Problem 1: Minimum Coins
```cpp
int minCoins(int coins[], int n, int amount) {
    vector<int> dp(amount + 1, INT_MAX);
    dp[0] = 0;
    
    for (int i = 1; i <= amount; i++) {
        for (int j = 0; j < n; j++) {
            if (coins[j] <= i && dp[i - coins[j]] != INT_MAX)
                dp[i] = min(dp[i], dp[i - coins[j]] + 1);
        }
    }
    
    return dp[amount] == INT_MAX ? -1 : dp[amount];
}
```

### Problem 2: Number of Ways
```cpp
int coinChangeWays(int coins[], int n, int amount) {
    vector<int> dp(amount + 1, 0);
    dp[0] = 1;
    
    for (int i = 0; i < n; i++) {
        for (int j = coins[i]; j <= amount; j++) {
            dp[j] += dp[j - coins[i]];
        }
    }
    
    return dp[amount];
}
```

---

## 14.6 Edit Distance (Levenshtein Distance)

### Problem
Minimum operations (insert, delete, replace) to convert string s1 to s2.

```cpp
int editDistance(string s1, string s2) {
    int m = s1.length(), n = s2.length();
    vector<vector<int>> dp(m + 1, vector<int>(n + 1));
    
    // Base cases
    for (int i = 0; i <= m; i++)
        dp[i][0] = i;
    for (int j = 0; j <= n; j++)
        dp[0][j] = j;
    
    for (int i = 1; i <= m; i++) {
        for (int j = 1; j <= n; j++) {
            if (s1[i-1] == s2[j-1])
                dp[i][j] = dp[i-1][j-1];
            else
                dp[i][j] = 1 + min({dp[i-1][j],    // Delete
                                    dp[i][j-1],    // Insert
                                    dp[i-1][j-1]}); // Replace
        }
    }
    
    return dp[m][n];
}
```
**Time:** O(m × n)

---

## 14.7 Matrix Chain Multiplication

### Problem
Find minimum number of multiplications needed to multiply chain of matrices.

```cpp
int matrixChainOrder(int dims[], int n) {
    vector<vector<int>> dp(n, vector<int>(n, 0));
    
    for (int len = 2; len < n; len++) {
        for (int i = 1; i < n - len + 1; i++) {
            int j = i + len - 1;
            dp[i][j] = INT_MAX;
            
            for (int k = i; k < j; k++) {
                int cost = dp[i][k] + dp[k+1][j] + 
                          dims[i-1] * dims[k] * dims[j];
                dp[i][j] = min(dp[i][j], cost);
            }
        }
    }
    
    return dp[1][n-1];
}
```
**Time:** O(n³)

---

## 📝 MCQs for Module 14

### Q1. Time complexity of DP solution for Fibonacci:
A. O(2ⁿ)  
B. O(n)  
C. O(log n)  
D. O(n²)

> **Answer: B**  
> **Explanation:** DP computes each Fibonacci number once, storing results for reuse.

### Q2. LCS of "ABCD" and "ACBD" is:
A. 2  
B. 3  
C. 4  
D. 1

> **Answer: B**  
> **Explanation:** LCS is "ABD" with length 3.

### Q3. Time complexity of 0/1 knapsack DP solution:
A. O(n)  
B. O(W)  
C. O(n × W)  
D. O(2ⁿ)

> **Answer: C**  
> **Explanation:** DP table of size n × W, each cell computed in O(1).

### Q4. Edit distance problem uses which operations?
A. Only insert  
B. Only delete  
C. Insert, delete, replace  
D. Only replace

> **Answer: C**  
> **Explanation:** Edit distance allows insert, delete, and replace operations.

### Q5. Matrix chain multiplication problem minimizes:
A. Number of matrices  
B. Size of matrices  
C. Number of scalar multiplications  
D. Memory usage

> **Answer: C**  
> **Explanation:** Goal is to minimize total scalar multiplications by optimal parenthesization.

---


# 🌟 MODULE 15: GREEDY ALGORITHMS

## 15.1 Activity Selection Problem

### Problem
Select maximum number of non-overlapping activities.

```cpp
struct Activity {
    int start, finish;
};

bool compare(Activity a, Activity b) {
    return a.finish < b.finish;
}

vector<int> activitySelection(Activity arr[], int n) {
    sort(arr, arr + n, compare);
    
    vector<int> result;
    result.push_back(0);  // Select first activity
    
    int lastFinish = arr[0].finish;
    
    for (int i = 1; i < n; i++) {
        if (arr[i].start >= lastFinish) {
            result.push_back(i);
            lastFinish = arr[i].finish;
        }
    }
    
    return result;
}
```
**Time:** O(n log n)

---

## 15.2 Huffman Coding

### Problem
Optimal prefix-free encoding for data compression.

```cpp
struct Node {
    char ch;
    int freq;
    Node *left, *right;
    
    Node(char c, int f) : ch(c), freq(f), left(NULL), right(NULL) {}
};

struct Compare {
    bool operator()(Node* a, Node* b) {
        return a->freq > b->freq;
    }
};

Node* buildHuffmanTree(char chars[], int freq[], int n) {
    priority_queue<Node*, vector<Node*>, Compare> pq;
    
    for (int i = 0; i < n; i++)
        pq.push(new Node(chars[i], freq[i]));
    
    while (pq.size() > 1) {
        Node* left = pq.top(); pq.pop();
        Node* right = pq.top(); pq.pop();
        
        Node* merged = new Node('$', left->freq + right->freq);
        merged->left = left;
        merged->right = right;
        
        pq.push(merged);
    }
    
    return pq.top();
}

void printCodes(Node* root, string code) {
    if (!root) return;
    
    if (root->ch != '$')
        cout << root->ch << ": " << code << endl;
    
    printCodes(root->left, code + "0");
    printCodes(root->right, code + "1");
}
```
**Time:** O(n log n)

---

## 15.3 Fractional Knapsack

### Problem
Maximize value with fractional items allowed.

```cpp
struct Item {
    int value, weight;
    double ratio;
};

bool compare(Item a, Item b) {
    return a.ratio > b.ratio;
}

double fractionalKnapsack(Item arr[], int n, int capacity) {
    // Calculate value/weight ratio
    for (int i = 0; i < n; i++)
        arr[i].ratio = (double)arr[i].value / arr[i].weight;
    
    sort(arr, arr + n, compare);
    
    double totalValue = 0;
    
    for (int i = 0; i < n; i++) {
        if (capacity >= arr[i].weight) {
            totalValue += arr[i].value;
            capacity -= arr[i].weight;
        } else {
            totalValue += arr[i].ratio * capacity;
            break;
        }
    }
    
    return totalValue;
}
```
**Time:** O(n log n)

---

## 15.4 Job Sequencing Problem

### Problem
Schedule jobs with deadlines to maximize profit.

```cpp
struct Job {
    char id;
    int deadline, profit;
};

bool compare(Job a, Job b) {
    return a.profit > b.profit;
}

vector<char> jobSequencing(Job arr[], int n) {
    sort(arr, arr + n, compare);
    
    int maxDeadline = 0;
    for (int i = 0; i < n; i++)
        maxDeadline = max(maxDeadline, arr[i].deadline);
    
    vector<int> slot(maxDeadline, -1);
    vector<char> result;
    
    for (int i = 0; i < n; i++) {
        // Find free slot from deadline backwards
        for (int j = arr[i].deadline - 1; j >= 0; j--) {
            if (slot[j] == -1) {
                slot[j] = i;
                result.push_back(arr[i].id);
                break;
            }
        }
    }
    
    return result;
}
```
**Time:** O(n² log n)

---

## 15.5 Minimum Spanning Tree (Prim's & Kruskal's)
*Covered in Module 10*

---

## 15.6 Dijkstra's Shortest Path
*Covered in Module 10*

---

## 15.7 Greedy vs Dynamic Programming

### When Greedy Works
* **Greedy Choice Property:** Local optimal → global optimal
* **Optimal Substructure:** Optimal solution contains optimal subproblems

### When Greedy Fails
* **0/1 Knapsack:** Needs DP, greedy doesn't work
* **Longest Path:** Needs DP or backtracking

### Examples

| Problem | Approach |
|---------|----------|
| Activity Selection | Greedy ✓ |
| Fractional Knapsack | Greedy ✓ |
| 0/1 Knapsack | DP ✓ |
| Huffman Coding | Greedy ✓ |
| Edit Distance | DP ✓ |
| Shortest Path (non-negative) | Greedy (Dijkstra) ✓ |
| Shortest Path (negative weights) | DP (Bellman-Ford) ✓ |

---

## 📝 MCQs for Module 15

### Q1. Fractional knapsack can be solved using:
A. Dynamic Programming  
B. Greedy Algorithm  
C. Backtracking  
D. Branch and Bound

> **Answer: B**  
> **Explanation:** Greedy approach (select by value/weight ratio) gives optimal solution for fractional knapsack.

### Q2. Activity selection problem uses greedy strategy based on:
A. Start time  
B. Finish time  
C. Duration  
D. Profit

> **Answer: B**  
> **Explanation:** Sort by finish time and select activities that don't overlap.

### Q3. Huffman coding is used for:
A. Sorting  
B. Data compression  
C. Encryption  
D. Hashing

> **Answer: B**  
> **Explanation:** Huffman coding creates optimal prefix-free codes for data compression.

### Q4. Time complexity of Huffman coding:
A. O(n)  
B. O(n log n)  
C. O(n²)  
D. O(2ⁿ)

> **Answer: B**  
> **Explanation:** Building heap and extracting min n times gives O(n log n).

### Q5. Which problem CANNOT be solved optimally using greedy approach?
A. Fractional Knapsack  
B. 0/1 Knapsack  
C. Activity Selection  
D. Huffman Coding

> **Answer: B**  
> **Explanation:** 0/1 Knapsack requires dynamic programming; greedy doesn't guarantee optimal solution.

---

# 🔤 MODULE 16: STRING ALGORITHMS

## 16.1 Pattern Matching Basics

### Naive Pattern Search
```cpp
void naiveSearch(string text, string pattern) {
    int n = text.length();
    int m = pattern.length();
    
    for (int i = 0; i <= n - m; i++) {
        int j;
        for (j = 0; j < m; j++) {
            if (text[i + j] != pattern[j])
                break;
        }
        if (j == m)
            cout << "Pattern found at index " << i << endl;
    }
}
```
**Time:** O((n-m+1) × m) = O(n × m)

---

## 16.2 KMP Algorithm (Knuth-Morris-Pratt)

### LPS Array (Longest Proper Prefix which is Suffix)
```cpp
vector<int> computeLPS(string pattern) {
    int m = pattern.length();
    vector<int> lps(m, 0);
    int len = 0;
    int i = 1;
    
    while (i < m) {
        if (pattern[i] == pattern[len]) {
            len++;
            lps[i] = len;
            i++;
        } else {
            if (len != 0) {
                len = lps[len - 1];
            } else {
                lps[i] = 0;
                i++;
            }
        }
    }
    
    return lps;
}
```

### KMP Search
```cpp
void KMPSearch(string text, string pattern) {
    int n = text.length();
    int m = pattern.length();
    
    vector<int> lps = computeLPS(pattern);
    
    int i = 0;  // index for text
    int j = 0;  // index for pattern
    
    while (i < n) {
        if (pattern[j] == text[i]) {
            i++;
            j++;
        }
        
        if (j == m) {
            cout << "Pattern found at index " << i - j << endl;
            j = lps[j - 1];
        } else if (i < n && pattern[j] != text[i]) {
            if (j != 0)
                j = lps[j - 1];
            else
                i++;
        }
    }
}
```
**Time:** O(n + m)

---

## 16.3 Rabin-Karp Algorithm

### Rolling Hash
```cpp
#define d 256  // Number of characters
#define q 101  // Prime number

void rabinKarp(string text, string pattern) {
    int n = text.length();
    int m = pattern.length();
    int h = 1;
    
    // h = d^(m-1) % q
    for (int i = 0; i < m - 1; i++)
        h = (h * d) % q;
    
    // Calculate hash for pattern and first window
    int p = 0;  // pattern hash
    int t = 0;  // text hash
    
    for (int i = 0; i < m; i++) {
        p = (d * p + pattern[i]) % q;
        t = (d * t + text[i]) % q;
    }
    
    // Slide pattern over text
    for (int i = 0; i <= n - m; i++) {
        if (p == t) {
            // Check characters one by one
            bool match = true;
            for (int j = 0; j < m; j++) {
                if (text[i + j] != pattern[j]) {
                    match = false;
                    break;
                }
            }
            if (match)
                cout << "Pattern found at index " << i << endl;
        }
        
        // Calculate hash for next window
        if (i < n - m) {
            t = (d * (t - text[i] * h) + text[i + m]) % q;
            if (t < 0)
                t += q;
        }
    }
}
```
**Time:** O(n + m) average, O(n × m) worst case

---

## 16.4 String Matching with Finite Automata

### Build Transition Table
```cpp
int getNextState(string pattern, int state, int x) {
    if (state < pattern.length() && x == pattern[state])
        return state + 1;
    
    // Check for longest proper suffix
    for (int ns = state; ns > 0; ns--) {
        if (pattern[ns - 1] == x) {
            bool match = true;
            for (int i = 0; i < ns - 1; i++) {
                if (pattern[i] != pattern[state - ns + 1 + i]) {
                    match = false;
                    break;
                }
            }
            if (match)
                return ns;
        }
    }
    
    return 0;
}
```
**Time:** O(m³ × Σ) preprocessing, O(n) matching

---

## 16.5 Longest Palindromic Substring

### Expand Around Center
```cpp
string longestPalindrome(string s) {
    if (s.empty()) return "";
    
    int start = 0, maxLen = 1;
    
    auto expandAroundCenter = [&](int left, int right) {
        while (left >= 0 && right < s.length() && s[left] == s[right]) {
            if (right - left + 1 > maxLen) {
                start = left;
                maxLen = right - left + 1;
            }
            left--;
            right++;
        }
    };
    
    for (int i = 0; i < s.length(); i++) {
        expandAroundCenter(i, i);      // Odd length
        expandAroundCenter(i, i + 1);  // Even length
    }
    
    return s.substr(start, maxLen);
}
```
**Time:** O(n²)

---

## 16.6 Anagram Problems

### Check if Two Strings are Anagrams
```cpp
bool areAnagrams(string s1, string s2) {
    if (s1.length() != s2.length())
        return false;
    
    sort(s1.begin(), s1.end());
    sort(s2.begin(), s2.end());
    
    return s1 == s2;
}

// Or using frequency count
bool areAnagramsFreq(string s1, string s2) {
    if (s1.length() != s2.length())
        return false;
    
    unordered_map<char, int> freq;
    
    for (char c : s1)
        freq[c]++;
    
    for (char c : s2) {
        freq[c]--;
        if (freq[c] < 0)
            return false;
    }
    
    return true;
}
```

---

## 16.7 String Compression

```cpp
string compress(string s) {
    string result = "";
    int count = 1;
    
    for (int i = 1; i <= s.length(); i++) {
        if (i < s.length() && s[i] == s[i-1]) {
            count++;
        } else {
            result += s[i-1];
            if (count > 1)
                result += to_string(count);
            count = 1;
        }
    }
    
    return result.length() < s.length() ? result : s;
}
```

---

## 16.8 Trie (Prefix Tree)

```cpp
struct TrieNode {
    TrieNode* children[26];
    bool isEndOfWord;
    
    TrieNode() {
        isEndOfWord = false;
        for (int i = 0; i < 26; i++)
            children[i] = NULL;
    }
};

class Trie {
private:
    TrieNode* root;
    
public:
    Trie() {
        root = new TrieNode();
    }
    
    void insert(string word) {
        TrieNode* current = root;
        
        for (char c : word) {
            int index = c - 'a';
            if (current->children[index] == NULL)
                current->children[index] = new TrieNode();
            current = current->children[index];
        }
        
        current->isEndOfWord = true;
    }
    
    bool search(string word) {
        TrieNode* current = root;
        
        for (char c : word) {
            int index = c - 'a';
            if (current->children[index] == NULL)
                return false;
            current = current->children[index];
        }
        
        return current->isEndOfWord;
    }
    
    bool startsWith(string prefix) {
        TrieNode* current = root;
        
        for (char c : prefix) {
            int index = c - 'a';
            if (current->children[index] == NULL)
                return false;
            current = current->children[index];
        }
        
        return true;
    }
};
```

---

## 📝 MCQs for Module 16

### Q1. Time complexity of KMP algorithm:
A. O(n²)  
B. O(n × m)  
C. O(n + m)  
D. O(n log m)

> **Answer: C**  
> **Explanation:** KMP preprocesses pattern in O(m) and searches in O(n), total O(n + m).

### Q2. Rabin-Karp uses which technique?
A. Dynamic programming  
B. Hashing  
C. Divide and conquer  
D. Greedy

> **Answer: B**  
> **Explanation:** Rabin-Karp uses rolling hash to compare pattern with text windows.

### Q3. Space complexity of Trie with n words of average length m:
A. O(n)  
B. O(m)  
C. O(n × m)  
D. O(n + m)

> **Answer: C**  
> **Explanation:** Worst case, no shared prefixes, all characters stored: O(n × m).

### Q4. Naive pattern matching has time complexity:
A. O(n)  
B. O(n + m)  
C. O(n × m)  
D. O(log n)

> **Answer: C**  
> **Explanation:** For each position in text (n-m), compare m characters.

### Q5. Trie is best used for:
A. Sorting integers  
B. Autocomplete/prefix search  
C. Graph traversal  
D. Matrix operations

> **Answer: B**  
> **Explanation:** Trie efficiently stores strings with common prefixes, ideal for autocomplete.

---

# 🚀 MODULE 17: ADVANCED DATA STRUCTURES

## 17.1 Segment Tree

### Build Segment Tree
```cpp
void buildSegmentTree(int arr[], int tree[], int start, int end, int node) {
    if (start == end) {
        tree[node] = arr[start];
        return;
    }
    
    int mid = (start + end) / 2;
    buildSegmentTree(arr, tree, start, mid, 2*node);
    buildSegmentTree(arr, tree, mid+1, end, 2*node+1);
    
    tree[node] = tree[2*node] + tree[2*node+1];
}
```

### Range Query
```cpp
int rangeQuery(int tree[], int start, int end, int l, int r, int node) {
    // No overlap
    if (r < start || end < l)
        return 0;
    
    // Complete overlap
    if (l <= start && end <= r)
        return tree[node];
    
    // Partial overlap
    int mid = (start + end) / 2;
    int leftSum = rangeQuery(tree, start, mid, l, r, 2*node);
    int rightSum = rangeQuery(tree, mid+1, end, l, r, 2*node+1);
    
    return leftSum + rightSum;
}
```

### Point Update
```cpp
void updateSegmentTree(int tree[], int start, int end, int index, int value, int node) {
    if (start == end) {
        tree[node] = value;
        return;
    }
    
    int mid = (start + end) / 2;
    
    if (index <= mid)
        updateSegmentTree(tree, start, mid, index, value, 2*node);
    else
        updateSegmentTree(tree, mid+1, end, index, value, 2*node+1);
    
    tree[node] = tree[2*node] + tree[2*node+1];
}
```

**Time:** Build O(n), Query O(log n), Update O(log n)

---

## 17.2 Fenwick Tree (Binary Indexed Tree)

```cpp
class FenwickTree {
private:
    vector<int> tree;
    int n;
    
public:
    FenwickTree(int size) {
        n = size;
        tree.resize(n + 1, 0);
    }
    
    void update(int index, int delta) {
        while (index <= n) {
            tree[index] += delta;
            index += index & (-index);
        }
    }
    
    int query(int index) {
        int sum = 0;
        while (index > 0) {
            sum += tree[index];
            index -= index & (-index);
        }
        return sum;
    }
    
    int rangeQuery(int left, int right) {
        return query(right) - query(left - 1);
    }
};
```

**Time:** Update O(log n), Query O(log n)

---

## 17.3 Disjoint Set Union (Union-Find)

```cpp
class DSU {
private:
    vector<int> parent, rank;
    
public:
    DSU(int n) {
        parent.resize(n);
        rank.resize(n, 0);
        for (int i = 0; i < n; i++)
            parent[i] = i;
    }
    
    int find(int x) {
        if (parent[x] != x)
            parent[x] = find(parent[x]);  // Path compression
        return parent[x];
    }
    
    void unite(int x, int y) {
        int px = find(x);
        int py = find(y);
        
        if (px == py) return;
        
        // Union by rank
        if (rank[px] < rank[py]) {
            parent[px] = py;
        } else if (rank[px] > rank[py]) {
            parent[py] = px;
        } else {
            parent[py] = px;
            rank[px]++;
        }
    }
    
    bool connected(int x, int y) {
        return find(x) == find(y);
    }
};
```

**Time:** O(α(n)) ≈ O(1) amortized (α is inverse Ackermann)

---

## 17.4 Suffix Array

```cpp
vector<int> buildSuffixArray(string s) {
    int n = s.length();
    vector<int> suffixArray(n);
    vector<pair<string, int>> suffixes(n);
    
    for (int i = 0; i < n; i++) {
        suffixes[i] = {s.substr(i), i};
    }
    
    sort(suffixes.begin(), suffixes.end());
    
    for (int i = 0; i < n; i++) {
        suffixArray[i] = suffixes[i].second;
    }
    
    return suffixArray;
}
```

**Applications:** Pattern matching, longest repeated substring

---

## 17.5 LRU Cache

```cpp
class LRUCache {
private:
    int capacity;
    list<int> lru;
    unordered_map<int, pair<int, list<int>::iterator>> cache;
    
public:
    LRUCache(int cap) : capacity(cap) {}
    
    int get(int key) {
        if (cache.find(key) == cache.end())
            return -1;
        
        // Move to front (most recently used)
        lru.erase(cache[key].second);
        lru.push_front(key);
        cache[key].second = lru.begin();
        
        return cache[key].first;
    }
    
    void put(int key, int value) {
        if (cache.find(key) != cache.end()) {
            // Update existing
            lru.erase(cache[key].second);
        } else if (cache.size() >= capacity) {
            // Remove LRU
            int lruKey = lru.back();
            lru.pop_back();
            cache.erase(lruKey);
        }
        
        // Add to front
        lru.push_front(key);
        cache[key] = {value, lru.begin()};
    }
};
```

**Time:** O(1) for both get and put

---

## 📝 MCQs for Module 17

### Q1. Segment tree query time complexity:
A. O(1)  
B. O(log n)  
C. O(n)  
D. O(n log n)

> **Answer: B**  
> **Explanation:** Segment tree divides range in half at each level, height = O(log n).

### Q2. Disjoint Set Union with path compression has time complexity:
A. O(1)  
B. O(log n)  
C. O(α(n))  
D. O(n)

> **Answer: C**  
> **Explanation:** With path compression and union by rank, operations are O(α(n)) amortized.

### Q3. Fenwick tree is also known as:
A. Segment tree  
B. Binary Indexed Tree  
C. Trie  
D. AVL tree

> **Answer: B**  
> **Explanation:** Fenwick tree and Binary Indexed Tree (BIT) are the same data structure.

### Q4. LRU Cache operations run in:
A. O(1)  
B. O(log n)  
C. O(n)  
D. O(n log n)

> **Answer: A**  
> **Explanation:** Using hash map + doubly linked list, both get and put are O(1).

### Q5. Suffix array is used for:
A. Sorting  
B. Pattern matching  
C. Graph traversal  
D. Priority queue

> **Answer: B**  
> **Explanation:** Suffix array efficiently solves pattern matching and substring problems.

---

# 📚 MODULE 18: REVISION & QUICK REFERENCE

## 18.1 Time Complexity Cheat Sheet

### Data Structures

| Data Structure | Access | Search | Insert | Delete | Space |
|----------------|--------|--------|--------|--------|-------|
| **Array** | O(1) | O(n) | O(n) | O(n) | O(n) |
| **Stack** | O(n) | O(n) | O(1) | O(1) | O(n) |
| **Queue** | O(n) | O(n) | O(1) | O(1) | O(n) |
| **Singly Linked List** | O(n) | O(n) | O(1) | O(1) | O(n) |
| **Doubly Linked List** | O(n) | O(n) | O(1) | O(1) | O(n) |
| **Hash Table** | - | O(1) | O(1) | O(1) | O(n) |
| **Binary Search Tree** | O(log n) | O(log n) | O(log n) | O(log n) | O(n) |
| **AVL Tree** | O(log n) | O(log n) | O(log n) | O(log n) | O(n) |
| **Binary Heap** | - | O(n) | O(log n) | O(log n) | O(n) |

### Sorting Algorithms

| Algorithm | Best | Average | Worst | Space | Stable |
|-----------|------|---------|-------|-------|--------|
| **Bubble** | O(n) | O(n²) | O(n²) | O(1) | Yes |
| **Selection** | O(n²) | O(n²) | O(n²) | O(1) | No |
| **Insertion** | O(n) | O(n²) | O(n²) | O(1) | Yes |
| **Merge** | O(n log n) | O(n log n) | O(n log n) | O(n) | Yes |
| **Quick** | O(n log n) | O(n log n) | O(n²) | O(log n) | No |
| **Heap** | O(n log n) | O(n log n) | O(n log n) | O(1) | No |
| **Counting** | O(n+k) | O(n+k) | O(n+k) | O(k) | Yes |
| **Radix** | O(d(n+k)) | O(d(n+k)) | O(d(n+k)) | O(n+k) | Yes |

### Graph Algorithms

| Algorithm | Time Complexity | Space | Use Case |
|-----------|-----------------|-------|----------|
| **BFS** | O(V + E) | O(V) | Shortest path (unweighted) |
| **DFS** | O(V + E) | O(V) | Cycle detection, topological sort |
| **Dijkstra** | O((V+E) log V) | O(V) | Shortest path (non-negative) |
| **Bellman-Ford** | O(V × E) | O(V) | Shortest path (negative weights) |
| **Floyd-Warshall** | O(V³) | O(V²) | All-pairs shortest path |
| **Prim's MST** | O((V+E) log V) | O(V) | Minimum spanning tree |
| **Kruskal's MST** | O(E log E) | O(V) | Minimum spanning tree |

---

## 18.2 Important Formulas

### Combinatorics
* **Permutation:** P(n, r) = n! / (n-r)!
* **Combination:** C(n, r) = n! / (r! × (n-r)!)
* **Sum of first n natural numbers:** n(n+1)/2
* **Sum of squares:** n(n+1)(2n+1)/6

### Tree Properties
* **Binary tree max nodes at level L:** 2^L
* **Perfect binary tree nodes:** 2^(h+1) - 1
* **Relation:** n = internal nodes + leaves
* **Binary tree:** leaves = internal nodes + 1 (for full tree)

### Graph Properties
* **Complete graph edges:** n(n-1)/2 (undirected)
* **Tree edges:** n - 1 (for n vertices)
* **Handshaking lemma:** Σ deg(v) = 2 × |E|

---

## 18.3 Problem-Solving Strategies

### 1. Two Pointers
**When:** Sorted array, pair problems, sliding window
**Example:** Two sum in sorted array, container with most water

### 2. Sliding Window
**When:** Contiguous subarray/substring problems
**Example:** Max sum subarray of size k, longest substring without repeat

### 3. Fast & Slow Pointers
**When:** Cycle detection, finding middle
**Example:** Linked list cycle, find middle of linked list

### 4. Binary Search Variations
**When:** Sorted data, search space can be divided
**Example:** Search in rotated array, find peak element

### 5. BFS/DFS
**When:** Tree/graph traversal, connectivity, paths
**Example:** Level order, shortest path, detect cycle

### 6. Dynamic Programming
**When:** Overlapping subproblems, optimal substructure
**Example:** Fibonacci, LCS, knapsack, edit distance

### 7. Greedy
**When:** Local optimal → global optimal
**Example:** Activity selection, Huffman coding, Dijkstra

### 8. Backtracking
**When:** Generate all possibilities, constraint satisfaction
**Example:** N-Queens, Sudoku, permutations

---

## 18.4 Common Coding Patterns

### Pattern 1: Frequency Counter
```cpp
unordered_map<int, int> freq;
for (int num : arr)
    freq[num]++;
```

### Pattern 2: Multiple Passes
```cpp
// Pass 1: Collect information
// Pass 2: Use information to solve
```

### Pattern 3: In-place Modification
```cpp
// Use array itself for storage
// Negative marking, swapping, etc.
```

### Pattern 4: Dummy Node (Linked List)
```cpp
Node* dummy = new Node(0);
dummy->next = head;
```

---

## 18.5 Interview Tips

### Before Coding
1. **Understand the problem:** Ask clarifying questions
2. **Think of examples:** Include edge cases
3. **Brute force first:** Establish baseline
4. **Optimize:** Think of better approach
5. **Walk through:** Verify logic with example

### While Coding
1. **Clean code:** Meaningful names, proper indentation
2. **Modular:** Break into functions if large
3. **Comments:** For complex logic
4. **Edge cases:** Handle null, empty, single element

### After Coding
1. **Dry run:** Test with examples
2. **Edge cases:** Empty input, single element, duplicates
3. **Complexity analysis:** State time and space
4. **Optimize further:** If possible

---

## 18.6 Must-Know Problems for BPSC TRE

### Arrays
1. Maximum subarray sum (Kadane's)
2. Two sum problem
3. Rotate array
4. Merge sorted arrays

### Linked Lists
1. Reverse linked list
2. Detect and remove cycle
3. Merge two sorted lists
4. Find middle element

### Trees
1. Tree traversals (inorder, preorder, postorder, level order)
2. Height and diameter
3. Lowest common ancestor
4. Check if BST

### Graphs
1. BFS and DFS implementation
2. Detect cycle
3. Shortest path (Dijkstra, BFS)
4. Topological sort

### Dynamic Programming
1. Fibonacci
2. Longest common subsequence
3. 0/1 Knapsack
4. Coin change
5. Edit distance

### Sorting & Searching
1. Merge sort and quick sort implementation
2. Binary search and variations
3. Search in rotated array

---

## 📝 Final MCQs for Module 18

### Q1. Which data structure provides O(1) average case for search, insert, delete?
A. Array  
B. Linked List  
C. Hash Table  
D. BST

> **Answer: C**  
> **Explanation:** Hash table with good hash function provides O(1) average for all three operations.

### Q2. For finding shortest path in unweighted graph, use:
A. Dijkstra  
B. BFS  
C. DFS  
D. Bellman-Ford

> **Answer: B**  
> **Explanation:** BFS finds shortest path (minimum edges) in unweighted graphs.

### Q3. Which sorting is best for large data that doesn't fit in RAM?
A. Quick Sort  
B. Heap Sort  
C. Merge Sort  
D. Insertion Sort

> **Answer: C**  
> **Explanation:** External merge sort efficiently handles data too large for RAM.

### Q4. Two pointers technique is useful for:
A. Tree traversal  
B. Sorted array problems  
C. Graph coloring  
D. Matrix multiplication

> **Answer: B**  
> **Explanation:** Two pointers efficiently solve many sorted array problems like two sum, triplet sum.

### Q5. Space complexity of recursive solution with n recursive calls:
A. O(1)  
B. O(log n)  
C. O(n)  
D. O(n²)

> **Answer: C**  
> **Explanation:** Each recursive call adds to call stack, n calls = O(n) space.

### Q6. Best approach for "find all subsets" problem:
A. Dynamic Programming  
B. Greedy  
C. Backtracking  
D. Divide and Conquer

> **Answer: C**  
> **Explanation:** Backtracking systematically generates all possible subsets.

### Q7. LRU Cache uses which data structures?
A. Array + Stack  
B. Hash Map + Doubly Linked List  
C. BST + Queue  
D. Heap + Array

> **Answer: B**  
> **Explanation:** Hash map for O(1) lookup, doubly linked list for O(1) removal and insertion.

### Q8. For range sum queries with updates, use:
A. Array  
B. Segment Tree or Fenwick Tree  
C. Linked List  
D. Stack

> **Answer: B**  
> **Explanation:** Segment tree and Fenwick tree provide O(log n) for both query and update.

---

# 🎓 CONCLUSION

Congratulations! You have completed the comprehensive DSA master notes covering all 18 modules. These notes are designed specifically for BPSC TRE (Computer Science) and similar competitive teaching exams.

## Key Takeaways

1. **Master the fundamentals:** Time/space complexity, basic data structures
2. **Practice implementations:** Code all major algorithms by hand
3. **Understand trade-offs:** When to use which data structure/algorithm
4. **Solve problems:** Practice on platforms like LeetCode, GeeksforGeeks
5. **Review regularly:** Especially complexity tables and key algorithms

## Recommended Study Plan

**Week 1-2:** Modules 1-5 (Basics, Arrays, Linked Lists, Stacks/Queues, Recursion)  
**Week 3-4:** Modules 6-8 (Trees, Heaps, Hashing)  
**Week 5-6:** Modules 9-10 (Graphs and Graph Algorithms)  
**Week 7-8:** Modules 11-12 (Searching and Sorting)  
**Week 9-10:** Modules 13-15 (Algorithm Design Paradigms, DP, Greedy)  
**Week 11-12:** Modules 16-17 (String Algorithms, Advanced DS)  
**Week 13-14:** Module 18 (Revision) + Practice MCQs

## Next Steps

1. Attempt the comprehensive MCQ practice sheet
2. Solve problems from each module
3. Implement all major algorithms from scratch
4. Take mock tests regularly
5. Review weak areas identified in practice

**Best of luck for BPSC TRE and your teaching career! 🎉**

---

**Document prepared by:** Senior Computer Science Faculty  
**Last updated:** 2024  
**For:** BPSC TRE, UPPSC Polytechnic Lecturer, STET, and similar exams

---

