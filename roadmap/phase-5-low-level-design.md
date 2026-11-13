# Phase 5: Low-Level Design (LLD)

**Difficulty:** Intermediate | **Estimated Duration:** 3–4 Weeks | **Topics:** 4

> **Overview:** Unifies all Low-Level Design content from Section 6 and removes the duplicate Design Patterns lists previously scattered in Sections 10 and 13.

## Why This Phase Is Ordered Here
LLD applies OOP (Phase 1), data structures (Phase 2), concurrency (Phase 3), and SOLID principles (Phase 4) to design extensible, thread-safe software components before scaling to multi-machine HLD (Phase 6).

## Topics in This Phase

### 5.1 Requirements Clarification, Domain Modeling & UML
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `8 hrs`
- **What It Covers:** Covers translating ambiguous requirements into entities, value objects, aggregates, invariants, and communicating designs with UML Class, Sequence, and State Machine diagrams.
- **Why It Is Important:** LLD interviews test how systematically you clarify scope, identify core entities, and communicate relationships before writing code.
- **Completion Criteria:** Can turn a problem prompt into a clean entity model and UML class/state diagram within 10 minutes.

- [ ] Clarify functional/non-functional requirements and define extension points without overengineering — `P0`
- [ ] Identify entities, value objects, aggregates, invariants, and object lifecycles — `P0`
- [ ] UML Class Diagrams: association, aggregation, composition, inheritance, realization — `P0`
- [ ] UML Sequence Diagrams (method calls, async boundaries) & State Machine Diagrams (transitions, guards) — `P1`

### 5.2 Design Patterns in Practice (Creational, Structural, Behavioral)
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `14 hrs`
- **What It Covers:** Consolidates all Creational, Structural, and Behavioral design patterns into one authoritative module focused on practical applicability and knowing when NOT to force a pattern.
- **Why It Is Important:** Patterns like Strategy, Factory, Observer, Builder, State, and Decorator solve recurring extensibility problems in LLD interviews and production codebases.
- **Completion Criteria:** Can implement top 8 design patterns from memory and justify trade-offs without forcing patterns unnecessarily.

- [ ] Creational Patterns: Factory / Abstract Factory (P0), Builder (P1), Singleton & thread-safety pitfalls (P1), Prototype (P2) — `P0`
- [ ] Behavioral Patterns: Strategy (P0), Observer / Pub-Sub (P0), State (P1), Command (P1), Chain of Responsibility, Iterator, Template Method — `P0`
- [ ] Structural Patterns: Adapter / Facade (P1), Decorator / Proxy (P1), Composite (P1), Bridge, Flyweight — `P1`
- [ ] Anti-overengineering: Recognize when NOT to introduce a design pattern — `P0`

### 5.3 Component Design, Persistence Boundaries & Thread Safety
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Advanced` | **Est. Study Time:** `10 hrs`
- **What It Covers:** Covers interface-first component contracts, Repository / Unit of Work patterns, fine-grained locking, immutability, atomic operations, and handling mid-interview requirement changes.
- **Why It Is Important:** Senior LLD rounds always probe concurrency (e.g., two users booking the same movie seat simultaneously) and schema/extensibility trade-offs.
- **Completion Criteria:** Can write thread-safe, interface-driven domain services that cleanly adapt to follow-up requirement changes.

- [ ] Interface-first design, stable public contracts, and dependency injection for testability — `P0`
- [ ] Repository / Unit of Work patterns, data access layering, and transaction boundaries — `P0`
- [ ] Thread safety in LLD: fine-grained locks, read-write locks, concurrent maps, immutability, race prevention — `P0`
- [ ] Demonstrating a requirement change without rewriting the core design — `P0`

### 5.4 Classic Low-Level Design (LLD) Interview Problems
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Advanced` | **Est. Study Time:** `20 hrs`
- **What It Covers:** Hands-on practice across all 12 classic LLD problems from the repository: LRU/LFU Cache, Parking Lot, Rate Limiter, Logging Framework, Notification Service, Elevator, Movie Booking, Splitwise, Vending Machine, In-Memory File System, Chess/Tic-Tac-Toe, and Library Management.
- **Why It Is Important:** Practicing full 45-minute LLD simulations builds the speed needed to define models, apply patterns, and write compilable code under time constraints.
- **Completion Criteria:** Can complete requirement scoping, class diagramming, and core working code for any of the 12 classic LLD problems in 45 minutes.

- [ ] Design a Cache with LRU / LFU eviction policies (HashMap + Doubly Linked List) — `P0`
- [ ] Design a Rate Limiter (Strategy interface for Token Bucket, Leaky Bucket, Sliding Window) — `P0`
- [ ] Design a Parking Lot (spot types, pricing strategies, tickets, concurrent entry gates) — `P0`
- [ ] Design a Logging Framework (appenders, log levels, thread safety) & Notification Framework (channels, retries) — `P0`
- [ ] Design an In-Memory File System (Composite/Trie directory tree) — `P0`
- [ ] Design a Movie Ticket Booking System (seat locking with TTL expiry) & Splitwise Expense Sharing System — `P1`
- [ ] Design an Elevator System (dispatch scheduling), Vending Machine (State pattern), Chess/Tic-Tac-Toe, and Library System — `P1`
