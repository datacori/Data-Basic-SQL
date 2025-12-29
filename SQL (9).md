# SQL Fundamentals Study (2025-12-25)
(Data Modeling Fundamentals: Identifier & Relationship)

---

## Learning Goals

- Understand the concept and characteristics of **Identifiers**
- Learn the definition of **Relationships**, including pairing, naming, and cardinality

---

## Identifier

### Definition
An **Identifier** is a determinant that uniquely distinguishes each entity within a single entity type.

- Every entity type must have **at least one identifier**
- Identifiers ensure that each entity instance can be uniquely recognized

---

### Characteristics of an Identifier

- Uniquely identifies all entities within an entity type
- Once defined, an identifier **should not be changed**
- Identifier attributes must always contain a value (cannot be NULL)
- Typically represented by **primary key attributes**

---

### Conceptual Example

An entity type (e.g., Company, Location, Person) is associated with identifiers such as:

- ID
- Email address

These identifiers uniquely distinguish each entity instance within the entity type.

---

## Key Takeaways

- Identifiers are essential for maintaining data integrity
- Every entity type requires at least one identifier
- Stable and meaningful identifiers are critical in database design
- Proper identifier design simplifies relationship mapping and normalization

---

## Types of Identifiers

Identifiers can be classified based on their role, origin, and structure.

---

### Primary Identifier vs. Secondary Identifier

**Primary Identifier**
- The representative and main identifier of an entity type
- There is **exactly one primary identifier** per entity type
- Used as the primary means of uniquely identifying entity instances

**Secondary Identifier**
- Identifies entities as an alternative to the primary identifier
- An entity type may have **two or more secondary identifiers**
- Often used depending on business requirements

📌 If an entity can be uniquely identified by two or more attributes, the choice of identifier depends on business rules.

---

### Internal Identifier vs. External Identifier

**Internal Identifier**
- Generated and managed within the entity type itself
- Exists independently without relying on other entity types

**External Identifier**
- Inherited from another entity type through a relationship
- Includes identifier attributes from a related entity
- Plays a linking role by connecting entity types

---

### Simple Identifier vs. Composite Identifier

**Simple Identifier**
- A primary identifier composed of a **single attribute**

**Composite Identifier**
- A primary identifier composed of **two or more attributes**
- Used when a single attribute is insufficient to uniquely identify an entity

---

### Surrogate Identifier

**Surrogate Identifier**
- Used when the primary identifier is a composite identifier
- Multiple attributes are combined into a single artificial attribute
- Simplifies key management by replacing complex composite identifiers

---

## Key Takeaways

- Identifiers can be classified by role, origin, and structure
- Each entity type must have one primary identifier
- Composite identifiers reflect real-world business rules
- Surrogate identifiers improve simplicity and performance in database design

---

## Relationship

A **relationship** defines how entities are connected to each other within a data model.

- Describes the **association between entity types**
- Represents how data in one entity is **related to data in another**
- Enables navigation and understanding of **business rules** within the model

### Examples of Relationships
- A **Person** works for a **Company**
- A **Person** lives in a **Location**
- A **Company** is located in a **Location**

Relationships help clarify how entities interact and depend on each other in real-world scenarios.

---

## Relationship Pairing

**Relationship pairing** expresses relationships as **explicit pairs of entities**, making them easier to understand and model.

- Represents relationships as **entity-to-entity connections**
- Clearly defines the **direction and meaning** of each relationship
- Often used to translate conceptual models into logical or physical designs

### Example

- James **works for** Apple
- James **is located in** Seoul
- James **lives in** Seoul

Each pairing describes a clear fact that can later be translated into foreign keys or associative tables.

---

## Key Points

- Relationships require **at least two entities**
- Relationship names should clearly describe the **business meaning**
- Relationship pairing helps transform abstract relationships into **concrete data structures**
- Relationships can later be implemented using **foreign keys** or **junction tables**

---

## Relationship Cardinality

**Relationship cardinality** describes how many instances of one entity can be associated with instances of another entity.

It defines the **numerical constraints** between entities in a relationship.

---

### 1:1 (One-to-One)

- Each instance of an entity is related to **exactly one** instance of another entity
- Both sides of the relationship have a one-to-one correspondence

**Example**
- One person owns one car

This type of relationship is relatively rare and often used for separating optional or sensitive information.

---

### 1:N (One-to-Many)

- One instance of an entity can be related to **multiple instances** of another entity
- The many-side entity is associated with only one instance of the one-side entity

**Example**
- One company employs many persons

This is the **most common** relationship type in relational databases.

---

### M:N (Many-to-Many)

- Multiple instances of one entity can be related to **multiple instances** of another entity
- Requires an **associative (junction) table** when implemented in a relational database

**Example**
- Many persons work on many projects

This relationship is resolved using a separate table containing foreign keys from both entities.

---

## Key Learnings

- Understanding the role of **identifiers (keys)** in entity design
- Defining and modeling **relationships** between entities

---

## Reflections

- Identifiers are concepts that are **directly applied to entity types**
- Relationships describe how **two entities influence and interact** with each other
- Cardinality represents the **meaning of quantity** between related entities
- Continuous review helped reinforce core modeling concepts
- Merry Christmas!
- Keep going 

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

Blog : https://blog.naver.com/datacori/224116677282


