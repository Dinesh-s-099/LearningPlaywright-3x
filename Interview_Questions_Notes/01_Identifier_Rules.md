# JavaScript Identifier Rules

## What is an Identifier?

An **identifier** is a name given to a variable, function, class, parameter, or any user-defined item in JavaScript.

```js
let userName = "Alice";   // 'userName' is an identifier
function greet() {}       // 'greet' is an identifier
```

---

## Rules for Naming Identifiers

| # | Rule                                                             | Valid Example        | Invalid Example       |
|---|------------------------------------------------------------------|----------------------|-----------------------|
| 1 | Must start with a **letter**, **underscore `_`**, or **dollar sign `$`** | `name`, `_count`, `$value` | `1name`, `@value`  |
| 2 | Can contain **letters, digits, underscores, dollar signs**       | `user1`, `_id`, `$x` | `user-name`, `user name` |
| 3 | **Cannot start with a digit**                                    | `value1`             | `1value`              |
| 4 | **Cannot use reserved keywords**                                 | `myLet`, `myClass`   | `let`, `class`, `for` |
| 5 | **Case-sensitive** — uppercase and lowercase are different       | `Name` ≠ `name`      | —                     |
| 6 | **No spaces allowed**                                            | `firstName`          | `first name`          |
| 7 | **No special characters** except `_` and `$`                    | `_temp`, `$el`       | `user@name`, `val#1`  |
| 8 | **No limit on length**, but keep it meaningful                   | `totalUserCount`     | —                     |

---

## Valid Identifier Examples

```js
let name = "John";
let _privateVar = 42;
let $dollar = true;
let camelCaseName = "ok";
let value1 = 100;
let __proto__Custom = {};
```

---

## Invalid Identifier Examples

```js
let 1name = "bad";       // ❌ Starts with a digit
let user-name = "bad";   // ❌ Hyphen not allowed
let for = 10;            // ❌ Reserved keyword
let my name = "bad";     // ❌ Space not allowed
let @email = "bad";      // ❌ Special character not allowed
```

---

## Naming Conventions (Best Practices)

| Convention      | Usage                              | Example                    |
|-----------------|------------------------------------|----------------------------|
| `camelCase`     | Variables and functions            | `getUserName`, `totalCount`|
| `PascalCase`    | Classes and constructors           | `UserProfile`, `CarModel`  |
| `UPPER_SNAKE`   | Constants                          | `MAX_SIZE`, `API_URL`      |
| `_underscore`   | Private or internal variables      | `_id`, `_helper`           |
| `$dollar`       | DOM elements or library variables  | `$btn`, `$input`           |

---

## Reserved Keywords (Cannot be used as Identifiers)

| Category         | Keywords                                                                 |
|------------------|--------------------------------------------------------------------------|
| Variable / Scope | `var`, `let`, `const`                                                   |
| Control Flow     | `if`, `else`, `switch`, `case`, `break`, `continue`, `default`          |
| Loops            | `for`, `while`, `do`                                                    |
| Functions        | `function`, `return`, `yield`                                           |
| Classes / OOP    | `class`, `extends`, `super`, `new`, `this`                              |
| Modules          | `import`, `export`, `from`, `as`                                        |
| Error Handling   | `try`, `catch`, `finally`, `throw`                                      |
| Types / Values   | `typeof`, `instanceof`, `void`, `null`, `undefined`, `true`, `false`   |
| Async            | `async`, `await`                                                        |
| Others           | `delete`, `in`, `of`, `with`, `debugger`                               |

---

## Quick Summary

- Start with: **letter**, **`_`**, or **`$`**
- Followed by: **letters**, **digits**, **`_`**, or **`$`**
- No **spaces**, no **special chars** (except `_` and `$`)
- No **reserved keywords**
- **Case-sensitive**: `myVar` ≠ `MyVar`
