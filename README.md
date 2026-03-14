# 🌳 Print Nodes at Kth Level of a Binary Tree (Java)

## 📌 Overview

This project demonstrates how to **print all nodes at a given level (Kth level)** in a **Binary Tree** using **recursion in Java**.

The program traverses the tree and prints all nodes that exist at the specified **level `k`**.

This is a common **Binary Tree traversal problem** used to understand **recursive tree traversal and level-based operations**.

---

# 🌿 Example Binary Tree

```id="tree_example"
        1
       / \
      2   3
     / \ / \
    4  5 6  7
```

---

# 🎯 Problem Statement

Given:

* `root` → Root node of the binary tree
* `k` → Target level

Print all nodes present at **level `k`**.

Example:

```id="example_input"
k = 3
```

Nodes at level 3:

```id="example_output"
4 5 6 7
```

---

# ⚙️ Algorithm

The algorithm uses **recursive traversal**.

### Steps

1️⃣ Start from the root node with **level = 1**
2️⃣ If the current level equals **k**, print the node value
3️⃣ Otherwise recursively call the function for:

* left subtree
* right subtree
  4️⃣ Increase the level by **1** during recursion

---

# 💻 Java Implementation

```java id="code_klevel"
public static void kLevel(Node root, int level, int k){

    if(root == null){
        return;
    }

    if(level == k){
        System.out.print(root.data + " ");
        return;
    }

    kLevel(root.left, level + 1, k);
    kLevel(root.right, level + 1, k);
}
```

---

# ▶️ Program Output

```id="output_k"
4 5 6 7
```

These are the nodes present at **level 3** of the binary tree.

---

# ⏱ Time and Space Complexity

| Complexity       | Value |
| ---------------- | ----- |
| Time Complexity  | O(n)  |
| Space Complexity | O(h)  |

Where:

* **n** = number of nodes
* **h** = height of the tree (recursion stack)

---

# 🧠 Concepts Used

* 🌳 Binary Trees
* 🔁 Recursion
* 📊 Tree Traversal
* 📍 Level-based Node Access

---

# 🎯 Learning Outcomes

After completing this program you will understand:

✔ How to traverse a binary tree recursively
✔ How to print nodes at a specific level
✔ How recursion helps solve tree problems
✔ Level-based tree operations

These concepts are important for **Data Structures and Algorithms (DSA)** and **technical interviews**.

---

# 👨‍💻 Author

Developed as part of **Data Structures and Algorithms practice** 🚀
