# JavaScript Keywords

## What is a Keyword?

A **keyword** is a reserved word that has a special, predefined meaning in the JavaScript language. These words are part of the syntax and cannot be used as identifiers (variable names, function names, class names, etc.).

**Example:**
```js
// ❌ Invalid — 'let' is a keyword
let let = 5; // SyntaxError

// ✅ Valid
let count = 5;
```

---

## Categories of JavaScript Keywords

---

### 1. Variable Declaration
Used to declare variables and constants.

| Keyword | Description |
|---------|-------------|
| `var`   | Function-scoped variable declaration (older style) |
| `let`   | Block-scoped variable declaration (ES6+) |
| `const` | Block-scoped constant declaration (ES6+) |

```js
var name = "Alice";
let age = 25;
const PI = 3.14;
```

---

### 2. Control Flow — Conditionals
Used to make decisions in code.

| Keyword | Description |
|---------|-------------|
| `if`      | Executes a block if condition is true |
| `else`    | Executes a block if `if` condition is false |
| `switch`  | Selects one of many code blocks to execute |
| `case`    | Defines a branch in `switch` |
| `default` | Fallback branch in `switch` |
| `break`   | Exits a loop or `switch` block |

```js
if (age > 18) {
  console.log("Adult");
} else {
  console.log("Minor");
}

switch (day) {
  case "Mon":
    console.log("Monday");
    break;
  default:
    console.log("Other day");
}
```

---

### 3. Control Flow — Loops
Used to repeat a block of code.

| Keyword    | Description |
|------------|-------------|
| `for`      | Loop with initialization, condition, and increment |
| `while`    | Loop that runs while a condition is true |
| `do`       | Executes block once, then checks condition |
| `continue` | Skips current iteration and goes to next |
| `break`    | Exits the loop |
| `in`       | Iterates over object keys (`for...in`) |
| `of`       | Iterates over iterable values (`for...of`) |

```js
for (let i = 0; i < 3; i++) { console.log(i); }

while (x > 0) { x--; }

do { x--; } while (x > 0);

for (let key in obj) { }
for (let val of arr) { }
```

---

### 4. Functions
Used to define and work with functions.

| Keyword    | Description |
|------------|-------------|
| `function` | Declares a function |
| `return`   | Returns a value from a function |
| `async`    | Declares an asynchronous function (ES2017+) |
| `await`    | Pauses async function until Promise resolves (ES2017+) |
| `yield`    | Pauses and resumes a generator function (ES6+) |

```js
function greet() {
  return "Hello";
}

async function fetchData() {
  const data = await fetch(url);
}

function* gen() {
  yield 1;
  yield 2;
}
```

---

### 5. Classes and Object-Oriented Programming
Used for class-based OOP (ES6+).

| Keyword      | Description |
|--------------|-------------|
| `class`      | Declares a class |
| `extends`    | Creates a subclass (inheritance) |
| `super`      | Calls the parent class constructor or methods |
| `new`        | Creates an instance of a class or constructor function |
| `this`       | Refers to the current object/context |
| `static`     | Defines a static method or property on the class |
| `get`        | Defines a getter method |
| `set`        | Defines a setter method |

```js
class Animal {
  constructor(name) {
    this.name = name;
  }
  static describe() { return "I am an animal"; }
}

class Dog extends Animal {
  constructor(name) {
    super(name);
  }
}

const d = new Dog("Rex");
```

---

### 6. Error Handling
Used to handle runtime errors gracefully.

| Keyword   | Description |
|-----------|-------------|
| `try`     | Wraps code that might throw an error |
| `catch`   | Handles the error thrown in `try` block |
| `finally` | Always executes after `try/catch`, regardless of result |
| `throw`   | Manually throws an error/exception |

```js
try {
  throw new Error("Something went wrong");
} catch (err) {
  console.error(err.message);
} finally {
  console.log("Always runs");
}
```

---

### 7. Modules (ES6+)
Used for importing and exporting code between files.

| Keyword   | Description |
|-----------|-------------|
| `import`  | Imports bindings from another module |
| `export`  | Exports bindings from the current module |
| `from`    | Specifies the source module path in `import` |
| `as`      | Creates an alias during import/export |
| `default` | Defines or imports the default export |

```js
import { greet } from './utils.js';
import * as utils from './utils.js';
export const PI = 3.14;
export default function() { }
```

---

### 8. Logical / Value Keywords
Special literal values and logical operators.

| Keyword     | Description |
|-------------|-------------|
| `true`      | Boolean true literal |
| `false`     | Boolean false literal |
| `null`      | Represents intentional absence of value |
| `undefined` | A variable declared but not assigned a value |
| `NaN`       | Not a Number (technically a global property, not keyword) |
| `Infinity`  | Represents infinite numeric value |

```js
let isActive = true;
let data = null;
let x; // x is undefined
```

---

### 9. Type Checking
Used to check or convert types.

| Keyword      | Description |
|--------------|-------------|
| `typeof`     | Returns the type of a value as a string |
| `instanceof` | Checks if an object is an instance of a class |
| `in`         | Checks if a property exists in an object |
| `void`       | Evaluates an expression and returns `undefined` |

```js
typeof "hello";          // "string"
[] instanceof Array;     // true
"name" in person;        // true
void 0;                  // undefined
```

---

### 10. Strict Mode & Miscellaneous

| Keyword      | Description |
|--------------|-------------|
| `debugger`   | Pauses execution for debugging in DevTools |
| `delete`     | Deletes a property from an object |
| `with`       | Extends the scope chain (deprecated, avoid using) |
| `label`      | Labels a statement for use with `break`/`continue` |

```js
debugger; // pauses here in browser DevTools

const obj = { a: 1 };
delete obj.a; // removes property 'a'
```

---

### 11. Future Reserved Keywords
These are reserved for future use and **cannot** be used as identifiers.

| Keyword      |
|--------------|
| `enum`       |
| `implements` |
| `interface`  |
| `package`    |
| `private`    |
| `protected`  |
| `public`     |
| `abstract`   |
| `arguments`  |
| `eval`       |

> In **strict mode**, many of these are strictly prohibited as identifiers.

---

## Complete Quick Reference — All JavaScript Keywords

```
async       await       break       case        catch
class       const       continue    debugger    default
delete      do          else        enum        export
extends     false       finally     for         from
function    get         if          implements  import
in          instanceof  interface   let         new
null        of          package     private     protected
public      return      set         static      super
switch      this        throw       true        try
typeof      undefined   var         void        while
with        yield
```

---

## Key Interview Points

- **`var` vs `let` vs `const`**: `var` is function-scoped and hoisted; `let`/`const` are block-scoped. `const` cannot be reassigned.
- **`typeof null`** returns `"object"` — this is a known JavaScript bug/quirk.
- **`undefined` vs `null`**: `undefined` means a variable exists but has no value; `null` is an intentional empty value.
- **`this` keyword** changes based on execution context (regular function vs arrow function vs class).
- **`async/await`** is syntactic sugar over Promises — makes async code look synchronous.
- **`yield`** is used only inside generator functions (`function*`).
- **`in` keyword** serves dual purposes: `for...in` loop AND property existence check.
