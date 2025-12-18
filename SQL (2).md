# SQL fundamentals study (2025-12-18)
---
## Learning goals

### Database Types and Characteristics

- Hierarchical Database
- Network Database
- Key-Value Database
- Relational Database
- Types of NoSQL Databases

---

## Hierarchical Database

A hierarchical database organizes data in a **tree-like structure**, where records are connected through **parent-child relationships**.

### Key Characteristics
- Data is structured as a tree
- Represents repetitive parent–child relationships
- Each parent record can have **multiple child records**
- Each child record has **only one parent record**

### Structure Overview
- **Root Record**: The top-level record in the hierarchy
- **Parent Record**: A record that owns one or more child records
- **Child Record**: A record that belongs to exactly one parent

### Disadvantages
- **Low flexibility** : Changes become difficult when one-to-one or one-to-many relationships need to be modified.

- **Data redundancy** is likely to occur.

- **Strong dependency between levels** : After adoption, changing business processes is difficult due to tight parent–child coupling.

This structure is efficient for representing **one-to-many relationships**, but it lacks flexibility when handling many-to-many relationships.

---

## Network Database

A network database represents data using a graph-like structure composed of nodes and sets, allowing more flexible relationships than a hierarchical model.

### Characteristics

- Data is represented as nodes and sets

- Nodes exist within a network, forming peer-to-peer relationships

- Each node can act as both : owner / member

- Designed to address limitations of hierarchical databases.

**Owner node**

- can have one or multiple member nodes

**Member node**

- Belongs to only one owner node per relatonship

- can participate in multiple relationships across the network

### Advantages

- Supports many-to-many relationships

- Reduces data redundancy compared to hierarchical databases

- More flexible structure for representing complex real-world relationships

### Limitations

- Complex structure makes design and maintenance difficult

- High dependency on predefined relationships

- Difficult to modify schema once implemented

- Limited use in modern systems due to complexity

---

## Key-Value Database

A **Key-Value Database** is a type of **NoSQL database** that stores data as simple **key–value pairs**, where each key is uniquely associated with a value.

### Key Characteristics
- A category of **NoSQL databases**
- Stores data in a **one-to-one mapping (Key → Value)**
- Uses keys to quickly **search, retrieve, and manage records**
- Optimized for storing and accessing **associative arrays**  
  (e.g., dictionaries, hash tables)
- Allows **schema-less design**, meaning data structures do not need to be predefined
- Suitable for **unstructured or semi-structured data**

### Advantages
- Very fast data access due to simple key-based lookup
- Simple data model and easy scalability
- Flexible structure without schema constraints

### Limitations
- Data duplication can easily occur
- Not suitable for complex queries or relationships
- Limited querying capabilities (key-based access only)

### Use Cases
- Caching systems
- Session management
- User preference storage
- Real-time applications

---

## Relational Database

A **Relational Database** is the most widely used type of database, where data is stored in **tables composed of rows and columns**.

### Key Characteristics
- The most commonly used database model
- Data is stored in **tables (relations)** with rows and columns
- Each table represents an entity, and each row represents a record
- Relationships between data are **predefined using keys**
- Uses a **fixed schema**, meaning the structure is defined in advance

### Core Concepts
- **Row (Tuple):** A single record in a table
- **Column (Attribute):** A field that defines a specific data type
- **Primary Key:** A unique identifier for each record
- **Foreign Key:** A key used to create relationships between tables

### Advantages
- Clear and structured data organization
- Strong data integrity and consistency
- Powerful querying using **SQL**
- Well-suited for complex queries and relationships

### Limitations
- Schema changes can be costly and complex
- Less flexible for handling unstructured data
- Scalability can be challenging for very large datasets

### Use Cases
- Business applications
- Financial systems
- Enterprise databases
- Systems requiring strong data consistency

### Common Relational Database Management Systems (RDBMS)

The following are widely used **Relational Database Management Systems**:

- **MySQL**  
  An open-source RDBMS commonly used for web applications and small to medium-sized systems.

- **Oracle Database**  
  A powerful enterprise-level RDBMS known for high performance, scalability, and security.

- **Microsoft SQL Server**  
  A relational database developed by Microsoft, widely used in enterprise environments and Windows-based systems.

- **PostgreSQL**  
  An advanced open-source RDBMS that supports complex queries and strong data integrity.

- **IBM DB2**  
  An enterprise-grade database system optimized for high-performance data processing.

- **SQLite**  
  A lightweight, file-based database commonly used in mobile applications and embedded systems.

---

## ERD (Entity relationship diagram)

A diagram that represents relationships between tables

Used for database design

- Logical model / Physical model

---

## Types of NoSQL databases

- **Keyvalue database**

Easy horizontal scaling

Cannot query based on value content

- **Document database**

Stores data as key-document format

Values are stored in hierachical structures(JSON-like)

- **Column-family database**

Allows different schemas per key

Excellent for large-scale data compression, distributed processing, and aggregaton

- **Graph database**

Represents data as nodes

Relationships are represented as edges

Used for social media and network analysis

---

## Key learnings

- Database types and their characteristics

- Hierarchical, Network, Key-Value, and Relational databases

- Overview of NoSQL categories

---

## Reflections

- Learned the fundamentals of four major database types

- Connected Python concepts (classes and inheritance) with database structures

- Practiced creating visual representations of database types using GPT

- Keep going!

---

## Resources

From Beginner to SQL & MySQL for Real-World Engineers (lecture materials, ZIP)

---

## Author

**RYU YEJIN**

Aspiring Data Analyst

From SQL fundamentals to real-world projects

Email : datacori00@gmail.com

Blog : https://blog.naver.com/datacori/224113470261
