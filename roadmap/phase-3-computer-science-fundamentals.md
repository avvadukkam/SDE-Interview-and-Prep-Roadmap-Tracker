# Phase 3: Computer Science Fundamentals

**Difficulty:** Intermediate | **Estimated Duration:** 4–5 Weeks | **Topics:** 6

> **Overview:** Unifies Operating Systems (Section 8), Concurrency & Memory (duplicated in Section 10), Networking (Sections 7 & 10), and Databases (Section 5) into the foundational systems layer required before building backend applications or distributed architectures.

## Why This Phase Is Ordered Here
You cannot reason about database connection pools, thread-safe services, or distributed system bottlenecks (Phase 6) without first understanding OS processes/threads, virtual memory, TCP/HTTP networking, and relational/NoSQL storage.

## Topics in This Phase

### 3.1 Operating Systems: Processes, Threads & Concurrency
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `14 hrs`
- **What It Covers:** Deduplicates and unifies OS processes vs. threads, CPU scheduling, synchronization primitives (mutexes, semaphores, monitors), deadlocks, and async concurrency.
- **Why It Is Important:** Backend engineers write multi-threaded and asynchronous services daily; concurrency bugs (race conditions, deadlocks) are prime interview topics.
- **Completion Criteria:** Can explain processes vs. threads, prevent race conditions and deadlocks, and implement producer-consumer synchronization.

- [ ] Processes vs. Threads, context switching, and Parallelism vs. Concurrency — `P0`
- [ ] Thread safety, Race conditions, Critical sections, and Synchronization primitives (Mutexes, Semaphores, Monitors) — `P0`
- [ ] Deadlock conditions (Coffman conditions) and Deadlock detection, prevention, and avoidance — `P0`
- [ ] Asynchronous programming: Event loops, Callbacks, Promises, Futures, and Coroutines — `P0`
- [ ] CPU Scheduling algorithms: FIFO, Round Robin, Shortest Job First, Earliest Deadline First (EDF), Fair Share, WFQ — `P1`

