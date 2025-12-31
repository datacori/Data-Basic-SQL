# SQL Fundamentals Study (2025-12-28)

---

## Learning Goals

### Data Modeling Basics and Extensions
- 1:1 / M:N relationship resolution
- Identification of entity types
- Handling relationships using keys

## Advanced Data Modeling
- Normalization and denormalization
- Primary Key (PK) and Foreign Key (FK) design
- Resolving 1:1 relationships
- Resolving M:N relationships
- Data partitioning and performance considerations
- Handling composite keys
- Understanding data types
- Subtype (supertype) modeling

---

## Resolving 1:1 Relationships

## Characteristics
- Each entity instance is related to **exactly one** instance of another entity
- Often both entities share a close dependency

---

## Resolution Strategies

### 1. Keep Separate Entities
- Use when both entities have independent meanings
- One entity’s PK becomes an FK in the other entity

---

### 2. Merge Entities
- Use when both entities have a **strong dependency**
- Combine attributes into a single entity
- Choose one PK to represent both entities

---

### 3. Use a Subtype Entity
- Use when one entity represents a specialized case of another
- Subtype inherits the PK of the supertype
- Suitable for optional or conditional attributes

---

## Resolving M:N Relationships

## Characteristics
- Many instances of one entity relate to many instances of another
- Cannot be directly implemented in relational databases

---

## Resolution Strategy

### Associative (Junction) Entity
- Create a new entity to resolve the M:N relationship
- Use PKs from both parent entities as:
  - Composite Primary Key, or
  - Separate PK with FKs
- Store relationship-specific attributes in the associative entity

**Example**
- Student ↔ Course  
→ Enrollment (StudentID, CourseID, EnrollmentDate)

---

## Key Takeaways

- 1:1 relationships require careful evaluation before implementation
- M:N relationships must always be resolved using associative entities
- PK/FK design directly affects data integrity and query performance
- Relationship resolution bridges conceptual models and physical databases

---

## Reflections

- Resolving relationships clarified how ERDs are translated into real tables
- Understanding PK/FK placement improved my schema design decisions
- This step made database modeling feel much more practical and concrete

---

## Entity Integration and Separation

## When to Integrate Entity Types

Entity types can be integrated when:

- They share common attributes
- Their lifecycles are similar or identical
- They can be expressed as a single entity type
- Integration simplifies the ERD structure

 **Benefit**:  
Reduces redundancy and simplifies the overall data model.

---

### When to Separate Entity Types

Entity types should be separated when:

- Attributes have different characteristics
- Data usage and access patterns differ
- Change cycles of attributes are different
- Specific business rules must be enforced

 **Trade-off**:  
While separation may increase complexity, it improves clarity and flexibility.

---

## History (Temporal) Data Management

## Concept
History management handles data that changes over time while preserving past values.

- Ensures that historical data is not lost
- Enables time-based analysis and tracking

---

## Common Approaches

- **Full History**  
  Stores all changes over time

- **Partial History**  
  Stores only specific attribute changes

- **Current State Only**  
  Maintains only the most recent data

---

## Normalization vs. Denormalization

## Normalization

- Reduces data redundancy
- Improves data consistency and integrity
- Results in more tables and relationships

---

## Denormalization

- Improves query performance
- Reduces join operations
- Simplifies read-heavy workloads
- Introduces controlled redundancy

 **Design Principle**:  
Choose normalization or denormalization based on system requirements and usage patterns.

---

## Ordering of Primary Key (PK) and Foreign Key (FK)

## When PK Ordering Matters

- If a PK is frequently used in search conditions
- When index-based performance optimization is required
- If the PK consists of multiple attributes

---

## PK–FK Design Considerations

- PK attribute order affects index efficiency
- FK attributes must match the referenced PK structure
- Proper PK/FK design can significantly improve query performance
- Indexes are often created based on PK and FK columns

---

## Key Takeaways

- Entity integration and separation depend on business rules and data characteristics
- History management is essential for time-variant data
- Normalization and denormalization are performance-driven design choices
- PK and FK ordering directly impacts database performance

---

## Performance-Oriented Data Modeling Principles

## Improving Performance by Splitting 1:1 Tables

When a 1:1 relationship results in frequent joins:

- Splitting tables can improve performance
- Useful when one table is accessed frequently while the other is rarely used
- Helps reduce unnecessary data reads
- Improves I/O efficiency by separating optional or infrequently accessed attributes

---

## Improving Performance with Multi-Valued Tables

When an entity contains repeating or multi-valued attributes:

- Separate them into a dedicated table
- Prevents excessive data duplication
- Enables more efficient indexing and querying
- Improves flexibility for future data expansion

---

## Improving Performance by Separating Frequently Changing Attributes

Attributes with high update frequency should be separated:

- Reduces locking and contention during updates
- Improves performance for read-heavy queries
- Allows optimized storage and indexing strategies
- Minimizes the impact of frequent updates on core entity data

---

## Improving Performance for Large-Volume, Read-Heavy Data

For entities with large data volumes and frequent reads:

- Optimize table structure for query performance
- Avoid unnecessary joins in critical query paths
- Use denormalization selectively when appropriate
- Design indexes based on access patterns

---

## Characteristics of a Good Data Model

A well-designed data model:

- Accurately reflects business rules
- Is flexible enough to adapt to change
- Ensures data consistency and integrity
- Supports efficient query performance
- Enables clear communication between business and technical teams

---

## Key Takeaways

- Data modeling decisions directly affect system performance
- Table separation can significantly improve efficiency in read-heavy systems
- Performance optimization should be driven by data access patterns
- A good data model balances accuracy, flexibility, and performance

---

## Key Learnings

- Understanding the importance of data model design and validation
- Designing performance-oriented data models
- Building scalable and maintainable database structures

---

## Reflections

- Gained a deeper understanding of how 1:1, 1:N, and M:N relationships impact database design
- Learned that resolving M:N relationships requires careful table structuring
- Realized that well-designed data models reduce development and maintenance time
- Continuous improvement is essential in data modeling

---

## Resources

- Fast Campus – **Practical SQL from Fundamentals to Projects**
- Database modeling practice materials and exercises

---

## Author

**RYU YEJIN** 

Aspiring Data Analyst  

Focusing on data modeling, SQL fundamentals, and performance-aware database design  

📧 Email: datacorio00@gmail.com

Blog : https://blog.naver.com/datacori/224126921268
