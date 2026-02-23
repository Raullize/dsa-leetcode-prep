[<- Back to Big O Notation](./README.md)

# O(n²): Quadratic Time

**O(n²)** (Quadratic Time) occurs when the performance is directly proportional to the square of the size of the input data set. This is common with algorithms that involve **nested iterations** over the data set.

## Example 1: Two Nested Loops (O(n²))

When you have a loop inside another loop, and both run `n` times, the total number of operations is `n * n = n²`.

```javascript
function logItems(n) {
    for(let i = 0; i < n; i++) {
        for(let j = 0; j < n; j++) {
            console.log(i, j) 
        }       
    } 
}

logItems(10)
```

### Analysis
*   **Outer Loop**: Runs `n` times.
*   **Inner Loop**: Runs `n` times for *each* iteration of the outer loop.
*   **Total Operations**: `n * n = n²`.
*   If `n = 10`, it runs `10 * 10 = 100` times.

---

## Example 2: Three Nested Loops (O(n³))

If we add another nested loop, the complexity increases to **O(n³)** (Cubic Time). While technically O(n³), it follows the same principle of polynomial growth where the exponent equals the depth of nested loops.

```javascript
function logItems(n) {
    for(let i = 0; i < n; i++) {
        for(let j = 0; j < n; j++) {
            for(let k = 0; k < n; k++) {
                console.log(i, j, k) 
            }       
        }       
    } 
}

logItems(10)
```

### Analysis
*   **Total Operations**: `n * n * n = n³`.
*   If `n = 10`, it runs `10 * 10 * 10 = 1,000` times.
*   **Key Takeaway**: Each level of nesting multiplies the time complexity by `n`.

## Visualization

| n (Input) | O(n) | O(n²) | O(n³) |
| :--- | :--- | :--- | :--- |
| 10 | 10 | 100 | 1,000 |
| 100 | 100 | 10,000 | 1,000,000 |
| 1,000 | 1,000 | 1,000,000 | 1,000,000,000 |

As you can see, **O(n²)** and **O(n³)** grow much faster than **O(n)**. Algorithms with this complexity are generally considered inefficient for large datasets.

---

[<- Back to Big O Notation](./README.md)
