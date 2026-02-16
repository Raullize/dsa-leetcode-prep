<- [Back to README.md](../README.md)

# Big O Notation

## Introduction

**Big O notation** is a mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity. In computer science, it is used to classify algorithms according to how their run time or space requirements grow as the input size grows.

### Time Complexity
Time complexity quantifies the amount of time taken by an algorithm to run as a function of the length of the string representing the input. It's not about the actual seconds, but the number of operations relative to the input size.

### Space Complexity
Space complexity is a measure of the amount of working storage an algorithm needs. That means how much memory, in the worst case, is needed at any point in the algorithm.

## Big O Basic Concepts

### O(1): Constant Time
*   **Description**: Doesn't depend on the size of the data set. The operation takes the same amount of time regardless of input size.
*   **Example**: Accessing an array element by its index.

### O(log n): Logarithmic Time
*   **Description**: Splits the data in each step (divide and conquer). The number of operations grows very slowly as input size increases.
*   **Example**: Binary search.

### O(n): Linear Time
*   **Description**: Directly proportional to the data set size. If you double the input, the time doubles.
*   **Example**: Looping through an array.

### O(n log n): Linearithmic Time
*   **Description**: A combination of linear and logarithmic time. Often seen in efficient sorting algorithms.
*   **Example**: Merge sort, quick sort.

### O(n²): Polynomial Time (Quadratic)
*   **Description**: Performance is directly proportional to the square of the size of the input data set. Often involves nested iterations.
*   **Example**: Bubble sort (nested loops).

## Complexity Bounds

### Omega (Ω) - Lower Bound
*   **What it means**: Omega (Ω) describes the best-case scenario for an algorithm.
*   **In simple terms**: It tells you the fastest an algorithm can run in the best circumstances.

### Theta (Θ) - Tight Bound
*   **In simple terms**: It tells you what to generally expect in terms of time complexity. It bounds a function from above and below.

### Big O (O) - Upper Bound (Worst Case)
*   **What it means**: Big O (O) describes the worst-case scenario for an algorithm.
*   **In simple terms**: It tells you the slowest an algorithm can run in the worst circumstances. This is the most commonly used metric because it guarantees that the algorithm will perform no worse than this.

## Useful Tips

### Best Case, Average Case, Worst Case
*   Consider all scenarios when analyzing an algorithm, but focus on the worst case (Big O) for reliability.

### Drop Non-Dominant Terms
*   When calculating complexity, focus on the term that grows the fastest.
*   *Example*: In `O(n² + n)`, `n²` grows much faster than `n` for large inputs, so we simplify it to `O(n²)`.

### Drop Constants
*   Big O notation ignores constants because we are interested in the growth rate.
*   *Example*: `O(2n)` simplifies to `O(n)`. `O(500)` simplifies to `O(1)`.

<- [Back to README.md](../README.md)