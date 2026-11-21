# Contact Management System Using Binary Search Tree (BST)

**Subject:** Data Structures  
**Subject Code:** CS25C08  
**Department:** Computer Science & Engineering (Artificial Intelligence & Machine Learning) - CSE(AIML)  
**Prepared By:** SELVA KUMAR. R  

---

## 📌 Project Overview
The **Contact Management System Using Binary Search Tree** is a web-based mini-project developed for the **Data Structures (CS25C08)** laboratory/curriculum. It demonstrates practical implementation of a **Binary Search Tree (BST)** data structure to store, search, organize, update, and delete contact details in real-time.

All operations strictly follow fundamental binary search tree algorithms, using the **Contact Name** as the unique key. The system maintains an alphabetical directory using **Inorder Traversal (Left → Root → Right)** and provides a live visual tree diagram.

---

## 🚀 Key Features

1. **Add New Contact (`insert`)**:
   - Stores Contact Name, Phone Number, and Email Address.
   - Prevents duplicate contact names (unique key validation).
   - Inserts nodes based on lexicographical (alphabetical) comparison.

2. **Search Contact (`search`)**:
   - Locates any contact in average $O(\log n)$ time complexity.
   - Traces and displays the exact BST traversal path (e.g., `Root → Branch Left → Branch Right → Found`).
   - Counts and displays the exact number of comparisons made.

3. **Display All Contacts (`inorderTraversal`)**:
   - Performs recursive Inorder Traversal ($L \to Root \to R$) to render all contacts in ascending alphabetical order ($A \to Z$).

4. **Update Contact (`update`)**:
   - Enables editing phone number, email address, or contact name.
   - If the name is changed, the system properly deletes the old node and re-inserts the updated node into the correct BST position to preserve the BST invariant.

5. **Delete Contact (`delete`)**:
   - Implements standard 3-case BST deletion:
     - **Case 1 (Leaf Node):** Node with zero children is removed.
     - **Case 2 (Single Child):** Node is replaced by its existing child.
     - **Case 3 (Two Children):** Node is replaced by its **Inorder Successor** (the smallest node in its right subtree).

6. **Clear All Contacts (`clear`)**:
   - Removes all stored contacts from the tree and Local Storage after user confirmation.

7. **Display Total Contacts (`countNodes`)**:
   - Dynamically computes and displays the total number of contacts and the height (depth) of the tree.

8. **Live Interactive Tree Visualizer**:
   - Draws a dynamic SVG tree diagram showing root, parent, and child relationships.
   - Clicking on a node or searching a contact highlights the node in the diagram.

9. **Data Persistence (Local Storage)**:
   - Uses **Preorder Traversal Serialization** to save tree nodes to browser Local Storage, ensuring that upon page reload the exact tree hierarchy is preserved.

---

## 🛠️ Technology Stack
- **HTML5:** Semantic structure, modal popups, responsive containers.
- **CSS3:** Modern UI with blue, white, and light-grey theme, glassmorphism ribbons, responsive grid, animations.
- **JavaScript (ES6+):** Pure object-oriented implementation of `BSTNode` and `BinarySearchTree` classes, DOM manipulation, SVG rendering.

---

## 💻 How to Run the Project

1. **Direct Execution:**
   - Double-click on `index.html` or right-click and choose **"Open with Google Chrome"** (or Microsoft Edge / Firefox / Safari).
   - **No web server, Node.js, or external library installation is required!**
   - The project works 100% offline.

---

## 📚 Data Structure Viva Preparation Guide

### 1. What is a Binary Search Tree (BST)?
A Binary Search Tree is a hierarchical node-based binary tree data structure where:
- The left subtree of a node contains only nodes with keys **less than** the node’s key.
- The right subtree of a node contains only nodes with keys **greater than** the node’s key.
- Both the left and right subtrees must also be binary search trees.

### 2. Why use Inorder Traversal for displaying contacts?
In a BST, an **Inorder Traversal** processes nodes in the order **Left Subtree $\to$ Root $\to$ Right Subtree**. By definition of a BST, this yields all keys in strictly ascending sorted (alphabetical) order without needing an extra sorting algorithm ($O(n)$ time).

### 3. How does BST Deletion handle a node with two children?
When deleting a node with two children:
1. Find its **Inorder Successor** (the node with the minimum key in the right subtree).
2. Copy the successor's data (name, phone, email) to the current node.
3. Recursively delete the inorder successor from the right subtree (which is guaranteed to have at most one child).

### 4. What are the Time and Space Complexities?

| Operation | Average Case | Worst Case (Skewed Tree) | Space Complexity |
| :--- | :--- | :--- | :--- |
| **Search** | $O(\log n)$ | $O(n)$ | $O(h)$ auxiliary stack |
| **Insertion** | $O(\log n)$ | $O(n)$ | $O(h)$ auxiliary stack |
| **Deletion** | $O(\log n)$ | $O(n)$ | $O(h)$ auxiliary stack |
| **Inorder Traversal** | $O(n)$ | $O(n)$ | $O(h)$ auxiliary stack |

*(where $n$ is the total number of contacts, and $h$ is the height of the tree)*.

---

## 🎓 Academic Submission Details
- **Project Title:** Contact Management System Using Binary Search Tree
- **Subject:** Data Structures
- **Subject Code:** CS25C08
- **Prepared By:** SELVA KUMAR. R
- **Department:** CSE(AIML)
