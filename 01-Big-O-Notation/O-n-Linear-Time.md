[<- Back to Big O Notation](./README.md)

# O(n): Linear Time

**O(n)** represents linear time complexity. This means the time it takes to complete the function is directly proportional to the size of the input (`n`).

## Example Code

This is the example used in the course:

```javascript
function logItems(n) {
    for(let i = 0; i < n; i++) {
        console.log(i)
    }
}

logItems(10)
```

## Analysis

*   **Proportional Growth**: In the example above, the `for` loop runs `n` times.
*   **Direct Relationship**:
    *   If `n = 10`, the loop runs 10 times.
    *   If `n = 1,000,000`, the loop runs 1,000,000 times.
*   **Conclusion**: As the input `n` increases, the number of operations increases linearly. This is the hallmark of **O(n)** complexity.

---

[<- Back to Big O Notation](./README.md)
