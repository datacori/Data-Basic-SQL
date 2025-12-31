# SQL Fundamentals Study (2025-12-27)

---

## Learning Goals 

- Understand the **concept and purpose of normalization**
- Learn each normal form:
  - 1st Normal Form (1NF)
  - 2nd Normal Form (2NF)
  - 3rd Normal Form (3NF)
  - Boyce–Codd Normal Form (BCNF)
  - 4th Normal Form (4NF)
  - 5th Normal Form (5NF)

---

## What is Normalization?

Normalization is a process of structuring data to **reduce redundancy** and **improve data integrity**.

- Eliminates unnecessary data duplication
- Prevents data inconsistency and update anomalies
- Organizes data into logically related tables

### Goals of Normalization

- Ensure each entity represents a **single subject**
- Store data efficiently without redundancy
- Maintain consistency when inserting, updating, or deleting data
- Improve database maintainability and scalability

---

## Object Analysis vs. Normalized Entity Analysis

### Object Analysis
- Focuses on real-world objects and behaviors
- Groups related attributes based on how objects behave
- Often used during early conceptual design

---

### Normalized Entity Analysis
- Focuses on **data structure and dependencies**
- Groups attributes based on functional dependencies
- Ensures entities are logically sound and free of anomalies

---

## Functional Dependency

A **functional dependency** describes a relationship where one attribute uniquely determines another.

- If attribute **A** determines attribute **B**, then **B** is functionally dependent on **A**
- **Determinant**: the attribute that determines another
- **Dependent**: the attribute whose value is determined

### Example
- `StudentID → Name, Grade`  
  (StudentID determines Name and Grade)

Understanding functional dependencies is essential for applying normalization rules correctly.

---

## Key Takeaways

- Normalization is essential for creating **clean and reliable database designs**
- Functional dependencies form the theoretical foundation of normalization
- Separating object analysis from normalized design improves data consistency

---

## Reflections

- Normalization clarified how poor design can lead to data anomalies
- Functional dependency helped explain why tables should be decomposed
- This process strengthens the logical foundation of relational databases

---

## Normal Forms: 1NF to 3NF

This section summarizes the core principles of database normalization from **First Normal Form (1NF)** to **Third Normal Form (3NF)**.

---

## First Normal Form (1NF)

A table is in **First Normal Form (1NF)** if:

- Each column contains **atomic (indivisible) values**
- There are **no repeating groups or multi-valued attributes**
- Each record can be uniquely identified

### Key Idea
> One cell = one value

**Example**
- A column storing multiple phone numbers violates 1NF
- Phone numbers must be separated into individual rows or a related table

---

## Second Normal Form (2NF)

A table is in **Second Normal Form (2NF)** if:

- It satisfies **1NF**
- All non-key attributes are **fully functionally dependent** on the entire primary key
- **Partial dependencies** are eliminated

### Key Idea
> No partial dependency on a composite key

**Example**
- If a table has a composite key `(StudentID, CourseID)`
- Attributes depending only on `StudentID` must be moved to a separate table

---

## Third Normal Form (3NF)

A table is in **Third Normal Form (3NF)** if:

- It satisfies **2NF**
- There are **no transitive dependencies**
- Non-key attributes depend **only on the primary key**

### Key Idea
> No dependency between non-key attributes

**Example**
- If `StudentID → DepartmentID` and `DepartmentID → DepartmentName`
- Then `DepartmentName` must be moved to a separate table

---

## Comparison Summary

| Normal Form | Main Rule | Problem Solved |
|------------|----------|----------------|
| 1NF | Atomic values | Repeating groups |
| 2NF | Full dependency | Partial dependency |
| 3NF | No transitive dependency | Indirect dependency |

---

## Key Takeaways

- Normalization systematically removes data redundancy
- Each normal form addresses a specific type of dependency problem
- Understanding dependencies is crucial for correct table decomposition

---

## Reflections

- Breaking tables step by step clarified why normalization must follow an order
- Identifying partial and transitive dependencies improved my schema design skills
- These rules form the foundation of reliable relational database design

---

## Advanced Normal Forms: BCNF, 4NF, and 5NF

This section covers advanced normalization forms that further refine database design beyond 3NF.

---

## Boyce–Codd Normal Form (BCNF)

A table is in **BCNF** if:

- It satisfies **3NF**
- Every **determinant** is a candidate key

### Why BCNF is Needed
- 3NF may still allow anomalies when:
  - A non-primary candidate key determines other attributes
- BCNF strengthens dependency rules to eliminate these issues

### Key Idea
> Every determinant must be a candidate key

---

## Fourth Normal Form (4NF)

A table is in **Fourth Normal Form (4NF)** if:

- It satisfies **BCNF**
- It has **no multi-valued dependencies**

### Multi-Valued Dependency
- Occurs when one attribute determines **multiple independent sets of values**
- Example:
  - A student can have multiple skills and multiple hobbies independently

### Key Idea
> Remove independent multi-valued attributes into separate tables

---

## Fifth Normal Form (5NF)

A table is in **Fifth Normal Form (5NF)** if:

- It satisfies **4NF**
- It has **no join dependencies**
- The table cannot be further decomposed without losing information

### Key Idea
> Decompose tables until no further lossless decomposition is possible

5NF is rarely required in practice but is useful in complex relational designs.

---

## Comparison Summary

| Normal Form | Focus | Problem Eliminated |
|------------|------|--------------------|
| BCNF | Determinants | Hidden dependency anomalies |
| 4NF | Multi-valued dependency | Redundant independent data |
| 5NF | Join dependency | Lossy decompositions |

---

## Key Takeaways

- BCNF strengthens 3NF by enforcing stricter key rules
- 4NF resolves issues caused by independent multi-valued attributes
- 5NF addresses complex join dependencies in advanced designs
- Higher normal forms improve **data integrity**, but practical trade-offs must be considered

---

## Reflections

- Understanding BCNF clarified why 3NF is sometimes insufficient
- Multi-valued dependencies highlighted subtle redundancy issues
- Learning higher normal forms improved my ability to evaluate schema quality

---

## Key Learnings

- Core concepts and characteristics of **data modeling normalization**
- Understanding normalization from **1NF to 5NF**

---

## Reflections

- Learned the normalization process in a **step-by-step and structured way**
- Creating visual summaries helped reinforce my understanding of each normal form
- Planning to explore better ways to upload and manage images on GitHub
- Keep going 🚀

---

## Resources

- *From Beginner to Practitioner: MySQL Basics, Query Writing, and Performance Optimization*  
  (Lecture materials)

---

## Author

**RYU YEJIN**  

Data Analysis Learning Log

From SQL Fundamentals to Practical Projects  

📧 Email: datacori00@gmail.com

Blog : https://blog.naver.com/datacori/224117741614
