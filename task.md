# 📦 Data Structures Overview

When we write programs, we often need to store and manage data in an organized way.  
A **data structure** is simply a method of arranging data so that operations on it (like searching, inserting, or deleting) become efficient.  

Think of it like choosing the right container:
- A **drawer** for clothes → array (fixed size, neat layout).
- A **chain of linked keys** → linked list (dynamic, each piece linked to the next).

---


## 📚 Arrays

- Stored in **contiguous memory blocks**.
- Direct access to elements by index → **O(1)** time.
- Downsides:
  - Fixed size.
  - Insert/delete in middle requires shifting → **O(n)**.

>Example (array of integers):


👉 **Code Example: Traversing an Array (C++)**
```cpp
int arr[5] = {10, 20, 30, 40,50};
for (int i = 0; i < 4; i++) {
    cout << arr[i] << " ";  // prints: 10 20 30 40
}


```
---
## 🔗 Linked Lists

- Made of **nodes** (data + pointer to next).

- Not stored in contiguous memory → traversal is O(n).

- Advantage: easy to insert/delete in O(1) (if node reference known).

>Example (singly linked list):


[10 | next] -> [20 | next] -> [30 | next]

```cpp

struct Node {
    int data;
    Node* next;
};

void insertAtHead(Node*& head, int val) {
    Node* newNode = new Node();
    newNode->data = val;
    newNode->next = head;
    head = newNode;
}
```
---
**⚖️ Arrays vs Linked Lists**
| *Feature*     | *Array*     | *Linked List*         |
| ----------- | ---------- | ------------------- |
| Memory      | Contiguous | Scattered           |
| Access      | O(1)       | O(n)                |
| Insertion   | O(n)       | O(1) (with pointer) |
| Deletion    | O(n)       | O(1) (with pointer) |
| Flexibility | Fixed size | Dynamic size        |


⏱️ Time and Space **Complexity**
- When analyzing algorithms, we use asymptotic notations:

- O (Big-O): Worst-case upper bound 🚨

- Ω (Omega): Best-case lower bound ✅

- Θ (Theta): Tight bound ↔️ (both best and worst same order)

Examples:

>Linear Search → O(n), Ω(1)

>Binary Search → Θ(log n)
---
**📝 Summary**
- *Arrays* = simple, fast access, but rigid size.

- *Linked Lists* = flexible, but slower access + pointer overhead.

- *Complexity analysis* (O, Ω, Θ) helps compare algorithms.

- Picking the right DS depends on the problem,   not just theory.

---

**🎯 Exercises (for practice)**
- >If you need instant access to the 50th element, which DS is better: array or linked list? Why?

- >Write complexities for inserting an element at the start of:

     >(a) An array

     >(b) A linked list

- >Match the notation with its meaning:

    > O, Ω, Θ

   >Worst-case, best-case, tight bound