# DBMS MCQ Sheet (260 Questions)

**Format:** Question → Options (A–D) → Correct Option → Explanation

---

## Q1. In SQL, the command 'CREATE' belongs to which category?

A. DCL  
B. DML  
C. TCL  
D. DDL  

> **Correct Option: D**  
> **Explanation:** CREATE defines schema objects, so it is DDL.

## Q2. In SQL, the command 'ALTER' belongs to which category?

A. TCL  
B. DCL  
C. DDL  
D. DML  

> **Correct Option: C**  
> **Explanation:** ALTER changes table structure, hence DDL.

## Q3. In SQL, the command 'DROP' belongs to which category?

A. DML  
B. TCL  
C. DCL  
D. DDL  

> **Correct Option: D**  
> **Explanation:** DROP removes schema objects, a DDL operation.

## Q4. In SQL, the command 'TRUNCATE' belongs to which category?

A. DML  
B. DCL  
C. DDL  
D. TCL  

> **Correct Option: C**  
> **Explanation:** TRUNCATE removes all rows via a DDL-style operation in most DBMS.

## Q5. In SQL, the command 'INSERT' belongs to which category?

A. DDL  
B. DCL  
C. TCL  
D. DML  

> **Correct Option: D**  
> **Explanation:** INSERT changes table data, hence DML.

## Q6. In SQL, the command 'UPDATE' belongs to which category?

A. DDL  
B. TCL  
C. DCL  
D. DML  

> **Correct Option: D**  
> **Explanation:** UPDATE modifies rows, so it is DML.

## Q7. In SQL, the command 'DELETE' belongs to which category?

A. DCL  
B. DDL  
C. DML  
D. TCL  

> **Correct Option: C**  
> **Explanation:** DELETE removes rows, so it is DML.

## Q8. In SQL, the command 'GRANT' belongs to which category?

A. DDL  
B. TCL  
C. DCL  
D. DML  

> **Correct Option: C**  
> **Explanation:** GRANT controls permissions, so it is DCL.

## Q9. In SQL, the command 'REVOKE' belongs to which category?

A. DCL  
B. DML  
C. DDL  
D. TCL  

> **Correct Option: A**  
> **Explanation:** REVOKE removes permissions, hence DCL.

## Q10. In SQL, the command 'COMMIT' belongs to which category?

A. DML  
B. DCL  
C. TCL  
D. DDL  

> **Correct Option: C**  
> **Explanation:** COMMIT ends a transaction and makes changes permanent, so it is TCL.

## Q11. In ACID properties, what best describes **Atomicity**?

A. Isolation from other concurrent transactions  
B. Permanence of committed data  
C. Moving from one valid state to another  
D. All-or-nothing execution of a transaction  

> **Correct Option: D**  
> **Explanation:** Atomicity means either all operations happen or none (rollback).

## Q12. In ACID properties, what best describes **Consistency**?

A. Committed changes survive failures  
B. Independent execution of transactions  
C. All-or-nothing execution  
D. A transaction preserves database constraints  

> **Correct Option: D**  
> **Explanation:** Consistency means constraints/invariants remain satisfied.

## Q13. In ACID properties, what best describes **Isolation**?

A. Committed changes survive failures  
B. All-or-nothing execution  
C. Concurrent transactions appear to run one-by-one  
D. Preserve constraints  

> **Correct Option: C**  
> **Explanation:** Isolation hides intermediate results from other transactions.

## Q14. In ACID properties, what best describes **Durability**?

A. Transactions preserve constraints  
B. Concurrent transactions appear serial  
C. All-or-nothing execution  
D. Committed changes persist even after a crash  

> **Correct Option: D**  
> **Explanation:** Durability ensures commit is permanent using logs/storage.

## Q15. Which statement best characterizes 1NF?

A. Eliminates repeating groups and ensures atomic attributes  
B. Eliminates partial dependency  
C. Eliminates multivalued dependency  
D. Eliminates transitive dependency  

> **Correct Option: A**  
> **Explanation:** 1NF requires each attribute value to be atomic (no repeating groups).

## Q16. Which statement best characterizes 2NF?

A. Eliminates join dependency  
B. Eliminates partial dependency  
C. Eliminates transitive dependency  
D. Eliminates repeating groups  

> **Correct Option: B**  
> **Explanation:** 2NF removes partial dependency on a composite key.

## Q17. Which statement best characterizes 3NF?

A. Eliminates partial dependency  
B. Eliminates multivalued dependency  
C. Eliminates repeating groups  
D. Eliminates transitive dependency  

> **Correct Option: D**  
> **Explanation:** 3NF removes non-key → non-key (transitive) dependencies.

## Q18. Which statement best characterizes BCNF?

A. No multivalued dependency  
B. Every non-key depends on key  
C. Every determinant is a super key  
D. No join dependency  

> **Correct Option: C**  
> **Explanation:** BCNF strengthens 3NF: for every FD X→Y, X must be a superkey.

## Q19. Which statement best characterizes 4NF?

A. Eliminates repeating groups  
B. Eliminates partial dependency  
C. Eliminates transitive dependency  
D. Eliminates multivalued dependency  

> **Correct Option: D**  
> **Explanation:** 4NF deals with multivalued dependencies (MVDs).

## Q20. Which statement best characterizes 5NF?

A. Eliminates join dependency (project-join NF)  
B. Eliminates partial dependency  
C. Eliminates multivalued dependency  
D. Eliminates transitive dependency  

> **Correct Option: A**  
> **Explanation:** 5NF addresses join dependencies not implied by candidate keys.

## Q21. What does a INNER JOIN do?

A. Returns only matching rows from both tables  
B. Returns all rows from right plus matches  
C. Returns all rows from both tables  
D. Returns all rows from left plus matches  

> **Correct Option: A**  
> **Explanation:** INNER JOIN keeps only rows satisfying the join condition in both tables.

## Q22. What does a LEFT OUTER JOIN do?

A. Returns all rows from left table and matching rows from right table  
B. All rows from both  
C. All rows from right and matching left  
D. Only matching rows  

> **Correct Option: A**  
> **Explanation:** LEFT JOIN preserves all left rows; missing right side becomes NULL.

## Q23. What does a RIGHT OUTER JOIN do?

A. Only matching rows  
B. All rows from both  
C. All rows from left and matching right  
D. Returns all rows from right table and matching rows from left table  

> **Correct Option: D**  
> **Explanation:** RIGHT JOIN preserves all right rows; missing left side becomes NULL.

## Q24. What does a FULL OUTER JOIN do?

A. All rows from left only  
B. All rows from right only  
C. Returns all rows from both tables, matching where possible  
D. Only matching rows  

> **Correct Option: C**  
> **Explanation:** FULL OUTER JOIN is union of left and right joins.

## Q25. What does a CROSS JOIN do?

A. Returns grouped rows  
B. Returns the Cartesian product of two tables  
C. Returns only matching rows  
D. Returns rows with duplicates removed  

> **Correct Option: B**  
> **Explanation:** CROSS JOIN pairs each row of one table with every row of the other.

## Q26. What does a SELF JOIN do?

A. Join between unrelated databases  
B. Join that requires three tables  
C. A table is joined with itself using aliases  
D. Join that returns only NULLs  

> **Correct Option: C**  
> **Explanation:** SELF JOIN uses aliases to relate rows within the same table (e.g., employee-manager).

## Q27. Which option best defines a **Super key**?

A. Attribute referring to another table  
B. Chosen candidate key for identification  
C. Minimal unique attribute set  
D. Any attribute set that uniquely identifies a tuple  

> **Correct Option: D**  
> **Explanation:** A super key may contain extra attributes but still uniquely identifies rows.

## Q28. Which option best defines a **Candidate key**?

A. Any unique attribute set  
B. A foreign key  
C. A minimal super key  
D. A non-unique attribute  

> **Correct Option: C**  
> **Explanation:** Candidate keys are minimal unique identifiers (no proper subset is unique).

## Q29. Which option best defines a **Primary key**?

A. A key used only for sorting  
B. Any super key  
C. A chosen candidate key that is UNIQUE and NOT NULL  
D. A key that may contain NULL  

> **Correct Option: C**  
> **Explanation:** Primary key is selected from candidate keys and cannot be NULL.

## Q30. Which option best defines a **Alternate key**?

A. Candidate keys not chosen as the primary key  
B. Keys that reference other tables  
C. Keys formed by combining two tables  
D. Keys that allow duplicates  

> **Correct Option: A**  
> **Explanation:** Alternate keys are the remaining candidate keys.

## Q31. Which option best defines a **Foreign key**?

