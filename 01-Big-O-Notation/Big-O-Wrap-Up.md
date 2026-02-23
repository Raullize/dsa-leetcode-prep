[<- Back to Big O Notation](./README.md)

# Big O: Wrap Up

Here is a quick summary of the Big O concepts we've covered, helping you identify them in your code.

## Quick Summary

| Complexity | Name | Key Identifier | Example |
| :--- | :--- | :--- | :--- |
| **O(1)** | Constant | **Constant** operations. No loops. | Accessing array index, basic math. |
| **O(log n)** | Logarithmic | **Divide and Conquer**. Input is split in half. | Binary Search. |
| **O(n)** | Linear | **Proportional**. Single loop over input. | For loop, `forEach`. |
| **O(n²)** | Quadratic | **Loop within a loop**. Nested iterations. | Bubble Sort, nested `for` loops. |

## Detailed Breakdown

### O(n²): Loop within a Loop
*   **Identification**: Look for nested loops where both loops iterate over the same data set.
*   **Growth**: Very fast. Not scalable for large inputs.

### O(n): Proportional
*   **Identification**: A single loop or a series of separate loops.
*   **Growth**: Smooth and linear. If input doubles, time doubles.

### O(log n): Divide and Conquer
*   **Identification**: The data set is repeatedly cut in half.
*   **Growth**: Very slow (efficient). Excellent for massive data sets.

### O(1): Constant
*   **Identification**: Direct access or simple operations that don't depend on input size.
*   **Growth**: None (Flat line). The most efficient.

## Resources

*   [**Big O Cheat Sheet**](https://www.bigocheatsheet.com/) - A comprehensive chart of complexities for common algorithms and data structures.

---

[<- Back to Big O Notation](./README.md)
