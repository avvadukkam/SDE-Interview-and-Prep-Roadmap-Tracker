# Phase 6: High-Level Design (HLD) and System Design

**Difficulty:** Advanced | **Estimated Duration:** 4–6 Weeks | **Topics:** 5

> **Overview:** Unifies System Architecture (Section 12), System Design (Section 13), Cloud Messaging (Section 3), Distributed File Systems (Section 8), and the 76-question `System Design/Microservices.md` guide, while adding missing CAP/PACELC and classic HLD case studies.

## Why This Phase Is Ordered Here
High-Level Design synthesizes networking (Phase 3), databases/NoSQL (Phase 3), APIs (Phase 4), and component design (Phase 5) to architect distributed systems serving millions of requests.

## Topics in This Phase

### 6.1 Scalability, Load Balancing, CDNs & API Gateways
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `12 hrs`
- **What It Covers:** Covers horizontal vs. vertical scaling, stateless service tiers, Consistent Hashing, L4 vs. L7 Load Balancing, DNS/Anycast routing, CDNs, and API Gateways.
- **Why It Is Important:** These are the entry-tier building blocks of every system design architecture diagram.
- **Completion Criteria:** Can diagram edge-to-service traffic flow (DNS -> CDN -> L7 LB -> API Gateway -> Stateless Services) and explain Consistent Hashing.

- [ ] Horizontal vs. Vertical scaling, Stateless vs. Stateful services, and Auto-scaling — `P0`
- [ ] Consistent Hashing: hash ring, virtual nodes, and minimizing key remapping on node churn — `P0`
- [ ] Load Balancing: L4 (TCP) vs. L7 (HTTP), Round Robin, Least Connections, Adaptive algorithms, Health checks — `P0`
- [ ] DNS Load Balancing, Anycast routing, and Content Delivery Networks (Push vs. Pull CDNs) — `P0`
- [ ] API Gateway: routing, TLS termination, rate limiting, authentication, and request aggregation — `P0`

### 6.2 Distributed Caching, Message Queues & Event-Driven Architecture
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Advanced` | **Est. Study Time:** `14 hrs`
- **What It Covers:** Consolidates duplicated caching and messaging sections into one module covering Cache-Aside, Write-Through/Write-Behind, cache stampede mitigation, RabbitMQ/SQS vs. Kafka/Kinesis, DLQs, and backpressure.
- **Why It Is Important:** Caching scales read-heavy workloads by 10–100x; asynchronous message queues decouple write-heavy and bursty workloads.
- **Completion Criteria:** Can select the right caching pattern and message broker (SQS vs. Kafka) and handle hot keys, stampedes, and poison messages.

- [ ] Caching Strategies: Cache-Aside, Read-Through, Write-Through, Write-Behind (Write-Back), and Refresh-Ahead — `P0`
- [ ] Cache Eviction, Invalidation, Hot Keys, and Cache Stampede / Thundering Herd prevention (mutex locks, jittered TTLs) — `P0`
- [ ] Message Queues (SQS, RabbitMQ): standard vs. FIFO, visibility timeout, retries, poison messages, Dead-Letter Queues (DLQ) — `P0`
- [ ] Event-Driven Architecture & Streaming (Apache Kafka, Kinesis, SNS/EventBridge): pub/sub fan-out, consumer groups, offset retention — `P0`
- [ ] Delivery guarantees (at-most-once, at-least-once, exactly-once), deduplication, and backpressure — `P0`

### 6.3 Database Scaling: Replication, Partitioning (Sharding) & Distributed Storage
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Advanced` | **Est. Study Time:** `14 hrs`
- **What It Covers:** Covers read replicas, leader-follower/multi-leader/leaderless replication, horizontal sharding strategies, hot shards, cross-shard joins, and distributed file/object systems (HDFS, Ceph, S3).
- **Why It Is Important:** The stateful data tier is the hardest part of any system to scale horizontally.
- **Completion Criteria:** Can choose partition keys, calculate quorum consistency (R + W > N), and mitigate replication lag and hot partitions.

- [ ] Replication: Single-Leader (Leader-Follower), Multi-Leader, and Leaderless (Dynamo-style quorum R + W > N) — `P0`
- [ ] Replication lag anomalies and Consistency models (Read-after-write, Monotonic reads, Eventual consistency) — `P0`
- [ ] Partitioning / Sharding: Range-based vs. Hash-based sharding, directory-based routing, and hot-partition mitigation — `P0`
- [ ] Distributed File & Object Storage: HDFS, Ceph, and S3 object storage architecture (moved from OS section) — `P1`

### 6.4 Microservices, Distributed Systems & CAP / Consensus
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Advanced` | **Est. Study Time:** `16 hrs`
- **What It Covers:** Covers CAP & PACELC theorems, consensus & leader election (Raft/Paxos), distributed transactions (Saga choreography vs. orchestration, 2PC, Outbox pattern), CQRS, Event Sourcing, Circuit Breakers, Service Mesh, and the preserved 76 Microservices Interview Q&A.
- **Why It Is Important:** Distributed systems trade off consistency, availability, and latency under network partitions; mastering these trade-offs is the core of HLD.
- **Completion Criteria:** Can defend CP vs. AP choices, design Saga workflows, and answer the repository's 76 microservices architecture questions.

- [ ] CAP Theorem (Consistency, Availability, Partition Tolerance) & PACELC Theorem (Latency vs. Consistency) — `P0`
- [ ] ACID vs. BASE, Eventual Consistency, and Consensus / Leader Election (Paxos, Raft, ZooKeeper/etcd) — `P0`
- [ ] Microservices Patterns: Service Discovery, Circuit Breaker, Bulkhead, Sidecar, Service Mesh (Istio/Linkerd), Strangler Fig — `P0`
- [ ] Distributed Transactions: Two-Phase Commit (2PC), Saga Pattern (Choreography vs. Orchestration), Transactional Outbox — `P0`
- [ ] Event Sourcing & CQRS (Command Query Responsibility Segregation) — `P1`
- [ ] Top 76 Microservices Architecture Interview Questions (Preserved from `System Design/Microservices.md`) — `P0`

### 6.5 Practical System Design (HLD) Interview Case Studies
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Advanced` | **Est. Study Time:** `20 hrs`
- **What It Covers:** Applies back-of-the-envelope capacity estimation (QPS, bandwidth, storage, p95 latency) and end-to-end architecture design to the most frequently asked HLD interview problems.
- **Why It Is Important:** System Design interviews require structuring a 45-minute deep dive from requirements and capacity math to APIs, data model, high-level diagram, and bottleneck resolution.
- **Completion Criteria:** Can drive a 45-minute HLD discussion unprompted, covering capacity math, APIs, data model, scaling, and failure modes.

- [ ] 4-Step HLD Framework: Requirements & Scope -> Capacity Estimation (QPS/Storage) -> High-Level Design -> Deep Dive & Bottlenecks — `P0`
- [ ] Design a URL Shortener (TinyURL) & Design a Distributed Rate Limiter — `P0`
- [ ] Design a Social Media News Feed (Twitter/Instagram fan-out-on-write vs. hybrid fan-out-on-read) — `P0`
- [ ] Design a Real-Time Chat System (WhatsApp/Slack WebSockets, presence, message ordering) — `P0`
- [ ] Design a Notification Service, Web Crawler, Payment System (idempotency & ledger), and Proximity/Ride-Sharing (QuadTree/Geohash) — `P1`