A. Chosen candidate key  
B. Attribute(s) in one table referencing a key in another table  
C. A multivalued attribute  
D. Minimal super key  

> **Correct Option: B**  
> **Explanation:** Foreign keys enforce referential integrity between tables.

## Q32. Which option best defines a **Composite key**?

A. A key made of two or more attributes  
B. A key derived from another key  
C. A key used for encryption  
D. A key that allows NULL  

> **Correct Option: A**  
> **Explanation:** Composite keys combine multiple attributes to uniquely identify a tuple.

## Q33. In an ER diagram, the symbol 'Rectangle' represents:

A. Entity set  
B. Attribute  
C. Relationship set  
D. Weak entity  

> **Correct Option: A**  
> **Explanation:** In ER diagrams, rectangles represent entity sets.

## Q34. In an ER diagram, the symbol 'Ellipse' represents:

A. Entity set  
B. Identifying relationship  
C. Attribute  
D. Relationship set  

> **Correct Option: C**  
> **Explanation:** Ellipses represent attributes.

## Q35. In an ER diagram, the symbol 'Diamond' represents:

A. Entity set  
B. Attribute  
C. Relationship set  
D. Weak entity  

> **Correct Option: C**  
> **Explanation:** Diamonds represent relationships between entity sets.

## Q36. In an ER diagram, the symbol 'Double rectangle' represents:

A. Multivalued attribute  
B. Derived attribute  
C. Relationship set  
D. Weak entity set  

> **Correct Option: D**  
> **Explanation:** Weak entities are drawn with double rectangles.

## Q37. In an ER diagram, the symbol 'Double ellipse' represents:

A. Derived attribute  
B. Multivalued attribute  
C. Composite attribute  
D. Weak entity  

> **Correct Option: B**  
> **Explanation:** Multivalued attributes are shown using double ellipses.

## Q38. In an ER diagram, the symbol 'Dashed ellipse' represents:

A. Derived attribute  
B. Weak entity  
C. Multivalued attribute  
D. Relationship set  

> **Correct Option: A**  
> **Explanation:** Derived attributes are shown with dashed ellipses.

## Q39. In relational algebra, what does Selection (σ) do?

A. Filters columns  
B. Filters rows based on a predicate  
C. Renames a relation  
D. Combines every row of two relations  

> **Correct Option: B**  
> **Explanation:** Selection chooses tuples satisfying a condition.

## Q40. In relational algebra, what does Projection (π) do?

A. Sorts tuples  
B. Selects rows only  
C. Adds new tuples  
D. Selects columns and removes duplicate tuples  

> **Correct Option: D**  
> **Explanation:** Projection returns specified attributes; in relational algebra duplicates are removed.

## Q41. In relational algebra, what does Cartesian product (×) do?

A. Subtracts tuples  
B. Returns only matching tuples  
C. Pairs each tuple of one relation with every tuple of another  
D. Returns common tuples only  

> **Correct Option: C**  
> **Explanation:** Cartesian product forms all combinations of tuples.

## Q42. In relational algebra, what does Union (∪) do?

A. Returns tuples in first but not second  
B. Returns tuples common to both  
C. Returns tuples in either relation (union-compatible relations)  
D. Returns all combinations  

> **Correct Option: C**  
> **Explanation:** Union requires union compatibility (same attributes/domains).

## Q43. In relational algebra, what does Set difference (-) do?

A. Renames attributes  
B. Returns tuples common to both  
C. Returns all combinations  
D. Returns tuples in first relation but not in second (union-compatible)  

> **Correct Option: D**  
> **Explanation:** Difference removes tuples present in the second relation.

## Q44. Which option best describes the anomaly **Dirty read**?

A. Two writes overwrite each other  
B. Reading uncommitted data from another transaction  
C. Seeing extra rows appear in repeated query  
D. Reading same row twice and getting different values  

> **Correct Option: B**  
> **Explanation:** Dirty read occurs when a transaction reads data written but not committed by another.

## Q45. Which option best describes the anomaly **Non-repeatable read**?

A. Reading uncommitted data  
B. Reading the same row twice and getting different values  
C. Two writes conflict  
D. Seeing new rows appear matching a predicate  

> **Correct Option: B**  
> **Explanation:** Another transaction commits an update between the two reads.

## Q46. Which option best describes the anomaly **Phantom read**?

A. Reading same row twice different  
B. Seeing new/deleted rows appear in repeated predicate query  
C. Lost update  
D. Reading uncommitted data  

> **Correct Option: B**  
> **Explanation:** Phantoms arise due to inserts/deletes that change the result set of a predicate.

## Q47. Which option best describes the anomaly **Lost update**?

A. Update that violates a constraint  
B. Reading uncommitted data  
C. Seeing extra rows  
D. Two transactions update same item; one update overwrites the other  

> **Correct Option: D**  
> **Explanation:** Lost update happens when concurrent updates are not properly isolated.

## Q48. Which statement is TRUE about the isolation level READ UNCOMMITTED?

A. Prevents dirty reads  
B. Prevents phantoms  
C. Allows dirty reads  
D. Prevents non-repeatable reads  

> **Correct Option: C**  
> **Explanation:** READ UNCOMMITTED is the weakest isolation; dirty reads can occur.

## Q49. Which statement is TRUE about the isolation level READ COMMITTED?

A. Guarantees serializability  
B. Prevents dirty reads but allows non-repeatable reads  
C. Allows dirty reads  
D. Prevents phantoms  

> **Correct Option: B**  
> **Explanation:** READ COMMITTED blocks dirty reads but updates between reads can occur.

## Q50. Which statement is TRUE about the isolation level REPEATABLE READ?

A. Allows dirty reads  
B. Prevents all anomalies  
C. Is weaker than READ COMMITTED  
D. Prevents non-repeatable reads but may allow phantom reads  

> **Correct Option: D**  
> **Explanation:** Repeatable read ensures same row reads consistent; phantoms may still appear.

## Q51. Which statement is TRUE about the isolation level SERIALIZABLE?

A. Only prevents lost updates  
B. Allows phantoms  
C. Only prevents dirty reads  
D. Prevents dirty, non-repeatable, and phantom reads  

> **Correct Option: D**  
> **Explanation:** SERIALIZABLE provides the strongest isolation equivalent to serial execution.

## Q52. Which statement is correct about B+ tree?

A. Keys stored only in internal nodes  
B. Unbalanced tree  
C. Not suitable for range queries  
D. All actual data pointers are stored at leaf level; leaves are linked  

> **Correct Option: D**  
> **Explanation:** B+ tree keeps data pointers in leaves and links leaves for efficient range scans.

## Q53. Which statement is correct about B-tree?

A. Keys and data pointers may appear in both internal and leaf nodes  
B. Works only with hashing  
C. Always unbalanced  
D. All keys only in leaves  

> **Correct Option: A**  
> **Explanation:** In B-trees, records/pointers can be stored in internal nodes as well.

## Q54. Which statement is correct about Hash index?

A. Optimized for equality search; poor for range queries  
B. Always keeps data sorted  
C. Requires full table scan  
D. Best for range queries  

> **Correct Option: A**  
> **Explanation:** Hashing maps keys to buckets; great for '=' lookups, weak for ranges.

## Q55. Which statement is correct about Clustered index?

A. Is always a secondary index  
B. Determines the physical order of rows on disk (typically one per table)  
C. Can exist unlimited times per table  
D. Stores only pointers, never affects row order  

> **Correct Option: B**  
> **Explanation:** Clustered index defines row order; many DBMS allow one clustered index.

## Q56. Which statement is correct about Dense index?

A. Has an index entry for every search-key value (often every record)  
B. Cannot be used for secondary indexes  
C. Has entries only for some blocks  
D. Requires sorted file only  

> **Correct Option: A**  
> **Explanation:** Dense index contains an entry for each record/key value.

## Q57. Which statement is correct about Sparse index?

A. Has index entries for only some search-key values (e.g., one per block)  
B. Has entries for every record  
C. Works only on unsorted files  
D. Requires hashing  

> **Correct Option: A**  
> **Explanation:** Sparse indexes are smaller but require ordered data file.

## Q58. Relation R has 5 tuples and relation S has 9 tuples. How many tuples will R × S have?

A. 14  
B. 45  
C. 56  
D. 44  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 5 × 9 = 45.

## Q59. Relation R has degree 3 and relation S has degree 2. What is the degree of R × S?

A. 6  
B. 1  
C. 3  
D. 5  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 3 + 2 = 5.

## Q60. Relation R has 9 tuples and relation S has 4 tuples. How many tuples will R × S have?

A. 36  
B. 33  
C. 47  
D. 13  

