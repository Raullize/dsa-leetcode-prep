[<- Back to Classes & Pointers](./README.md)

# Pointers (References)

Understanding how JavaScript handles memory is crucial for data structures. JavaScript doesn't have "pointers" in the traditional C++ sense, but it uses **references** for objects.

## Value vs. Reference

### Primitive Types (Value)

Primitives (numbers, strings, booleans) are passed by **value**. A copy of the value is created.

```javascript
let num1 = 5;
let num2 = num1; // Copies the value 5

num1 = 10;

console.log(num1); // 10
console.log(num2); // 5 (Stays 5, because it was a copy)
```

### Objects (Reference)

Objects (including arrays) are passed by **reference**. The variable doesn't hold the object itself, but a *pointer* (reference) to the place in memory where the object is stored.

```javascript
let obj1 = { value: 11 };
let obj2 = obj1; // Copies the REFERENCE (pointer), not the object

obj1.value = 22;

console.log(obj1.value); // 22
console.log(obj2.value); // 22 (Changed too!)
```

**Why?** Because both `obj1` and `obj2` point to the **same address** in memory. Changing the object through one reference affects all variables pointing to it.

## Moving Pointers

We can change what a variable points to.

```javascript
let obj3 = { value: 22 };

obj2 = obj3; // obj2 now points to the new object { value: 22 }
             // obj1 still points to the old object { value: 11 } (if we hadn't changed it above)
```

## Garbage Collection

What happens if no variable points to an object anymore?

```javascript
let obj1 = { value: 11 };
let obj2 = obj1;

// obj1 and obj2 point to { value: 11 }

obj1 = { value: 22 }; // obj1 points to a new object
obj2 = obj1;          // obj2 now ALSO points to the new object { value: 22 }

// What happened to { value: 11 }?
// No variable points to it anymore. It is "unreachable".
```

### Garbage Collection Process
JavaScript has an automatic **Garbage Collector**. It constantly monitors objects in memory.
*   If an object has **zero** variables pointing to it (like the `{ value: 11 }` above), it is considered "garbage".
*   The Garbage Collector will automatically free up that memory so it can be used again.

This is fundamental in Linked Lists: if you remove a node by changing the pointer of the previous node, the removed node is automatically cleaned up by the Garbage Collector.

---

[<- Back to Classes & Pointers](./README.md)
