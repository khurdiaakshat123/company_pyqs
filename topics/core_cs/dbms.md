# Database Management Systems (DBMS) Cheatsheet 🗄️

## 1. ACID Properties
- **Atomicity:** "All or nothing" execution of transactions. Handled by undo logs / write-ahead logging (WAL).
- **Consistency:** Database transitions from one valid state to another, satisfying all schema constraints.
- **Isolation:** Concurrent transactions execute without interfering with one another.
- **Durability:** Committed transactions persist even in the event of power loss or crash (redo logs).

## 2. Transaction Isolation Levels
| Level | Dirty Read | Non-Repeatable Read | Phantom Read |
|---|---|---|---|
| **Read Uncommitted** | Allowed | Allowed | Allowed |
| **Read Committed** | Prevented | Allowed | Allowed |
| **Repeatable Read** | Prevented | Prevented | Allowed (MySQL InnoDB prevents via Next-Key Locks) |
| **Serializable** | Prevented | Prevented | Prevented |

## 3. Database Normalization
- **1NF:** Atomic attribute values, no repeating groups, unique column names.
- **2NF:** 1NF + No partial dependencies (every non-prime attribute fully depends on candidate key).
- **3NF:** 2NF + No transitive dependencies ($A \to B$ and $B \to C$).
- **BCNF:** Stricter version of 3NF: For every functional dependency $X \to Y$, $X$ must be a super key.

## 4. Indexing & Storage Engines
- **B-Tree vs. B+ Tree:**
  - B+ Tree stores all records only at leaf nodes, while internal nodes store only routing keys.
  - B+ Tree leaf nodes are linked sequentially as a doubly linked list, enabling fast range scans.
- **Clustered vs. Non-Clustered Index:**
  - **Clustered:** Determines physical order of data on disk. Only one per table (typically Primary Key).
  - **Non-Clustered (Secondary):** Separate structure with pointers back to the clustered index/row ID.

## 5. SQL vs. NoSQL
- **SQL (Relational):** Structured, schema-enforced, ACID-compliant, scale vertically (PostgreSQL, MySQL).
- **NoSQL:** Flexible schemas, horizontal partitioning, BASE properties (MongoDB, Cassandra, DynamoDB, Redis).