> **Correct Option: A**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 9 × 4 = 36.

## Q61. Relation R has degree 2 and relation S has degree 8. What is the degree of R × S?

A. 8  
B. 10  
C. 11  
D. 6  

> **Correct Option: B**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 2 + 8 = 10.

## Q62. Relation R has 25 tuples and relation S has 30 tuples. How many tuples will R × S have?

A. 742  
B. 750  
C. 55  
D. 766  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 25 × 30 = 750.

## Q63. Relation R has degree 6 and relation S has degree 6. What is the degree of R × S?

A. 0  
B. 6  
C. 13  
D. 12  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 6 + 6 = 12.

## Q64. Relation R has 13 tuples and relation S has 15 tuples. How many tuples will R × S have?

A. 28  
B. 191  
C. 197  
D. 195  

> **Correct Option: D**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 13 × 15 = 195.

## Q65. Relation R has degree 5 and relation S has degree 5. What is the degree of R × S?

A. 11  
B. 0  
C. 5  
D. 10  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 5 + 5 = 10.

## Q66. Relation R has 8 tuples and relation S has 19 tuples. How many tuples will R × S have?

A. 27  
B. 152  
C. 166  
D. 146  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 8 × 19 = 152.

## Q67. Relation R has degree 5 and relation S has degree 3. What is the degree of R × S?

A. 5  
B. 9  
C. 2  
D. 8  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 5 + 3 = 8.

## Q68. Relation R has 3 tuples and relation S has 22 tuples. How many tuples will R × S have?

A. 25  
B. 67  
C. 66  
D. 63  

> **Correct Option: C**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 3 × 22 = 66.

## Q69. Relation R has degree 6 and relation S has degree 8. What is the degree of R × S?

A. 8  
B. 14  
C. 2  
D. 15  

> **Correct Option: B**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 6 + 8 = 14.

## Q70. Relation R has 29 tuples and relation S has 14 tuples. How many tuples will R × S have?

A. 406  
B. 405  
C. 43  
D. 419  

> **Correct Option: A**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 29 × 14 = 406.

## Q71. Relation R has degree 2 and relation S has degree 3. What is the degree of R × S?

A. 5  
B. 3  
C. 6  
D. 1  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 2 + 3 = 5.

## Q72. Relation R has 6 tuples and relation S has 8 tuples. How many tuples will R × S have?

A. 14  
B. 29  
C. 50  
D. 48  

> **Correct Option: D**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 6 × 8 = 48.

## Q73. Relation R has degree 4 and relation S has degree 3. What is the degree of R × S?

A. 8  
B. 1  
C. 4  
D. 7  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 4 + 3 = 7.

## Q74. Relation R has 18 tuples and relation S has 29 tuples. How many tuples will R × S have?

A. 524  
B. 505  
C. 47  
D. 522  

> **Correct Option: D**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 18 × 29 = 522.

## Q75. Relation R has degree 6 and relation S has degree 3. What is the degree of R × S?

A. 10  
B. 3  
C. 6  
D. 9  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 6 + 3 = 9.

## Q76. Relation R has 14 tuples and relation S has 5 tuples. How many tuples will R × S have?

A. 19  
B. 89  
C. 50  
D. 70  

> **Correct Option: D**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 14 × 5 = 70.

## Q77. Relation R has degree 6 and relation S has degree 3. What is the degree of R × S?

A. 9  
B. 10  
C. 6  
D. 3  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 6 + 3 = 9.

## Q78. Relation R has 10 tuples and relation S has 8 tuples. How many tuples will R × S have?

A. 18  
B. 80  
C. 91  
D. 72  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 10 × 8 = 80.

## Q79. Relation R has degree 7 and relation S has degree 7. What is the degree of R × S?

A. 14  
B. 15  
C. 0  
D. 7  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 7 + 7 = 14.

## Q80. Relation R has 26 tuples and relation S has 4 tuples. How many tuples will R × S have?

A. 85  
B. 30  
C. 124  
D. 104  

> **Correct Option: D**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 26 × 4 = 104.

## Q81. Relation R has degree 2 and relation S has degree 5. What is the degree of R × S?

A. 8  
B. 5  
C. 7  
D. 3  

> **Correct Option: C**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 2 + 5 = 7.

## Q82. Relation R has 30 tuples and relation S has 4 tuples. How many tuples will R × S have?

A. 120  
B. 130  
C. 114  
D. 34  

> **Correct Option: A**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 30 × 4 = 120.

## Q83. Relation R has degree 3 and relation S has degree 4. What is the degree of R × S?

A. 4  
B. 1  
C. 8  
D. 7  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 3 + 4 = 7.

## Q84. Relation R has 23 tuples and relation S has 5 tuples. How many tuples will R × S have?

A. 115  
B. 119  
C. 28  
D. 111  

> **Correct Option: A**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 23 × 5 = 115.

## Q85. Relation R has degree 3 and relation S has degree 4. What is the degree of R × S?

A. 7  
B. 4  
C. 8  
D. 1  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 3 + 4 = 7.

## Q86. Relation R has 8 tuples and relation S has 23 tuples. How many tuples will R × S have?

A. 193  
B. 184  
C. 167  
D. 31  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 8 × 23 = 184.

## Q87. Relation R has degree 7 and relation S has degree 8. What is the degree of R × S?

A. 16  
B. 1  
C. 8  
D. 15  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 7 + 8 = 15.

## Q88. Relation R has 28 tuples and relation S has 10 tuples. How many tuples will R × S have?

A. 38  
B. 291  
C. 280  
D. 275  

> **Correct Option: C**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 28 × 10 = 280.

## Q89. Relation R has degree 2 and relation S has degree 2. What is the degree of R × S?

A. 2  
B. 4  
C. 5  
D. 0  

> **Correct Option: B**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 2 + 2 = 4.

## Q90. Relation R has 5 tuples and relation S has 4 tuples. How many tuples will R × S have?

A. 9  
B. 20  
C. 38  
D. 18  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 5 × 4 = 20.

## Q91. Relation R has degree 7 and relation S has degree 3. What is the degree of R × S?

A. 11  
B. 7  
C. 10  
D. 4  

> **Correct Option: C**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 7 + 3 = 10.

## Q92. Relation R has 11 tuples and relation S has 13 tuples. How many tuples will R × S have?

A. 131  
B. 143  
C. 24  
D. 145  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 11 × 13 = 143.

## Q93. Relation R has degree 8 and relation S has degree 8. What is the degree of R × S?

A. 17  
B. 8  
C. 0  
D. 16  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 8 + 8 = 16.

## Q94. Relation R has 21 tuples and relation S has 25 tuples. How many tuples will R × S have?

A. 46  
B. 531  
C. 525  
D. 519  

> **Correct Option: C**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 21 × 25 = 525.

## Q95. Relation R has degree 3 and relation S has degree 3. What is the degree of R × S?

A. 7  
B. 6  
C. 0  
D. 3  

> **Correct Option: B**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 3 + 3 = 6.

## Q96. Relation R has 10 tuples and relation S has 7 tuples. How many tuples will R × S have?

A. 57  
B. 17  
C. 74  
D. 70  

> **Correct Option: D**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 10 × 7 = 70.

## Q97. Relation R has degree 8 and relation S has degree 7. What is the degree of R × S?

A. 15  
B. 8  
C. 16  
D. 1  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 8 + 7 = 15.

## Q98. Which clause is logically evaluated first in a SELECT query?

A. SELECT  
B. ORDER BY  
C. FROM  
D. WHERE  

> **Correct Option: C**  
> **Explanation:** SQL logically starts by forming the source row set using FROM (and JOIN).

## Q99. Which clause filters groups after GROUP BY?

A. WHERE  
B. ORDER BY  
C. FROM  
D. HAVING  

> **Correct Option: D**  
> **Explanation:** HAVING applies conditions on groups after aggregation.

## Q100. Which clause filters individual rows before grouping?

A. WHERE  
B. ORDER BY  
C. HAVING  
D. SELECT  

> **Correct Option: A**  
> **Explanation:** WHERE filters rows before GROUP BY forms groups.

## Q101. What is the main purpose of the SQL constraint PRIMARY KEY?

A. Only improves query speed  
B. Allows multiple NULLs and duplicates  
C. Allows duplicates  
D. Enforces uniqueness and disallows NULL  

> **Correct Option: D**  
> **Explanation:** Primary key uniquely identifies each row and cannot be NULL.

## Q102. What is the main purpose of the SQL constraint UNIQUE?

A. Enforces uniqueness of column values (NULL handling is DBMS-specific)  
B. Disallows duplicates and NULL always  
C. Allows duplicates  
D. Enforces referential integrity  

