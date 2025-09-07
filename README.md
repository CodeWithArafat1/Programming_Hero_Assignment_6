<!-- ## 1) Difference between `var`, `let`, and `const`

- **`var`**

  - Function-scoped.
  - Can be redeclared and updated.
  - Hoisted (initialized with `undefined`).

- **`let`**

  - Block-scoped.
  - Can be updated but **cannot be redeclared** in the same scope.
  - Not initialized until its definition is evaluated (Temporal Dead Zone).

- **`const`**

  - Block-scoped.
  - Cannot be updated or redeclared.
  - Must be initialized at the time of declaration.
  - For objects and arrays, the **reference cannot change**, but the content can be modified.

  2. Difference between map(), forEach(), and filter()

-**`forEach()`**

- Executes a function on each array element.
- Does not return a new array (returns undefined).

-**`map()`**

- Executes a function on each array element.
- Returns a new array containing the results.

-**`filter()`**

- Executes a function on each array element.
- Returns a new array containing elements that pass a condition.

## 3) Arrow Functions in ES6

- Arrow functions provide a shorter syntax to write functions and do not have their own this context.
- Syntax:
  // Traditional function
  function sum(a, b) {
  return a + b;
  }

// Arrow function
const sum = (a, b) => a + b;

- Single expression returns automatically.
- No binding of this, arguments, or super.

## 4) Destructuring Assignment in ES6

Destructuring allows extracting values from arrays or objects into separate variables.

Array Destructuring:

const arr = [1, 2, 3];
const [a, b] = arr;
console.log(a, b); // 1 2


5) Template Literals in ES6

Template literals provide an easier way to create strings with interpolation and multi-line support.

Syntax:

const name = 'Alice';
const age = 25;

// Using template literals
const message = `Hello, my name is ${name} and I am ${age} years old.`;
console.log(message);

Differences from string concatenation:

Uses backticks ` instead of quotes.

Supports ${} for embedding expressions. -->

## 1. Difference between `var`, `let`, and `const`

Understanding variable declarations is crucial for managing scope and immutability in JavaScript.

### `var`

- **Scope**: Function-scoped. A variable declared with `var` is accessible throughout the function in which it is declared.
- **Re-declaration & Updating**: Can be redeclared and updated within its scope.
- **Hoisting**: It is hoisted to the top of its scope and initialized with a value of `undefined`.

### `let`

- **Scope**: Block-scoped (`{}`). A variable declared with `let` is only accessible within the block it's defined in.
- **Re-declaration & Updating**: Can be updated but **cannot be redeclared** in the same scope.
- **Hoisting**: It is hoisted but not initialized. Accessing it before declaration results in a `ReferenceError` (this is known as the Temporal Dead Zone).

### `const`

- **Scope**: Block-scoped (`{}`).
- **Re-declaration & Updating**: Cannot be updated or redeclared. It must be initialized at the time of declaration.
- **Immutability**: The variable's reference is immutable. For primitive types, this means the value cannot change. For objects and arrays, the reference to the object/array cannot change, but the properties or elements within can be modified.

---

## 2. Difference between `map()`, `forEach()`, and `filter()`

These are common array iteration methods with distinct use cases.

### `forEach()`

- **Purpose**: Executes a provided function once for each array element.
- **Return Value**: Returns `undefined`. It is used for its side effects (e.g., logging to the console, modifying an external variable).
- **Chaining**: Cannot be chained with other array methods like `map()`, `filter()`, etc.

### `map()`

- **Purpose**: Creates a new array populated with the results of calling a provided function on every element in the calling array.
- **Return Value**: A **new array** of the same length as the original array.
- **Chaining**: Can be chained with other array methods.

### `filter()`

- **Purpose**: Creates a new array with all elements that pass the test implemented by the provided function.
- **Return Value**: A **new array** containing only the elements that returned `true` from the callback function. The length can be less than or equal to the original array's length.
- **Chaining**: Can be chained with other array methods.

---

## 3. Arrow Functions in ES6

Arrow functions offer a more concise syntax for writing function expressions.

- They provide a shorter syntax compared to traditional function expressions.
- They do not have their own `this` context. Instead, they inherit `this` from the parent scope (lexical `this`).
- They also do not have their own `arguments` object or `super` binding.
- If the function body is a single expression, the `return` is implicit.

### Syntax Example

```javascript
// Traditional function
function sum(a, b) {
  return a + b;
}

// Arrow function
const sumArrow1 = (a, b) => {
  return a + b;
};

// Arrow function
const sumArrow2 = (a, b) => a + b;
```

## 4. Destructuring Assignment in ES6

- Destructuring is a convenient way to extract values from arrays or properties from objects into distinct variables.

```
const person = {
  firstName: 'John',
  lastName: 'Doe',
  age: 30
};


const { firstName, age } = person;
console.log(firstName, age);
```

## 5. Template Literals in ES6

- Template literals or template strings provide an enhanced syntax for working with strings, allowing for embedded expressions and multi-line strings.

```
const name = 'Arafat Nill';
const age = 21;

// template literals string
const message = `Hello, my name is ${name} and I am ${age} years old.`;
```
