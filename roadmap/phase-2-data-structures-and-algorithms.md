# Phase 2: Data Structures and Algorithms

**Difficulty:** Intermediate | **Estimated Duration:** 6–8 Weeks | **Topics:** 11

> **Overview:** Consolidated and properly sequenced from the original repository's separate 'Algorithms' (Section 2), 'Data Structures' (Section 4), and 'Problem-solving and Coding' (Section 9) sections so each data structure is learned before the algorithms that depend on it.

## Why This Phase Is Ordered Here
Linear structures (Arrays, Linked Lists, Stacks, Queues, Hash Tables) must precede Searching/Sorting and hierarchical structures (Trees, Heaps, Tries), which in turn unlock Graphs, Greedy, Backtracking, and Dynamic Programming.

## Topics in This Phase

### 2.1 Arrays, Strings & Two-Pointer / Sliding Window Patterns
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Beginner` | **Est. Study Time:** `16 hrs`
- **What It Covers:** Covers contiguous memory arrays, dynamic arrays, string manipulation, prefix sums, two pointers, sliding window, and Kadane's algorithm.
- **Why It Is Important:** Arrays and strings account for over 35% of SDE coding interview questions and form the backing storage for hash tables and heaps.
- **Completion Criteria:** Can immediately recognize and code Two Pointers, Sliding Window, and Prefix Sum solutions in O(N) time.

- [ ] Static vs. Dynamic arrays, contiguous memory indexing, and 2D matrices — `P0`
- [ ] Two Pointers pattern (opposite ends, same direction, partitioning) — `P0`
- [ ] Sliding Window pattern (fixed and variable length windows) — `P0`
- [ ] Maximum Subarray Sum (Kadane's Algorithm) and Prefix Sums — `P0`
- [ ] String fundamentals: Palindrome check, anagram check, immutability, StringBuilder — `P0`

### 2.2 Linked Lists & Pointer Manipulation
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Beginner` | **Est. Study Time:** `10 hrs`
- **What It Covers:** Covers singly, doubly, and circular linked lists, dummy head nodes, in-place reversal, and Floyd's fast-and-slow pointer cycle detection.
- **Why It Is Important:** Tests pointer precision and underpins LRU caches, hash table chaining, deque implementations, and OS free-lists.
- **Completion Criteria:** Can manipulate list pointers without losing references or triggering null-pointer bugs.