> **Correct Option: A**  
> **Explanation:** UNIQUE prevents duplicate non-NULL values; some DBMS allow a NULL (or multiple).

## Q103. What is the main purpose of the SQL constraint FOREIGN KEY?

A. Ensures row uniqueness  
B. Ensures attribute is atomic  
C. Ensures sorted order  
D. Ensures referenced value exists in parent table  

> **Correct Option: D**  
> **Explanation:** Foreign keys enforce referential integrity.

## Q104. What is the main purpose of the SQL constraint CHECK?

A. Restricts column values based on a condition  
B. Starts a transaction  
C. Grants permissions  
D. Creates an index  

> **Correct Option: A**  
> **Explanation:** CHECK enforces domain-like predicates (e.g., salary > 0).

## Q105. What is the main purpose of the SQL constraint NOT NULL?

A. Disallows updates  
B. Disallows duplicates  
C. Disallows inserts  
D. Disallows NULL values in a column  

> **Correct Option: D**  
> **Explanation:** NOT NULL ensures every row has a value for the column.

## Q106. In TCL, what does COMMIT do?

A. Makes all changes of the current transaction permanent  
B. Undoes changes  
C. Grants privileges  
D. Creates a savepoint  

> **Correct Option: A**  
> **Explanation:** COMMIT ends the transaction and makes its changes durable.

## Q107. In TCL, what does ROLLBACK do?

A. Makes changes permanent  
B. Undoes changes made in the current transaction since last COMMIT  
C. Optimizes query  
D. Adds a column  

> **Correct Option: B**  
> **Explanation:** ROLLBACK restores the database to the last committed state (or savepoint).

## Q108. In TCL, what does SAVEPOINT do?

A. Deletes a table  
B. Marks a point within a transaction to roll back to  
C. Ends a transaction  
D. Creates a view  

> **Correct Option: B**  
> **Explanation:** SAVEPOINT allows partial rollback inside a transaction.

## Q109. Which statement best describes the DBMS feature 'Data abstraction'?

A. Prevents normalization  
B. Creates redundancy  
C. Hides storage details and shows only necessary views  
D. Disables security  

> **Correct Option: C**  
> **Explanation:** DBMS provides levels of abstraction (external/conceptual/internal).

## Q110. Which statement best describes the DBMS feature 'Data security'?

A. Stores data in plaintext  
B. Eliminates transactions  
C. Duplicates data across files  
D. Restricts unauthorized access using authorization mechanisms  

> **Correct Option: D**  
> **Explanation:** DBMS supports GRANT/REVOKE and roles/privileges.

## Q111. Which statement best describes the DBMS feature 'Concurrency control'?

A. Eliminates indexes  
B. Allows safe simultaneous access by multiple users  
C. Forces serial execution always  
D. Removes need for transactions  

> **Correct Option: B**  
> **Explanation:** Locking/MVCC prevent anomalies under concurrent access.

## Q112. Which statement best describes the DBMS feature 'Backup and recovery'?

A. Restores data after crashes using logs and backups  
B. Makes queries slower by design  
C. Prevents schema changes  
D. Avoids using disk  

> **Correct Option: A**  
> **Explanation:** Recovery manager uses logs (UNDO/REDO) and checkpoints.

## Q113. A deadlock in DBMS occurs when:

A. A query uses ORDER BY  
B. A transaction finishes too quickly  
C. A table has no primary key  
D. Two or more transactions wait indefinitely for each other’s locks  

> **Correct Option: D**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q114. A deadlock in DBMS occurs when:

A. Two or more transactions wait indefinitely for each other’s locks  
B. A transaction finishes too quickly  
C. A query uses ORDER BY  
D. A table has no primary key  

> **Correct Option: A**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q115. A deadlock in DBMS occurs when:

A. Two or more transactions wait indefinitely for each other’s locks  
B. A query uses ORDER BY  
C. A transaction finishes too quickly  
D. A table has no primary key  

> **Correct Option: A**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q116. A deadlock in DBMS occurs when:

A. A table has no primary key  
B. A query uses ORDER BY  
C. Two or more transactions wait indefinitely for each other’s locks  
D. A transaction finishes too quickly  

> **Correct Option: C**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q117. A deadlock in DBMS occurs when:

A. A transaction finishes too quickly  
B. Two or more transactions wait indefinitely for each other’s locks  
C. A table has no primary key  
D. A query uses ORDER BY  

> **Correct Option: B**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q118. A deadlock in DBMS occurs when:

A. A query uses ORDER BY  
B. Two or more transactions wait indefinitely for each other’s locks  
C. A transaction finishes too quickly  
D. A table has no primary key  

> **Correct Option: B**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q119. A deadlock in DBMS occurs when:

A. A query uses ORDER BY  
B. Two or more transactions wait indefinitely for each other’s locks  
C. A transaction finishes too quickly  
D. A table has no primary key  

> **Correct Option: B**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q120. A deadlock in DBMS occurs when:

A. Two or more transactions wait indefinitely for each other’s locks  
B. A transaction finishes too quickly  
C. A table has no primary key  
D. A query uses ORDER BY  

> **Correct Option: A**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q121. A deadlock in DBMS occurs when:

A. Two or more transactions wait indefinitely for each other’s locks  
B. A table has no primary key  
C. A transaction finishes too quickly  
D. A query uses ORDER BY  

> **Correct Option: A**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q122. A deadlock in DBMS occurs when:

A. Two or more transactions wait indefinitely for each other’s locks  
B. A query uses ORDER BY  
C. A table has no primary key  
D. A transaction finishes too quickly  

> **Correct Option: A**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q123. What is the main purpose of the SQL constraint UNIQUE? (Choose the best answer.)

A. Enforces uniqueness of column values (NULL handling is DBMS-specific)  
B. Disallows duplicates and NULL always  
C. Allows duplicates  
D. Enforces referential integrity  

> **Correct Option: A**  
> **Explanation:** UNIQUE prevents duplicate non-NULL values; some DBMS allow a NULL (or multiple).

## Q124. A deadlock in DBMS occurs when: (Choose the best answer.)

A. A table has no primary key  
B. A query uses ORDER BY  
C. Two or more transactions wait indefinitely for each other’s locks  
D. A transaction finishes too quickly  

> **Correct Option: C**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q125. What is the main purpose of the SQL constraint UNIQUE? (Choose the best answer.)

A. Enforces uniqueness of column values (NULL handling is DBMS-specific)  
B. Disallows duplicates and NULL always  
C. Allows duplicates  
D. Enforces referential integrity  

> **Correct Option: A**  
> **Explanation:** UNIQUE prevents duplicate non-NULL values; some DBMS allow a NULL (or multiple).

## Q126. Relation R has degree 3 and relation S has degree 3. What is the degree of R × S? (Choose the best answer.)

A. 7  
B. 6  
C. 0  
D. 3  

> **Correct Option: B**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 3 + 3 = 6.

## Q127. What does a LEFT OUTER JOIN do? (Choose the best answer.)

A. Returns all rows from left table and matching rows from right table  
B. All rows from both  
C. All rows from right and matching left  
D. Only matching rows  

> **Correct Option: A**  
> **Explanation:** LEFT JOIN preserves all left rows; missing right side becomes NULL.

## Q128. Relation R has degree 3 and relation S has degree 4. What is the degree of R × S? (Choose the best answer.)

A. 7  
B. 4  
C. 8  
D. 1  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 3 + 4 = 7.

## Q129. In ACID properties, what best describes **Atomicity**? (Choose the best answer.)

A. Isolation from other concurrent transactions  
B. Permanence of committed data  
C. Moving from one valid state to another  
D. All-or-nothing execution of a transaction  

> **Correct Option: D**  
> **Explanation:** Atomicity means either all operations happen or none (rollback).

## Q130. In an ER diagram, the symbol 'Double ellipse' represents: (Choose the best answer.)

A. Derived attribute  
B. Multivalued attribute  
C. Composite attribute  
D. Weak entity  

> **Correct Option: B**  
> **Explanation:** Multivalued attributes are shown using double ellipses.

## Q131. Relation R has 8 tuples and relation S has 19 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 27  
B. 152  
C. 166  
D. 146  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 8 × 19 = 152.

## Q132. Relation R has degree 3 and relation S has degree 4. What is the degree of R × S? (Choose the best answer.)

A. 7  
B. 4  
C. 8  
D. 1  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 3 + 4 = 7.

## Q133. Relation R has 30 tuples and relation S has 4 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 120  
B. 130  
C. 114  
D. 34  

