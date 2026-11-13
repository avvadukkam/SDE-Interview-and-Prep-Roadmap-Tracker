# Phase 1: Programming Foundations

**Difficulty:** Beginner | **Estimated Duration:** 2–3 Weeks | **Topics:** 6

> **Overview:** Establishes fluency in a core programming language (Python, Java, C++, or Go), execution memory model (Stack vs. Heap), recursion, exception handling, and Big-O complexity analysis before tackling data structures.

## Why This Phase Is Ordered Here
Every data structure, algorithm, and system component is expressed in code. Mastering control flow, memory layout, recursion, and Big-O notation first prevents rote memorization in Phase 2.

## Topics in This Phase

### 1.1 Programming Fundamentals & Language Mechanics
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Beginner` | **Est. Study Time:** `12 hrs`
- **What It Covers:** Covers variables, primitive and reference types, control flow, type systems, and programming paradigms (imperative, procedural, declarative, event-driven).
- **Why It Is Important:** Writing bug-free interview code requires deep familiarity with how your primary language handles types, mutability, pass-by-value vs. reference, and scoping.
- **Completion Criteria:** Can write clean loops, conditionals, type conversions, and string manipulations in your primary language without syntax lookups.

- [ ] Variables, primitive types, and control flow (conditionals, loops, short-circuiting) — `P0`
- [ ] Static vs. Dynamic typing & Strong vs. Weak typing — `P1`
- [ ] Nominal vs. Structural typing — `P1`
- [ ] Programming paradigms: Imperative, Procedural, Declarative, and Event-driven — `P1`
- [ ] Regular expressions: pattern matching, capture groups, and pitfalls — `P1`

### 1.2 Functions, Call Stack & Functional Concepts
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Beginner` | **Est. Study Time:** `10 hrs`
- **What It Covers:** Covers function execution frames, base cases and recursive decomposition, tail recursion, closures, and higher-order functions.
- **Why It Is Important:** Recursion is the direct foundation for trees, graphs, divide-and-conquer, backtracking, and dynamic programming.
- **Completion Criteria:** Can trace recursive call trees, identify stack depth, and convert simple recursion to iteration using an explicit stack.

- [ ] Call stack frames, base cases, and recursive leap of faith — `P0`
- [ ] Tail recursion and stack overflow prevention — `P0`
- [ ] Lambda expressions, closures, pure functions, and higher-order functions — `P1`
- [ ] Referential transparency and immutability — `P1`
- [ ] Mutual recursion, anonymous recursion, and Lambda calculus basics — `P2`

### 1.3 Memory Layout & Garbage Collection
- **Tier:** `Should Learn (P1)` | **Difficulty:** `Beginner` | **Est. Study Time:** `8 hrs`
- **What It Covers:** Explains how programs organize memory across code, data, stack, and heap segments, and how automatic garbage collectors reclaim memory.
- **Why It Is Important:** Understanding stack vs. heap allocation explains pointer semantics, object overhead, memory leaks, and latency spikes in production services.
- **Completion Criteria:** Can explain stack vs. heap trade-offs and compare reference counting with generational mark-and-sweep GC.

- [ ] Stack vs. Heap memory allocation and lifetimes — `P0`
- [ ] Data segment vs. Code segment — `P1`
- [ ] Manual vs. Automatic memory management — `P1`
- [ ] Tracing (Mark and Sweep) vs. Reference counting garbage collection — `P0`
- [ ] Generational Garbage Collection (Young/Old generations, stop-the-world pauses) — `P1`

### 1.4 Object-Oriented Programming (OOP) Foundations
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Beginner` | **Est. Study Time:** `10 hrs`
- **What It Covers:** Covers classes, objects, interfaces, encapsulation, abstraction, inheritance, polymorphism, and composition vs. inheritance.
- **Why It Is Important:** OOP provides the vocabulary for structuring modular code and is the direct prerequisite for Low-Level Design (Phase 5).
- **Completion Criteria:** Can design clean class hierarchies, use interfaces for polymorphism, and refactor brittle inheritance into composition.

- [ ] Classes, objects, constructors, interfaces, and abstract classes — `P0`
- [ ] Encapsulation and access modifiers (state hiding & invariants) — `P0`
- [ ] Abstraction and interface contracts — `P0`
- [ ] Inheritance and Polymorphism (compile-time overloading vs. runtime overriding) — `P0`
- [ ] Composition vs. Inheritance: why to favor composition over deep class hierarchies — `P0`

### 1.5 Error Handling, Exceptions & Debugging Basics
- **Tier:** `Should Learn (P1)` | **Difficulty:** `Beginner` | **Est. Study Time:** `6 hrs`
- **What It Covers:** Covers exception hierarchies, error propagation, resource cleanup (try/finally/context managers), exceptions vs. error codes, and systematic debugging.
- **Why It Is Important:** Production-grade code and LLD solutions require predictable error handling, invariant validation, and fast root-cause debugging.
- **Completion Criteria:** Consistently validates inputs, handles edge cases cleanly, and uses step debugging effectively.

- [ ] Exception handling mechanisms (try/catch/finally, context managers) — `P1`
- [ ] Error propagation, custom domain exceptions, and error recovery — `P1`
- [ ] Exceptions vs. Error codes / Result types & exception safety — `P1`
- [ ] Debugging techniques: interactive debuggers, breakpoints, print/log debugging, rubber ducking — `P1`

### 1.6 Problem-Solving Strategy & Time/Space Complexity
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Beginner` | **Est. Study Time:** `10 hrs`
- **What It Covers:** Covers asymptotic analysis (Big-O, Big-Omega, Big-Theta), worst/average/amortized complexity, auxiliary space vs. input space, and structured problem-solving steps.
- **Why It Is Important:** Every coding interview ends with a complexity analysis; Big-O determines whether an algorithm scales or times out.
- **Completion Criteria:** Can state and justify exact time and space complexity (including recursion stack) for any code you write.

- [ ] Big O (upper bound), Big Omega (lower bound), and Big Theta (tight bound) notations — `P0`
- [ ] Time complexity of loops, nested loops, and recursive recurrence relations — `P0`
- [ ] Space complexity analysis: auxiliary heap space vs. recursion call stack space — `P0`
- [ ] Space-time trade-offs and amortized complexity (e.g., dynamic array resizing) — `P1`
- [ ] Structured problem-solving: Understand -> Plan -> Break down -> Solve simpler -> Implement -> Test — `P1`
