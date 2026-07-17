# 🚀 The Complete JavaScript Guide — Beginner to Advanced

> A deep, chapter-wise reference for mastering **Core JavaScript** concepts. Every concept ships with a concise definition, interview Q&A, and code. Based on the Namaste JavaScript series by Akshay Saini.

![JavaScript](https://img.shields.io/badge/JavaScript-ES6%2B-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Interview](https://img.shields.io/badge/Interview-Ready-4CAF50?style=for-the-badge)
![Chapters](https://img.shields.io/badge/Chapters-27-FF6B6B?style=for-the-badge)

---

## 📑 Table of Contents

<a id="part-1"></a>
### Part I — JavaScript Engine & Execution

| #   | Chapter                                                                                  | Key Concepts                                                                                     |
| --- | ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| 1   | [Execution Context](#chapter-1--execution-context)                                       | Execution Context, Memory Component (Variable Environment), Code Component (Thread of Execution), Two Phases (Memory Creation & Code Execution), GEC |
| 2   | [Execution & Call Stack](#chapter-2--execution--call-stack)                               | Call Stack, LIFO, Push/Pop of ECs, Stack Overflow, `Maximum call stack size exceeded`             |
| 3   | [Hoisting](#chapter-3--hoisting)                                                         | Variable hoisting (`var` → `undefined`), Function hoisting (full body), Function Expressions not hoisted, `let`/`const` TDZ preview |
| 4   | [Functions & Variable Environments](#chapter-4--functions--variable-environments)         | Each call → new EC, isolated Variable Environments, return value lifecycle, EC destruction        |

<a id="part-2"></a>
### Part II — Global Environment & Variables

| #   | Chapter                                                                                                     | Key Concepts                                                                                           |
| --- | ----------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| 5   | [Shortest JS Program, `window` & `this`](#chapter-5--shortest-js-program-window--this)                      | Empty file setup, `window` global object, `this === window`, `var` attaches to `window`, `let`/`const` don't, `globalThis` |
| 6   | [`undefined` vs Not Defined](#chapter-6--undefined-vs-not-defined)                                          | `undefined` (memory allocated, no value yet) vs `ReferenceError` (never declared), `typeof` checks     |

<a id="part-3"></a>
### Part III — Scope & Closures

| #   | Chapter                                                                                          | Key Concepts                                                                                          |
| --- | ------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------- |
| 7   | [Scope & Lexical Environment](#chapter-7--scope--lexical-environment)                            | Scope, Lexical Environment, Scope Chain, how JS resolves variables outward                            |
| 8   | [`let`, `const` & Temporal Dead Zone](#chapter-8--let-const--temporal-dead-zone)                  | `let` vs `const` vs `var`, TDZ, `ReferenceError`, block-scoped vs function-scoped, re-declaration     |
| 9   | [Block Scope & Shadowing](#chapter-9--block-scope--shadowing)                                    | `{}` blocks, block scope for `let`/`const`, shadowing, illegal shadowing, `var` leaks out of blocks   |
| 10  | [Closures](#chapter-10--closures)                                                                | What is a closure, function + lexical environment, closures persist after outer fn returns              |
| 11  | [`setTimeout` & Closures](#chapter-11--settimeout--closures)                                     | Classic `var` loop + `setTimeout` problem, fix with `let` or IIFE, closure captures reference not value |
| 12  | [Closures Interview Questions](#chapter-12--closures-interview-questions)                        | Data hiding, encapsulation, module pattern, function factories, garbage collection & closures           |

<a id="part-4"></a>
### Part IV — Functions Deep Dive

| #   | Chapter                                                                                                   | Key Concepts                                                                                       |
| --- | --------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| 13  | [First-Class & Anonymous Functions](#chapter-13--first-class--anonymous-functions)                         | Function Statement vs Expression vs Declaration, Anonymous functions, First-Class Functions          |
| 14  | [Callbacks & Event Listeners](#chapter-14--callbacks--event-listeners)                                     | What is a callback, async operations with callbacks, Event Listeners, closures inside listeners      |

<a id="part-5"></a>
### Part V — Async JavaScript & Engine Internals

| #   | Chapter                                                                                        | Key Concepts                                                                                         |
| --- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| 15  | [Asynchronous JS & Event Loop](#chapter-15--asynchronous-js--event-loop)                       | Web APIs, Callback Queue, Microtask Queue, Event Loop, `setTimeout`/DOM APIs/`fetch` flow, starvation |
| 16  | [JS Engine & V8 Architecture](#chapter-16--js-engine--v8-architecture)                         | JS Runtime Environment, V8 engine, Parsing → AST → Interpreter → Compiler, JIT, GC                  |
| 17  | [Trust Issues with `setTimeout`](#chapter-17--trust-issues-with-settimeout)                     | `setTimeout` is not guaranteed timing, concurrency model, 0ms timeout misconception                   |

<a id="part-6"></a>
### Part VI — Functional Programming

| #   | Chapter                                                                                                              | Key Concepts                                                                       |
| --- | -------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| 18  | [Higher-Order Functions & Functional Programming](#chapter-18--higher-order-functions--functional-programming)        | HOF definition, functions as arguments, functions returning functions, abstraction   |
| 19  | [`map`, `filter` & `reduce`](#chapter-19--map-filter--reduce)                                                        | `.map()` (transform), `.filter()` (select), `.reduce()` (accumulate), chaining       |

<a id="part-7"></a>
### Part VII — Promises & Modern Async

| #   | Chapter                                                                                                 | Key Concepts                                                                       |
| --- | ------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| 20  | [Callback Hell](#chapter-20--callback-hell)                                                             | Pyramid of Doom, inversion of control, trust issues with callbacks                  |
| 21  | [Promises](#chapter-21--promises)                                                                       | Promise object, `pending`/`fulfilled`/`rejected`, `.then()`, immutability, `fetch`  |
| 22  | [Promise Chaining & Error Handling](#chapter-22--promise-chaining--error-handling)                       | `.then()` chaining, `.catch()`, `.finally()`, `Promise.all/allSettled/race/any`      |
| 23  | [`async`/`await`](#chapter-23--async--await)                                                              | `async` functions, `await` keyword, error handling with `try/catch`                  |

<a id="part-8"></a>
### Part VIII — The `this` Keyword Deep Dive

| #   | Chapter                                                                                       | Key Concepts                                                                                           |
| --- | --------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| 24  | [`this` Keyword in JavaScript](#chapter-24--this-keyword)                       | `this` in global scope, inside functions (strict vs non-strict), objects/methods, arrow fns, `call`/`apply`/`bind` |

<a id="part-9"></a>
### Part IX — Performance Patterns

| #   | Chapter                                       | Key Concepts                                                                                                    |
| --- | --------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| 25  | [Debouncing](#chapter-25--debouncing)         | Delay execution until inactivity, timer reset, search box optimization, `clearTimeout`, custom implementation    |
| 26  | [Throttling](#chapter-26--throttling)         | Fixed-rate execution, cooldown, scroll/resize handling, custom implementation, debounce vs throttle comparison    |
| 27  | [Polyfills & Prototype Internals](#chapter-27--polyfills--prototype)         | Polyfills, prototype chain, `__proto__`, `Object.getPrototypeOf`, `Array.prototype.map`, `filter`, `reduce`, `bind` polyfills    |

<a id="part-10"></a>
### Part X — Reference

| #   | Chapter                                                                                        | Key Concepts                                                       |
| --- | ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| 28  | [Cheat Sheet & Interview Quick-Fire](#chapter-28--cheat-sheet)           | All interview Qs consolidated, comparison tables, gotchas           |

---

# Part I — JavaScript Engine & Execution

---

<a id="chapter-1--execution-context"></a>

## Chapter 1 — Execution Context &nbsp; <sup>[⬆ Back to Menu](#part-1)</sup>

### What is Execution Context?

**Everything in JavaScript happens inside an Execution Context.** It's the environment where JS code is evaluated and executed — a container with two compartments: one for storing data (Memory), one for running code (Code).

### How It Works

An Execution Context has exactly **two components**:

| Component | Also Called | What It Does |
|-----------|------------|--------------|
| **Memory Component** | Variable Environment | Stores all variables and functions as **key-value pairs**. Variables start as `undefined`; functions are stored with their entire body. |
| **Code Component** | Thread of Execution | Executes code **one line at a time**, in order. Only one line runs at a time — this is what makes JS **single-threaded**. |

#### The Two Phases of Execution

When the JS engine runs a program, every Execution Context goes through two distinct phases:

**Phase 1 — Memory Creation Phase:**
- JS scans the **entire code** before executing anything
- Allocates memory for every variable → assigned `undefined`
- Allocates memory for every function → stored **fully** (entire function body)
- This is why hoisting works — memory is allocated before code runs

**Phase 2 — Code Execution Phase:**
- JS executes the code line by line
- Variables get their actual values assigned (replacing `undefined`)
- Function calls create **new** Execution Contexts (which go through their own Phase 1 + Phase 2)

#### Global Execution Context (GEC)

When a JS program starts, a **Global Execution Context** is created automatically. It is the outermost context — everything at the top level of your script runs inside the GEC. There is only one GEC per program.

#### JavaScript is Synchronous and Single-Threaded

| Property | Meaning |
|----------|---------|
| **Single-threaded** | Only one command executes at a time — one call stack |
| **Synchronous** | Commands execute in a specific, sequential order — one after another |

> ⚠️ JavaScript can _behave_ asynchronously (via Event Loop, Web APIs, Promises) but its **core execution model** is synchronous and single-threaded.

### Code Example

```javascript
var n = 2;

function square(num) {
  var ans = num * num;
  return ans;
}

var square2 = square(n);
var square4 = square(4);
```

**Phase 1 — Memory Allocation:**
```
n       → undefined
square  → function square(num) { var ans = num * num; return ans; }
square2 → undefined
square4 → undefined
```

**Phase 2 — Code Execution:**
```
n = 2                        (line 1 executed)
square2 = square(2) called   (new Execution Context created)
  ├─ Phase 1: ans → undefined
  ├─ Phase 2: ans = 2 * 2 = 4
  └─ returns 4 → square2 = 4   (EC destroyed)
square4 = square(4) called   (another new Execution Context created)
  ├─ Phase 1: ans → undefined
  ├─ Phase 2: ans = 4 * 4 = 16
  └─ returns 16 → square4 = 16 (EC destroyed)
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "Variables are created when JS reaches that line" | ❌ Variables are allocated in Phase 1 **before** any code runs |
| "Functions are called when JS sees the `function` keyword" | ❌ Function **declarations** are stored in Phase 1; they're only **called** when the `()` invocation is reached in Phase 2 |
| "JS is multi-threaded because of async" | ❌ JS has one thread. Async behavior comes from the Event Loop + Web APIs, not multiple threads |


<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;"> 

- **Q: What is an Execution Context?**
  - A: An Execution Context is an environment where JavaScript code is evaluated and executed. It has two components: Memory (Variable Environment) for storing variables/functions as key-value pairs, and Code (Thread of Execution) for running code line by line.

- **Q: What are the two phases of an Execution Context?**
  - A: Phase 1 is the Memory Creation Phase — variables get `undefined` and functions get stored fully. Phase 2 is the Code Execution Phase — code runs line by line and variables receive their actual values.

- **Q: What is the Global Execution Context?**
  - A: The GEC is the default context created when a JS program starts. All top-level code runs in the GEC. There is only one GEC per program.

- **Q: Why is JS called single-threaded?**
  - A: Because it has only one Call Stack — it can do only one thing at a time. Even async operations are managed through the Event Loop, not additional threads.

- **Q: When does a new Execution Context get created?**
  - A: Every time a function is **invoked** (called with `()`). The new EC goes through its own Phase 1 and Phase 2, then gets destroyed after returning.
  </div>
</details>
</div>

### Key Takeaways

- Every JS program starts by creating a **Global Execution Context**
- An Execution Context = **Memory Component** + **Code Component**
- Phase 1 allocates memory (variables → `undefined`, functions → full body)
- Phase 2 executes code line by line
- Each **function call** creates a brand new Execution Context
- JS is **synchronous** and **single-threaded** — one thing at a time

---

<a id="chapter-2--execution--call-stack"></a>

## Chapter 2 — Execution & Call Stack &nbsp; <sup>[⬆ Back to Menu](#part-1)</sup>

### What is the Call Stack?

The **Call Stack** is a stack data structure that manages Execution Contexts using **LIFO** (Last In, First Out). It tracks which EC is currently running and which are waiting.

**Also known as:** Execution Context Stack, Program Stack, Control Stack, Runtime Stack, Machine Stack.

### How It Works

| Step | Action | Stack State |
|------|--------|-------------|
| Program starts | GEC created, pushed to stack | `[GEC]` |
| Function called | New EC created, pushed on top | `[GEC, EC(fn)]` |
| Function returns | EC popped off the stack | `[GEC]` |
| Program ends | GEC popped | `[]` (empty) |

**Rules:**
1. The **GEC** is always the **first** pushed and the **last** popped
2. A function call **pushes** a new EC on top
3. A function return **pops** that EC off
4. The engine always executes the **topmost** EC on the stack

#### Stack Overflow

If functions call each other infinitely (e.g. unbounded recursion), the Call Stack fills up completely. The engine throws a `RangeError: Maximum call stack size exceeded`.

```javascript
// ❌ This causes Stack Overflow
function infinite() {
  return infinite(); // pushes forever, never pops
}
infinite(); // RangeError: Maximum call stack size exceeded
```

### Code Example

```javascript
var n = 2;

function square(num) {
  var ans = num * num;
  return ans;
}

var square2 = square(n);
var square4 = square(4);
```

**Call Stack trace:**

```
Step 1: GEC created → pushed
  Stack: [GEC]

Step 2: Memory Phase complete → Code Execution begins
  n = 2

Step 3: square(2) called → new EC created, pushed
  Stack: [GEC, EC(square(2))]
  Inside EC: ans = 2 * 2 = 4, return 4

Step 4: square(2) returns → EC popped
  Stack: [GEC]
  square2 = 4

Step 5: square(4) called → new EC created, pushed
  Stack: [GEC, EC(square(4))]
  Inside EC: ans = 4 * 4 = 16, return 16

Step 6: square(4) returns → EC popped
  Stack: [GEC]
  square4 = 16

Step 7: Program ends → GEC popped
  Stack: [] (empty)
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "The call stack runs things in parallel" | ❌ Only the **topmost** EC runs at any time — everything else waits |
| "Stack Overflow means out of memory (RAM)" | ❌ It means the **call stack** exceeded its frame limit, not that your system ran out of memory |
| "The GEC is removed when the first function runs" | ❌ The GEC stays at the bottom of the stack until the **entire program** finishes |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;"> 

- **Q: What is the Call Stack?**
  - A: The Call Stack is a stack data structure used by the JS engine to manage Execution Contexts. It follows LIFO — the last context pushed is the first to be popped.

- **Q: What happens to the Call Stack when a function is called?**
  - A: A new Execution Context is created for that function and pushed onto the top of the Call Stack. When the function returns, its context is popped off.

- **Q: What is a Stack Overflow?**
  - A: When recursion (or repeated function calls) fills the Call Stack beyond its limit, the engine throws `RangeError: Maximum call stack size exceeded`. This is called a Stack Overflow.

- **Q: What other names does the Call Stack go by?**
  - A: Execution Context Stack, Program Stack, Control Stack, Runtime Stack, Machine Stack.

- **Q: Can JS run multiple functions at the same time on the Call Stack?**
  - A: No. JS has a single Call Stack and is single-threaded. Only the topmost EC executes at any given moment.


  </div>
</details>
</div>

### Key Takeaways

- The Call Stack manages all Execution Contexts using **LIFO** order
- GEC is the **first** pushed; it's the **last** popped (when the program ends)
- Every function call **pushes** a new EC; every return **pops** it
- The Call Stack is always visible in browser **DevTools** — use it for debugging
- Unbounded recursion causes **Stack Overflow** (`Maximum call stack size exceeded`)
- JS has only **one** call stack — it can only do one thing at a time

---

<a id="chapter-3--hoisting"></a>

## Chapter 3 — Hoisting &nbsp; <sup>[⬆ Back to Menu](#part-1)</sup>

### What is Hoisting?

**Hoisting** lets you access variables and call functions before they appear in the source code. Since **memory is allocated in Phase 1** before any code runs, all variables and functions are already in memory by the time line 1 executes.

### How It Works

#### Variable Hoisting (`var`)

During Phase 1, `var x = 5;` stores `x → undefined`. The assignment `x = 5` only happens in Phase 2 when that line is reached.

```javascript
console.log(x); // undefined  (not an error!)
var x = 5;
console.log(x); // 5
```

#### Function Hoisting

Function **declarations** are stored **completely** in memory during Phase 1 — the entire function body is available. You can call them before their definition.

```javascript
greet(); // "Hello!" — works perfectly

function greet() {
  console.log("Hello!");
}
```

#### The Key Difference: `var` vs Function Declaration

| | `var` | Function Declaration |
|---|---|---|
| Phase 1 value | `undefined` | Full function body |
| Usable before declaration? | Partially — exists but value is `undefined` | Yes — fully callable |
| Type before declaration | `undefined` | `function` |

#### Function Expressions Are NOT Hoisted Like Declarations

When a function is assigned to a variable (`var fn = function() {}`), it follows **variable hoisting** rules — the variable gets `undefined` in Phase 1, not the function body.

```javascript
console.log(getName); // undefined
getName();             // ❌ TypeError: getName is not a function

var getName = function () {
  console.log("Namaste");
};
```

#### Arrow Functions Follow the Same Rule

```javascript
console.log(add); // undefined
add(2, 3);        // ❌ TypeError: add is not a function

var add = (a, b) => a + b;
```

#### `let` and `const` — Temporal Dead Zone (Preview)

`let` and `const` are **also hoisted**, but placed in a **Temporal Dead Zone** (TDZ) — a special state where the variable exists in memory but **cannot be accessed** until its declaration line. Accessing them early throws a `ReferenceError`.

```javascript
console.log(y); // ❌ ReferenceError: Cannot access 'y' before initialization
let y = 10;
```

> 💡 **TDZ is covered in full detail in [Chapter 8](#chapter-8--let-const--temporal-dead-zone).**

### Code Example

```javascript
getName();           // ✅ "Namaste JavaScript" (function declaration — fully hoisted)
console.log(x);      // undefined  (var hoisted with undefined)
// console.log(y);   // ❌ ReferenceError (let is in TDZ)

var x = 7;
let y = 5;

function getName() {
  console.log("Namaste JavaScript");
}
```

**What happens behind the scenes:**

```
Phase 1 — Memory Creation:
  x       → undefined
  y       → <in TDZ, cannot access>
  getName → function getName() { console.log("Namaste JavaScript"); }

Phase 2 — Code Execution:
  getName()       → prints "Namaste JavaScript" (function is fully available)
  console.log(x)  → prints undefined (x exists but not yet assigned)
  x = 7           → x is now 7
  y = 5           → y exits TDZ, now accessible with value 5
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "Hoisting physically moves code to the top" | ❌ Nothing moves. Memory is allocated in Phase 1 **before** Phase 2 runs — the code stays where it is |
| "`let` is not hoisted" | ❌ `let` **is** hoisted — but it's in the TDZ until its declaration. That's different from "not hoisted" |
| "Arrow functions are hoisted like regular functions" | ❌ Arrow functions assigned to `var`/`let`/`const` follow **variable** hoisting rules, not function hoisting |
| "You can safely use `var` before declaration" | ⚠️ You _can_, but you'll get `undefined` — which can cause subtle bugs that are hard to debug |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;"> 

- **Q: What is hoisting?**
  - A: Hoisting is a behavior where variable and function declarations are "lifted" to the top of their scope before code executes. In reality, memory is allocated for them in Phase 1 of Execution Context creation — the code doesn't physically move.

- **Q: What is the value of a `var` variable before its assignment line?**
  - A: `undefined`. The variable exists in memory from Phase 1, but its assigned value hasn't been set yet.

- **Q: Can you call a function before its declaration?**
  - A: Yes — for **function declarations** only. Their entire body is stored in Phase 1. But function **expressions** assigned to variables cannot be called before the assignment line (you'll get `TypeError: not a function`).

- **Q: What happens if you access a `let` or `const` variable before its declaration?**
  - A: A `ReferenceError` is thrown because `let`/`const` are in the Temporal Dead Zone until their declaration line is reached.

- **Q: What is the difference between `undefined` and `ReferenceError` in hoisting?**
  - A: `undefined` means the variable **exists in memory** (hoisted with `var`) but hasn't been assigned yet. `ReferenceError` means the variable is either **not declared at all** or is in the **TDZ** (`let`/`const`).


  </div>
</details>
</div>

### Key Takeaways

- Hoisting is a result of the **Memory Creation Phase** (Phase 1) of Execution Context
- `var` variables are hoisted with value `undefined`
- Function **declarations** are hoisted with their **full body** — callable anywhere in scope
- Function **expressions** (`var fn = function() {}`) follow `var` hoisting — the variable is `undefined` until assigned
- Arrow functions assigned to variables follow the **same rule** as function expressions
- `let` and `const` are hoisted but sit in the **Temporal Dead Zone** — accessing them early throws `ReferenceError`
- **Best practice**: Always declare variables at the top of their scope to avoid hoisting surprises

---

<a id="chapter-4--functions--variable-environments"></a>

## Chapter 4 — Functions & Variable Environments &nbsp; <sup>[⬆ Back to Menu](#part-1)</sup>

### What are Variable Environments?

Each function call creates its own Execution Context with its own **Variable Environment** — the memory space storing all local variables and parameters for that specific invocation. Variables don't leak between calls.

### How It Works

When JavaScript invokes a function, the engine:

| Step | Action | Effect |
|------|--------|--------|
| 1 | Creates a new Execution Context (EC) | Fresh environment for this call |
| 2 | Pushes EC onto the Call Stack | Engine tracks who's running |
| 3 | Runs Phase 1 (Memory Allocation) | Local variables → `undefined`, parameters → argument values |
| 4 | Runs Phase 2 (Code Execution) | Assignments and logic execute |
| 5 | Returns the result | Value passed to calling context |
| 6 | Pops EC from Call Stack | **EC is destroyed** — all local variables are gone |

#### Variable Environments Are Isolated

Each EC has its own Variable Environment. A variable named `x` in one function call has **no connection** to a variable named `x` in another call — even if they're calls to the same function.

#### Return Value Lifecycle

When a function executes `return ans`:
1. The value is passed back to the **calling context** (the EC below on the stack)
2. The function's EC is **immediately deleted**
3. The variable in the calling context receives the returned value

### Code Example

```javascript
var x = 1;

a(); // call before declaration — works due to hoisting
b();
console.log(x); // 1

function a() {
  var x = 10; // local to a()'s EC — completely separate from global x
  console.log(x); // 10
}

function b() {
  var x = 100; // local to b()'s EC — separate from both global x and a()'s x
  console.log(x); // 100
}
```

**Output:** `10`, `100`, `1`

**Step-by-step execution:**

```
GEC created:
  Memory: { x: undefined, a: fn a, b: fn b }
  Code: x = 1

a() called → EC_a created → pushed onto stack
  EC_a Memory: { x: undefined }
  EC_a Code:   x = 10; console.log(x) → prints 10
  EC_a returned → popped off stack, DELETED

b() called → EC_b created → pushed onto stack
  EC_b Memory: { x: undefined }
  EC_b Code:   x = 100; console.log(x) → prints 100
  EC_b returned → popped off stack, DELETED

console.log(x) → uses GEC's x = 1 → prints 1
```

**Key observation**: Three variables named `x` existed at different times, each in their own Variable Environment. They never interfere with each other.

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "A function's local variables persist after it returns" | ❌ The EC is **destroyed** when the function returns — local variables are gone (unless captured in a closure) |
| "Same-named variables in different functions point to the same memory" | ❌ Each EC has its **own** Variable Environment — names can collide without conflict |
| "GEC can access a function's local variables" | ❌ The scope chain goes **outward** (function → global), never **inward** (global → function) |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;"> 

- **Q: What happens inside the JS engine when a function is called?**
  - A: A new Execution Context is created. It goes through Phase 1 (memory allocation for local variables) and Phase 2 (code execution). The EC is pushed onto the Call Stack when the function starts and popped when it returns.

- **Q: Does a function's local variable affect variables outside it?**
  - A: No. Each function has its own Variable Environment (memory space). A `var x` inside a function is completely separate from a `var x` outside it.

- **Q: What happens to a function's EC after it returns?**
  - A: The EC is popped off the Call Stack and **destroyed**. All local variables in it are gone — unless they are captured in a closure.

- **Q: Can the GEC access variables inside a function?**
  - A: No. Functions can access variables from outer scopes via the **scope chain**, but the GEC cannot reach into a function's local EC.

- **Q: If I call the same function twice, do the two calls share variables?**
  - A: No. Each invocation creates a **separate** Execution Context with its own Variable Environment. They are completely isolated.


  </div>
</details>
</div>

### Key Takeaways

- Every function call creates a **fresh, independent** Execution Context
- Local variables live in the function's **Variable Environment** and are isolated from other ECs
- The same function called twice creates **two separate ECs** — they don't share memory
- When a function returns, its EC is **destroyed** — local variables are cleaned up
- The Call Stack manages the order: **GEC at the bottom**, active function EC at the top
- This isolation is fundamental to how **scope** and **closures** work in JavaScript

---

<a id="chapter-5--shortest-js-program-window--this"></a>

## Chapter 5 — Shortest JS Program, `window` & `this` &nbsp; <sup>[⬆ Back to Menu](#part-2)</sup>

### What are `window` and `this`?

Even an empty JS file triggers setup — the engine creates a **GEC**, a **`window` object** (browser's global object), and binds **`this`** to `window` at the global level.

### How It Works

#### The Shortest JS Program

An empty `.js` file is the shortest valid JavaScript program. Even with zero lines of user code, the JS engine:

| Step | What the engine creates | Purpose |
|------|------------------------|---------|
| 1 | **Global Execution Context (GEC)** | The outermost execution environment |
| 2 | **`window` object** (browser) | Global object — container for all browser APIs |
| 3 | **`this` keyword** | At global scope, `this === window` |

#### The `window` Object

`window` is the **global object** created by the browser's JS runtime. It represents the browser window and serves as the global scope container.

- All global `var` variables and function declarations become **properties of `window`**
- Built-in browser APIs (`setTimeout`, `console`, `fetch`, `localStorage`) are all properties of `window`
- You can access window properties with or without the `window.` prefix

#### `var` vs `let`/`const` on `window`

| Declaration | Attaches to `window`? | Example |
|------------|----------------------|---------|
| `var x = 10` | ✅ Yes | `window.x === 10` → `true` |
| `let y = 20` | ❌ No | `window.y` → `undefined` |
| `const z = 30` | ❌ No | `window.z` → `undefined` |
| `function foo() {}` | ✅ Yes | `window.foo` → the function |

#### `this` at the Global Level

At the global level (outside any function), `this` refers to the global object:

```javascript
console.log(this === window); // true (in browsers, at global scope)
```

#### Different Runtimes, Different Global Objects

| Runtime | Global Object | `this` at global scope |
|---------|--------------|----------------------|
| **Browser** | `window` | `this === window` |
| **Node.js** | `global` | `this === module.exports` (in modules) |
| **Web Workers** | `self` | `this === self` |
| **Universal** | `globalThis` (ES2020) | Works everywhere |

### Code Example

```javascript
// Even an empty file would create GEC + window + this.
// Adding some code to demonstrate:

var course = "Namaste JavaScript";
let instructor = "Akshay Saini";

console.log(window.course);     // "Namaste JavaScript"   (var → attaches to window)
console.log(window.instructor); // undefined               (let → does NOT attach)
console.log(this === window);   // true                    (at global scope)
console.log(this.course);       // "Namaste JavaScript"   (this === window)
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "`let` variables are accessible on `window`" | ❌ Only `var` declarations and function declarations attach to `window`. `let`/`const` create global bindings but **not** window properties |
| "`this` always equals `window`" | ❌ `this === window` only at the **global scope** in browsers. Inside functions, methods, classes, and arrow functions, `this` varies (covered in [Chapter 24](#chapter-24--this-keyword)) |
| "An empty JS file does nothing" | ❌ The engine creates GEC, `window`, and `this` — significant setup happens even with no user code |
| "`window` and `global` are the same thing" | ❌ `window` is browser-only. Node.js uses `global`. Use `globalThis` for cross-environment code |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;"> 

- **Q: What is the shortest JavaScript program?**
  - A: An empty file. Even with no user code, the engine creates the GEC, `window` object, and `this` binding.

- **Q: What is the `window` object?**
  - A: The `window` object is the global object in browser environments. It contains all global `var` variables, function declarations, and built-in browser APIs. It's the value of `this` at the global scope.

- **Q: What does `this` equal at the global scope in a browser?**
  - A: `this` equals the `window` object. `this === window` is `true` at the global level.

- **Q: Do `let` and `const` variables attach to the `window` object?**
  - A: No. Only `var` variables and function declarations at the global level become properties of `window`. `let` and `const` create global bindings in a separate scope that isn't on `window`.

- **Q: What is `globalThis`?**
  - A: `globalThis` is a standardized way (ES2020) to access the global object across all environments — whether browser (`window`), Node.js (`global`), or Web Workers (`self`).

- **Q: If I declare `var a = 10` at the top level, is `window.a` equal to `10`?**
  - A: Yes. Top-level `var` declarations become properties of the global object (`window` in browsers).


  </div>
</details>
</div>

### Key Takeaways

- JS engine creates **GEC**, **`window`**, and **`this`** even for an empty file
- `window` is the global object in browsers — it holds all browser APIs and global `var` variables
- At the global scope: **`this === window`** (in browsers)
- **`var`** globals become properties of `window`; **`let`/`const`** globals do **not**
- The global object differs per environment: `window` (browser), `global` (Node.js), `globalThis` (universal)
- Use **`globalThis`** when writing cross-environment JavaScript

---

<a id="chapter-6--undefined-vs-not-defined"></a>

## Chapter 6 — `undefined` vs Not Defined &nbsp; <sup>[⬆ Back to Menu](#part-2)</sup>

### What is `undefined`?

`undefined` is JS's placeholder value — assigned automatically during Phase 1 to variables that exist but have no value yet. **"Not defined"** is a `ReferenceError` thrown when a variable was never declared at all.

### How It Works

| Scenario | Result |
|----------|--------|
| `var x; console.log(x)` | `undefined` — declared, no value yet |
| `console.log(x); var x = 5` | `undefined` — hoisted |
| `console.log(z)` (z never declared) | `ReferenceError: z is not defined` |

#### `undefined` vs `null`

- `undefined` = **engine's default** — "not yet assigned"
- `null` = **programmer's choice** — "intentionally empty"

```javascript
var a;          // undefined (engine assigned)
var b = null;   // null (programmer assigned)

console.log(typeof a); // "undefined"
console.log(typeof b); // "object" (historical JS quirk)
```

#### Checking for `undefined`

```javascript
var a;
if (typeof a === 'undefined') {
  console.log("safest check — works even on undeclared variables");
}
```

### Code Example

```javascript
var x;
console.log(x);         // undefined (declared, not assigned)
console.log(typeof x);  // "undefined"

x = 7;
console.log(x);         // 7

// console.log(y);      // ReferenceError: y is not defined

// undefined is falsy
if (!x) console.log("falsy"); // not printed — x is 7
var a;
if (!a) console.log("falsy"); // printed — undefined is falsy
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "`undefined` and `not defined` are the same" | ❌ `undefined` = variable exists, no value. "Not defined" = variable never declared → `ReferenceError` |
| "Assigning `undefined` manually is fine" | ⚠️ Use `null` to represent "no value" — `undefined` should be the engine's signal, not yours |
| "`undefined` and `null` are equal" | ⚠️ `undefined == null` is `true` (loose), but `undefined === null` is `false` (strict) |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;"> 

- **Q: What is `undefined` in JavaScript?**
  - A: A primitive value auto-assigned during Memory Creation Phase to variables that exist but haven't been given a value yet.

- **Q: What does "not defined" mean?**
  - A: A `ReferenceError` — the variable was never declared in any accessible scope.

- **Q: Difference between `undefined` and `null`?**
  - A: `undefined` is set by the engine (no value yet). `null` is set by the programmer (intentionally empty). `typeof undefined` is `"undefined"`; `typeof null` is `"object"`.

- **Q: Is `undefined` falsy?**
  - A: Yes. Along with `null`, `0`, `""`, `false`, and `NaN`.


  </div>
</details>
</div>

### Key Takeaways

- `undefined` = variable exists in memory but has no assigned value
- "Not defined" = `ReferenceError` — never declared
- `undefined !== null` — both "empty" but different meanings
- Never assign `undefined` manually — use `null` instead
- `typeof x === 'undefined'` is the safest check (works on undeclared vars too)

---

# Part III — Scope & Closures

---

<a id="chapter-7--scope--lexical-environment"></a>

## Chapter 7 — Scope & Lexical Environment &nbsp; <sup>[⬆ Back to Menu](#part-3)</sup>

### What is Scope?

**Scope** determines where a variable can be accessed. **Lexical Environment** is the mechanism behind scope — each EC carries its local memory + a reference to its parent's Lexical Environment, forming the **Scope Chain**.

### How It Works

#### Lexical Environment

```
Lexical Environment = Local Memory + Reference to Parent's Lexical Environment
```

Every EC has a Lexical Environment. The GEC's parent reference is `null` (top of the chain).

"Lexical" means *where the code is written* — a function's scope is determined by its position in the source code, not where it's called from.

#### Scope Chain Lookup

When JS encounters a variable:

| Step | Action |
|------|--------|
| 1 | Search current EC's local memory |
| 2 | Not found → follow parent reference to parent's Lexical Environment |
| 3 | Keep going up the chain |
| 4 | Reached GEC and still not found → `ReferenceError` |

### Code Example

```javascript
function a() {
  var x = 10;
  c(); // called from inside a — but scope depends on WHERE c is DEFINED
}

function c() {
  // c is defined at the GLOBAL level (lexically)
  console.log(x); // ReferenceError: x is not defined
}

a();
```

**Contrast — lexical nesting:**

```javascript
function outer() {
  var x = 10;

  function inner() {
    console.log(x); // 10 — inner is defined INSIDE outer
  }

  inner();
}
outer();
```

```
Scope chain lookup for 'x' inside inner():
  1. inner()'s local memory → not found
  2. outer()'s lexical environment → found! x = 10
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "A function can access variables of whoever *calls* it" | ❌ Scope is determined by where the function is *written*, not where it's called (lexical scope) |
| "The scope chain only goes one level up" | ❌ It chains all the way up to the GEC |
| "`var` is block-scoped" | ❌ `var` is function-scoped; only `let`/`const` are block-scoped |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;"> 

- **Q: What is scope in JavaScript?**
  - A: The region of code where a variable is accessible — determined by where it's declared.

- **Q: What is a Lexical Environment?**
  - A: Local memory + a reference to the parent's Lexical Environment. Created alongside every Execution Context.

- **Q: What is the Scope Chain?**
  - A: The chain of Lexical Environments linked from child → parent → … → GEC. JS traverses it upward to resolve variable names.

- **Q: What determines a function's scope?**
  - A: Where it is *written* (defined) in the source code — not where it's called. This is lexical (static) scope.


  </div>
</details>
</div>

### Key Takeaways

- Every EC creates a Lexical Environment = local memory + parent reference
- The **Scope Chain** links Lexical Environments from inner to outer
- JavaScript uses **lexical scope** — scope is determined at write-time, not call-time
- Variable lookup walks up the chain; failure → `ReferenceError`
- `var` is function-scoped; `let`/`const` are block-scoped
- GEC's parent reference is `null` — it's the top

---

<a id="chapter-8--let-const--temporal-dead-zone"></a>

## Chapter 8 — `let`, `const` & Temporal Dead Zone &nbsp; <sup>[⬆ Back to Menu](#part-3)</sup>

### What is the Temporal Dead Zone?

`let` and `const` **are** hoisted, but unlike `var` they sit in the **Temporal Dead Zone (TDZ)** — a period from hoisting to declaration where any access throws `ReferenceError`. `var` goes to `window` with `undefined`; `let`/`const` go to a separate memory space.

### How It Works

#### `let` vs `const` vs `var`

| Feature | `var` | `let` | `const` |
|---------|-------|-------|---------|
| Scope | Function | Block | Block |
| Hoisting | `undefined` | TDZ | TDZ |
| Reassignment | ✅ Yes | ✅ Yes | ❌ No |
| Redeclaration | ✅ Yes | ❌ No | ❌ No |
| Must initialize | No | No | **Yes** |
| On `window` | ✅ Yes | ❌ No | ❌ No |

#### The Three Error Types

**ReferenceError — TDZ access:**
```javascript
console.log(a); // ReferenceError: Cannot access 'a' before initialization
let a = 10;
```

**SyntaxError — `const` without initializer / redeclaring `let`:**
```javascript
const c;      // SyntaxError: Missing initializer in const declaration
let x = 5;
let x = 10;   // SyntaxError: Identifier 'x' has already been declared
```

**TypeError — reassigning `const`:**
```javascript
const d = 5;
d = 10;       // TypeError: Assignment to constant variable
```

### Code Example

```javascript
// console.log(a); // ReferenceError — a is in TDZ
let a = 10;
console.log(a); // 10

console.log(b); // undefined — var hoisted normally
var b = 20;

const c = 30;
// c = 40;        // TypeError: Assignment to constant variable

a = 50;           // ✅ let allows reassignment
// let a = 60;    // SyntaxError: already declared
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "`let` and `const` are not hoisted" | ❌ They ARE hoisted — but placed in the TDZ, not initialized to `undefined` |
| "`const` means the value can't change" | ⚠️ `const` prevents reassignment of the binding, but object/array contents CAN be mutated |
| "TDZ only applies to `const`" | ❌ Both `let` and `const` have a TDZ |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;"> 

- **Q: Are `let` and `const` hoisted?**
  - A: Yes. But they're placed in the TDZ — accessing them before declaration throws `ReferenceError`.

- **Q: What is the Temporal Dead Zone?**
  - A: The time between hoisting and the declaration line. The variable exists in memory but is inaccessible.

- **Q: What error does `const x;` throw?**
  - A: `SyntaxError: Missing initializer in const declaration`. `const` must be initialized at declaration.

- **Q: Difference between `let` and `const`?**
  - A: Both are block-scoped with TDZ. `const` cannot be reassigned and must be initialized. `let` allows reassignment.


  </div>
</details>
</div>

### Key Takeaways

- All three (`var`, `let`, `const`) are hoisted — but `let`/`const` go into TDZ
- TDZ = hoisted but inaccessible until declaration line
- `const` must be initialized at declaration; cannot be reassigned
- `let` cannot be redeclared in the same scope
- `var` attaches to `window`; `let`/`const` do not
- **Best practice**: prefer `const` → `let` → avoid `var`

---

<a id="chapter-9--block-scope--shadowing"></a>

## Chapter 9 — Block Scope & Shadowing &nbsp; <sup>[⬆ Back to Menu](#part-3)</sup>

### What is Block Scope?

A **block** `{ }` groups statements together. `let` and `const` inside a block are scoped to that block — invisible outside. `var` ignores block scope entirely. **Shadowing** is when an inner-scope variable hides an outer-scope variable of the same name.

### How It Works

#### Block Scope — `let`/`const` vs `var`

```javascript
{
  let a = 10;
  const b = 20;
  var c = 30;
}

console.log(c); // 30  — var leaks out of the block
console.log(a); // ReferenceError — let is block-scoped
console.log(b); // ReferenceError — const is block-scoped
```

#### Shadowing

```javascript
let y = 1;
{
  let y = 2;            // NEW block-scoped variable — shadows outer y
  console.log(y);       // 2
}
console.log(y);         // 1 — outer y unchanged
```

```javascript
var x = 1;
{
  var x = 2;            // SAME variable — var has no block scope
  console.log(x);       // 2
}
console.log(x);         // 2 — outer x was modified!
```

#### Illegal Shadowing

Shadowing `let`/`const` with `var` is a `SyntaxError` because `var` escapes the block and conflicts with the outer binding.

| Outer | Inner | Valid? |
|-------|-------|--------|
| `var` | `var` | ✅ (same variable) |
| `var` | `let` | ✅ (new block-scoped) |
| `let` | `let` | ✅ (new block-scoped) |
| `let` | `var` | ❌ **SyntaxError** |
| `const` | `var` | ❌ **SyntaxError** |
| `const` | `let`/`const` | ✅ |

### Code Example

```javascript
var x = 1;
let y = 2;
const z = 3;

{
  var x = 11;    // same var x — overwrites global x
  let y = 22;    // new block-scoped y
  const z = 33;  // new block-scoped z

  console.log(x); // 11
  console.log(y); // 22
  console.log(z); // 33
}

console.log(x); // 11 — var was modified
console.log(y); // 2  — let was shadowed, outer unchanged
console.log(z); // 3  — const was shadowed, outer unchanged
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "`var` is block-scoped" | ❌ `var` is function/global-scoped — it leaks out of `{ }` blocks |
| "Shadowing always modifies the outer variable" | ❌ Only `var` shadowing `var` modifies the same variable. `let`/`const` create new independent bindings |
| "You can shadow `let` with `var` in a block" | ❌ That's illegal shadowing — `SyntaxError` |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;"> 

- **Q: What is a block in JavaScript?**
  - A: A pair of `{ }` that groups statements. Also called a compound statement. Creates block scope for `let`/`const`.

- **Q: What is shadowing?**
  - A: When an inner-scope variable has the same name as an outer-scope variable, temporarily hiding it within that scope.

- **Q: What is illegal shadowing?**
  - A: Shadowing `let`/`const` with `var` in a block. `var` would escape the block and conflict with the outer `let`/`const` → `SyntaxError`.

- **Q: Can you shadow `var` with `let`?**
  - A: Yes. `let` creates a new block-scoped binding that shadows the `var` within the block.


  </div>
</details>
</div>

### Key Takeaways

- `{ }` blocks create scope for `let`/`const` but **not** for `var`
- `var` leaks out of blocks — scoped to enclosing function or global only
- Shadowing with `let`/`const` creates independent variables — outer is unchanged
- Shadowing with `var` on `var` modifies the **same** variable
- Shadowing `let`/`const` with `var` is **illegal** → `SyntaxError`

---

<a id="chapter-10--closures"></a>

## Chapter 10 — Closures &nbsp; <sup>[⬆ Back to Menu](#part-3)</sup>

### What is a Closure?

A **closure** is a function bundled with a reference to its outer lexical environment — it remembers variables from its enclosing scope even after that outer function has returned. Closures capture **references**, not values.

### How It Works

#### Basic Closure

```javascript
function x() {
  var a = 9;
  function y() {
    console.log(a); // closure — y remembers a
  }
  return y;
}

var z = x();  // x() returns y, x's EC is destroyed
z();          // 9 — but y still accesses a through the closure
```

#### Closures Capture References, Not Values

```javascript
function counter() {
  var count = 0;
  return function() {
    count++;
    return count;
  };
}

const increment = counter();
console.log(increment()); // 1
console.log(increment()); // 2
console.log(increment()); // 3
// count persists — closure holds a reference to it
```

#### Nested Closures

```javascript
function b() {
  var e = 99;
  function w() {
    var c = 9;
    function d() {
      console.log(c, e); // d closes over both w's and b's scope
    }
    d();
  }
  w();
}
b(); // 9 99
```

#### Advantages — Practical Patterns

**Data Hiding (Module Pattern):**
```javascript
function createCounter() {
  var count = 0; // private
  return {
    increment: function() { count++; },
    decrement: function() { count--; },
    getCount:  function() { return count; }
  };
}

const ctr = createCounter();
ctr.increment(); ctr.increment();
console.log(ctr.getCount()); // 2
console.log(ctr.count);      // undefined — private!
```

**Currying:**
```javascript
function multiply(x) {
  return function(y) { return x * y; };
}
const double = multiply(2);
console.log(double(5)); // 10
```

**Memoization:**
```javascript
function memoize(fn) {
  var cache = {};
  return function(n) {
    if (cache[n] !== undefined) return cache[n];
    cache[n] = fn(n);
    return cache[n];
  };
}
```

#### Disadvantages

- **Memory**: closed-over variables can't be garbage-collected while the closure exists
- **Memory leaks**: event listeners or long-lived closures that are never cleaned up
- Set large closed-over variables to `null` when done to help GC

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "Closures copy the value of outer variables" | ❌ They capture a **reference** — if the outer variable changes, the closure sees the new value |
| "A closure only forms when the function is returned" | ❌ Closures form at **definition time** — whether the function is returned, called inline, or passed as a callback |
| "Closures only access the immediate parent scope" | ❌ They access **all** enclosing scopes via the scope chain |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;"> 

- **Q: What is a closure?**
  - A: A function bundled with a reference to its outer lexical environment. It can access outer variables even after the outer function returns.

- **Q: Do closures capture references or values?**
  - A: References. If the outer variable changes, the closure sees the updated value.

- **Q: What are closures used for?**
  - A: Data hiding (module pattern), currying, memoization, counters, `setTimeout` with correct values.

- **Q: What are the downsides of closures?**
  - A: Over-consumption of memory — closed-over variables persist as long as the closure is reachable. Can cause memory leaks if not cleaned up.


  </div>
</details>
</div>

### Key Takeaways

- Closure = function + its lexical environment (reference to outer scope)
- Closures **remember** outer variables even after the outer function returns
- They capture **references**, not snapshots
- Key patterns: module pattern, currying, memoization, counters
- Downside: closed-over variables persist in memory — clean up when done
- Closures arise naturally from lexical scoping — no special syntax needed

---

<a id="chapter-11--settimeout--closures"></a>

## Chapter 11 — `setTimeout` & Closures &nbsp; <sup>[⬆ Back to Menu](#part-3)</sup>

### What is the `setTimeout` + Loop Problem?

`setTimeout` doesn't pause JS — it defers a callback. In a `var` loop, all callbacks share a **single** variable binding. By the time they fire, the loop is done and the variable holds the final value. Fix: use `let` (new binding per iteration) or IIFE.

### How It Works

#### The Classic Problem

```javascript
for (var i = 1; i <= 5; i++) {
  setTimeout(function() {
    console.log(i);
  }, i * 1000);
}
// Output: 6 6 6 6 6 (NOT 1 2 3 4 5)
```

**Why?** `var i` is function/global-scoped — **one** `i` shared by all 5 callbacks. Loop finishes → `i` is `6` → all callbacks read `6`.

#### Solution 1: `let` (Block Scope)

```javascript
for (let i = 1; i <= 5; i++) {
  setTimeout(function() {
    console.log(i);
  }, i * 1000);
}
// Output: 1 2 3 4 5 ✅
```

`let` creates a **new binding** per iteration — each callback closes over its own `i`.

#### Solution 2: IIFE with `var`

```javascript
for (var i = 1; i <= 5; i++) {
  (function(j) {
    setTimeout(function() {
      console.log(j); // closes over j — unique per iteration
    }, j * 1000);
  })(i);
}
// Output: 1 2 3 4 5 ✅
```

IIFE captures the current `i` as `j` in a new function scope.

### Code Example

```javascript
// Problem
function printNumbers_WRONG() {
  for (var i = 1; i <= 5; i++) {
    setTimeout(() => console.log(i), i * 1000);
  }
}
// 6 6 6 6 6

// Fix 1: let
function printNumbers_LET() {
  for (let i = 1; i <= 5; i++) {
    setTimeout(() => console.log(i), i * 1000);
  }
}
// 1 2 3 4 5

// Fix 2: IIFE
function printNumbers_IIFE() {
  for (var i = 1; i <= 5; i++) {
    (function(j) {
      setTimeout(() => console.log(j), j * 1000);
    })(i);
  }
}
// 1 2 3 4 5
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "`setTimeout` pauses JavaScript" | ❌ JS never pauses — `setTimeout` schedules a callback via the Event Loop |
| "`setTimeout(fn, 0)` runs immediately" | ❌ Even 0ms is deferred until the Call Stack is empty |
| "Each iteration of a `var` loop gets its own `i`" | ❌ `var` is function-scoped — all iterations share one `i` |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
 <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;"> 

- **Q: What does `for (var i=1; i<=5; i++) { setTimeout(() => console.log(i), i*1000); }` print?**
  - A: `6 6 6 6 6`. All callbacks close over the same `var i`, which is `6` when they fire.

- **Q: How do you fix it?**
  - A: Use `let` instead of `var` (each iteration gets its own binding), or wrap in an IIFE.

- **Q: Why does `let` fix the problem?**
  - A: `let` is block-scoped — each loop iteration creates a new `i` binding. Each callback's closure captures a different `i`.

- **Q: Does `setTimeout(fn, 0)` execute immediately?**
  - A: No. It defers to after the current call stack is empty, via the Event Loop.


  </div>
</details>
</div>

### Key Takeaways

- `setTimeout` defers execution — never blocks synchronous code
- `var` loop + `setTimeout` = all callbacks share **one** variable → classic pitfall
- `let` creates a **new binding per iteration** — closures capture distinct values
- IIFE wraps each iteration in its own scope — same fix when `var` is required
- Even `setTimeout(fn, 0)` runs **after** the current stack clears

---

<a id="chapter-12--closures-interview-questions"></a>

## Chapter 12 — Closures Interview Questions &nbsp; <sup>[⬆ Back to Menu](#part-3)</sup>

<details>
<summary><strong>Q1: What is a Closure?</strong></summary>

A function + reference to its outer lexical environment. Access to outer variables persists even after the outer function returns.

```javascript
function outer() {
  var x = 10;
  function inner() { console.log(x); }
  return inner;
}
const fn = outer();
fn(); // 10
```
</details>

<details>
<summary><strong>Q2: Does a closure form even if the function isn't returned?</strong></summary>

**Yes.** Closures form at definition time — whether the function is returned, called internally, or passed as a callback.

```javascript
function outer() {
  var x = 10;
  function inner() { console.log(x); }
  inner(); // called inside, not returned — still a closure
}
outer(); // 10
```
</details>

<details>
<summary><strong>Q3: Does `let` vs `var` affect closures?</strong></summary>

**No.** Both `var` and `let` are captured by closures. The only difference is scoping rules.
</details>

<details>
<summary><strong>Q4: Can closures access outer function parameters?</strong></summary>

**Yes.** Parameters are part of the function's scope — closures capture them.

```javascript
function outer(str) {
  return function() { console.log(str); };
}
const fn = outer("Hello!");
fn(); // "Hello!"
```
</details>

<details>
<summary><strong>Q5: Do closures work across multiple nesting levels?</strong></summary>

**Yes.** A function closes over **all** enclosing scopes, not just the immediate parent.

```javascript
function outermost() {
  var a = 1;
  function middle() {
    var b = 2;
    function inner() { console.log(a, b); }
    return inner;
  }
  return middle;
}
const fn = outermost()();
fn(); // 1 2
```
</details>

<details>
<summary><strong>Q6: Tricky — Shadowing Inside a Closure</strong></summary>

```javascript
function counter() {
  var count = 0;
  return function() {
    var count = 0; // ← shadows the outer count!
    count++;
    console.log(count);
  };
}
const inc = counter();
inc(); // 1
inc(); // 1 — always 1, not incrementing!
inc(); // 1
```

**Why?** The inner `var count = 0` creates a **new** local variable each call, shadowing the closed-over `count`. The outer `count` is never touched. Remove the inner `var count = 0` to fix.
</details>

<details>
<summary><strong>Q7: Advantages of Closures</strong></summary>

- **Module pattern** — private state with public API
- **Currying** — partial function application
- **Memoization** — caching results
- **Data hiding** — encapsulation without classes
- **`setTimeout`** — preserving values in async callbacks
- **Stateful functions** — counters without globals
</details>

<details>
<summary><strong>Q8: Data Hiding with Closures</strong></summary>

```javascript
function createCounter() {
  var count = 0; // private
  return {
    increment: function() { count++; console.log(count); },
    decrement: function() { count--; console.log(count); },
    getCount:  function() { return count; }
  };
}

const ctr = createCounter();
ctr.increment(); // 1
ctr.increment(); // 2
ctr.decrement(); // 1
console.log(ctr.count);      // undefined — count is private
console.log(ctr.getCount()); // 1
```
</details>

<details>
<summary><strong>Q9: Disadvantages of Closures</strong></summary>

- **Memory over-consumption** — closed-over variables stay in memory as long as the closure exists
- **Memory leaks** — event listeners or collections holding closures prevent GC
- **Fix**: remove listeners when done; set large variables to `null`
</details>

### Key Takeaways

- Closures form at **definition time** — regardless of whether the function is returned
- They close over **all** enclosing scopes, including parameters
- `var`/`let` both work — scoping rules differ but closures capture both
- Watch for **shadowing** inside returned functions — it can silently break closures
- **Module pattern** = closures for encapsulation — most important practical use
- Clean up closures (remove listeners, nullify references) to prevent memory leaks

---

# Part IV — Functions Deep Dive

---

<a id="chapter-13--first-class--anonymous-functions"></a>

## Chapter 13 — First-Class & Anonymous Functions &nbsp; <sup>[⬆ Back to Menu](#part-4)</sup>

### What are First-Class Functions?

Functions in JavaScript are **first-class citizens** — they can be assigned to variables, passed as arguments, returned from other functions, and stored in data structures. This makes functional programming possible in JS.

### How It Works

#### Function Statement vs Function Expression

| | Function Statement (Declaration) | Function Expression |
|---|---|---|
| Syntax | `function greet() { }` | `var greet = function() { }` |
| Hoisted? | ✅ Fully hoisted — callable before its line | ❌ Variable hoisted as `undefined` → `TypeError` if called early |
| Standalone? | Yes | Must be assigned to a variable |

```javascript
// Function Statement — can call before declaration
greet(); // "Hello!" ✅
function greet() { console.log("Hello!"); }

// Function Expression — cannot call before assignment
// sayHi(); // TypeError: sayHi is not a function
var sayHi = function() { console.log("Hi!"); };
sayHi(); // "Hi!" ✅
```

#### Anonymous Functions

A function without a name. Cannot stand alone as a statement (`SyntaxError`) — must be used as a value.

```javascript
// ✅ Valid: assigned to variable
var fn = function() { console.log("anonymous"); };

// ✅ Valid: passed as argument
setTimeout(function() { console.log("timer"); }, 1000);

// ❌ Invalid: standalone
// function() { }  // SyntaxError: Function statements must have a name
```

#### Named Function Expressions

A function expression where the function also has a name. The name is only accessible **inside** the function itself (useful for recursion). It does NOT exist in the outer scope.

```javascript
var greet = function sayHello() {
  console.log("Hello!");
  // sayHello() — accessible here (recursion)
};

greet();     // "Hello!" ✅
// sayHello(); // ReferenceError — not accessible outside
```

Named expressions are preferred for debugging — the name appears in stack traces.

#### Parameters vs Arguments

- **Parameters**: placeholders in the function definition
- **Arguments**: actual values passed at call time

```javascript
function add(a, b) { return a + b; } // a, b = parameters
add(3, 5);                            // 3, 5 = arguments
```

#### First-Class Functions — All Four Powers

```javascript
// 1. Assigned to variable
const square = function(x) { return x * x; };

// 2. Passed as argument
[1, 2, 3].map(function(x) { return x * 2; }); // [2, 4, 6]

// 3. Returned from function
function multiplier(factor) {
  return function(x) { return x * factor; };
}
const double = multiplier(2);
console.log(double(5)); // 10

// 4. Stored in data structure
const ops = { add: (a, b) => a + b, sub: (a, b) => a - b };
```

### Code Example

```javascript
// Function Statement
function a() { console.log("statement"); }
a();

// Function Expression
var b = function() { console.log("expression"); };
b();

// Named Function Expression
var c = function named() {
  console.log("named expression");
};
c();
// named(); // ReferenceError

// First-class: function as return value
function outer() {
  return function inner() { console.log("returned from outer"); };
}
var returned = outer();
returned();
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "Function expressions are hoisted like declarations" | ❌ Only the variable is hoisted (`undefined`); calling before assignment → `TypeError` |
| "Anonymous functions can stand alone" | ❌ `function() { }` as a statement → `SyntaxError`. Must be used as a value |
| "Named function expression name is accessible outside" | ❌ The name is only accessible inside the function body — outer scope can't see it |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;">

- **Q: What is the difference between a function statement and a function expression?**
  - A: A function statement is fully hoisted — callable anywhere in its scope. A function expression assigns a function to a variable — only the variable is hoisted (as `undefined`). Calling before assignment throws `TypeError`.

- **Q: What is an anonymous function?**
  - A: A function without a name. Must be used as a value (assigned, passed, returned). A standalone anonymous function is a `SyntaxError`.

- **Q: What is a named function expression?**
  - A: A function expression where the function has a name accessible only inside itself (for recursion/self-reference). The outer scope cannot access it. Useful for debugging — name appears in stack traces.

- **Q: What does "first-class function" mean?**
  - A: Functions can be used as values — assigned to variables, passed as arguments, returned from functions, stored in data structures. This makes JS naturally suited for functional programming.
  </div>
</details>
</div>

### Key Takeaways

- Function statement = fully hoisted; callable before its line
- Function expression = only variable hoisted (`undefined`); function is not
- Anonymous function = no name; must be used as a value, cannot stand alone
- Named function expression = name visible only inside itself (not in outer scope)
- Parameters = placeholders in definition; Arguments = actual values at call time
- First-class functions = assignable, passable, returnable — foundation for FP

---

<a id="chapter-14--callbacks--event-listeners"></a>

## Chapter 14 — Callbacks & Event Listeners &nbsp; <sup>[⬆ Back to Menu](#part-4)</sup>

### What is a Callback?

A **callback** is a function passed as an argument to another function, to be invoked later. Callbacks are how JS hooks into async operations (timers, events, network) despite being single-threaded.

### How It Works

#### Basic Callback

```javascript
function greet(name, callback) {
  console.log("Hello, " + name);
  callback();
}

greet("Akshay", function() {
  console.log("Goodbye!");
});
// Hello, Akshay
// Goodbye!
```

#### Callbacks Enable Async Code

```javascript
console.log("Before");
setTimeout(function() {
  console.log("Inside timeout"); // async — fires later
}, 2000);
console.log("After");
// Before → After → Inside timeout (after 2s)
```

The callback is stored by the Web API, then pushed to the Callback Queue after the delay. The Event Loop moves it to the Call Stack when the stack is empty.

#### Event Listeners

Event listeners attach callbacks to DOM elements and fire when the event occurs:

```javascript
document.getElementById("btn").addEventListener("click", function() {
  console.log("Button clicked!");
});
```

#### Closures with Event Listeners

```javascript
function attachCounter() {
  var count = 0; // private state via closure
  document.getElementById("btn").addEventListener("click", function() {
    count++;
    console.log("Clicked " + count + " times");
  });
}
attachCounter();
```

Each click increments `count` — the listener callback closes over it and keeps it alive.

#### Memory: Remove Event Listeners!

Event listeners form closures → referenced variables **cannot** be garbage collected while the listener is active. This causes memory leaks on pages with many elements.

```javascript
const handler = function() { console.log("clicked"); };

element.addEventListener("click", handler);
// Later, when no longer needed:
element.removeEventListener("click", handler); // frees memory
```

> **Note**: `removeEventListener` requires the **same function reference**. Anonymous inline functions cannot be removed — use named references for long-lived listeners.

### Code Example

```javascript
// 1. Basic callback
function doFirst(callback) {
  console.log("First");
  callback();
}
doFirst(function() { console.log("Second (via callback)"); });

// 2. setTimeout — async callback
setTimeout(function() { console.log("After 2 seconds"); }, 2000);

// 3. Event listener with closure counter
(function() {
  var count = 0;
  document.getElementById("btn").addEventListener("click", function() {
    count++;
    console.log("Click count:", count);
  });
})();
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "Callbacks are always asynchronous" | ❌ `map`, `filter`, `forEach` use synchronous callbacks. Only Web API callbacks (timers, events) are async |
| "Anonymous event listeners can be removed easily" | ❌ `removeEventListener` requires the same reference — anonymous functions can't be referenced again |
| "Event listeners clean themselves up" | ❌ They persist until explicitly removed with `removeEventListener`, holding memory via closures |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;">

- **Q: What is a callback function?**
  - A: A function passed as an argument to another function, to be invoked later — either synchronously (e.g., `map`) or after an async operation completes (e.g., `setTimeout`).

- **Q: How do callbacks enable asynchronous behavior?**
  - A: When an async operation completes, the browser places the callback into the Callback Queue. The Event Loop moves it to the Call Stack when the stack is empty — the main thread stays free while waiting.

- **Q: Why should you remove event listeners?**
  - A: Event listeners form closures — they keep referenced variables in memory permanently. Removing them with `removeEventListener` allows GC to free the memory.

- **Q: Why are anonymous functions a problem for `removeEventListener`?**
  - A: `removeEventListener` requires the same function reference. An anonymous inline function can't be referenced again, so the listener can never be removed.
  </div>
</details>
</div>

### Key Takeaways

- A callback = function passed as argument, called later
- Callbacks give JS access to the async world (timers, events, fetch)
- Event listeners use callbacks and often form closures to maintain state
- Closures in event listeners keep variables alive — cannot be GC'd while active
- Always `removeEventListener` when done — use named references, not anonymous functions
- Heavy unremoved listeners (scroll, click, mousemove) on many elements → page slowdown

---

# Part V — Async JavaScript & Engine Internals

---

<a id="chapter-15--asynchronous-js--event-loop"></a>

## Chapter 15 — Asynchronous JS & Event Loop &nbsp; <sup>[⬆ Back to Menu](#part-5)</sup>

### What is the Event Loop?

The **Event Loop** is JS's coordinator — it continuously checks if the Call Stack is empty and whether there's work in the queues. It moves callbacks from the **Microtask Queue** (higher priority) and **Callback Queue** (lower priority) to the Call Stack for execution.

### How It Works

#### The Browser Runtime Environment

The JS engine alone has only the Call Stack + Memory Heap. The **browser** adds:

| Component | Purpose |
|-----------|---------|
| **Web APIs** | `setTimeout`, `fetch`, DOM APIs, `console`, `localStorage`, Geolocation |
| **Callback Queue** (Task Queue) | Holds callbacks from `setTimeout`, DOM events |
| **Microtask Queue** | Holds Promise `.then()`, `queueMicrotask()`, `MutationObserver` callbacks |
| **Event Loop** | Coordinator that moves items from queues → Call Stack |

> Web APIs are NOT part of JavaScript — they're browser superpowers exposed via the `window` object.

#### Step-by-Step: How Async Code Runs

```javascript
console.log("Start");

setTimeout(function cb() {
  console.log("Timer callback");
}, 5000);

console.log("End");
```

| Step | What Happens |
|------|-------------|
| 1 | GEC pushed to Call Stack |
| 2 | `console.log("Start")` → prints "Start" |
| 3 | `setTimeout(cb, 5000)` → delegates to Web API; timer starts |
| 4 | `console.log("End")` → prints "End" |
| 5 | GEC popped — Call Stack empty |
| 6 | After 5000ms, Web API moves `cb` to Callback Queue |
| 7 | Event Loop: stack empty + queue has `cb` → pushes `cb` to stack |
| 8 | `cb` executes → prints "Timer callback" → popped |

**Output:** `Start` → `End` → `Timer callback` (after 5s)

#### Callback Queue vs Microtask Queue

| Queue | Contents | Priority |
|-------|----------|----------|
| **Microtask Queue** | Promise `.then()`/`.catch()`/`.finally()`, `queueMicrotask()`, `MutationObserver` | 🔴 **Higher** — drained completely first |
| **Callback Queue** | `setTimeout`/`setInterval`, DOM event callbacks | 🔵 **Lower** — one item per Event Loop tick |

```javascript
console.log("Start");

setTimeout(function() {
  console.log("setTimeout");
}, 0);

Promise.resolve().then(function() {
  console.log("Promise");
});

console.log("End");

// Output:
// Start
// End
// Promise      ← microtask (higher priority)
// setTimeout   ← callback queue (lower priority)
```

#### Starvation

If microtasks continuously create more microtasks, the Callback Queue **never** gets a turn → **starvation**. Task Queue callbacks starve because microtasks never stop.

### Code Example

```javascript
// Full priority demonstration
console.log("1 - Script start");

setTimeout(function() {
  console.log("4 - setTimeout (0ms)");
}, 0);

Promise.resolve()
  .then(function() {
    console.log("3 - Promise.then");
  });

console.log("2 - Script end");

// Output:
// 1 - Script start
// 2 - Script end
// 3 - Promise.then    (microtask — higher priority)
// 4 - setTimeout (0ms) (callback queue — lower priority)
```

```javascript
// fetch uses microtask queue for .then()
fetch("https://api.example.com/data")
  .then(response => response.json())  // microtask queue
  .then(data => console.log(data));   // microtask queue
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "JS handles async on its own" | ❌ JS is single-threaded — async is handled by Web APIs provided by the browser/Node.js |
| "`setTimeout` and Promises have the same queue priority" | ❌ Promise callbacks go to the Microtask Queue (higher priority); `setTimeout` goes to the Callback Queue (lower) |
| "The Event Loop is part of the JS engine" | ❌ The Event Loop is part of the browser/runtime environment, not the JS engine itself |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;">

- **Q: What is the Event Loop?**
  - A: A continuously running mechanism that checks if the Call Stack is empty, then moves items from the Microtask Queue (first) and Callback Queue to the Call Stack for execution.

- **Q: What is the difference between the Callback Queue and Microtask Queue?**
  - A: Microtask Queue has higher priority (Promise callbacks, MutationObserver). Callback Queue has lower priority (`setTimeout`, DOM events). The Event Loop drains all microtasks before processing one callback.

- **Q: What is starvation?**
  - A: When microtasks continuously generate more microtasks, preventing the Callback Queue from ever being processed.

- **Q: Can `setTimeout(fn, 0)` guarantee immediate execution?**
  - A: No. The callback goes to the Callback Queue and runs only after: current sync code finishes, Call Stack is empty, and all microtasks are drained.
  </div>
</details>
</div>

### Key Takeaways

- JS is single-threaded — the browser provides Web APIs for async operations
- Web APIs handle async work off the main thread; push callbacks to queues when done
- **Microtask Queue**: Promise callbacks — **higher priority**, drained completely first
- **Callback Queue**: `setTimeout`/event callbacks — **lower priority**
- Event Loop: stack empty → drain all microtasks → take one task from Callback Queue
- Starvation: infinite microtasks prevent the Callback Queue from ever running
- `setTimeout(fn, 0)` defers to after sync code + all microtasks

---

<a id="chapter-16--js-engine--v8-architecture"></a>

## Chapter 16 — JS Engine & V8 Architecture &nbsp; <sup>[⬆ Back to Menu](#part-5)</sup>

### What is the JS Engine?

The JS engine is **software** (not hardware) that takes JavaScript source code and produces machine code. V8 (Chrome/Node.js) is written in C++. It lives inside the **JavaScript Runtime Environment (JRE)**, which also includes Web APIs, the Event Loop, and queues.

### How It Works

#### JavaScript Runtime Environment (JRE)

```
JRE = JS Engine + APIs + Event Loop + Callback Queue + Microtask Queue
```

| Environment | Engine | APIs |
|-------------|--------|------|
| Chrome / Node.js | **V8** | Web APIs / Node APIs |
| Firefox | **SpiderMonkey** | Web APIs |
| Safari | **JavaScriptCore** (Nitro) | Web APIs |

#### The 3 Steps: Parsing → Compilation → Execution

```
Source Code → Parser → AST → Ignition (Interpreter) → Bytecode → Execute
                                  ↓
                          TurboFan (Compiler) — watches hot paths
                                  ↓
                        Optimized Machine Code → Execute (faster)
```

**Step 1 — Parsing:**
1. **Tokenization (Lexical Analysis):** Code → tokens (`let`, `a`, `=`, `7`)
2. **Syntax Parsing:** Tokens → **AST** (Abstract Syntax Tree) — a tree representing program structure

**Step 2 — JIT Compilation (Just-In-Time):**
- **Ignition** (Interpreter): AST → bytecode; starts executing immediately (fast startup)
- **TurboFan** (Compiler): Monitors execution; compiles frequently-run ("hot") code paths into optimized machine code (fast peak performance)
- **Deoptimization**: If assumptions become invalid (e.g., type change), V8 falls back to interpreted code

**Step 3 — Execution:**
- **Memory Heap**: Stores objects, variables, functions
- **Call Stack**: Manages execution order (LIFO)

#### Garbage Collection — Mark and Sweep

V8's **Orinoco** garbage collector uses **Mark and Sweep**:

| Phase | Action |
|-------|--------|
| **Mark** | Traverse from root references → mark all reachable objects as "alive" |
| **Sweep** | Free memory of all unmarked (unreachable) objects |

#### V8 Components Summary

| Component | Role |
|-----------|------|
| **Parser** | Tokenization + AST generation |
| **Ignition** | Interpreter — AST → bytecode, starts execution |
| **TurboFan** | Optimizing compiler — hot code → machine code |
| **Orinoco** | Garbage collector (Mark and Sweep) |
| **Memory Heap** | Object/variable storage |
| **Call Stack** | Function call management (LIFO) |

### Code Example

```javascript
// Type stability helps V8 optimize — TurboFan loves predictable types

// GOOD — stable types allow TurboFan optimization
function addNumbers(a, b) {
  return a + b;
}
addNumbers(1, 2);      // V8 sees: always numbers
addNumbers(3, 4);      // optimizes for number addition
addNumbers(100, 200);  // fast path!

// BAD — type change causes deoptimization
addNumbers("hello", "world"); // string concatenation
// V8 deoptimizes — falls back to generic handler
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "The JS engine is hardware/a chip" | ❌ It's software written in C++ (V8) or other languages |
| "JavaScript is purely interpreted" | ❌ Modern engines use JIT — a hybrid of interpretation and compilation |
| "Garbage collection must be triggered manually" | ❌ V8's Orinoco GC runs automatically — unreachable objects are freed without developer intervention |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;">

- **Q: What is a JavaScript Runtime Environment?**
  - A: The JRE is a container that enables JS to run. It includes the JS engine, Web/Node APIs, Event Loop, and queues. Different environments have different JREs but all execute ECMAScript-compliant JS.

- **Q: What is JIT compilation?**
  - A: Just-In-Time compilation combines interpretation and compilation. The interpreter starts executing immediately; the compiler monitors execution and optimizes hot code paths into efficient machine code at runtime.

- **Q: What is an AST?**
  - A: An Abstract Syntax Tree — a tree-structured representation of source code generated by the parser. It's handed to the interpreter/compiler for code generation.

- **Q: What are Ignition and TurboFan?**
  - A: Ignition is V8's interpreter (AST → bytecode, starts execution). TurboFan is V8's optimizing compiler (hot code → machine code for speed).

- **Q: What is Mark and Sweep?**
  - A: V8's garbage collection algorithm. It marks all reachable objects from roots, then sweeps (frees) all unreachable objects.
  </div>
</details>
</div>

### Key Takeaways

- JRE = JS engine + APIs + Event Loop + queues — different per environment
- The JS engine is **software** (C++), not hardware
- Parsing: tokenization → AST (structural blueprint)
- JIT = Interpreter (fast start) + Compiler (optimized hot paths)
- V8: Parser → Ignition → TurboFan → Orinoco (GC)
- Type-stable code helps TurboFan optimize; type changes → deoptimization
- Mark and Sweep GC frees unreachable objects automatically

---

<a id="chapter-17--trust-issues-with-settimeout"></a>

## Chapter 17 — Trust Issues with `setTimeout` &nbsp; <sup>[⬆ Back to Menu](#part-5)</sup>

### What are the Trust Issues?

`setTimeout(fn, delay)` guarantees a **minimum** delay, not an exact one. The callback can't run until the Call Stack is empty — if the main thread is blocked with synchronous work, timers fire late. **The #1 rule of JS: never block the main thread.**

### How It Works

#### What `setTimeout` Actually Guarantees

```
Actual delay ≥ Specified delay
```

The timer counts down correctly in the Web API. But once it expires, the callback goes to the Callback Queue and must **wait** for:
1. Current synchronous code to finish
2. Call Stack to be empty
3. All microtasks to be drained

#### The Blocking Problem

```javascript
console.log("Start");

setTimeout(function() {
  console.log("Callback"); // should fire after 2s
}, 2000);

// Blocking for 10 seconds
let start = Date.now();
while (Date.now() - start < 10000) { /* busy wait */ }

console.log("End");
```

**Output:**
```
Start
End          ← after ~10 seconds (blocked!)
Callback     ← fires immediately after "End" — ~10s total, NOT 2s!
```

The timer expired at 2s, but the callback waited in the queue for 8 more seconds because the main thread was busy.

#### `setTimeout(fn, 0)` — Zero Delay

Even 0ms doesn't mean "immediate":

```javascript
console.log("A");
setTimeout(function() { console.log("B"); }, 0);
console.log("C");
// Output: A → C → B
```

The callback still goes through Web API → Callback Queue → Event Loop → Call Stack.

#### Real-World Solutions for Heavy Work

| Scenario | Solution |
|----------|----------|
| Heavy computation in browser | **Web Workers** (separate thread) |
| Large data loops | Break into chunks with `setTimeout(fn, 0)` |
| Synchronous file/image processing | Use async APIs |
| Many DOM updates in a loop | `requestAnimationFrame` or batching |

### Code Example

```javascript
console.log("Start");

setTimeout(function cb() {
  console.log("Callback — fired after setTimeout");
}, 5000);

// Blocking for 10 seconds
console.log("Blocking starts");
let endTime = Date.now() + 10000;
while (Date.now() < endTime) { /* blocking main thread */ }
console.log("Blocking ends");

// Output:
// Start
// Blocking starts
// Blocking ends          (after ~10 seconds)
// Callback — fired       (immediately after — ~10s, not 5s!)
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "`setTimeout(fn, 1000)` fires in exactly 1000ms" | ❌ It guarantees a **minimum** delay — actual time depends on Call Stack availability |
| "`setTimeout(fn, 0)` means immediate" | ❌ It's still deferred — runs after sync code + microtasks |
| "Timers are part of the JS engine" | ❌ Timers are a **Web API** — the browser counts down, not the JS engine |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;">

- **Q: Does `setTimeout(fn, 1000)` guarantee execution after exactly 1000ms?**
  - A: No. It guarantees the callback won't fire **before** 1000ms. Actual time = delay + time waiting for the Call Stack to clear.

- **Q: What happens to a `setTimeout` callback when the main thread is blocked?**
  - A: The timer counts down correctly in the Web API. When it expires, the callback moves to the Callback Queue. But it can only run after the Call Stack becomes empty — so it waits.

- **Q: What does `setTimeout(fn, 0)` do?**
  - A: Defers `fn` with a 0ms minimum delay. It executes only after all synchronous code and all microtasks (Promises) finish.

- **Q: How can you handle CPU-intensive work without blocking the main thread?**
  - A: Use **Web Workers** (separate thread), break work into chunks with `setTimeout(fn, 0)`, or use `requestAnimationFrame` for DOM updates.
  </div>
</details>
</div>

### Key Takeaways

- `setTimeout` provides a **minimum** delay guarantee — not a precise one
- Callback waits in the Callback Queue until the Call Stack is empty
- Blocking the main thread delays **all** pending timers and event callbacks
- `setTimeout(fn, 0)` still defers — sync code and microtasks run first
- **Golden rule: never block the main thread** — keep synchronous operations fast
- For heavy work: Web Workers; for DOM batching: `requestAnimationFrame`

---

# Part VI — Functional Programming

---

<a id="chapter-18--higher-order-functions--functional-programming"></a>

## Chapter 18 — Higher-Order Functions & Functional Programming &nbsp; <sup>[⬆ Back to Menu](#part-6)</sup>

### What is a Higher-Order Function?

A **Higher-Order Function (HOF)** takes one or more functions as arguments, or returns a function as its result. HOFs abstract over **behavior**, not just data — they're the cornerstone of functional programming.

### How It Works

#### HOF — Takes a Function as Argument

```javascript
function doTwice(fn) {
  fn();
  fn();
}
doTwice(function() { console.log("Hello!"); });
// Hello!
// Hello!
```

#### HOF — Returns a Function

```javascript
function multiplier(factor) {
  return function(number) { return number * factor; };
}
const double = multiplier(2);
const triple = multiplier(3);
console.log(double(5)); // 10
console.log(triple(5)); // 15
```

#### Imperative vs Functional

**Imperative** — describes *how* step by step:
```javascript
const radius = [3, 1, 2, 4];
const areas = [];
for (let i = 0; i < radius.length; i++) {
  areas.push(Math.PI * radius[i] * radius[i]);
}
```

**Functional** — describes *what*, delegates *how* to the HOF:
```javascript
const area = (r) => Math.PI * r * r;
const areas = radius.map(area); // behavior passed to HOF
```

The math is now reusable, testable in isolation, and the intent is clear.

#### Principles of Functional Programming

| Principle | Description |
|-----------|-------------|
| **Pure functions** | Same input → same output; no side effects |
| **Immutability** | Don't modify existing data — create new values |
| **Declarative style** | Express *what* you want, not *how* |
| **Composition** | Combine small functions to build complex behavior |

```javascript
// Pure — no side effects, deterministic
function add(a, b) { return a + b; }

// Impure — modifies external state
let count = 0;
function increment() { count++; }
```

#### Building Your Own HOF

```javascript
Array.prototype.calculate = function(logic) {
  const output = [];
  for (let i = 0; i < this.length; i++) {
    output.push(logic(this[i]));
  }
  return output;
};

const radius = [3, 1, 2, 4];
const area = (r) => Math.PI * r * r;
const circumference = (r) => 2 * Math.PI * r;

console.log(radius.calculate(area));
console.log(radius.calculate(circumference));
// This is exactly how Array.prototype.map works internally
```

### Code Example

```javascript
const radius = [3, 1, 2, 4];

// Imperative — repeated logic, only formula changes
function getArea(arr) {
  const output = [];
  for (let i = 0; i < arr.length; i++) output.push(Math.PI * arr[i] * arr[i]);
  return output;
}

function getCircumference(arr) {
  const output = [];
  for (let i = 0; i < arr.length; i++) output.push(2 * Math.PI * arr[i]);
  return output;
}
// Problem: repeated iteration logic!

// Functional — extract varying behavior
const area = (r) => Math.PI * r * r;
const circumference = (r) => 2 * Math.PI * r;
const diameter = (r) => 2 * r;

function calculate(arr, logic) {
  return arr.map(logic);
}

console.log(calculate(radius, area));
console.log(calculate(radius, circumference));
console.log(calculate(radius, diameter));
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "HOFs are complex and only for advanced developers" | ❌ `map`, `filter`, `forEach`, `setTimeout` are all HOFs — you already use them daily |
| "Functional and imperative can't coexist" | ❌ JS is multi-paradigm — you mix both styles freely |
| "Pure functions can read external state" | ❌ A pure function depends **only** on its inputs — reading external state makes it impure |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;">

- **Q: What is a Higher-Order Function?**
  - A: A function that takes other functions as arguments, or returns a function. Examples: `map`, `filter`, `reduce`, `setTimeout`, `addEventListener`.

- **Q: What is the benefit of higher-order functions?**
  - A: They abstract over behavior — instead of writing specialized loops for every operation, you write one generic HOF that accepts behavior as a parameter. Reduces repetition, improves readability, enables composition.

- **Q: What is a pure function?**
  - A: A function that always returns the same output for the same input and has no side effects (no external state modification, no I/O).

- **Q: How does functional programming differ from imperative?**
  - A: Imperative describes *how* (explicit loops, mutations). Functional describes *what* (using `map`/`filter`/`reduce`), delegating the *how* to HOFs. Functional code is more declarative and composable.
  </div>
</details>
</div>

### Key Takeaways

- HOF = takes a function as argument, returns a function, or both
- HOFs abstract over **behavior** — the "how" is the HOF, the "what" is the passed function
- Functional programming: pure functions, immutability, declarative style, composition
- Built-in HOFs: `map`, `filter`, `reduce`, `forEach`, `find`, `some`, `every`
- Separating logic from iteration → highly reusable, composable code
- Build your own HOFs to understand `map`/`filter`/`reduce` internally

---

<a id="chapter-19--map-filter--reduce"></a>

## Chapter 19 — `map`, `filter` & `reduce` &nbsp; <sup>[⬆ Back to Menu](#part-6)</sup>

### What are `map`, `filter`, and `reduce`?

Three essential HOFs on `Array.prototype`. **`map`** transforms each element, **`filter`** selects elements by condition, **`reduce`** accumulates all elements into a single value. All return new values — the original array is never mutated.

### How It Works

#### `map` — Transform Each Element

```
[a, b, c]  →  map(fn)  →  [fn(a), fn(b), fn(c)]
```

Returns a new array of the **same length**. Each element is `fn(original)`.

```javascript
const arr = [1, 2, 3, 4, 5];
const doubled = arr.map(x => x * 2);
console.log(doubled); // [2, 4, 6, 8, 10]
console.log(arr);     // [1, 2, 3, 4, 5] — unchanged
```

#### `filter` — Select by Condition

```
[a, b, c]  →  filter(fn)  →  [elements where fn(x) is truthy]
```

Returns a new array with **only** elements that pass the test (possibly shorter).

```javascript
const arr = [1, 2, 3, 4, 5, 6, 7, 8];
const evens = arr.filter(x => x % 2 === 0);
console.log(evens); // [2, 4, 6, 8]
```

#### `reduce` — Accumulate to a Single Value

```
[a, b, c]  →  reduce(fn, initial)  →  single value
```

Takes a reducer `(accumulator, current) => newAccumulator` and an optional initial value. Returns **one** value of any type.

```javascript
const arr = [1, 2, 3, 4, 5];
const sum = arr.reduce((acc, curr) => acc + curr, 0);
console.log(sum); // 15
```

#### Comparison Table

| Method | Returns | Purpose |
|--------|---------|---------|
| `map` | New array (same length) | Transform each element |
| `filter` | New array (≤ original length) | Select elements matching condition |
| `reduce` | Single value (any type) | Accumulate into one result |

#### Chaining

```javascript
const users = [
  { firstName: "Akshad", age: 21 },
  { firstName: "Jarad", age: 22 },
  { firstName: "Arijit", age: 33 },
  { firstName: "Tupac", age: 25 }
];

// Get names of users under 30
const under30Names = users
  .filter(user => user.age < 30)
  .map(user => user.firstName);

console.log(under30Names); // ["Akshad", "Jarad", "Tupac"]
```

#### `reduce` Can Replace Both

```javascript
// filter + map using only reduce
const names = users.reduce((acc, curr) => {
  if (curr.age < 30) acc.push(curr.firstName);
  return acc;
}, []);
// ["Akshad", "Jarad", "Tupac"]
```

### Code Example

```javascript
const arr = [5, 1, 8, 7, 4];

// map — transform
console.log(arr.map(x => x * 2));          // [10, 2, 16, 14, 8]
console.log(arr.map(x => x.toString(2)));  // ['101','1','1000','111','100']

// filter — select
console.log(arr.filter(x => x % 2 !== 0)); // [5, 1, 7]
console.log(arr.filter(x => x > 4));       // [5, 8, 7]

// reduce — accumulate
const sum = arr.reduce((acc, curr) => acc + curr, 0);
console.log(sum); // 25

const max = arr.reduce((acc, curr) => acc < curr ? curr : acc, 0);
console.log(max); // 8

// reduce with objects — group by age
const users = [
  { firstName: "Akshad", age: 21 },
  { firstName: "Jarad", age: 22 },
  { firstName: "Arijit", age: 33 },
  { firstName: "Tupac", age: 25 }
];

const ageCount = users.reduce((acc, curr) => {
  acc[curr.age] = (acc[curr.age] || 0) + 1;
  return acc;
}, {});
console.log(ageCount); // { 21: 1, 22: 1, 33: 1, 25: 1 }
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "`map` can return a shorter array" | ❌ `map` always returns the same length. Use `filter` to remove elements |
| "`reduce` only works with numbers" | ❌ `reduce` can accumulate to any type: objects, arrays, strings, booleans |
| "These methods mutate the original array" | ❌ `map`, `filter`, `reduce` all return **new** values — original is unchanged |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;">

- **Q: What does `map` return?**
  - A: A new array of the same length, where each element is the result of calling the provided function on the corresponding original element. The original array is not modified.

- **Q: What is the difference between `map` and `filter`?**
  - A: `map` transforms every element → same-length array. `filter` selects elements by condition → possibly shorter array.

- **Q: What does the `reduce` accumulator do?**
  - A: Carries the "running total" across iterations. Each call receives the current accumulator and current element, returns the new accumulator value. The final accumulator is returned.

- **Q: When should you use `reduce` over `map` + `filter`?**
  - A: When you need a non-array result (sum, max, count, object grouping), or when chaining `filter` + `map` would iterate twice and you want a single pass.
  </div>
</details>
</div>

### Key Takeaways

- `map`: transform each element → new array of same length
- `filter`: keep elements matching a predicate → new array (possibly shorter)
- `reduce`: accumulate all elements → single value of any type
- All three return new values — original array is **never** mutated
- Chain them: `array.filter(...).map(...)` for multi-step transformations
- `reduce` is the most flexible — can implement `map` and `filter`
- Prefer `map`/`filter`/`reduce` over `for` loops for cleaner, declarative code

---

# Part VII — Promises & Async Patterns

---

<a id="chapter-20--callback-hell"></a>

## Chapter 20 — Callback Hell &nbsp; <sup>[⬆ Back to Menu](#part-7)</sup>

### What is Callback Hell?

**Callback Hell** (Pyramid of Doom) is the pattern where multiple sequential async operations result in deeply nested callbacks. The code grows rightward, becoming impossible to read and maintain. It exposed two fundamental problems with callbacks that motivated Promises.

### How It Works

#### The Good: Callbacks Are Essential

Callbacks are the foundation of async JS — used everywhere: `setTimeout`, `addEventListener`, `fetch`. A simple callback is perfectly fine:

```javascript
setTimeout(function() {
  console.log("async after 1 second");
}, 1000);
```

#### Problem 1: Callback Hell (Pyramid of Doom)

Sequential async operations that depend on each other force callbacks inside callbacks:

```javascript
// E-commerce order flow
createOrder(cart, function(orderId) {
  proceedToPayment(orderId, function(paymentInfo) {
    showOrderSummary(paymentInfo, function(balance) {
      updateWalletBalance(balance, function() {
        sendConfirmationEmail(function() {
          console.log("Order complete");
          // >>>>>> — grows rightward like a pyramid!
        });
      });
    });
  });
});
```

Problems:
- Grows **horizontally** (not vertically)
- Hard to follow, maintain, or debug
- Error handling becomes a nightmare

#### Problem 2: Inversion of Control

When you pass a callback to a third-party function, **you surrender control** over when, how, and how many times it is invoked. You trust the receiving function — a trust that can be violated:

```javascript
// What if createOrder calls the callback twice?
// What if it never calls it?
// What if it passes the wrong orderId?
createOrder(cart, function(orderId) {
  proceedToPayment(orderId);
});
```

Risks of Inversion of Control:
- Callback called **0, 1, or many** times
- Called with **wrong arguments**
- Errors silently **swallowed**

### Code Example

```javascript
// Simulated async API functions
function createOrder(cart, callback) {
  const orderId = "ORD123";
  callback(orderId);
}
function proceedToPayment(orderId, callback) {
  callback({ success: true, orderId });
}
function showOrderSummary(paymentInfo, callback) {
  console.log("Summary:", paymentInfo);
  callback();
}

// The Pyramid of Doom
createOrder(["shoes", "shirt"], function(orderId) {
  console.log("Order created:", orderId);
  proceedToPayment(orderId, function(paymentInfo) {
    console.log("Payment done:", paymentInfo);
    showOrderSummary(paymentInfo, function() {
      console.log("Summary shown — order complete");
    });
  });
});
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "Callbacks are the problem" | ❌ Simple callbacks are fine. The problem is sequential, dependent async ops with deeply nested callbacks |
| "Just name the callbacks to flatten them" | ⚠️ Helps readability but doesn't solve Inversion of Control |
| "This only happens with third-party code" | ❌ IoC can happen with any function you hand a callback to |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;">

- **Q: What is callback hell?**
  - A: Callback hell (Pyramid of Doom) is a pattern where sequential async operations result in deeply nested callbacks. Code grows horizontally and becomes difficult to read, maintain, and debug.

- **Q: What is inversion of control?**
  - A: IoC occurs when you pass a callback to another function (especially third-party), surrendering control over when/how/how often your callback runs. You trust the receiving function to call it correctly — a trust that may be violated.

- **Q: How does callback hell differ from simply using callbacks?**
  - A: Simple callbacks (setTimeout, event listeners) are fine. Callback hell specifically refers to nesting callbacks for sequential, dependent async operations. The problem is the structure, not callbacks themselves.

- **Q: What solutions exist for callback hell and IoC?**
  - A: Promises (ES6) and async/await (ES2017). Promises return an object representing the future result — you chain `.then()` instead of nesting, and the Promise API (not third-party code) calls your handler exactly once.
  </div>
</details>
</div>

### Key Takeaways

- Callbacks are essential for async JS — the problem is sequential, dependent operations
- Callback Hell = nested callbacks → Pyramid of Doom → code grows rightward
- Inversion of Control = surrendering callback execution to another function
- IoC risks: callback called 0 or many times, wrong args, errors swallowed
- **Promises** solve both problems — introduced in Chapter 21

---

<a id="chapter-21--promises"></a>

## Chapter 21 — Promises &nbsp; <sup>[⬆ Back to Menu](#part-7)</sup>

### What is a Promise?

A **Promise** is an object representing the eventual completion or failure of an async operation. It serves as a **placeholder for a future value** and comes with guaranteed, predictable behavior — solving both Callback Hell and Inversion of Control.

### How It Works

#### The Three States

```
pending  →  fulfilled (has a resolved value)
         →  rejected  (has a reason/error)
```

Once settled (fulfilled or rejected), a Promise **never changes state** — it's immutable.

| State | Description | Terminal? |
|-------|-------------|-----------|
| `pending` | Async operation in progress | No |
| `fulfilled` | Resolved with a value | ✅ Yes |
| `rejected` | Failed with a reason | ✅ Yes |

#### How Promises Solve Inversion of Control

With callbacks you hand your function to a third party. With Promises, **the third party returns a Promise** and you attach your handler yourself via `.then()`. The Promise API calls your handler — not the third party.

```javascript
// Callback — third party controls the callback
createOrder(cart, function(orderId) { /* createOrder decides when/if this runs */ });

// Promise — YOU control what happens with the result
const orderPromise = createOrder(cart); // returns a promise
orderPromise.then(function(orderId) {   // YOU attach the handler
  proceedToPayment(orderId);            // Promise API calls this exactly once
});
```

#### How Promises Solve Callback Hell

Instead of nesting, Promises **chain** — flat and readable:

```javascript
createOrder(cart)
  .then(orderId => proceedToPayment(orderId))
  .then(paymentInfo => showOrderSummary(paymentInfo))
  .then(() => updateWalletBalance())
  .catch(err => console.error("Failed:", err));
```

#### Creating Promises

```javascript
const promise = new Promise(function(resolve, reject) {
  // async operation here
  const success = true;
  if (success) {
    resolve("Data loaded!"); // fulfills the promise
  } else {
    reject(new Error("Failed to load")); // rejects the promise
  }
});
```

The function passed to `new Promise()` is the **executor**. It receives:
- `resolve(value)` — fulfills with `value`
- `reject(reason)` — rejects with `reason`

#### Consuming Promises

```javascript
promise
  .then(value => console.log(value))       // fulfilled handler
  .catch(error => console.error(error))    // rejection handler
  .finally(() => console.log("settled"));  // always runs
```

#### Promise Guarantees

1. `.then()` handlers are **always called asynchronously** (Microtask Queue)
2. Handlers are called **exactly once**
3. Handlers added after the Promise settles **still get called**
4. Multiple `.then()` can be chained

### Code Example

```javascript
function getOrderId(cart) {
  return new Promise(function(resolve, reject) {
    setTimeout(() => {
      if (cart.length > 0) {
        resolve("ORDER_456");
      } else {
        reject(new Error("Cart is empty"));
      }
    }, 1000);
  });
}

getOrderId(["shoes", "shirt"])
  .then(function(orderId) {
    console.log("Order created:", orderId);
    return new Promise(resolve => setTimeout(() => resolve({ orderId, paid: true }), 500));
  })
  .then(function(paymentInfo) {
    console.log("Payment done:", paymentInfo);
  })
  .catch(function(error) {
    console.error("Error:", error.message);
  });
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "A Promise is guaranteed to succeed" | ❌ A Promise can be rejected — always handle `.catch()` |
| "Promises are synchronous" | ❌ `.then()` handlers always run asynchronously via the Microtask Queue |
| "A Promise can change state multiple times" | ❌ Once settled (fulfilled or rejected), the state is immutable |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;">

- **Q: What is a Promise in JavaScript?**
  - A: An object representing the eventual completion or failure of an async operation. It's a placeholder for a future value with three states: pending, fulfilled, or rejected. Once settled, the state never changes.

- **Q: How does a Promise solve Inversion of Control?**
  - A: With callbacks, you hand your function to a third party. With Promises, the third party returns a Promise — you attach your handler via `.then()`. The Promise API (not the third party) invokes it exactly once.

- **Q: What are the three states of a Promise?**
  - A: `pending` (initial), `fulfilled` (resolved with a value), `rejected` (failed with a reason). Fulfilled and rejected are terminal — state never changes after settling.

- **Q: What is the difference between `resolve` and `reject`?**
  - A: `resolve(value)` fulfills the Promise — `.then()` receives `value`. `reject(reason)` rejects it — `.catch()` receives `reason`.
  </div>
</details>
</div>

### Key Takeaways

- A Promise = placeholder for a future async value
- Three states: `pending` → `fulfilled` or `rejected` (immutable once settled)
- Solves IoC: `.then()` called by Promise API, not third-party code — exactly once
- Solves Callback Hell: flat `.then()` chaining vs nested callbacks
- Create: `new Promise((resolve, reject) => {...})`
- Consume: `.then(fn)`, `.catch(fn)`, `.finally(fn)`
- Handlers always run asynchronously (Microtask Queue)

---

<a id="chapter-22--promise-chaining--error-handling"></a>

## Chapter 22 — Promise Chaining & Error Handling &nbsp; <sup>[⬆ Back to Menu](#part-7)</sup>

### What is Promise Chaining?

Promise chaining converts nested callbacks into a flat, readable sequential flow. Each `.then()` can return a value or Promise, which the next `.then()` receives. Rejection **skips all `.then()` handlers** and propagates to the nearest `.catch()`.

### How It Works

#### The Golden Rule: Always `return`

If you don't `return` from a `.then()`, the next step gets `undefined`:

```javascript
// ❌ WRONG — no return
createOrder(cart)
  .then(function(orderId) {
    proceedToPayment(orderId); // not returned!
  })
  .then(function(paymentInfo) {
    console.log(paymentInfo); // undefined!
  });

// ✅ CORRECT — always return
createOrder(cart)
  .then(function(orderId) {
    return proceedToPayment(orderId); // returned!
  })
  .then(function(paymentInfo) {
    console.log(paymentInfo); // correct value
  });
```

#### `.catch()` Placement Matters

**End of chain** — catches all rejections:
```javascript
step1()
  .then(() => step2())
  .then(() => step3())
  .catch(err => console.error("Something failed:", err));
```

**Middle of chain** — partial recovery, chain continues:
```javascript
step1()
  .then(() => step2())
  .catch(err => {
    console.error("Handled:", err);
    // returns undefined → chain CONTINUES to next .then()
  })
  .then(() => step3()); // runs even if step2 rejected (if .catch recovered)
```

#### Rejection Propagation

Rejection **skips all `.then()` handlers** until it finds a `.catch()`:

```javascript
Promise.reject(new Error("Step 1 failed"))
  .then(() => { console.log("Step 2"); }) // SKIPPED
  .then(() => { console.log("Step 3"); }) // SKIPPED
  .catch(err => console.error(err.message)); // "Step 1 failed"
```

#### Rethrowing Errors

In a `.catch()`, you can rethrow to prevent recovery:

```javascript
.catch(function(err) {
  if (err.type === 'network') {
    return fallbackData; // recoverable — chain continues
  }
  throw err; // not recoverable — keeps propagating
})
```

#### `.finally()` — Always Runs

`.finally()` runs regardless of success or failure — ideal for cleanup:

```javascript
showLoadingSpinner();
fetchData()
  .then(data => displayData(data))
  .catch(err => showError(err))
  .finally(() => hideLoadingSpinner()); // always runs
```

### Code Example

```javascript
function createOrder(cart) {
  return new Promise((resolve, reject) => {
    if (!cart || cart.length === 0) reject(new Error("Cart is empty"));
    setTimeout(() => resolve("ORDER_" + Date.now()), 500);
  });
}
function proceedToPayment(orderId) {
  return new Promise(resolve => {
    setTimeout(() => resolve({ orderId, amount: 99.99, paid: true }), 500);
  });
}
function showOrderSummary(paymentInfo) {
  return new Promise(resolve => {
    console.log("Summary:", paymentInfo);
    resolve("Summary shown");
  });
}

createOrder(["shoes", "shirt"])
  .then(orderId => {
    console.log("Order:", orderId);
    return proceedToPayment(orderId); // must return!
  })
  .then(paymentInfo => {
    console.log("Payment:", paymentInfo);
    return showOrderSummary(paymentInfo); // must return!
  })
  .then(msg => console.log(msg))
  .catch(err => console.error("Failed:", err.message))
  .finally(() => console.log("Order flow complete"));
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "Rejection skips `.catch()` too" | ❌ Rejection skips **`.then()`** handlers, not `.catch()` |
| "One `.catch()` at the end is always enough" | ❌ Sometimes you need partial recovery in the middle — placement matters |
| "`.finally()` receives the result value" | ❌ `.finally()` receives no arguments — use `.then()` or `.catch()` for the value |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;">

- **Q: What happens if you don't `return` from a `.then()` handler?**
  - A: The next `.then()` receives `undefined`. The chain doesn't wait for any async operation started in that handler.

- **Q: How does rejection propagate through a Promise chain?**
  - A: Rejection skips all `.then()` handlers until it reaches the nearest `.catch()`. If there's no `.catch()`, it becomes an unhandled rejection.

- **Q: Can you continue a Promise chain after a `.catch()`?**
  - A: Yes. If `.catch()` returns a resolved value or resolved Promise, the chain continues with the next `.then()`. If it throws or returns a rejected Promise, rejection propagates.

- **Q: What is `.finally()` used for?**
  - A: It runs its callback regardless of success or failure — ideal for cleanup (hiding spinners, releasing resources) that must always happen.
  </div>
</details>
</div>

### Key Takeaways

- Always `return` from `.then()` handlers — no return = `undefined` downstream
- `.catch()` at end catches all rejections from all steps above
- `.catch()` in middle allows partial recovery — chain continues if it doesn't rethrow
- Rejection skips `.then()` handlers and falls to the nearest `.catch()`
- Multiple `.catch()` handlers allow granular recovery at different stages
- `.finally()` always runs — use for cleanup, not for values
- Flat Promise chains are far more readable than nested callbacks

---

<a id="chapter-23--async--await"></a>

## Chapter 23 — `async` / `await` &nbsp; <sup>[⬆ Back to Menu](#part-7)</sup>

### What is `async`/`await`?

`async`/`await` is **syntactic sugar over Promises** — it lets you write async code that looks and reads like synchronous code, while remaining fully non-blocking. `async` makes a function return a Promise. `await` suspends the async function (not the JS engine) until a Promise settles.

### How It Works

#### The `async` Keyword

- Makes the function always return a Promise
- Non-Promise returns are auto-wrapped in `Promise.resolve(value)`
- If the function throws, the returned Promise is rejected

```javascript
async function greet() {
  return "Hello!";
}
// Equivalent to:
function greet() {
  return Promise.resolve("Hello!");
}
greet().then(msg => console.log(msg)); // "Hello!"
```

#### The `await` Keyword

- Only usable **inside an `async` function**
- Suspends the function until the awaited Promise settles, then returns the resolved value
- **Does NOT block the JS engine** — other code continues running

```javascript
async function fetchUser() {
  const response = await fetch("https://api.example.com/user"); // suspend
  const user = await response.json(); // suspend again
  return user; // resume when both done
}
```

#### What Actually Happens Behind the Scenes

When `await` is hit:
1. The async function **suspends** — its EC is removed from the Call Stack
2. The JS engine **continues** with other code — not blocked
3. When the awaited Promise settles, the function's continuation is queued in the **Microtask Queue**
4. The Event Loop **resumes** the function from where it left off

```javascript
console.log("Before");

async function example() {
  console.log("Inside async — before await");
  await Promise.resolve(); // suspends → goes to microtask queue
  console.log("Inside async — after await"); // resumes from microtask queue
}

example();
console.log("After");

// Output:
// Before
// Inside async — before await
// After
// Inside async — after await  ← resumed via microtask queue
```

#### Error Handling — `try`/`catch`

```javascript
async function fetchData() {
  try {
    const response = await fetch("https://api.example.com/data");
    if (!response.ok) throw new Error(`HTTP error: ${response.status}`);
    const data = await response.json();
    return data;
  } catch (error) {
    console.error("Fetch failed:", error.message);
    throw error; // rethrow if needed
  }
}
```

#### `async`/`await` vs `.then()` — Both Are Equivalent

```javascript
// Promise chain
function processOrder(cart) {
  return createOrder(cart)
    .then(orderId => proceedToPayment(orderId))
    .then(paymentInfo => showOrderSummary(paymentInfo))
    .catch(err => console.error(err));
}

// Equivalent async/await
async function processOrder(cart) {
  try {
    const orderId = await createOrder(cart);
    const paymentInfo = await proceedToPayment(orderId);
    await showOrderSummary(paymentInfo);
  } catch (err) {
    console.error(err);
  }
}
```

`async`/`await` is preferred because: reads top-to-bottom, same indentation level, standard control flow (`if`, `for`, `try/catch`).

#### Sequential vs Parallel Awaits

```javascript
// Sequential — total ~2s
const a = await fetchA(); // wait ~1s
const b = await fetchB(); // then wait ~1s

// Parallel — total ~1s (concurrent)
const [a, b] = await Promise.all([fetchA(), fetchB()]);
```

### Code Example

```javascript
// async/await with error handling
async function fetchPost(id) {
  try {
    const res = await fetch(`https://jsonplaceholder.typicode.com/posts/${id}`);
    if (!res.ok) throw new Error(`Failed: ${res.status}`);
    const post = await res.json();
    console.log("Title:", post.title);
  } catch (err) {
    console.error("Error:", err.message);
  } finally {
    console.log("Fetch attempt complete");
  }
}
fetchPost(1);

// async IIFE — top-level await workaround
(async () => {
  const data = await fetchPost(2);
  console.log(data);
})();
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "The JS engine waits when `await` is hit" | ❌ Only the async function suspends — the engine continues running other code |
| "`await` can be used outside `async` functions" | ❌ `await` can only be used inside `async` functions (or top-level modules with top-level await) |
| "Sequential `await` is always fine" | ❌ Sequential awaits for independent operations waste time — use `Promise.all` for parallel execution |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;">

- **Q: What does `async` do to a function?**
  - A: Makes the function always return a Promise. Non-Promise returns are wrapped in `Promise.resolve()`. The function can use `await` inside it.

- **Q: Is the JS engine waiting when `await` is encountered?**
  - A: No. The async function is suspended and its EC leaves the Call Stack. The JS engine continues other code. When the awaited Promise settles, the function is resumed via the Microtask Queue.

- **Q: How do you handle errors in `async`/`await`?**
  - A: Use `try`/`catch`/`finally` blocks. The `catch` block receives the rejection reason.

- **Q: What is the difference between `async`/`await` and `.then()` chaining?**
  - A: Functionally equivalent — `async`/`await` is syntactic sugar over Promises. `async`/`await` is preferred for readability: reads like sync code, uses standard control flow, avoids indentation creep.

- **Q: How do you run multiple async operations in parallel?**
  - A: Use `await Promise.all([p1, p2, p3])`. Sequential `await` runs one at a time; `Promise.all` runs concurrently and waits for all to settle.
  </div>
</details>
</div>

### Key Takeaways

- `async` function always returns a Promise — non-Promise values auto-wrapped
- `await` suspends the **function**, not the JS engine — other code keeps running
- Suspended async functions resume via the Microtask Queue
- `async`/`await` = syntactic sugar over Promises — equivalent behavior, cleaner syntax
- Error handling: `try`/`catch`/`finally` (same as synchronous)
- Sequential `await` = serial; `await Promise.all([...])` = parallel
- Prefer `async`/`await` for complex async flows with multiple steps

---

# Part VIII — The `this` Keyword

---

<a id="chapter-24--this-keyword"></a>

## Chapter 24 — The `this` Keyword &nbsp; <sup>[⬆ Back to Menu](#part-8)</sup>

### What is `this`?

`this` is a special keyword whose value is determined **at call time** by how a function is invoked — not by where it's defined. Arrow functions are the exception: they capture `this` lexically from their enclosing scope at definition time.

### How It Works

#### Summary Table — All `this` Rules

| Context | `this` value |
|---------|-------------|
| Global scope (browser) | `window` |
| Regular function (non-strict) | `window` (this substitution) |
| Regular function (strict mode) | `undefined` |
| Object method `obj.fn()` | `obj` |
| `call(thisArg, ...)` | `thisArg` |
| `apply(thisArg, [...])` | `thisArg` |
| `bind(thisArg)` | `thisArg` (permanent — new function) |
| Arrow function | Lexical (enclosing scope's `this`) |
| Class constructor/method | The class instance |
| DOM event handler (regular fn) | The DOM element |

#### Rule 1 — Global Context

```javascript
console.log(this);           // window (browser)
console.log(this === window); // true
```

#### Rule 2 — Regular Function

```javascript
function show() { console.log(this); }
show(); // window (non-strict) or undefined (strict)

'use strict';
function showStrict() { console.log(this); } // undefined
```

**`this` substitution**: In non-strict mode, if `this` would be `undefined` or `null`, JS substitutes the global object. Strict mode disables this.

#### Rule 3 — Object Method

`this` = the object before the dot when the method is called:

```javascript
const person = {
  name: "Akshay",
  greet: function() { console.log("Hello, " + this.name); }
};
person.greet(); // "Hello, Akshay"

// Detached method — this lost!
const greetFn = person.greet;
greetFn(); // "Hello, undefined" — this is now window/undefined
```

#### Rule 4 — `call`, `apply`, `bind`

All three explicitly set `this`:

```javascript
function greet(greeting) { console.log(greeting + ", " + this.name); }
const user = { name: "Akshad" };

greet.call(user, "Hello");           // "Hello, Akshad" — invokes immediately
greet.apply(user, ["Namaste"]);      // "Namaste, Akshad" — args as array
const boundGreet = greet.bind(user); // returns new function, permanently bound
boundGreet("Hi");                    // "Hi, Akshad"
```

| Method | Invokes immediately? | Args format | Returns |
|--------|---------------------|-------------|---------|
| `call` | ✅ Yes | Individual | Result |
| `apply` | ✅ Yes | Array | Result |
| `bind` | ❌ No | Individual (partial) | New function |

#### Rule 5 — Arrow Functions (Lexical `this`)

Arrow functions **do not have their own `this`**. They inherit `this` from the enclosing lexical scope at definition time:

```javascript
const obj = {
  name: "Akshay",
  greetArrow: () => {
    console.log(this.name); // NOT obj — enclosing scope (window/undefined)
  },
  greetRegular: function() {
    const inner = () => {
      console.log(this.name); // IS obj — inherits from greetRegular's this
    };
    inner();
  }
};
obj.greetArrow();  // undefined (window.name)
obj.greetRegular(); // "Akshay"

// Perfect use: timer in object method
const timer = {
  count: 0,
  start: function() {
    setInterval(() => {
      this.count++; // correctly refers to timer (lexical this from start)
      console.log(this.count);
    }, 1000);
  }
};
```

#### Rule 6 — Classes

```javascript
class Person {
  constructor(name) { this.name = name; }
  greet() { console.log("Hi, " + this.name); }
}
const p = new Person("Akshad");
p.greet(); // "Hi, Akshad"
```

#### Rule 7 — DOM Event Handlers

```javascript
// Regular function — this = the element
document.getElementById("btn").addEventListener("click", function() {
  console.log(this); // <button> element
});

// Arrow function — this = enclosing scope (window)
document.getElementById("btn").addEventListener("click", () => {
  console.log(this); // window (or undefined in strict)
});
```

### Code Example

```javascript
// 1. Global
console.log(this === window); // true

// 2. Regular function
function showThis() { console.log(this); } // window
showThis();

// 3. Strict mode
function showStrict() { 'use strict'; console.log(this); } // undefined
showStrict();

// 4. Object method
const student = { name: "Akshad", print: function() { console.log(this.name); } };
student.print(); // "Akshad"

// 5. call/apply/bind
const teacher = { name: "Akshay" };
student.print.call(teacher);   // "Akshay"
student.print.apply(teacher);  // "Akshay"
student.print.bind(teacher)(); // "Akshay"

// 6. Arrow — lexical this
const obj = {
  name: "LexicalTest",
  getArrow: function() {
    const arrow = () => console.log(this.name); // inherits from getArrow
    arrow();
  }
};
obj.getArrow(); // "LexicalTest"
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "`this` is always the object where the method is defined" | ❌ `this` depends on **how it's called** — detaching a method loses the binding |
| "Arrow functions have `this` set to `null`" | ❌ Arrows have no own `this` — they inherit it lexically from the enclosing scope |
| "`bind` invokes the function" | ❌ `bind` returns a new function with `this` permanently set — it does NOT call it |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;">

- **Q: What is `this` in JavaScript?**
  - A: A keyword referring to the object currently executing the code. Its value is determined by how the function is called — dynamic (except arrow functions, which capture `this` lexically).

- **Q: What is `this` substitution?**
  - A: In non-strict mode, if `this` would be `undefined` or `null` in a function call, JS substitutes the global object (`window`). Strict mode disables this substitution.

- **Q: What is the difference between `call`, `apply`, and `bind`?**
  - A: All three set `this`. `call` invokes immediately with individual args. `apply` invokes immediately with args as array. `bind` returns a new function with `this` permanently set — doesn't call it.

- **Q: Why don't arrow functions have their own `this`?**
  - A: Arrow functions capture `this` from their surrounding lexical context at definition time. They're ideal for callbacks inside methods where you need to preserve the outer `this`.

- **Q: What is `this` inside a DOM event handler?**
  - A: For a regular function handler, `this` is the DOM element that triggered the event. For an arrow function handler, `this` is the enclosing lexical context (usually `window`).
  </div>
</details>
</div>

### Key Takeaways

- `this` is **dynamic** — determined by call site, not definition site
- Global: `this === window` (browser) or `global` (Node.js)
- Regular function non-strict: `this` → global; strict: `this` → `undefined`
- `this` substitution: non-strict `undefined`/`null` → global object
- Object method: `this` → the object before the dot
- `call`/`apply`: set `this` temporarily, invoke immediately
- `bind`: return new function with `this` permanently bound
- Arrow functions: no own `this` — lexically inherit from enclosing scope
- DOM handlers (regular fn): `this` → the DOM element

---

# Part IX — Performance Patterns

### What are Debouncing and Throttling?

Two performance optimization techniques that control how often a function executes in response to high-frequency events (scroll, resize, keypress). They prevent performance issues caused by firing expensive functions too rapidly.

<a id="chapter-25--debouncing"></a>
## Chapter 25 — Debouncing &nbsp; <sup>[⬆ Back to Menu](#part-9)</sup>

**Debounce** delays function execution until a specified time has passed **since the last call**. If the function is called again before the delay expires, the timer resets.

> Use case: Search-as-you-type, form validation on input, window resize handler.

```javascript
function debounce(fn, delay) {
  let timer;
  return function(...args) {
    clearTimeout(timer); // reset the timer on every call
    timer = setTimeout(() => {
      fn.apply(this, args); // call only after delay with no new calls
    }, delay);
  };
}

const searchInput = document.getElementById("search");
const debouncedSearch = debounce(function(e) {
  console.log("Searching for:", e.target.value);
  // API call here — only fires 300ms after user stops typing
}, 300);

searchInput.addEventListener("input", debouncedSearch);
```

**Timeline:**
```
User types: h-e-l-l-o (each keystroke within 300ms of the previous)
Debounced:  [        ] → fires once, 300ms after "o" is typed
```
---
<a id="chapter-26--throttling"></a>
## Chapter 26 — Throttling &nbsp; <sup>[⬆ Back to Menu](#part-9)</sup>

**Throttle** ensures the function executes **at most once per interval**, no matter how many times it's triggered. Unlike debounce, it fires immediately (leading edge) and then ignores calls until the interval passes.

> Use case: Scroll event handlers, mouse move tracking, resize listeners where you need periodic updates.

```javascript
function throttle(fn, interval) {
  let lastTime = 0;
  return function(...args) {
    const now = Date.now();
    if (now - lastTime >= interval) {
      lastTime = now;
      fn.apply(this, args); // execute if enough time has passed
    }
  };
}

const throttledScroll = throttle(function() {
  console.log("Scroll position:", window.scrollY);
  // Updates at most once per 200ms during scroll
}, 200);

window.addEventListener("scroll", throttledScroll);
```

**Timeline:**
```
Scroll events: ↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑↑ (continuous)
Throttled:     ↑   ↑   ↑   ↑   ↑     (once per 200ms)
```

#### Debounce vs Throttle

| | Debounce | Throttle |
|---|----------|----------|
| **When to use** | After activity stops | During continuous activity |
| **Fires** | Once after last call + delay | At most once per interval |
| **First execution** | After delay (trailing edge) | Immediately (leading edge) |
| **Example** | Search input, form validation | Scroll, mousemove, resize |

### Code Example

```javascript
// Complete debounce implementation
function debounce(fn, delay) {
  let timer;
  return function(...args) {
    clearTimeout(timer);
    timer = setTimeout(() => fn.apply(this, args), delay);
  };
}

// Complete throttle implementation
function throttle(fn, interval) {
  let lastTime = 0;
  return function(...args) {
    const now = Date.now();
    if (now - lastTime >= interval) {
      lastTime = now;
      fn.apply(this, args);
    }
  };
}

// Usage
const onSearch = debounce(function(query) {
  fetch(`/api/search?q=${query}`).then(r => r.json()).then(console.log);
}, 400);

const onScroll = throttle(function() {
  // Update sticky header, load more content, etc.
}, 100);

document.getElementById("search").addEventListener("input", e => onSearch(e.target.value));
window.addEventListener("scroll", onScroll);
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "Debounce and throttle are the same thing" | ❌ Debounce fires after inactivity; throttle fires at fixed intervals during activity |
| "Debounce always fires immediately" | ❌ By default, debounce fires on the trailing edge (after delay). A leading-edge variant exists but requires extra code |
| "These are only browser concepts" | ❌ Both patterns apply anywhere you need to rate-limit function calls — Node.js, CLI tools, etc. |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;">

- **Q: What is debouncing?**
  - A: Debouncing delays a function's execution until a specified time has elapsed since the last call. If called again before the delay, the timer resets. Used for search inputs, form validation — fires once after the user stops interacting.

- **Q: What is throttling?**
  - A: Throttling ensures a function executes at most once per interval, regardless of how many times it's triggered. Used for scroll/resize events where periodic updates are needed.

- **Q: When would you use debounce vs throttle?**
  - A: Use **debounce** when you want to react *after* activity stops (typing in a search box). Use **throttle** when you need *regular* updates *during* continuous activity (scroll position tracking).

- **Q: How do you implement a debounce function?**
  - A: Create a closure with a `timer` variable. Return a function that clears the previous timer and sets a new one each time it's called. The actual function only executes when `setTimeout` fires — i.e., after the delay with no new calls.
  </div>
</details>
</div>

### Key Takeaways

- Debounce: fires once after `delay` ms of **inactivity** — ideal for search inputs
- Throttle: fires at most once per `interval` — ideal for scroll/resize events
- Both use closures to maintain state (timer or lastTime) between calls
- Debounce resets the timer on each call — only the last call triggers execution
- Throttle ignores calls that arrive too soon — guarantees maximum call frequency
- Both return a new function that wraps the original with rate-limiting logic

---

<a id="chapter-27--polyfills--prototype"></a>

## Chapter 27 — Polyfills & Prototype Internals &nbsp; <sup>[⬆ Back to Menu](#part-9)</sup>

### What are Polyfills?

A **polyfill** is code that implements a modern feature for browsers/environments that don't natively support it. Writing polyfills requires understanding `Array.prototype` — the prototype-based inheritance system that powers all built-in array methods.

### How It Works

#### JavaScript's Prototype Chain

Every object in JavaScript has an internal `[[Prototype]]` link pointing to another object. When you access a property or method, JS looks up the prototype chain until it finds it or reaches `null`.

```javascript
const arr = [1, 2, 3];
// arr → Array.prototype → Object.prototype → null

arr.map;          // found on Array.prototype
arr.hasOwnProperty; // found on Object.prototype
```

#### Polyfill for `Array.prototype.map`

```javascript
// Check if map doesn't exist (for demonstration)
Array.prototype.myMap = function(callback) {
  const result = [];
  for (let i = 0; i < this.length; i++) {
    result.push(callback(this[i], i, this));
    //                   ^value  ^index ^array (same signature as native map)
  }
  return result;
};

// Usage — identical to native map
const doubled = [1, 2, 3].myMap(x => x * 2);
console.log(doubled); // [2, 4, 6]
```

#### Polyfill for `Array.prototype.filter`

```javascript
Array.prototype.myFilter = function(callback) {
  const result = [];
  for (let i = 0; i < this.length; i++) {
    if (callback(this[i], i, this)) { // include if truthy
      result.push(this[i]);
    }
  }
  return result;
};

const evens = [1, 2, 3, 4, 5].myFilter(x => x % 2 === 0);
console.log(evens); // [2, 4]
```

#### Polyfill for `Array.prototype.reduce`

```javascript
Array.prototype.myReduce = function(callback, initialValue) {
  let acc = initialValue !== undefined ? initialValue : this[0];
  let startIndex = initialValue !== undefined ? 0 : 1;

  for (let i = startIndex; i < this.length; i++) {
    acc = callback(acc, this[i], i, this);
  }
  return acc;
};

const sum = [1, 2, 3, 4, 5].myReduce((acc, curr) => acc + curr, 0);
console.log(sum); // 15
```

#### Polyfill for `Function.prototype.bind`

```javascript
Function.prototype.myBind = function(context, ...args) {
  const fn = this; // the original function
  return function(...innerArgs) {
    return fn.apply(context, [...args, ...innerArgs]);
  };
};

function greet(greeting, punctuation) {
  console.log(greeting + ", " + this.name + punctuation);
}
const user = { name: "Akshad" };
const boundGreet = greet.myBind(user, "Hello");
boundGreet("!"); // "Hello, Akshad!"
```

#### Why the Callback Signature Matters

Native `map`/`filter`/`reduce` callbacks receive **(value, index, array)** — not just the value. Polyfills must replicate this signature for compatibility:

```javascript
[10, 20, 30].map((value, index, array) => {
  return `${index}: ${value} of ${array.length}`;
});
// ["0: 10 of 3", "1: 20 of 3", "2: 30 of 3"]
```

### Common Mistakes

| Mistake | Why It's Wrong |
|---------|---------------|
| "Polyfills always override native methods" | ❌ Always check `if (!Array.prototype.myMethod)` before adding to avoid overwriting native implementations |
| "Adding to `Array.prototype` is always safe" | ⚠️ It pollutes the global prototype — all arrays get the method. Use with care in libraries |
| "The reduce callback only gets (acc, curr)" | ❌ Native reduce callback signature is `(acc, curr, index, array)` — polyfills should match |

<div style="font-size: 22px; color: red">
<details>
  <summary><strong>Interview Questions (Click to View)</strong></summary>
  <div style="font-size: 0.9rem; color: black; background:#fff; border:2px solid red; border-radius: 10px;">

- **Q: What is a polyfill?**
  - A: Code that implements a modern feature for browsers/environments that don't natively support it. Polyfills replicate the API and behavior of the native feature using existing capabilities.

- **Q: How would you polyfill `Array.prototype.map`?**
  - A: Add `myMap` to `Array.prototype`. Inside, iterate with a `for` loop, call `callback(this[i], i, this)` for each element, push the result to an output array, and return that array.

- **Q: What is the difference between prototype and `__proto__`?**
  - A: `prototype` is a property of **constructor functions/classes** — it's the object that becomes the `[[Prototype]]` of instances. `__proto__` is the instance's link to its prototype. `Object.getPrototypeOf(obj)` is the modern equivalent of `obj.__proto__`.

- **Q: How do you polyfill `Function.prototype.bind`?**
  - A: Return a new function from `myBind` that calls the original function with `apply(context, [...capturedArgs, ...newArgs])`. Use a closure to capture the `context` and any pre-bound arguments.
  </div>
</details>
</div>

### Key Takeaways

- Polyfill = code implementing a feature for environments that don't support it natively
- All array methods live on `Array.prototype` — the prototype chain makes them accessible on every array
- Polyfill `map`: iterate, call callback with `(value, index, arr)`, push to result, return result
- Polyfill `filter`: iterate, include element if callback returns truthy
- Polyfill `reduce`: accumulate with initial value, iterate, return final accumulator
- Polyfill `bind`: return a new function using closure + `apply`
- Always replicate the native callback signature: `(value, index, array)`

---

# Part X — JavaScript Cheat Sheet

---

<a id="chapter-28--cheat-sheet"></a>

## Chapter 27 — JavaScript Cheat Sheet &nbsp; <sup>[⬆ Back to Menu](#part-10)</sup>

> A quick-reference summary of every major concept covered in this guide — organized for last-minute interview prep.

---

### Core Concepts (Chapters 1–6)

| Concept | One-line Summary |
|---------|-----------------|
| **Execution Context** | Environment where JS code evaluates. Memory phase (store vars) → Code phase (run line by line) |
| **Call Stack** | LIFO stack of Execution Contexts — pops when function returns |
| **Hoisting** | `var` → `undefined`; `function` → fully hoisted; `let`/`const` → TDZ error |
| **Global EC** | Created automatically — has `window`, `this`, global vars |
| **`window`/`this`** | In GEC: `this === window`. `var` → on `window`; `let`/`const` → not on `window` |
| **`undefined`** | Placeholder assigned in Phase 1. NOT the same as not defined (`ReferenceError`) |

---

### Scope & Closures (Chapters 7–12)

| Concept | One-line Summary |
|---------|-----------------|
| **Lexical Environment** | Local memory + reference to parent lexical env — forms the scope chain |
| **Scope Chain** | JS traverses from inner → outer scopes to resolve variables |
| **TDZ** | `let`/`const` are in TDZ from start of scope until their declaration line |
| **Block Scope** | `let`/`const` scoped to `{}` blocks; `var` leaks to function/global scope |
| **Shadowing** | Inner `let`/`const` shadows outer. Illegal: `let` outer + `var` inner (can't cross scope boundary) |
| **Closure** | Function bundled with its lexical environment — carries variables from outer scope |
| **`setTimeout` + closures** | Use `let` (block-scoped) or IIFE to create fresh `i` for each loop iteration |
| **Module Pattern** | IIFE returning an object of functions — uses closures for private state |

---

### Functions Deep Dive (Chapters 13–14)

| Concept | One-line Summary |
|---------|-----------------|
| **Function Statement** | Fully hoisted — callable before its line |
| **Function Expression** | Only variable hoisted (`undefined`) — `TypeError` if called early |
| **Anonymous Function** | No name — must be a value (assigned/passed/returned), can't stand alone |
| **Named Function Expr** | Name only accessible inside function body (for recursion) |
| **First-Class Functions** | Functions are values: assignable, passable as args, returnable |
| **Callback** | Function passed as argument, invoked later (sync or async) |
| **Event Listener** | Attach callback to DOM event; forms closure; must `removeEventListener` to free memory |

---

### Async JS & Engine (Chapters 15–17)

| Concept | One-line Summary |
|---------|-----------------|
| **Web APIs** | Browser extras (`setTimeout`, `fetch`, DOM) — not part of JS engine |
| **Callback Queue** | Holds `setTimeout`/event callbacks — lower priority |
| **Microtask Queue** | Holds Promise `.then()`, `queueMicrotask()` — **higher priority**, drained first |
| **Event Loop** | Stack empty → drain all microtasks → take one callback queue item |
| **Starvation** | Infinite microtasks prevent Callback Queue from ever running |
| **JIT Compilation** | Ignition (interpreter) + TurboFan (optimizing compiler) = fast startup + hot-path optimization |
| **V8 Components** | Parser → AST → Ignition → bytecode → TurboFan → machine code. Orinoco = GC |
| **Mark and Sweep** | GC: mark reachable objects, sweep (free) unreachable ones |
| **`setTimeout` trust** | Minimum delay guarantee — actual time = delay + wait for stack to clear |
| **Never block main thread** | Heavy sync work → delays timers, events, rendering. Use Web Workers |

---

### Functional Programming (Chapters 18–19)

| Concept | One-line Summary |
|---------|-----------------|
| **HOF** | Function that takes or returns a function: `map`, `filter`, `reduce`, `setTimeout` |
| **Pure Function** | Same input → same output, no side effects |
| **`map`** | Transform each element → new array of same length |
| **`filter`** | Select elements by condition → new array (possibly shorter) |
| **`reduce`** | Accumulate all elements → single value of any type |
| **Chain** | `arr.filter(...).map(...)` — each method operates on the previous result |

---

### Promises & Async (Chapters 20–23)

| Concept | One-line Summary |
|---------|-----------------|
| **Callback Hell** | Nested callbacks for sequential async ops — Pyramid of Doom |
| **Inversion of Control** | Handing your callback to third-party — lose control of when/how it runs |
| **Promise** | Object: placeholder for future value. States: pending → fulfilled/rejected (immutable) |
| **Promise solves IoC** | Third party returns Promise; you attach `.then()` — Promise API calls it exactly once |
| **Promise chaining** | Flat `.then()` chain replaces nesting — always `return` from `.then()` handlers |
| **`.catch()` placement** | End = catches all; middle = partial recovery; rejection skips `.then()` |
| **`.finally()`** | Always runs — use for cleanup (no args received) |
| **`async` function** | Always returns a Promise — non-Promise return auto-wrapped |
| **`await`** | Suspends async function (not engine) until Promise settles — resumes via Microtask Queue |
| **Parallel with `Promise.all`** | `await Promise.all([p1, p2])` runs concurrently — faster than sequential `await` |

---

### `this` Keyword (Chapter 24)

| Context | `this` |
|---------|--------|
| Global scope (browser) | `window` |
| Regular fn (non-strict) | `window` (substitution) |
| Regular fn (strict) | `undefined` |
| Method call `obj.fn()` | `obj` |
| `call(ctx)` / `apply(ctx, [])` | `ctx` |
| `bind(ctx)` | `ctx` (returns new fn) |
| Arrow function | Lexical (enclosing scope) |
| Class constructor/method | Instance |
| DOM event (regular fn) | DOM element |

---

### Performance & Internals (Chapters 25–26)

| Concept | One-line Summary |
|---------|-----------------|
| **Debounce** | Delay execution until `delay` ms after last call — trailing edge, resets on each call |
| **Throttle** | Execute at most once per `interval` — ignores calls that arrive too soon |
| **When to debounce** | Search-as-you-type, form validation — react after user stops |
| **When to throttle** | Scroll/resize/mousemove — periodic updates during continuous activity |
| **Polyfill** | Code implementing a modern feature in environments that don't support it |
| **Prototype chain** | `arr → Array.prototype → Object.prototype → null` |

---

### Quick Interview Patterns

```javascript
// Closure counter
function makeCounter() {
  let count = 0;
  return { inc: () => ++count, get: () => count };
}

// Debounce
const debouncedFn = debounce(() => console.log("fired"), 300);

// Promise chain
fetchUser(id)
  .then(user => fetchPosts(user.id))
  .then(posts => render(posts))
  .catch(console.error);

// async/await equivalent
async function loadPosts(id) {
  try {
    const user = await fetchUser(id);
    const posts = await fetchPosts(user.id);
    render(posts);
  } catch (e) { console.error(e); }
}

// this — explicit binding
const greet = function() { return "Hi, " + this.name; };
greet.call({ name: "Akshad" }); // "Hi, Akshad"

// Polyfill map
Array.prototype.myMap = function(cb) {
  const out = [];
  for (let i = 0; i < this.length; i++) out.push(cb(this[i], i, this));
  return out;
};
```

---

> **Study tip:** The most commonly tested topics in JS interviews are: closures, the event loop (microtask vs callback queue), Promise chaining, `async`/`await` internals, and `this` binding rules. Master these five areas and you'll be prepared for 90% of JS interview questions.

<div align="center">

### 🎉 You've completed the JavaScript journey!

Generated with ❤️ for JavaScript developers — happy coding!

</div>