> **Correct Option: A**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 30 × 4 = 120.

## Q134. Relation R has 26 tuples and relation S has 4 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 85  
B. 30  
C. 124  
D. 104  

> **Correct Option: D**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 26 × 4 = 104.

## Q135. In relational algebra, what does Set difference (-) do? (Choose the best answer.)

A. Renames attributes  
B. Returns tuples common to both  
C. Returns all combinations  
D. Returns tuples in first relation but not in second (union-compatible)  

> **Correct Option: D**  
> **Explanation:** Difference removes tuples present in the second relation.

## Q136. In ACID properties, what best describes **Consistency**? (Choose the best answer.)

A. Committed changes survive failures  
B. Independent execution of transactions  
C. All-or-nothing execution  
D. A transaction preserves database constraints  

> **Correct Option: D**  
> **Explanation:** Consistency means constraints/invariants remain satisfied.

## Q137. What is the main purpose of the SQL constraint NOT NULL? (Choose the best answer.)

A. Disallows updates  
B. Disallows duplicates  
C. Disallows inserts  
D. Disallows NULL values in a column  

> **Correct Option: D**  
> **Explanation:** NOT NULL ensures every row has a value for the column.

## Q138. Relation R has degree 8 and relation S has degree 7. What is the degree of R × S? (Choose the best answer.)

A. 15  
B. 8  
C. 16  
D. 1  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 8 + 7 = 15.

## Q139. Which option best defines a **Foreign key**? (Choose the best answer.)

A. Chosen candidate key  
B. Attribute(s) in one table referencing a key in another table  
C. A multivalued attribute  
D. Minimal super key  

> **Correct Option: B**  
> **Explanation:** Foreign keys enforce referential integrity between tables.

## Q140. Relation R has degree 7 and relation S has degree 8. What is the degree of R × S? (Choose the best answer.)

A. 16  
B. 1  
C. 8  
D. 15  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 7 + 8 = 15.

## Q141. In relational algebra, what does Projection (π) do? (Choose the best answer.)

A. Sorts tuples  
B. Selects rows only  
C. Adds new tuples  
D. Selects columns and removes duplicate tuples  

> **Correct Option: D**  
> **Explanation:** Projection returns specified attributes; in relational algebra duplicates are removed.

## Q142. Which option best defines a **Primary key**? (Choose the best answer.)

A. A key used only for sorting  
B. Any super key  
C. A chosen candidate key that is UNIQUE and NOT NULL  
D. A key that may contain NULL  

> **Correct Option: C**  
> **Explanation:** Primary key is selected from candidate keys and cannot be NULL.

## Q143. What is the main purpose of the SQL constraint CHECK? (Choose the best answer.)

A. Restricts column values based on a condition  
B. Starts a transaction  
C. Grants permissions  
D. Creates an index  

> **Correct Option: A**  
> **Explanation:** CHECK enforces domain-like predicates (e.g., salary > 0).

## Q144. What does a SELF JOIN do? (Choose the best answer.)

A. Join between unrelated databases  
B. Join that requires three tables  
C. A table is joined with itself using aliases  
D. Join that returns only NULLs  

> **Correct Option: C**  
> **Explanation:** SELF JOIN uses aliases to relate rows within the same table (e.g., employee-manager).

## Q145. Which statement best characterizes 4NF? (Choose the best answer.)

A. Eliminates repeating groups  
B. Eliminates partial dependency  
C. Eliminates transitive dependency  
D. Eliminates multivalued dependency  

> **Correct Option: D**  
> **Explanation:** 4NF deals with multivalued dependencies (MVDs).

## Q146. In SQL, the command 'TRUNCATE' belongs to which category? (Choose the best answer.)

A. DML  
B. DCL  
C. DDL  
D. TCL  

> **Correct Option: C**  
> **Explanation:** TRUNCATE removes all rows via a DDL-style operation in most DBMS.

## Q147. In SQL, the command 'UPDATE' belongs to which category? (Choose the best answer.)

A. DDL  
B. TCL  
C. DCL  
D. DML  

> **Correct Option: D**  
> **Explanation:** UPDATE modifies rows, so it is DML.

## Q148. Which option best defines a **Composite key**? (Choose the best answer.)

A. A key made of two or more attributes  
B. A key derived from another key  
C. A key used for encryption  
D. A key that allows NULL  

> **Correct Option: A**  
> **Explanation:** Composite keys combine multiple attributes to uniquely identify a tuple.

## Q149. Relation R has degree 2 and relation S has degree 8. What is the degree of R × S? (Choose the best answer.)

A. 8  
B. 10  
C. 11  
D. 6  

> **Correct Option: B**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 2 + 8 = 10.

## Q150. Relation R has degree 7 and relation S has degree 7. What is the degree of R × S? (Choose the best answer.)

A. 14  
B. 15  
C. 0  
D. 7  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 7 + 7 = 14.

## Q151. Which statement best describes the DBMS feature 'Data abstraction'? (Choose the best answer.)

A. Prevents normalization  
B. Creates redundancy  
C. Hides storage details and shows only necessary views  
D. Disables security  

> **Correct Option: C**  
> **Explanation:** DBMS provides levels of abstraction (external/conceptual/internal).

## Q152. Which clause filters groups after GROUP BY? (Choose the best answer.)

A. WHERE  
B. ORDER BY  
C. FROM  
D. HAVING  

> **Correct Option: D**  
> **Explanation:** HAVING applies conditions on groups after aggregation.

## Q153. In SQL, the command 'COMMIT' belongs to which category? (Choose the best answer.)

A. DML  
B. DCL  
C. TCL  
D. DDL  

> **Correct Option: C**  
> **Explanation:** COMMIT ends a transaction and makes changes permanent, so it is TCL.

## Q154. Relation R has degree 3 and relation S has degree 2. What is the degree of R × S? (Choose the best answer.)

A. 6  
B. 1  
C. 3  
D. 5  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 3 + 2 = 5.

## Q155. Which statement is correct about Hash index? (Choose the best answer.)

A. Optimized for equality search; poor for range queries  
B. Always keeps data sorted  
C. Requires full table scan  
D. Best for range queries  

> **Correct Option: A**  
> **Explanation:** Hashing maps keys to buckets; great for '=' lookups, weak for ranges.

## Q156. A deadlock in DBMS occurs when: (Choose the best answer.)

A. Two or more transactions wait indefinitely for each other’s locks  
B. A transaction finishes too quickly  
C. A query uses ORDER BY  
D. A table has no primary key  

> **Correct Option: A**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q157. Relation R has degree 2 and relation S has degree 5. What is the degree of R × S? (Choose the best answer.)

A. 8  
B. 5  
C. 7  
D. 3  

> **Correct Option: C**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 2 + 5 = 7.

## Q158. Relation R has 18 tuples and relation S has 29 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 524  
B. 505  
C. 47  
D. 522  

> **Correct Option: D**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 18 × 29 = 522.

## Q159. What does a CROSS JOIN do? (Choose the best answer.)

A. Returns grouped rows  
B. Returns the Cartesian product of two tables  
C. Returns only matching rows  
D. Returns rows with duplicates removed  

> **Correct Option: B**  
> **Explanation:** CROSS JOIN pairs each row of one table with every row of the other.

## Q160. Relation R has 11 tuples and relation S has 13 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 131  
B. 143  
C. 24  
D. 145  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 11 × 13 = 143.

## Q161. Relation R has 5 tuples and relation S has 4 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 9  
B. 20  
C. 38  
D. 18  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 5 × 4 = 20.

## Q162. Which statement is TRUE about the isolation level REPEATABLE READ? (Choose the best answer.)

A. Allows dirty reads  
B. Prevents all anomalies  
C. Is weaker than READ COMMITTED  
D. Prevents non-repeatable reads but may allow phantom reads  

> **Correct Option: D**  
> **Explanation:** Repeatable read ensures same row reads consistent; phantoms may still appear.

## Q163. Relation R has 13 tuples and relation S has 15 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 28  
B. 191  
C. 197  
D. 195  

> **Correct Option: D**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 13 × 15 = 195.

## Q164. Which statement is correct about B+ tree? (Choose the best answer.)

A. Keys stored only in internal nodes  
B. Unbalanced tree  
C. Not suitable for range queries  
D. All actual data pointers are stored at leaf level; leaves are linked  

> **Correct Option: D**  
> **Explanation:** B+ tree keeps data pointers in leaves and links leaves for efficient range scans.

## Q165. Which option best defines a **Composite key**? (Choose the best answer.)

A. A key made of two or more attributes  
B. A key derived from another key  
C. A key used for encryption  
D. A key that allows NULL  

