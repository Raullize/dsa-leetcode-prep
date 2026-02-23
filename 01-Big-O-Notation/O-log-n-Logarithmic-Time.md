[<- Back to Big O Notation](./README.md)

# O(log n): Logarithmic Time

**O(log n)** represents logarithmic time complexity. This is highly efficient and typically associated with algorithms that use a **Divide and Conquer** strategy.

## The Concept: Divide and Conquer

In **O(log n)** algorithms, the problem size is cut in fraction (usually half) with each step. This means that even if the input size (`n`) grows significantly, the number of operations grows very slowly.

## Example: Binary Search

Imagine searching for a specific number in a **sorted array**. Instead of checking every single element (which would be O(n)), we can split the array in half at each step.

### Scenario
We have a sorted array of 8 items: `[1, 2, 3, 4, 5, 6, 7, 8]`.
Let's find the number **1**.

### Steps

1.  **Step 1**: Start with the full array (8 items).
    *   `[1, 2, 3, 4, 5, 6, 7, 8]`
    *   Split in half. Is 1 in the first half or second half? First half.
    *   Items remaining: 4 (`[1, 2, 3, 4]`)

2.  **Step 2**: Take the remaining 4 items.
    *   `[1, 2, 3, 4]`
    *   Split in half. Is 1 in the first half? Yes.
    *   Items remaining: 2 (`[1, 2]`)

3.  **Step 3**: Take the remaining 2 items.
    *   `[1, 2]`
    *   Split in half. Is 1 in the first half? Yes.
    *   Items remaining: 1 (`[1]`) -> **Found it!**

### Analysis

*   **Input Size (n)**: 8
*   **Operations**: 3 steps ($2^3 = 8$, so $\log_2 8 = 3$)

If we double the input size to **16**, it would only take **4 steps** ($\log_2 16 = 4$).
If we have **1,000,000** items, it only takes roughly **20 steps**!

**Key Takeaway**: O(log n) is extremely efficient for large datasets because it repeatedly discards large portions of the data.

---

[<- Back to Big O Notation](./README.md)
