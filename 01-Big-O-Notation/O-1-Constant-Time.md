[<- Back to Big O Notation](./README.md)

# O(1): Constant Time

**O(1)** (Constant Time) is the most efficient Big O complexity. It means that the number of operations stays the same, regardless of the size of the input (`n`).

## Example Code

A common example is accessing a specific element in an array by its index, or performing a simple mathematical operation.

```javascript
function addItems(n) {
    return n + n
}

// Or accessing an array
// console.log(items[0])
```

## Analysis

*   **Independence from Input**: In the `addItems` function, whether `n` is 1 or 1,000,000, the computer performs exactly **one** addition operation.
*   **Constant Operations**: The number of steps does not grow. It remains constant.
*   **Graph**: On a graph of Time vs. Input Size, O(1) is a flat horizontal line.

**Key Takeaway**: It is the "gold standard" for efficiency. You cannot get faster than constant time.

---

[<- Back to Big O Notation](./README.md)