> **Correct Option: A**  
> **Explanation:** Composite keys combine multiple attributes to uniquely identify a tuple.

## Q166. Which statement best characterizes 4NF? (Choose the best answer.)

A. Eliminates repeating groups  
B. Eliminates partial dependency  
C. Eliminates transitive dependency  
D. Eliminates multivalued dependency  

> **Correct Option: D**  
> **Explanation:** 4NF deals with multivalued dependencies (MVDs).

## Q167. Relation R has 23 tuples and relation S has 5 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 115  
B. 119  
C. 28  
D. 111  

> **Correct Option: A**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 23 × 5 = 115.

## Q168. Relation R has degree 2 and relation S has degree 2. What is the degree of R × S? (Choose the best answer.)

A. 2  
B. 4  
C. 5  
D. 0  

> **Correct Option: B**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 2 + 2 = 4.

## Q169. In SQL, the command 'CREATE' belongs to which category? (Choose the best answer.)

A. DCL  
B. DML  
C. TCL  
D. DDL  

> **Correct Option: D**  
> **Explanation:** CREATE defines schema objects, so it is DDL.

## Q170. A deadlock in DBMS occurs when: (Choose the best answer.)

A. Two or more transactions wait indefinitely for each other’s locks  
B. A query uses ORDER BY  
C. A transaction finishes too quickly  
D. A table has no primary key  

> **Correct Option: A**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q171. Relation R has degree 8 and relation S has degree 7. What is the degree of R × S? (Choose the best answer.)

A. 15  
B. 8  
C. 16  
D. 1  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 8 + 7 = 15.

## Q172. Which statement best describes the DBMS feature 'Concurrency control'? (Choose the best answer.)

A. Eliminates indexes  
B. Allows safe simultaneous access by multiple users  
C. Forces serial execution always  
D. Removes need for transactions  

> **Correct Option: B**  
> **Explanation:** Locking/MVCC prevent anomalies under concurrent access.

## Q173. Which clause filters groups after GROUP BY? (Choose the best answer.)

A. WHERE  
B. ORDER BY  
C. FROM  
D. HAVING  

> **Correct Option: D**  
> **Explanation:** HAVING applies conditions on groups after aggregation.

## Q174. A deadlock in DBMS occurs when: (Choose the best answer.)

A. Two or more transactions wait indefinitely for each other’s locks  
B. A transaction finishes too quickly  
C. A query uses ORDER BY  
D. A table has no primary key  

> **Correct Option: A**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q175. In ACID properties, what best describes **Durability**? (Choose the best answer.)

A. Transactions preserve constraints  
B. Concurrent transactions appear serial  
C. All-or-nothing execution  
D. Committed changes persist even after a crash  

> **Correct Option: D**  
> **Explanation:** Durability ensures commit is permanent using logs/storage.

## Q176. Which clause filters individual rows before grouping? (Choose the best answer.)

A. WHERE  
B. ORDER BY  
C. HAVING  
D. SELECT  

> **Correct Option: A**  
> **Explanation:** WHERE filters rows before GROUP BY forms groups.

## Q177. Which statement is correct about Clustered index? (Choose the best answer.)

A. Is always a secondary index  
B. Determines the physical order of rows on disk (typically one per table)  
C. Can exist unlimited times per table  
D. Stores only pointers, never affects row order  

> **Correct Option: B**  
> **Explanation:** Clustered index defines row order; many DBMS allow one clustered index.

## Q178. Which option best defines a **Primary key**? (Choose the best answer.)

A. A key used only for sorting  
B. Any super key  
C. A chosen candidate key that is UNIQUE and NOT NULL  
D. A key that may contain NULL  

> **Correct Option: C**  
> **Explanation:** Primary key is selected from candidate keys and cannot be NULL.

## Q179. What does a RIGHT OUTER JOIN do? (Choose the best answer.)

A. Only matching rows  
B. All rows from both  
C. All rows from left and matching right  
D. Returns all rows from right table and matching rows from left table  

> **Correct Option: D**  
> **Explanation:** RIGHT JOIN preserves all right rows; missing left side becomes NULL.

## Q180. What is the main purpose of the SQL constraint FOREIGN KEY? (Choose the best answer.)

A. Ensures row uniqueness  
B. Ensures attribute is atomic  
C. Ensures sorted order  
D. Ensures referenced value exists in parent table  

> **Correct Option: D**  
> **Explanation:** Foreign keys enforce referential integrity.

## Q181. Relation R has 5 tuples and relation S has 4 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 9  
B. 20  
C. 38  
D. 18  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 5 × 4 = 20.

## Q182. Relation R has degree 5 and relation S has degree 3. What is the degree of R × S? (Choose the best answer.)

A. 5  
B. 9  
C. 2  
D. 8  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 5 + 3 = 8.

## Q183. Relation R has 9 tuples and relation S has 4 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 36  
B. 33  
C. 47  
D. 13  

> **Correct Option: A**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 9 × 4 = 36.

## Q184. In SQL, the command 'DELETE' belongs to which category? (Choose the best answer.)

A. DCL  
B. DDL  
C. DML  
D. TCL  

> **Correct Option: C**  
> **Explanation:** DELETE removes rows, so it is DML.

## Q185. Relation R has 6 tuples and relation S has 8 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 14  
B. 29  
C. 50  
D. 48  

> **Correct Option: D**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 6 × 8 = 48.

## Q186. Which option best defines a **Composite key**? (Choose the best answer.)

A. A key made of two or more attributes  
B. A key derived from another key  
C. A key used for encryption  
D. A key that allows NULL  

> **Correct Option: A**  
> **Explanation:** Composite keys combine multiple attributes to uniquely identify a tuple.

## Q187. A deadlock in DBMS occurs when: (Choose the best answer.)

A. A query uses ORDER BY  
B. Two or more transactions wait indefinitely for each other’s locks  
C. A transaction finishes too quickly  
D. A table has no primary key  

> **Correct Option: B**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q188. Which statement best describes the DBMS feature 'Data abstraction'? (Choose the best answer.)

A. Prevents normalization  
B. Creates redundancy  
C. Hides storage details and shows only necessary views  
D. Disables security  

> **Correct Option: C**  
> **Explanation:** DBMS provides levels of abstraction (external/conceptual/internal).

## Q189. Which statement best characterizes 2NF? (Choose the best answer.)

A. Eliminates join dependency  
B. Eliminates partial dependency  
C. Eliminates transitive dependency  
D. Eliminates repeating groups  

> **Correct Option: B**  
> **Explanation:** 2NF removes partial dependency on a composite key.

## Q190. Relation R has degree 3 and relation S has degree 2. What is the degree of R × S? (Choose the best answer.)

A. 6  
B. 1  
C. 3  
D. 5  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 3 + 2 = 5.

## Q191. Which statement best characterizes BCNF? (Choose the best answer.)

A. No multivalued dependency  
B. Every non-key depends on key  
C. Every determinant is a super key  
D. No join dependency  

> **Correct Option: C**  
> **Explanation:** BCNF strengthens 3NF: for every FD X→Y, X must be a superkey.

## Q192. What is the main purpose of the SQL constraint FOREIGN KEY? (Choose the best answer.)

A. Ensures row uniqueness  
B. Ensures attribute is atomic  
C. Ensures sorted order  
D. Ensures referenced value exists in parent table  

> **Correct Option: D**  
> **Explanation:** Foreign keys enforce referential integrity.

## Q193. Relation R has 9 tuples and relation S has 4 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 36  
B. 33  
C. 47  
D. 13  

> **Correct Option: A**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 9 × 4 = 36.

## Q194. Relation R has 8 tuples and relation S has 23 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 193  
B. 184  
C. 167  
D. 31  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 8 × 23 = 184.

## Q195. Relation R has 3 tuples and relation S has 22 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 25  
B. 67  
C. 66  
D. 63  

> **Correct Option: C**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 3 × 22 = 66.

## Q196. Relation R has 6 tuples and relation S has 8 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 14  
B. 29  
C. 50  
D. 48  

> **Correct Option: D**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 6 × 8 = 48.

## Q197. Relation R has degree 6 and relation S has degree 3. What is the degree of R × S? (Choose the best answer.)

A. 9  
B. 10  
C. 6  
D. 3  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 6 + 3 = 9.

## Q198. In relational algebra, what does Cartesian product (×) do? (Choose the best answer.)

A. Subtracts tuples  
B. Returns only matching tuples  
C. Pairs each tuple of one relation with every tuple of another  
D. Returns common tuples only  

> **Correct Option: C**  
> **Explanation:** Cartesian product forms all combinations of tuples.