- [ ] Singly linked lists, Doubly linked lists, and Circular linked lists — `P0`
- [ ] Fast and slow pointers (Floyd's Tortoise and Hare cycle detection & middle finding) — `P0`
- [ ] In-place reversal, merging sorted lists, and dummy sentinel nodes — `P0`
- [ ] Skip lists (probabilistic O(log N) search) — `P1`
- [ ] Unrolled linked lists & Lock-free linked lists (moved from P0 to Optional/Advanced P2) — `P2`

### 2.3 Stacks, Queues & Monotonic Structures
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Beginner` | **Est. Study Time:** `10 hrs`
- **What It Covers:** Covers LIFO stacks, FIFO queues, circular queues, double-ended queues (Deques), expression evaluation, and monotonic stacks/queues.
- **Why It Is Important:** Stacks power DFS, backtracking, and parsing; queues power BFS, rate buffers, and asynchronous task scheduling.
- **Completion Criteria:** Can implement stack/queue ADTs and solve monotonic stack problems in O(N) time.

- [ ] Stack implementations (array-based and linked-list-based) & expression evaluation — `P0`
- [ ] Queue implementations, Circular queue, and BFS/scheduling applications — `P0`
- [ ] Double-ended queue (Deque) and sliding window maximum — `P1`
- [ ] Monotonic Stack (Next Greater Element, Daily Temperatures, Largest Rectangle in Histogram) — `P0`
- [ ] Priority stacks — `P2`

### 2.4 Hash Tables & Probabilistic Data Structures
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `10 hrs`
- **What It Covers:** Covers hash functions, load factors, collision resolution (chaining vs. open addressing), and space-efficient probabilistic structures (Bloom Filters, Count-Min Sketch).
- **Why It Is Important:** Hash tables turn O(N) searches into O(1) lookups in coding problems and underpin database hash indexes and distributed caches.
- **Completion Criteria:** Can implement a hash table from scratch and use hash maps/sets to optimize O(N^2) lookups to O(N).

- [ ] Hash functions, uniform distribution, load factor, and rehashing — `P0`
- [ ] Collision resolution: Separate Chaining vs. Open Addressing (linear/quadratic probing) — `P0`
- [ ] Robin Hood Hashing & Cuckoo Hashing (reclassified from P0 to P1/P2) — `P1`
- [ ] Bloom Filters (false positive trade-offs) & Count-Min Sketch for high-scale systems — `P2`
- [ ] Perfect Hashing — `P2`

### 2.5 Searching, Sorting & Divide-and-Conquer
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `14 hrs`
- **What It Covers:** Covers binary search on sorted arrays and monotonic answer spaces, comparison sorts (Merge, Quick, Heap, TimSort), non-comparison sorts (Counting, Radix, Bucket), and Divide & Conquer.
- **Why It Is Important:** Binary search and sorting are fundamental building blocks for interval merging, greedy algorithms, and database index scans.
- **Completion Criteria:** Can write bug-free binary search on boundary conditions and explain stability, in-place, and time complexity of major sorts.

- [ ] Binary Search (1D/2D arrays, Peak Element, Rotated Sorted Array, Binary Search on Answer) — `P0`
- [ ] Merge Sort (stable O(N log N)), Quick Sort (partitioning & pivot selection), and QuickSelect — `P0`
- [ ] Insertion Sort, Selection Sort, Bubble Sort, and hybrid Tim Sort — `P1`
- [ ] Non-comparison sorts: Counting Sort, Radix Sort, and Bucket Sort — `P1`
- [ ] Exponential/Ternary Search & Closest Pair of Points (Divide & Conquer) — `P1`
- [ ] Academic sorts & D&C: Strassen's Matrix, Karatsuba, FFT, Shell/Bitonic/Cycle/Pancake Sort — `P2`

### 2.6 Trees, Binary Search Trees & Balanced Search Trees
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `16 hrs`
- **What It Covers:** Covers binary trees, DFS (preorder, inorder, postorder) and BFS (level-order) traversals, Binary Search Trees (BST), self-balancing trees (AVL, Red-Black), and B/B+ Trees.
- **Why It Is Important:** Trees model hierarchical data (DOM, file systems, ASTs) and database indexes (B-Trees/LSM-Trees), and are heavily tested in interviews.
- **Completion Criteria:** Can solve recursive and iterative tree traversal problems and explain BST balancing and B+ Tree branching.

- [ ] Binary Trees: Complete, Full, and Perfect binary trees; DFS & BFS level-order traversals — `P0`
- [ ] Binary Search Trees (BST): validation, insertion, deletion, Lowest Common Ancestor (LCA) — `P0`
- [ ] Self-balancing BSTs: AVL Trees (rotations) and Red-Black Trees (invariants) — `P1`
- [ ] B-Trees and B+ Trees (disk-page alignment and database indexing foundation) — `P0`
- [ ] Advanced tree variants: Splay Trees, Radix Trees, Scapegoat Trees, Tango Trees — `P2`

### 2.7 Heaps, Priority Queues & Top-K Patterns
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `8 hrs`
- **What It Covers:** Covers binary min-heaps and max-heaps, array representation of complete binary trees, O(N) heapify, Heap Sort, and Two-Heap / Top-K patterns.
- **Why It Is Important:** Heaps enable O(log N) priority scheduling, Top-K streaming queries, Median maintenance, and Dijkstra's / Prim's graph algorithms.
- **Completion Criteria:** Can implement a binary heap and solve Top-K, K-way merge, and Two-Heap streaming problems.

- [ ] Min-Heap and Max-Heap array indexing, sift-up, sift-down, and O(N) build-heap — `P0`
- [ ] Heap Sort (in-place O(N log N) sorting) — `P0`
- [ ] Top-K elements, K-way merge, and Two-Heaps pattern (Find Median from Data Stream) — `P0`

### 2.8 Graphs, Traversals, Shortest Paths & Spanning Trees
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `18 hrs`
- **What It Covers:** Unifies graph representations, BFS/DFS traversals, cycle detection, topological sorting, Union-Find (DSU), shortest paths (Dijkstra, Bellman-Ford, Floyd-Warshall), and MSTs (Kruskal, Prim).
- **Why It Is Important:** Graphs model networks, dependencies, social graphs, and routing; they bridge core DSA and distributed system topology.
- **Completion Criteria:** Can fluently code BFS, DFS, Kahn's Topological Sort, Union-Find, and Dijkstra's algorithm.

- [ ] Graph representations (Adjacency List, Adjacency Matrix, Edge List) & Directed/Undirected/Weighted/Bipartite graphs — `P0`
- [ ] Graph Traversals (BFS & DFS), Connected Components, and Cycle Detection (directed & undirected) — `P0`
- [ ] Topological Sorting (Kahn's BFS in-degree algorithm & DFS postorder) and Disjoint Set Union (Union-Find) — `P0`
- [ ] Shortest Path Algorithms: Dijkstra's (non-negative weights), Bellman-Ford (negative weights), Floyd-Warshall (all-pairs) — `P0`
- [ ] Minimum Spanning Trees (MST): Kruskal's Algorithm and Prim's Algorithm — `P0`
- [ ] Planar/Eulerian graphs, Incidence matrix, and Kosaraju's Strongly Connected Components — `P2`

### 2.9 Greedy Algorithms & Interval Scheduling
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Intermediate` | **Est. Study Time:** `8 hrs`
- **What It Covers:** Covers greedy-choice property, optimal substructure, interval scheduling, Fractional Knapsack, Huffman coding, and exchange arguments.
- **Why It Is Important:** Greedy algorithms yield fast O(N log N) or O(N) solutions when local optimal choices guarantee global optimality.
- **Completion Criteria:** Can distinguish greedy-solvable problems from DP problems and solve interval scheduling problems.

- [ ] Greedy choice property vs. Dynamic Programming; Fractional Knapsack Problem — `P0`
- [ ] Activity Selection Problem, Job Sequencing with Deadlines, and Interval Scheduling — `P1`
- [ ] Huffman Coding (prefix-free compression trees) — `P1`
- [ ] Greedy Set Cover and Greedy Graph Coloring approximations — `P2`

### 2.10 Backtracking & Dynamic Programming (DP)
- **Tier:** `Must Learn (P0)` | **Difficulty:** `Advanced` | **Est. Study Time:** `22 hrs`
- **What It Covers:** Progresses naturally from exhaustive recursive search (Backtracking with pruning) to overlapping subproblems (Top-Down Memoization and Bottom-Up Tabulation).
- **Why It Is Important:** Backtracking and DP represent the capstone of algorithmic problem solving in coding interviews.
- **Completion Criteria:** Can define state, transition equation, and base cases for 1D/2D DP and prune backtracking trees cleanly.

- [ ] Backtracking: state-space tree pruning, Subsets, Permutations, Combination Sum, N-Queens — `P0`
- [ ] DP Foundations: Overlapping subproblems, optimal substructure, Memoization (top-down) vs. Tabulation (bottom-up) — `P0`
- [ ] 1D & Knapsack DP: Fibonacci, Climbing Stairs, Coin Change, 0/1 Knapsack, Subset Sum, Rod Cutting — `P0`
- [ ] String & Sequence DP: Longest Common Subsequence (LCS), Longest Increasing Subsequence (LIS), Edit Distance — `P1`
- [ ] Interval & Matrix DP: Matrix Chain Multiplication, Grid Unique Paths — `P1`

### 2.11 Tries, String Matching & Bit Manipulation
- **Tier:** `Should Learn (P1)` | **Difficulty:** `Advanced` | **Est. Study Time:** `12 hrs`
- **What It Covers:** Covers Prefix Trees (Tries), rolling string hashes, pattern matching (KMP, Rabin-Karp), bit manipulation tricks, and advanced suffix structures.
- **Why It Is Important:** Tries power autocomplete and IP routing; bit manipulation enables compact state representation and O(1) parity checks.
- **Completion Criteria:** Can implement a Trie from scratch and apply XOR/bitmask operations without lookup.

- [ ] Trie (Prefix Tree): insertion, prefix search, DFS/BFS in a Trie, autocomplete — `P0`
- [ ] Bit Manipulation: XOR properties, bitmasks, power-of-two checks, counting set bits — `P1`
- [ ] String Hashing, Rolling Hash (Rabin-Karp), Longest Common Prefix (LCP), Longest Palindromic Substring — `P1`
- [ ] Pattern Matching: Knuth-Morris-Pratt (KMP), Z-Algorithm, Boyer-Moore, Aho-Corasick — `P1`
- [ ] Competitive String Structures: Manacher's, Suffix Array/Tree/Automaton, Burrows-Wheeler, Baker-Bird — `P2`
