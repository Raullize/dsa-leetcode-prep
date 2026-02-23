[<- Back to Big O Notation](./README.md)

# Big O: Arrays

Arrays are one of the most fundamental data structures. Understanding the Big O complexity of their built-in operations is crucial for writing efficient code.

## Array Structure

Consider an array with the following elements:

```javascript
const myArray = [11, 3, 23, 7];
// Indexes:       0   1   2   3
```

## O(1): Constant Time Operations

Operations that add or remove elements at the **end** of the array are O(1) because they don't require re-indexing the existing elements.

### Push (Add to end)
```javascript
myArray.push(17); 
// [11, 3, 23, 7, 17]
```
*   **Complexity**: **O(1)**
*   **Reason**: The computer knows exactly where the array ends and just adds the new item. No other items are moved.

### Pop (Remove from end)
```javascript
myArray.pop(); 
// [11, 3, 23, 7]
```
*   **Complexity**: **O(1)**
*   **Reason**: We simply remove the last item. No re-indexing required.

## O(n): Linear Time Operations

Operations that add or remove elements at the **beginning** or **middle** of the array are O(n) because all subsequent elements must be re-indexed (shifted).

### Shift (Remove from beginning)
```javascript
myArray.shift();
// Removes 11.
// 3 moves to index 0
// 23 moves to index 1
// 7 moves to index 2
```
*   **Complexity**: **O(n)**
*   **Reason**: We removed index 0, so every other item has to shift one place to the left to fill the gap.

### Unshift (Add to beginning)
```javascript
myArray.unshift(11);
// Adds 11 to index 0.
// All existing items must shift to the right to make room.
```
*   **Complexity**: **O(n)**
*   **Reason**: We need to insert at index 0, so we have to move index 0 to 1, 1 to 2, etc., for the entire array.

### Splice (Add/Remove at specific index)
```javascript
myArray.splice(1, 0, 'Hi');
// Inserts 'Hi' at index 1.
// [11, 'Hi', 3, 23, 7]
```
*   **Complexity**: **O(n)**
*   **Reason**: Similar to `unshift`, if you insert in the middle, all elements after that point must be shifted to new indexes.

## Summary

| Operation | Method | Complexity |
| :--- | :--- | :--- |
| Add to end | `push` | **O(1)** |
| Remove from end | `pop` | **O(1)** |
| Add to beginning | `unshift` | **O(n)** |
| Remove from beginning | `shift` | **O(n)** |
| Find by Index | `myArray[i]` | **O(1)** |
| Find by Value | `forEach`, `map`, `find` | **O(n)** |

---

[<- Back to Big O Notation](./README.md)