## Q199. Relation R has degree 8 and relation S has degree 7. What is the degree of R × S? (Choose the best answer.)

A. 15  
B. 8  
C. 16  
D. 1  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 8 + 7 = 15.

## Q200. A deadlock in DBMS occurs when: (Choose the best answer.)

A. Two or more transactions wait indefinitely for each other’s locks  
B. A query uses ORDER BY  
C. A transaction finishes too quickly  
D. A table has no primary key  

> **Correct Option: A**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q201. Which statement is correct about Sparse index? (Choose the best answer.)

A. Has index entries for only some search-key values (e.g., one per block)  
B. Has entries for every record  
C. Works only on unsorted files  
D. Requires hashing  

> **Correct Option: A**  
> **Explanation:** Sparse indexes are smaller but require ordered data file.

## Q202. Relation R has degree 7 and relation S has degree 7. What is the degree of R × S? (Choose the best answer.)

A. 14  
B. 15  
C. 0  
D. 7  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 7 + 7 = 14.

## Q203. What is the main purpose of the SQL constraint NOT NULL? (Choose the best answer.)

A. Disallows updates  
B. Disallows duplicates  
C. Disallows inserts  
D. Disallows NULL values in a column  

> **Correct Option: D**  
> **Explanation:** NOT NULL ensures every row has a value for the column.

## Q204. Relation R has degree 8 and relation S has degree 8. What is the degree of R × S? (Choose the best answer.)

A. 17  
B. 8  
C. 0  
D. 16  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 8 + 8 = 16.

## Q205. A deadlock in DBMS occurs when: (Choose the best answer.)

A. Two or more transactions wait indefinitely for each other’s locks  
B. A query uses ORDER BY  
C. A transaction finishes too quickly  
D. A table has no primary key  

> **Correct Option: A**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q206. Relation R has degree 5 and relation S has degree 5. What is the degree of R × S? (Choose the best answer.)

A. 11  
B. 0  
C. 5  
D. 10  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 5 + 5 = 10.

## Q207. Which statement is correct about Clustered index? (Choose the best answer.)

A. Is always a secondary index  
B. Determines the physical order of rows on disk (typically one per table)  
C. Can exist unlimited times per table  
D. Stores only pointers, never affects row order  

> **Correct Option: B**  
> **Explanation:** Clustered index defines row order; many DBMS allow one clustered index.

## Q208. In TCL, what does ROLLBACK do? (Choose the best answer.)

A. Makes changes permanent  
B. Undoes changes made in the current transaction since last COMMIT  
C. Optimizes query  
D. Adds a column  

> **Correct Option: B**  
> **Explanation:** ROLLBACK restores the database to the last committed state (or savepoint).

## Q209. A deadlock in DBMS occurs when: (Choose the best answer.)

A. A transaction finishes too quickly  
B. Two or more transactions wait indefinitely for each other’s locks  
C. A table has no primary key  
D. A query uses ORDER BY  

> **Correct Option: B**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q210. Relation R has degree 2 and relation S has degree 3. What is the degree of R × S? (Choose the best answer.)

A. 5  
B. 3  
C. 6  
D. 1  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 2 + 3 = 5.

## Q211. Relation R has 5 tuples and relation S has 9 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 14  
B. 45  
C. 56  
D. 44  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 5 × 9 = 45.

## Q212. A deadlock in DBMS occurs when: (Choose the best answer.)

A. Two or more transactions wait indefinitely for each other’s locks  
B. A query uses ORDER BY  
C. A transaction finishes too quickly  
D. A table has no primary key  

> **Correct Option: A**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q213. What does a INNER JOIN do? (Choose the best answer.)

A. Returns only matching rows from both tables  
B. Returns all rows from right plus matches  
C. Returns all rows from both tables  
D. Returns all rows from left plus matches  

> **Correct Option: A**  
> **Explanation:** INNER JOIN keeps only rows satisfying the join condition in both tables.

## Q214. Relation R has 10 tuples and relation S has 7 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 57  
B. 17  
C. 74  
D. 70  

> **Correct Option: D**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 10 × 7 = 70.

## Q215. Which statement best describes the DBMS feature 'Concurrency control'? (Choose the best answer.)

A. Eliminates indexes  
B. Allows safe simultaneous access by multiple users  
C. Forces serial execution always  
D. Removes need for transactions  

> **Correct Option: B**  
> **Explanation:** Locking/MVCC prevent anomalies under concurrent access.

## Q216. Relation R has degree 2 and relation S has degree 8. What is the degree of R × S? (Choose the best answer.)

A. 8  
B. 10  
C. 11  
D. 6  

> **Correct Option: B**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 2 + 8 = 10.

## Q217. Relation R has 5 tuples and relation S has 9 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 14  
B. 45  
C. 56  
D. 44  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 5 × 9 = 45.

## Q218. In an ER diagram, the symbol 'Ellipse' represents: (Choose the best answer.)

A. Entity set  
B. Identifying relationship  
C. Attribute  
D. Relationship set  

> **Correct Option: C**  
> **Explanation:** Ellipses represent attributes.

## Q219. Relation R has degree 8 and relation S has degree 7. What is the degree of R × S? (Choose the best answer.)

A. 15  
B. 8  
C. 16  
D. 1  

> **Correct Option: A**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 8 + 7 = 15.

## Q220. Which option best defines a **Composite key**? (Choose the best answer.)

A. A key made of two or more attributes  
B. A key derived from another key  
C. A key used for encryption  
D. A key that allows NULL  

> **Correct Option: A**  
> **Explanation:** Composite keys combine multiple attributes to uniquely identify a tuple.

## Q221. In TCL, what does SAVEPOINT do? (Choose the best answer.)

A. Deletes a table  
B. Marks a point within a transaction to roll back to  
C. Ends a transaction  
D. Creates a view  

> **Correct Option: B**  
> **Explanation:** SAVEPOINT allows partial rollback inside a transaction.

## Q222. Relation R has 30 tuples and relation S has 4 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 120  
B. 130  
C. 114  
D. 34  

> **Correct Option: A**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 30 × 4 = 120.

## Q223. In an ER diagram, the symbol 'Double rectangle' represents: (Choose the best answer.)

A. Multivalued attribute  
B. Derived attribute  
C. Relationship set  
D. Weak entity set  

> **Correct Option: D**  
> **Explanation:** Weak entities are drawn with double rectangles.

## Q224. Which clause filters groups after GROUP BY? (Choose the best answer.)

A. WHERE  
B. ORDER BY  
C. FROM  
D. HAVING  

> **Correct Option: D**  
> **Explanation:** HAVING applies conditions on groups after aggregation.

## Q225. Which clause filters individual rows before grouping? (Choose the best answer.)

A. WHERE  
B. ORDER BY  
C. HAVING  
D. SELECT  

> **Correct Option: A**  
> **Explanation:** WHERE filters rows before GROUP BY forms groups.

## Q226. Relation R has degree 5 and relation S has degree 3. What is the degree of R × S? (Choose the best answer.)

A. 5  
B. 9  
C. 2  
D. 8  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 5 + 3 = 8.

## Q227. Relation R has degree 6 and relation S has degree 6. What is the degree of R × S? (Choose the best answer.)

A. 0  
B. 6  
C. 13  
D. 12  

> **Correct Option: D**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 6 + 6 = 12.

## Q228. Relation R has degree 2 and relation S has degree 5. What is the degree of R × S? (Choose the best answer.)

A. 8  
B. 5  
C. 7  
D. 3  

> **Correct Option: C**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 2 + 5 = 7.

## Q229. Which option best defines a **Foreign key**? (Choose the best answer.)

A. Chosen candidate key  
B. Attribute(s) in one table referencing a key in another table  
C. A multivalued attribute  
D. Minimal super key  

> **Correct Option: B**  
> **Explanation:** Foreign keys enforce referential integrity between tables.

## Q230. In an ER diagram, the symbol 'Double rectangle' represents: (Choose the best answer.)

A. Multivalued attribute  
B. Derived attribute  
C. Relationship set  
D. Weak entity set  

> **Correct Option: D**  
> **Explanation:** Weak entities are drawn with double rectangles.

## Q231. Which statement is correct about Sparse index? (Choose the best answer.)

A. Has index entries for only some search-key values (e.g., one per block)  
B. Has entries for every record  
C. Works only on unsorted files  
D. Requires hashing  

> **Correct Option: A**  
> **Explanation:** Sparse indexes are smaller but require ordered data file.

## Q232. In SQL, the command 'COMMIT' belongs to which category? (Choose the best answer.)

A. DML  
B. DCL  
C. TCL  
D. DDL  

