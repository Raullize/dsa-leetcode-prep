[<- Back to Big O Notation](./README.md)

# Drop Constants

When calculating Big O complexity, we are interested in how the number of operations grows as the input size (`n`) increases. Constant factors do not change the growth rate, so we simplify the notation by "dropping the constants".

## Example Code

Consider the following function with two separate loops:

```javascript
function logItems(n) {
    // First loop: O(n)
    for(let i = 0; i < n; i++) {
        console.log(i) 
    }

    // Second loop: O(n)
    for(let j = 0; j < n; j++) {
        console.log(j) 
    }       
}

logItems(3)
```

## Analysis

1.  **Count the Operations**:
    *   The first loop runs `n` times.
    *   The second loop also runs `n` times.
    *   Total operations ≈ `n + n = 2n`.

2.  **Initial Complexity**:
    *   Mathematically, this is **O(2n)**.

3.  **Dropping the Constant**:
    *   Big O notation looks at the long-term growth rate.
    *   Whether it's `1n`, `2n`, or `100n`, the growth is still **linear**.
    *   Therefore, we drop the constant `2` and simplify it to **O(n)**.

**Rule**: Always remove fixed numbers (constants) from the final Big O expression.

---

[<- Back to Big O Notation](./README.md)
