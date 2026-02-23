[<- Back to Big O Notation](./README.md)

# Different Terms for Input

When an algorithm takes multiple inputs, the Big O complexity depends on *all* of them. You cannot just say `O(n)` if there are two distinct variables.

## Example Code

Consider a function that takes two parameters, `a` and `b`.

```javascript
function logItems(a, b) {
    // Loop through 'a'
    for(let i = 0; i < a; i++) {
        console.log(i)
    }

    // Loop through 'b'
    for(let j = 0; j < b; j++) {
        console.log(j)
    }
}
```

## Analysis

1.  **Independent Inputs**:
    *   The first loop depends on the size of `a`.
    *   The second loop depends on the size of `b`.
    *   We don't know if `a` is bigger, smaller, or equal to `b`.

2.  **Common Mistake**:
    *   It is **NOT** `O(n)`.
    *   It is **NOT** `O(n + n) = O(2n) = O(n)`.

3.  **Correct Complexity**:
    *   Since `a` and `b` are different inputs, the complexity is **O(a + b)**.

## Nested Loops with Different Inputs

If the loops were nested:

```javascript
function logItems(a, b) {
    for(let i = 0; i < a; i++) {
        for(let j = 0; j < b; j++) {
            console.log(i, j)
        }
    }
}
```

*   **Complexity**: **O(a * b)**
*   This is similar to `O(n²)`, but since the inputs can be different sizes, we must represent both.

**Key Takeaway**: Always identify if your variables represent the same input set (`n`) or different input sets (`a`, `b`, `m`, `n`, etc.).

---

[<- Back to Big O Notation](./README.md)
