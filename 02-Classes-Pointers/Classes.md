[<- Back to Classes & Pointers](./README.md)

# Classes in JavaScript

Classes in JavaScript are a template for creating objects. They encapsulate data with code to work on that data.

## The "Cookie Cutter" Analogy

Think of a **Class** as a **Cookie Cutter**.
*   The cookie cutter isn't the cookie itself; it's the *template* used to make cookies.
*   The **Instances** (Objects) are the **Cookies** made from that cutter.
*   All cookies made from the same cutter have the same basic shape and structure, but they can have different "flavors" (properties like color, value, etc.).

### Example: Cookie Class

```javascript
class Cookie {
    constructor(color) {
        this.color = color;
    }

    getColor() {
        return this.color;
    }

    setColor(color) {
        this.color = color;
    }
}

// Creating new instances (Cookies)
let cookieOne = new Cookie('green');
let cookieTwo = new Cookie('blue');

cookieOne.getColor(); // Output: green
cookieTwo.getColor(); // Output: blue

cookieOne.setColor('yellow');
cookieOne.getColor(); // Output: yellow
```

In this example:
1.  `Cookie` is the **Class** (the cutter).
2.  `cookieOne` and `cookieTwo` are **Instances** (the actual cookies).
3.  `constructor` is a special method for creating and initializing an object created with a class.

## Classes in Data Structures

Classes are essential when building data structures like Linked Lists, Trees, or Graphs. They allow us to define the structure and the behaviors (methods) of that structure in one place.

### Example: LinkedList Class Structure

Here is how we might structure a `LinkedList` class. We define the methods (like `push`, `pop`, `shift`) that will manipulate the list, but the implementation logic resides inside these methods.

```javascript
class LinkedList {
    // The constructor initializes the new list
    constructor(value) {
        // ... creates the first node
    }

    // Adds a new node to the end
    push(value) {
        // ...
    }

    // Adds a new node to the beginning
    unshift(value) {
        // ...
    }

    // Inserts a node at a specific index
    insert(index, value) {
        // ...
    }

    // Removes a node from a specific index
    remove(index) {
        // ...
    }

    // Removes the last node
    pop() {
        // ...
    }

    // Removes the first node
    shift() {
        // ...
    }
}

// Usage
// const myLinkedList = new LinkedList(10);
// myLinkedList.push(5);
```

By defining these methods within the class, any instance of `LinkedList` we create will automatically have the ability to perform these operations.

---

[<- Back to Classes & Pointers](./README.md)
