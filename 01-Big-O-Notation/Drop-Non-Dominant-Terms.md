[<- Back to Big O Notation](./README.md)

# Drop Non-Dominant Terms

When calculating Big O complexity, we focus on the term that grows the fastest as the input size (`n`) increases. Terms that grow slower are considered "non-dominant" and are removed from the final notation.

## Example Code

Consider the following function which has a nested loop followed by a single loop:

```javascript
function logItems(n) {
    // Nested loop: O(n²)
    for(let i = 0; i < n; i++) {
        for(let j = 0; j < n; j++) {
            console.log(i, j) 
        }       
    } 

    // Single loop: O(n)
    for(let k = 0; k < n; k++) {
        console.log(k)
    }
}

logItems(10)
```

## Analysis

1.  **Break Down the Operations**:
    *   The first part (nested loop) runs `n * n = n²` times.
    *   The second part (single loop) runs `n` times.
    *   **Total Operations**: `n² + n`.

2.  **Identify the Dominant Term**:
    *   As `n` becomes very large, `n²` becomes significantly larger than `n`.
    *   Example: If `n = 1000`:
        *   `n² = 1,000,000`
        *   `n = 1,000`
        *   The `n` part is negligible compared to `n²`.

3.  **Simplification**:
    *   We drop the non-dominant term (`n`).
    *   `O(n² + n)` becomes **O(n²)**.

**Rule**: Keep only the term with the highest order of growth.

---

[<- Back to Big O Notation](./README.md)
