# SQL Fundamentals Study (2025-12-24)

## Learning Goals

This section focuses on understanding the concept of **Entity** in database design.

- Definition of an Entity
- Characteristics of an Entity
- Types and classification of Entities
- Attributes, classification, and naming conventions

---

## Entity

An **Entity** is a logically identifiable unit that represents information required for business operations and data management.

### Key Characteristics
- Represents a real-world object or concept that needs to be stored and managed
- Can exist conceptually even before being implemented in a database
- Serves as the foundation for database table design

### Entity Type and Entity Set
- **Entity Type**: A category that defines a group of entities with the same attributes
- **Entity Set**: A collection of entities belonging to the same entity type

### Examples of Entities
- People (e.g., customers, employees)
- Places (e.g., cities, locations)
- Objects (e.g., products, items)
- Concepts or events that require data storage

In relational databases, **entities are typically implemented as tables**.

---

## Entity Classification Examples

- *Apple* → Company  
- *Seoul* → Location  
- *James* → Person  
- *Amazon* → Organization  

These examples illustrate how individual entities belong to specific entity types.

---

## Key Takeaways

- Entities represent core objects or concepts in database design
- Clear entity definition is essential for effective data modeling
- Entity types help organize and standardize database structures

---

## Entity Type Characteristics

An **Entity Type** defines a group of entities that share the same structure and attributes within a database system.

### Key Characteristics
- Must represent information that is essential and must be managed within the system
- Each entity instance can be uniquely identified
- Exists conceptually as a collection of related entities
- Actively used in business processes and workflows
- Must include at least one **attribute**
- Must participate in at least one relationship with another entity type

---

## Entity Type Classification & Attributes

This document summarizes core concepts of **Entity Types and Attributes** used in data modeling and database design.

---

## Entity Type Classification

### 1. Classification by Nature

### Tangible Entity
- Represents a **physical object**
- Can be stored and used continuously  
- Example: Product, Employee

### Conceptual Entity
- Represents an **abstract concept**
- Does not have physical form  
- Example: Contract, Category

### Event Entity
- Represents an **event or transaction**
- Occurs during business operations
- Typically generated frequently  
- Example: Order, Payment

---

### 2. Classification by Time of Occurrence

### Basic Entity
- Exists independently within a business domain
- Created as a foundational entity
- Often acts as a **parent entity**

### Central Entity
- Derived from a basic entity
- Plays a **core role** in business processes

### Associative (Action) Entity
- Generated from **two or more parent entities**
- Frequently changes over time
- Often accumulates transactional data  
- Example: OrderDetail, Enrollment

---

## Entity Naming Conventions

- Use **business terms** commonly used in the domain
- Avoid abbreviations
- Use **singular nouns** only

---

## Attributes

- An attribute is the **smallest unit of data** that cannot be further divided
- Each entity must contain **one or more attributes** that describe its characteristics
- Attributes store **specific values** that define the entity in detail

---

## Key Takeaways

- Clear entity classification improves **data model readability**
- Proper naming conventions enhance **communication between stakeholders**
- Well-defined attributes ensure **data consistency and integrity**

---

## Attribute Classification

Attributes can be classified based on how they are defined and used in business and system design.

---

### Basic Attributes
- Attributes defined through **business analysis**
- Exist naturally in the business domain
- Examples:
  - Code values
  - Identification numbers

---

### Designed Attributes
- Attributes that **do not exist in the business domain**
- Derived during the **database or system design phase**
- Typically used as identifiers (keys)

---

### Derived Attributes
- Attributes generated through **calculation or transformation**
- Values are not stored directly but derived from other attributes
- Example:
  - Calculated amounts
  - Aggregated values

---

## Attribute Naming Rules

- Attribute names should clearly reflect their **meaning within the entity**
- Use **standardized terminology** to avoid confusion
- Follow consistent naming conventions across the model

---

### Key Takeaways

- Proper attribute classification improves **data accuracy and maintainability**
- Separating basic, designed, and derived attributes helps clarify **data ownership**
- Consistent naming rules reduce ambiguity in database design

---

## Key Learnings

- Clear distinction between **entities and entity types**
- Understanding attributes as the **minimum unit of data**
- Overview of different **NoSQL database types**

---

## Reflections

- Summarizing content in writing helped identify areas where my understanding was still vague
- I realized that an entity ultimately represents a **set of data**
- Every entity type must include **at least one attribute**
- Continuous documentation reinforces long-term learning  
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

Blog : https://blog.naver.com/datacori/224116647070
