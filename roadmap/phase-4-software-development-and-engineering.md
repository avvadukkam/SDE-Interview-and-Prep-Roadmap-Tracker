# Phase 4: Software Development and Engineering

**Difficulty:** Intermediate | **Estimated Duration:** 3–4 Weeks | **Topics:** 5

> **Overview:** Brings together Version Control (Section 15), Software Development Methodologies, Coding Best Practices (Section 9), Software Testing Foundations (Section 14), and Application Architecture (Section 12) so learners can build, test, and structure real-world services.

## Why This Phase Is Ordered Here
Before designing complex object models (Phase 5) or distributed architectures (Phase 6), an engineer needs mastery of Git, CLI workflows, clean code/SOLID, automated testing, and REST/RPC API design.

## Topics in This Phase

### 4.1 Git & Version Control Workflows
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Beginner` | **Est. Study Time:** `6 hrs`
- **What It Covers:** Covers Git internals (commits, trees, blobs, refs), branching strategies, merge vs. rebase, conflict resolution, `git bisect`, and pull request code review workflows.
- **Why It Is Important:** Version control and collaborative code review are daily engineering essentials.
- **Completion Criteria:** Can branch, rebase interactively, resolve conflicts, and use `reflog`/`bisect` confidently.

- [ ] Git fundamentals: staging, commits, branches, HEAD, and remote tracking (GitHub, GitLab, Bitbucket) — `P0`
- [ ] Git Merge vs. Git Rebase, squash commits, cherry-pick, reflog, and resolving merge conflicts — `P0`
- [ ] Collaborative workflows: trunk-based development, feature branches, and code reviews — `P1`

### 4.2 Linux, Shell & Command-Line Fundamentals
- **Tier:** `Should Learn (P1)` | **Difficulty:** `Beginner` | **Est. Study Time:** `8 hrs`
- **What It Covers:** Covers POSIX file permissions, standard streams (stdin/stdout/stderr), pipes, process management (`ps`, `top`, `kill`), network diagnostics (`curl`, `netstat`/`ss`, `dig`), and text processing.
- **Why It Is Important:** Backend servers, containers, and CI runners run on Linux; CLI fluency is crucial for debugging production systems.
- **Completion Criteria:** Can inspect logs, diagnose CPU/memory/port issues, and chain shell commands comfortably.

- [ ] File navigation, permissions (`chmod`, `chown`), symlinks, and standard streams/pipes (`|`, `>`, `2>&1`) — `P0`
- [ ] Text & log inspection (`grep`, `awk`, `sed`, `jq`, `tail -f`, `less`) — `P1`
- [ ] Process, memory, disk, and network diagnostics (`ps`, `top`, `lsof`, `df`, `du`, `curl`, `ss`) — `P1`

### 4.3 SDLC, Clean Code & SOLID Principles
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `10 hrs`
- **What It Covers:** Consolidates duplicated coverage of Clean Code, DRY, KISS, YAGNI, Law of Demeter, Cohesion/Coupling, and the 5 SOLID principles from Sections 6, 9, and 13.
- **Why It Is Important:** Interviewers grade coding and LLD rounds heavily on modularity, naming, separation of concerns, and adherence to SOLID principles.
- **Completion Criteria:** Can spot SOLID violations in existing code and refactor toward clean interfaces and dependency injection.

- [ ] Code readability, naming conventions, modularity, high cohesion, and loose coupling — `P0`
- [ ] DRY (Don't Repeat Yourself), KISS (Keep It Simple), YAGNI, and Law of Demeter — `P0`
- [ ] Single Responsibility Principle (SRP) & Open/Closed Principle (OCP) — `P0`
- [ ] Liskov Substitution Principle (LSP) & Interface Segregation Principle (ISP) — `P0`
- [ ] Dependency Inversion Principle (DIP), Dependency Injection, and Inversion of Control — `P0`
- [ ] Software Development Lifecycle (SDLC): Agile, iterative delivery, and code review culture — `P1`

### 4.4 Software Testing Foundations & Quality Engineering
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `10 hrs`
- **What It Covers:** Covers the testing pyramid (unit, integration, E2E), test doubles (mocks, stubs, fakes, spies), contract testing, database integration testing, and property-based testing.
- **Why It Is Important:** Writing testable code and verifying edge cases separates senior engineering candidates from pure competitive programmers.
- **Completion Criteria:** Can design unit and integration tests using mocks/fakes and test boundary/failure cases systematically.

- [ ] Unit, integration, end-to-end (E2E), and acceptance tests; Testing Pyramid vs. Testing Trophy — `P0`
- [ ] Test doubles: Mocks, stubs, fakes, spies, and deterministic fixtures — `P0`
- [ ] Test coverage metrics and their limitations; boundary-value analysis — `P0`
- [ ] API contract tests (consumer-driven contracts), database migration tests, and Testcontainers — `P1`
- [ ] Concurrency tests, fault injection, idempotency tests, and property-based/fuzz testing — `P1`

### 4.5 API Development & Application Architecture
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `12 hrs`
- **What It Covers:** Covers RESTful API design, idempotency, pagination, versioning, gRPC/GraphQL comparison, Layered Architecture (Presentation, Business Logic, Data Access), and monolith vs. SOA.
- **Why It Is Important:** Clean API design and layered service architecture bridge single-process code and multi-service High-Level Design.
- **Completion Criteria:** Can design REST/gRPC API contracts with pagination, versioning, and idempotency guarantees.

- [ ] RESTful API design: resource naming, HTTP verbs, status codes, pagination (cursor vs. offset), filtering — `P0`
- [ ] API Versioning (URI, header, query), Idempotency keys, and safe retries — `P0`
- [ ] REST vs. gRPC (Protocol Buffers, HTTP/2 streaming) vs. GraphQL trade-offs — `P0`
- [ ] Layered Architecture: Presentation, Business Logic, Data Access (Repository), and Cross-cutting concerns — `P1`
- [ ] Monolithic Architecture vs. Service-Oriented Architecture (SOA) & 12-Factor App principles — `P1`
