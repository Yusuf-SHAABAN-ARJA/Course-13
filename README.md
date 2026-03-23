# Data Structures — Course 13 🗂️

8 C++ projects implementing core data structures from scratch, built to apply the concepts learned in Dr. Mohammad Abu-Hadhoud's Data Structures Level 1 course on [Programming Advices](https://www.programmingadvices.com).

Each project builds on the previous one — the structures are designed to work together through inheritance and composition, rather than being isolated exercises.

---

## Projects Overview

| # | Project | Data Structure | Description |
|---|---------|---------------|-------------|
| 1 | Double Linked List | `clsDblLinkedList<T>` | Generic doubly linked list with insert, delete, find, reverse, and traversal |
| 2 | Queue (Linked List-based) | `clsMyQueue<T>` | Queue built on top of the Double Linked List with 7 extensions |
| 3 | Stack (Linked List-based) | `clsMyStack<T>` | Stack built on top of the Queue using inheritance |
| 4 | Dynamic Array | `clsDynamicArray<T>` | Resizable array with manual memory management — insert, delete, find, reverse |
| 5 | Queue (Array-based) | `clsMyQueueArr<T>` | Queue interface reimplemented over the Dynamic Array |
| 6 | Stack (Array-based) | `clsMyStackArr<T>` | Stack built on top of the Array-based Queue using inheritance |
| 7 | Smart String — Undo/Redo | `clsMyString` | String class with full Undo/Redo support implemented using two stacks |
| 8 | Queue Line System | `clsQueueLine` | Real-world ticket queue simulation with issue, serve, and wait-time estimation |

---

## Structure Relationships

```
clsDblLinkedList<T>
    └── clsMyQueue<T>          (uses DblLinkedList internally)
            └── clsMyStack<T>  (inherits from Queue, overrides Push)

clsDynamicArray<T>
    └── clsMyQueueArr<T>       (uses DynamicArray internally)
            └── clsMyStackArr<T> (inherits from QueueArr, overrides Push)

clsMyString                    (uses two std::stack for Undo/Redo)
clsQueueLine                   (uses std::queue + std::stack internally)
```

---

## Key Concepts Applied

- **Templates** — all data structures are generic and work with any data type
- **Inheritance** — Stack inherits from Queue to reuse logic and only override `Push`
- **Composition** — Queue wraps the Linked List / Dynamic Array internally
- **Manual memory management** — Dynamic Array uses `new` and `delete[]` explicitly
- **Two-Stack pattern** — used in the Smart String to implement Undo/Redo history
- **Real-world modeling** — Queue Line simulates a ticket system with wait-time calculation

---

## Tech Stack

| | |
|---|---|
| Language | C++ |
| IDE | Visual Studio Community |
| Standard | C++17 |

---

## Course Info

These projects were built to apply concepts from **Data Structures Level 1** by Dr. Mohammad Abu-Hadhoud on the [Programming Advices](https://www.programmingadvices.com) platform — a course covering linked lists, stacks, queues, dynamic arrays, and their real-world applications in C++.

---

## Author

**Yusuf SHAABAN ARJA**