> **Correct Option: C**  
> **Explanation:** COMMIT ends a transaction and makes changes permanent, so it is TCL.

## Q233. Relation R has 11 tuples and relation S has 13 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 131  
B. 143  
C. 24  
D. 145  

> **Correct Option: B**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 11 × 13 = 143.

## Q234. In an ER diagram, the symbol 'Double ellipse' represents: (Choose the best answer.)

A. Derived attribute  
B. Multivalued attribute  
C. Composite attribute  
D. Weak entity  

> **Correct Option: B**  
> **Explanation:** Multivalued attributes are shown using double ellipses.

## Q235. Which option best defines a **Foreign key**? (Choose the best answer.)

A. Chosen candidate key  
B. Attribute(s) in one table referencing a key in another table  
C. A multivalued attribute  
D. Minimal super key  

> **Correct Option: B**  
> **Explanation:** Foreign keys enforce referential integrity between tables.

## Q236. In an ER diagram, the symbol 'Diamond' represents: (Choose the best answer.)

A. Entity set  
B. Attribute  
C. Relationship set  
D. Weak entity  

> **Correct Option: C**  
> **Explanation:** Diamonds represent relationships between entity sets.

## Q237. In relational algebra, what does Set difference (-) do? (Choose the best answer.)

A. Renames attributes  
B. Returns tuples common to both  
C. Returns all combinations  
D. Returns tuples in first relation but not in second (union-compatible)  

> **Correct Option: D**  
> **Explanation:** Difference removes tuples present in the second relation.

## Q238. In relational algebra, what does Cartesian product (×) do? (Choose the best answer.)

A. Subtracts tuples  
B. Returns only matching tuples  
C. Pairs each tuple of one relation with every tuple of another  
D. Returns common tuples only  

> **Correct Option: C**  
> **Explanation:** Cartesian product forms all combinations of tuples.

## Q239. A deadlock in DBMS occurs when: (Choose the best answer.)

A. Two or more transactions wait indefinitely for each other’s locks  
B. A query uses ORDER BY  
C. A transaction finishes too quickly  
D. A table has no primary key  

> **Correct Option: A**  
> **Explanation:** Deadlock is a cyclic wait: each transaction holds a lock and requests another lock held by a different transaction.

## Q240. Relation R has 29 tuples and relation S has 14 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 406  
B. 405  
C. 43  
D. 419  

> **Correct Option: A**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 29 × 14 = 406.

## Q241. In ACID properties, what best describes **Atomicity**? (Choose the best answer.)

A. Isolation from other concurrent transactions  
B. Permanence of committed data  
C. Moving from one valid state to another  
D. All-or-nothing execution of a transaction  

> **Correct Option: D**  
> **Explanation:** Atomicity means either all operations happen or none (rollback).

## Q242. Which statement best characterizes BCNF? (Choose the best answer.)

A. No multivalued dependency  
B. Every non-key depends on key  
C. Every determinant is a super key  
D. No join dependency  

> **Correct Option: C**  
> **Explanation:** BCNF strengthens 3NF: for every FD X→Y, X must be a superkey.

## Q243. Which statement best characterizes 5NF? (Choose the best answer.)

A. Eliminates join dependency (project-join NF)  
B. Eliminates partial dependency  
C. Eliminates multivalued dependency  
D. Eliminates transitive dependency  

> **Correct Option: A**  
> **Explanation:** 5NF addresses join dependencies not implied by candidate keys.

## Q244. Which option best defines a **Alternate key**? (Choose the best answer.)

A. Candidate keys not chosen as the primary key  
B. Keys that reference other tables  
C. Keys formed by combining two tables  
D. Keys that allow duplicates  

> **Correct Option: A**  
> **Explanation:** Alternate keys are the remaining candidate keys.

## Q245. Which statement is TRUE about the isolation level REPEATABLE READ? (Choose the best answer.)

A. Allows dirty reads  
B. Prevents all anomalies  
C. Is weaker than READ COMMITTED  
D. Prevents non-repeatable reads but may allow phantom reads  

> **Correct Option: D**  
> **Explanation:** Repeatable read ensures same row reads consistent; phantoms may still appear.

## Q246. Relation R has degree 2 and relation S has degree 2. What is the degree of R × S? (Choose the best answer.)

A. 2  
B. 4  
C. 5  
D. 0  

> **Correct Option: B**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 2 + 2 = 4.

## Q247. Which statement best characterizes 5NF? (Choose the best answer.)

A. Eliminates join dependency (project-join NF)  
B. Eliminates partial dependency  
C. Eliminates multivalued dependency  
D. Eliminates transitive dependency  

> **Correct Option: A**  
> **Explanation:** 5NF addresses join dependencies not implied by candidate keys.

## Q248. Relation R has degree 7 and relation S has degree 3. What is the degree of R × S? (Choose the best answer.)

A. 11  
B. 7  
C. 10  
D. 4  

> **Correct Option: C**  
> **Explanation:** Degree of Cartesian product = degree(R) + degree(S) = 7 + 3 = 10.

## Q249. Which option best defines a **Candidate key**? (Choose the best answer.)

A. Any unique attribute set  
B. A foreign key  
C. A minimal super key  
D. A non-unique attribute  

> **Correct Option: C**  
> **Explanation:** Candidate keys are minimal unique identifiers (no proper subset is unique).

## Q250. In SQL, the command 'REVOKE' belongs to which category? (Choose the best answer.)

A. DCL  
B. DML  
C. DDL  
D. TCL  

> **Correct Option: A**  
> **Explanation:** REVOKE removes permissions, hence DCL.

## Q251. Which statement is correct about Hash index? (Choose the best answer.)

A. Optimized for equality search; poor for range queries  
B. Always keeps data sorted  
C. Requires full table scan  
D. Best for range queries  

> **Correct Option: A**  
> **Explanation:** Hashing maps keys to buckets; great for '=' lookups, weak for ranges.

## Q252. Which statement is correct about B-tree? (Choose the best answer.)

A. Keys and data pointers may appear in both internal and leaf nodes  
B. Works only with hashing  
C. Always unbalanced  
D. All keys only in leaves  

> **Correct Option: A**  
> **Explanation:** In B-trees, records/pointers can be stored in internal nodes as well.

## Q253. In relational algebra, what does Set difference (-) do? (Choose the best answer.)

A. Renames attributes  
B. Returns tuples common to both  
C. Returns all combinations  
D. Returns tuples in first relation but not in second (union-compatible)  

> **Correct Option: D**  
> **Explanation:** Difference removes tuples present in the second relation.

## Q254. Relation R has 29 tuples and relation S has 14 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 406  
B. 405  
C. 43  
D. 419  

> **Correct Option: A**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 29 × 14 = 406.

## Q255. Relation R has 9 tuples and relation S has 4 tuples. How many tuples will R × S have? (Choose the best answer.)

A. 36  
B. 33  
C. 47  
D. 13  

> **Correct Option: A**  
> **Explanation:** Cartesian product pairs each tuple of R with each tuple of S, so tuples = 9 × 4 = 36.

## Q256. Which statement is correct about Hash index? (Choose the best answer.)

A. Optimized for equality search; poor for range queries  
B. Always keeps data sorted  
C. Requires full table scan  
D. Best for range queries  

> **Correct Option: A**  
> **Explanation:** Hashing maps keys to buckets; great for '=' lookups, weak for ranges.

## Q257. In SQL, the command 'GRANT' belongs to which category? (Choose the best answer.)

A. DDL  
B. TCL  
C. DCL  
D. DML  

> **Correct Option: C**  
> **Explanation:** GRANT controls permissions, so it is DCL.

## Q258. Which option best defines a **Super key**? (Choose the best answer.)

A. Attribute referring to another table  
B. Chosen candidate key for identification  
C. Minimal unique attribute set  
D. Any attribute set that uniquely identifies a tuple  

> **Correct Option: D**  
> **Explanation:** A super key may contain extra attributes but still uniquely identifies rows.

## Q259. In TCL, what does ROLLBACK do? (Choose the best answer.)

A. Makes changes permanent  
B. Undoes changes made in the current transaction since last COMMIT  
C. Optimizes query  
D. Adds a column  

> **Correct Option: B**  
> **Explanation:** ROLLBACK restores the database to the last committed state (or savepoint).

## Q260. Which statement is correct about Hash index? (Choose the best answer.)

A. Optimized for equality search; poor for range queries  
B. Always keeps data sorted  
C. Requires full table scan  
D. Best for range queries  

> **Correct Option: A**  
> **Explanation:** Hashing maps keys to buckets; great for '=' lookups, weak for ranges.
