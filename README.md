# README

## Description

This program implements a Binary Search Tree (BST) and finds the k-th smallest element in the BST using an iterative in-order traversal with a stack. The program allows the user to input the number of nodes in the BST, the node values, and the value of k to determine the k-th smallest element.

## Limitations

- The program assumes unique node values in the BST.
- The value of `k` must be within the valid range (1 to n).
- Input values must be integers.

## Time and Space Complexity

- **Time Complexity:** O(H + k), where H is the height of the BST. In the worst case (unbalanced BST), H = O(n), making the complexity O(n). For a balanced BST, H = O(log n), so the complexity becomes O(log n + k).
- **Space Complexity:** O(H), where H is the height of the BST, required for the stack used in iterative traversal. In the worst case, it is O(n) for an unbalanced BST and O(log n) for a balanced BST.

## Why Iterative and Not Recursive?

- **Iterative Approach:** Uses an explicit stack, avoiding function call overhead and potential stack overflow for large BSTs.
- **Recursive Approach:** Although simpler to implement, recursion requires additional memory for function call stacks, leading to potential stack overflow in deep trees. The iterative approach is more memory efficient and avoids unnecessary recursive calls.

## Compilation and Execution

### Compilation:

To compile the program, use the following command:

```sh
g++ -o bin/kth_smallest src/kth_smallest.cpp
```