### 3.2 Virtual Memory, Paging & File Systems
- **Tier:** `Should Learn (P1)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `10 hrs`
- **What It Covers:** Covers virtual address spaces, demand paging, page tables, TLB, page replacement policies (LRU, FIFO, Clock), memory-mapped files, and local/network file systems.
- **Why It Is Important:** Explains how databases use `mmap` and buffer pools, why page faults hurt p99 latency, and how OS caching works.
- **Completion Criteria:** Can trace a virtual address lookup (TLB -> Page Table -> Disk Page Fault) and explain journaling file systems.

- [ ] Virtual Memory, Demand Paging, Page Tables, TLB, and Page Faults — `P0`
- [ ] Page Replacement Algorithms: LRU, FIFO, Optimal, and Clock algorithm — `P1`
- [ ] Buddy memory allocation and Memory-mapped files (mmap) — `P1`
- [ ] File Systems: Inodes, Journaling file systems (ext3, ext4), File system encryption, and Network file systems (NFS, SMB) — `P1`

### 3.3 Computer Networks, TCP/IP, DNS & HTTP
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `12 hrs`
- **What It Covers:** Covers the OSI & TCP/IP models, TCP vs. UDP (3-way handshake, flow/congestion control), DNS resolution, sockets, RPC, and HTTP/1.1, HTTP/2, HTTP/3, and TLS.
- **Why It Is Important:** Every web request, API call, and microservice interaction traverses DNS, TCP/UDP, TLS, and HTTP.
- **Completion Criteria:** Can trace the end-to-end lifecycle of an HTTPS request from DNS resolution to socket teardown.

- [ ] TCP/IP stack & OSI model layers — `P0`
- [ ] TCP vs. UDP: 3-way handshake, reliability, flow control, congestion control, and QUIC/UDP use cases — `P0`
- [ ] DNS (Domain Name System): hierarchical resolution process, record types (A, AAAA, CNAME, NS), and TTL caching — `P0`
- [ ] HTTP protocol: Request methods (GET, POST, PUT, PATCH, DELETE), Status codes (2xx–5xx), headers, HTTP/1.1 vs. HTTP/2 vs. HTTP/3 — `P0`
- [ ] Client-server architecture, OS Sockets, WebSockets, and Remote Procedure Call (RPC / gRPC) — `P1`

### 3.4 Relational Databases (SQL), Normalization & Transactions
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `16 hrs`
- **What It Covers:** Covers relational schema design, constraints, normal forms (1NF–BCNF), SQL DDL/DML/DQL/DCL, Joins, Window Functions, ACID properties, and Transaction Isolation Levels.
- **Why It Is Important:** Relational databases remain the default transactional store for business-critical software; SQL and ACID isolation are tested in both coding and system design rounds.
- **Completion Criteria:** Can write complex Joins/Window functions, normalize schemas to 3NF/BCNF, and explain SQL isolation levels.

- [ ] Relational schema constraints (Primary Key, Foreign Key, Unique, Check, Default) & Normalization (1NF, 2NF, 3NF, BCNF) — `P0`
- [ ] SQL Queries (DQL): Joins (Inner, Left/Right/Full Outer, Cross), GROUP BY/HAVING, Subqueries, and Window Functions — `P0`
- [ ] SQL DDL (CREATE, ALTER, DROP), DML (INSERT, UPDATE, DELETE, MERGE/UPSERT, TRUNCATE), and DCL (GRANT, REVOKE) — `P0`
- [ ] Transactions & ACID Properties (Atomicity, Consistency, Isolation, Durability) with COMMIT/ROLLBACK — `P0`
- [ ] Transaction Isolation Levels: Read Uncommitted, Read Committed, Repeatable Read, Serializable (dirty/non-repeatable/phantom reads) — `P0`
- [ ] Views, Materialized Views, Stored Procedures, Functions, and Triggers (BEFORE/AFTER) — `P1`

### 3.5 Database Indexing & Query Optimization
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `10 hrs`
- **What It Covers:** Covers B-Tree and B+ Tree indexes, clustered vs. non-clustered indexes, composite indexes (leftmost prefix rule), bitmap indexes, covering indexes, and `EXPLAIN ANALYZE` query plans.
- **Why It Is Important:** Bad indexing is the #1 cause of database bottlenecks in production systems; interviewers regularly ask how to optimize slow queries.
- **Completion Criteria:** Can design composite indexes for query access patterns and read `EXPLAIN` plans to eliminate sequential scans.

- [ ] B-Tree vs. B+ Tree storage internals and Clustered vs. Secondary indexes — `P0`
- [ ] Composite Indexes, column ordering (leftmost prefix rule), and Covering Indexes — `P0`
- [ ] Bitmap Indexing, Hash Indexing, and Full-Text / Inverted Indexes — `P1`
- [ ] Query execution plans (`EXPLAIN ANALYZE`), index selectivity, and write-amplification trade-offs — `P0`

### 3.6 NoSQL Databases (Key-Value, Document, Column-Family, Graph)
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `10 hrs`
- **What It Covers:** Covers the 4 NoSQL categories—Key-Value (Redis/DynamoDB), Document (MongoDB), Wide-Column (Cassandra), and Graph (Neo4j)—plus LSM-Trees vs. B-Trees and SQL vs. NoSQL selection criteria.
- **Why It Is Important:** System design interviews require choosing the right storage engine (SQL, Document, Key-Value, Columnar, or Graph) for each workload's read/write/consistency profile.
- **Completion Criteria:** Can justify when to use Relational, Key-Value, Document, Wide-Column, or Graph databases based on access patterns.

- [ ] Key-Value stores (Redis, DynamoDB): in-memory caching, partition keys, TTLs — `P0`
- [ ] Document databases (MongoDB): schema flexibility, embedding vs. referencing, indexing — `P1`
- [ ] Column-family stores (Cassandra, Bigtable): LSM-Trees, SSTables, high write throughput, time-series — `P1`
- [ ] Graph databases (Neo4j): traversal-heavy social/recommendation relationships — `P1`
- [ ] SQL vs. NoSQL decision framework and ACID vs. BASE trade-offs — `P0`
