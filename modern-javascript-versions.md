# ⚡ Modern JavaScript — ES2017 to ES2025 &nbsp; <sup> 👉 [Back to JavaScript Guide](https://github.com/harshit2490/javascript-guide/blob/main/README.md)</sup>

> A concise, code-first reference covering every major ECMAScript feature from ES8 (2017) through ES16 (2025). Interview-focused with real examples for each feature.

![JavaScript](https://img.shields.io/badge/JavaScript-ES2017--ES2025-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Interview](https://img.shields.io/badge/Interview-Ready-4CAF50?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-blue?style=for-the-badge)

---

<a id="toc"></a>
## 📚 Table of Contents

| Version | Year | Key Features |
|---------|------|-------------|
| [ES2017 (ES8)](#es2017-es8) | 2017 | `async`/`await`, `Object.values/entries`, String padding, `Object.getOwnPropertyDescriptors` |
| [ES2018 (ES9)](#es2018-es9) | 2018 | Object rest/spread, `Promise.finally`, Async iteration |
| [ES2019 (ES10)](#es2019-es10) | 2019 | `Array.flat/flatMap`, `Object.fromEntries`, `String.trimStart/trimEnd`, Optional catch |
| [ES2020 (ES11)](#es2020-es11) | 2020 | Optional chaining `?.`, Nullish coalescing `??`, `BigInt`, `Promise.allSettled`, Dynamic import |
| [ES2021 (ES12)](#es2021-es12) | 2021 | `String.replaceAll`, `Promise.any`, Logical assignment `&&=` `\|\|=` `??=`, Numeric separators |
| [ES2022 (ES13)](#es2022-es13) | 2022 | `Array.at()`, `Object.hasOwn()`, Top-level `await`, Class fields (public/private), `Error.cause` |
| [ES2023 (ES14)](#es2023-es14) | 2023 | `Array.findLast/findLastIndex`, Immutable array methods `toSorted/toReversed/toSpliced/with` |
| [ES2024 (ES15)](#es2024-es15) | 2024 | `Promise.withResolvers`, `Object.groupBy`, `Map.groupBy`, `ArrayBuffer.resize` |
| [ES2025 (ES16)](#es2025-es16) | 2025 | `Iterator` helpers, `RegExp` features, `Promise.try`, `Set` methods |
| [ES2026 (ES17)](#es2026-es17) | 2026 | `Temporal API`, `Math.sumPrecise`, `Error.isError`, `Array.fromAsync`, `Iterator.concat`, `Map.getOrInsert`, `Uint8Array` base64/hex, JSON improvements |

---

<a id="es2017-es8"></a>
## ES2017 (ES8) — 2017 &nbsp; <sup>[⬆ Back to Menu](#toc)</sup>

---

### 1. `async` / `await`

> Syntactic sugar over Promises — write async code that reads like sync code.

**How it works:**
- `async` function always returns a Promise
- `await` suspends the function (not the engine) until the Promise settles
- Resumes via Microtask Queue

```javascript
// Without async/await
function fetchUser() {
  return fetch('/api/user')
    .then(res => res.json())
    .then(user => user);
}

// With async/await
async function fetchUser() {
  const res = await fetch('/api/user');
  const user = await res.json();
  return user;
}

// Error handling
async function getData() {
  try {
    const res = await fetch('https://jsonplaceholder.typicode.com/posts/1');
    if (!res.ok) throw new Error(`HTTP error: ${res.status}`);
    const data = await res.json();
    console.log(data.title);
  } catch (err) {
    console.error('Failed:', err.message);
  } finally {
    console.log('Done');
  }
}

// Parallel execution — avoid sequential when independent
const [users, posts] = await Promise.all([
  fetch('/api/users').then(r => r.json()),
  fetch('/api/posts').then(r => r.json())
]);
```

> 💡 **Interview tip:** `await` doesn't block the JS thread — the function is suspended and removed from the Call Stack. Other code runs while it waits.

---

### 2. `Object.values()` and `Object.entries()`

> Iterate over an object's values or key-value pairs — the missing companions to `Object.keys()`.

```javascript
const person = { name: 'Akshay', age: 30, city: 'Mumbai' };

// Object.keys() — already existed in ES5
Object.keys(person);    // ['name', 'age', 'city']

// Object.values() — NEW in ES2017
Object.values(person);  // ['Akshay', 30, 'Mumbai']

// Object.entries() — NEW in ES2017
Object.entries(person); // [['name', 'Akshay'], ['age', 30], ['city', 'Mumbai']]

// Common use: iterate like a Map
for (const [key, value] of Object.entries(person)) {
  console.log(`${key}: ${value}`);
}
// name: Akshay
// age: 30
// city: Mumbai

// Transform object values
const prices = { apple: 1.5, banana: 0.5, cherry: 3.0 };
const discounted = Object.fromEntries(             // ES2019
  Object.entries(prices).map(([k, v]) => [k, v * 0.9])
);
// { apple: 1.35, banana: 0.45, cherry: 2.70 }
```

---

### 3. String Padding — `padStart()` and `padEnd()`

> Pad a string to a target length with a given character.

```javascript
// padStart(targetLength, padString)
'5'.padStart(3, '0');      // '005' — useful for IDs, clocks
'hello'.padStart(8, '*');  // '***hello'
'hi'.padStart(5);          // '   hi' — default pad is space

// padEnd(targetLength, padString)
'hello'.padEnd(8, '.');    // 'hello...'
'42'.padEnd(5, '0');       // '42000'

// Real-world: format a clock
const hours = '9';
const mins = '5';
console.log(`${hours.padStart(2,'0')}:${mins.padStart(2,'0')}`); // '09:05'

// Align table output
const items = [['apple', '1.50'], ['banana', '0.50'], ['cherry', '3.00']];
items.forEach(([name, price]) => {
  console.log(name.padEnd(10) + price.padStart(6));
});
// apple       1.50
// banana      0.50
// cherry      3.00
```

---

### 4. `Object.getOwnPropertyDescriptors()`

> Get all property descriptors of an object — essential for proper object cloning.

```javascript
const obj = {
  name: 'Akshay',
  get greeting() { return `Hello, ${this.name}`; }
};

// Shallow clone loses getter
const badClone = Object.assign({}, obj);
console.log(Object.getOwnPropertyDescriptor(badClone, 'greeting'));
// {value: 'Hello, Akshay', writable: true, ...} — getter is gone!

// Proper clone preserving getters/setters
const goodClone = Object.defineProperties(
  {},
  Object.getOwnPropertyDescriptors(obj)
);
console.log(goodClone.greeting); // 'Hello, Akshay' — getter works!

// What a descriptor looks like
Object.getOwnPropertyDescriptor(obj, 'name');
// { value: 'Akshay', writable: true, enumerable: true, configurable: true }
```

---

### 5. Trailing Commas in Function Parameters

> Trailing commas are now allowed in function parameter lists and calls — cleaner diffs.

```javascript
// ES2017 allows trailing commas in params and args
function add(
  a,
  b,   // ← trailing comma now valid
) {
  return a + b;
}

add(
  1,
  2,   // ← trailing comma in call also valid
);

// Benefit: git diff shows only the changed line, not the comma addition
```

---
<a id="es2018-es9"></a>
## ES2018 (ES9) — 2018 &nbsp; <sup>[⬆ Back to Menu](#toc)</sup>

---

### 6. Object Rest and Spread (`...` for Objects)

> The `...` spread/rest syntax extended to objects (previously only arrays in ES6).

```javascript
// Spread — clone and merge objects
const defaults = { color: 'blue', size: 'M', quantity: 1 };
const custom   = { color: 'red', quantity: 5 };

const order = { ...defaults, ...custom };
// { color: 'red', size: 'M', quantity: 5 }
// Later properties override earlier ones

// Clone an object (shallow)
const original = { a: 1, b: { c: 2 } };
const clone = { ...original }; // top-level copy
clone.a = 99;       // ✅ doesn't affect original
clone.b.c = 99;     // ❌ .b is still a reference

// Rest — extract specific props, collect the rest
const { name, age, ...rest } = { name: 'Akshay', age: 30, city: 'Mumbai', role: 'Dev' };
console.log(name); // 'Akshay'
console.log(age);  // 30
console.log(rest); // { city: 'Mumbai', role: 'Dev' }

// Common pattern: remove a key from an object immutably
const { password, ...safeUser } = userFromDB;
// safeUser is now the user object without the password field
```

---

### 7. `Promise.prototype.finally()`

> Run cleanup code regardless of Promise success or failure.

```javascript
// Without finally — duplicated cleanup
showSpinner();
fetchData()
  .then(data => { displayData(data); hideSpinner(); })
  .catch(err => { showError(err); hideSpinner(); }); // ← duplicated!

// With finally — clean
showSpinner();
fetchData()
  .then(data => displayData(data))
  .catch(err => showError(err))
  .finally(() => hideSpinner()); // always runs

// Important: finally doesn't receive the resolved value
Promise.resolve(42)
  .then(val => { console.log(val); return val; }) // 42
  .finally(() => {
    // No value received here — don't return anything meaningful
    console.log('Cleanup');
  })
  .then(val => console.log(val)); // 42 — value passes through
```

---

### 8. Async Iteration — `for await...of`

> Iterate over async data sources (streams, paginated APIs) one item at a time.

```javascript
// Async generator
async function* asyncNumbers() {
  yield await Promise.resolve(1);
  yield await Promise.resolve(2);
  yield await Promise.resolve(3);
}

// Consume with for await...of
async function main() {
  for await (const num of asyncNumbers()) {
    console.log(num); // 1, 2, 3 — each waits for the previous
  }
}
main();

// Real-world: paginated API
async function* fetchPages(url) {
  let page = 1;
  while (true) {
    const res = await fetch(`${url}?page=${page}`);
    const data = await res.json();
    if (data.items.length === 0) break;
    yield data.items;
    page++;
  }
}

async function processAll() {
  for await (const items of fetchPages('/api/products')) {
    items.forEach(item => console.log(item.name));
  }
}
```

---

### 9. RegExp Improvements

> Named capture groups, lookbehind assertions, dotAll flag.

```javascript
// Named capture groups — (?<name>pattern)
const dateRegex = /(?<year>\d{4})-(?<month>\d{2})-(?<day>\d{2})/;
const { groups } = '2024-07-17'.match(dateRegex);
console.log(groups.year);  // '2024'
console.log(groups.month); // '07'
console.log(groups.day);   // '17'

// dotAll flag (s) — . now matches newlines too
const text = 'Hello\nWorld';
console.log(/Hello.World/.test(text));   // false — . doesn't match \n
console.log(/Hello.World/s.test(text));  // true  — with /s flag

// Lookbehind assertion — match only if preceded by...
const prices = ['$100', '€200', '$300'];
// Match numbers preceded by $
prices.forEach(p => {
  const match = p.match(/(?<=\$)\d+/);
  if (match) console.log('USD amount:', match[0]);
});
// USD amount: 100
// USD amount: 300
```

---
<a id="es2019-es10"></a>
## ES2019 (ES10) — 2019 &nbsp; <sup>[⬆ Back to Menu](#toc)</sup>

---

### 10. `Array.prototype.flat()` and `flatMap()`

> Flatten nested arrays and map+flatten in one step.

```javascript
// flat(depth) — defaults to depth 1
const nested = [1, [2, 3], [4, [5, 6]]];
nested.flat();    // [1, 2, 3, 4, [5, 6]] — 1 level
nested.flat(2);   // [1, 2, 3, 4, 5, 6]  — 2 levels
nested.flat(Infinity); // fully flatten regardless of depth

// Remove empty slots
[1, , , 4, , 6].flat(); // [1, 4, 6]

// flatMap — map then flatten 1 level (more efficient than .map().flat())
const sentences = ['Hello World', 'Namaste JavaScript'];
const words = sentences.flatMap(s => s.split(' '));
// ['Hello', 'World', 'Namaste', 'JavaScript']

// flatMap use case: one-to-many transformation
const orders = [
  { id: 1, items: ['shoe', 'shirt'] },
  { id: 2, items: ['hat'] }
];
const allItems = orders.flatMap(order => order.items);
// ['shoe', 'shirt', 'hat']
```

---

### 11. `Object.fromEntries()`

> Convert an array of `[key, value]` pairs (or a Map) into an object — inverse of `Object.entries()`.

```javascript
// From array of entries
const entries = [['name', 'Akshay'], ['age', 30]];
const obj = Object.fromEntries(entries);
// { name: 'Akshay', age: 30 }

// Perfect pair with Object.entries() — transform objects
const prices = { apple: 1.5, banana: 0.5, cherry: 3.0 };

// Double all prices
const doubled = Object.fromEntries(
  Object.entries(prices).map(([k, v]) => [k, v * 2])
);
// { apple: 3, banana: 1, cherry: 6 }

// Filter object by value
const expensive = Object.fromEntries(
  Object.entries(prices).filter(([, v]) => v > 1)
);
// { apple: 1.5, cherry: 3.0 }

// From a Map
const map = new Map([['a', 1], ['b', 2]]);
Object.fromEntries(map); // { a: 1, b: 2 }
```

---

### 12. `String.trimStart()` and `trimEnd()`

> Trim whitespace from the start or end only — more specific than `trim()`.

```javascript
const str = '   hello world   ';

str.trim();      // 'hello world'       — both sides
str.trimStart(); // 'hello world   '    — left side only
str.trimEnd();   // '   hello world'    — right side only

// Aliases (non-standard but supported)
str.trimLeft();  // same as trimStart()
str.trimRight(); // same as trimEnd()

// Use case: preserve intentional leading/trailing spaces
const code = '    const x = 1;';
code.trimStart(); // 'const x = 1;' — remove indentation
```

---

### 13. Optional Catch Binding

> Omit the `catch` parameter when you don't need the error object.

```javascript
// Before ES2019 — had to bind the error even if unused
try {
  JSON.parse(invalidJson);
} catch (e) { // e is required even if not used
  console.log('Invalid JSON');
}

// ES2019 — parameter is optional
try {
  JSON.parse(invalidJson);
} catch {
  console.log('Invalid JSON'); // no e needed
}

// Practical use: feature detection
function isPromiseSupported() {
  try {
    new Promise(() => {});
    return true;
  } catch {
    return false;
  }
}
```

---

### 14. `Array.prototype.sort()` — Stable Sort (Guaranteed)

```javascript
// Before ES2019 — sort stability was implementation-dependent
// From ES2019 — sort is guaranteed to be STABLE
// Elements with equal keys maintain their original relative order

const students = [
  { name: 'Alice', grade: 'A' },
  { name: 'Bob',   grade: 'B' },
  { name: 'Carol', grade: 'A' },
  { name: 'Dave',  grade: 'B' },
];

// Sort by grade — Alice and Carol (both 'A') will stay in original order
students.sort((a, b) => a.grade.localeCompare(b.grade));
// Alice (A), Carol (A), Bob (B), Dave (B) — stable!
```

---
<a id="es2020-es11"></a>
## ES2020 (ES11) — 2020 &nbsp; <sup>[⬆ Back to Menu](#toc)</sup>

---

### 15. Optional Chaining — `?.`

> Safely access deeply nested properties without a chain of `&&` checks.

```javascript
const user = {
  profile: {
    address: {
      city: 'Mumbai'
    }
  }
};

// Without optional chaining — verbose
const city = user && user.profile && user.profile.address && user.profile.address.city;

// With ?. — clean
const city = user?.profile?.address?.city; // 'Mumbai'

// If any part is null/undefined, returns undefined (no error thrown)
const zip = user?.profile?.address?.zip;   // undefined — no crash
const phone = user?.contact?.phone;        // undefined — user.contact doesn't exist

// Works with method calls too
const name = user?.getName?.();             // calls only if getName exists
const item = arr?.[0];                      // optional array access

// Combine with ?? for a fallback
const displayCity = user?.profile?.address?.city ?? 'Unknown';
// 'Mumbai' or 'Unknown' if city is null/undefined

// Real-world API response
const result = apiResponse?.data?.users?.[0]?.name ?? 'Anonymous';
```

---

### 16. Nullish Coalescing — `??`

> Return the right-hand value only when the left is `null` or `undefined` (not just any falsy value).

```javascript
// The problem with ||
const count = 0;
const display = count || 'No items'; // 'No items' — WRONG! 0 is falsy

// ?? only triggers on null/undefined
const display = count ?? 'No items'; // 0 — CORRECT!

// Other falsy values that || would mishandle
'' || 'default'  // 'default' — string was ""
'' ?? 'default'  // ''        — empty string is a valid value

false || 'yes'   // 'yes'
false ?? 'yes'   // false — false is not null/undefined

// Practical use: config/settings
function createUser(settings) {
  const name     = settings.name     ?? 'Guest';
  const darkMode = settings.darkMode ?? false;   // false is valid!
  const retries  = settings.retries  ?? 3;       // 0 would be wrong with ||
  return { name, darkMode, retries };
}

createUser({ name: '', darkMode: false, retries: 0 });
// { name: '', darkMode: false, retries: 0 } — all correct with ??
```

---

### 17. `BigInt`

> Work with integers larger than `Number.MAX_SAFE_INTEGER` (2⁵³ - 1).

```javascript
// The problem with regular numbers
console.log(Number.MAX_SAFE_INTEGER); // 9007199254740991
console.log(9007199254740991 + 1);    // 9007199254740992 ✅
console.log(9007199254740991 + 2);    // 9007199254740992 ❌ — precision lost!

// BigInt — suffix with n or use BigInt()
const big = 9007199254740991n;
console.log(big + 1n); // 9007199254740992n ✅
console.log(big + 2n); // 9007199254740993n ✅

const fromString = BigInt('12345678901234567890');

// Cannot mix BigInt and Number
console.log(1n + 1);   // TypeError!
console.log(1n + 1n);  // 2n ✅

// Comparison works across types
console.log(1n == 1);  // true  (loose equality)
console.log(1n === 1); // false (strict equality — different types)

// Use cases: crypto, database IDs, financial calculations
const twitterId = 1234567890123456789n; // beyond safe integer range
```

---

### 18. `Promise.allSettled()`

> Wait for all promises regardless of outcome — never rejects, gives you full results.

```javascript
const promises = [
  fetch('/api/users'),
  fetch('/api/posts'),
  fetch('/api/invalid-endpoint') // this will fail
];

// Promise.all — rejects if ANY rejects
Promise.all(promises).catch(err => console.log('All failed:', err));

// Promise.allSettled — always resolves with an array of outcomes
const results = await Promise.allSettled(promises);

results.forEach((result, i) => {
  if (result.status === 'fulfilled') {
    console.log(`Promise ${i} succeeded:`, result.value);
  } else {
    console.log(`Promise ${i} failed:`, result.reason.message);
  }
});

// Comparison table
// Promise.all         — wait for all, fail fast on first rejection
// Promise.allSettled  — wait for all, report every outcome (fulfilled or rejected)
// Promise.race        — settle as soon as first settles (success or fail)
// Promise.any         — resolve on first fulfillment, reject if ALL reject
```

---

### 19. `globalThis`

> A universal way to access the global object in any environment.

```javascript
// Problem: global object is different everywhere
// Browser: window
// Node.js: global
// Web Worker: self
// ES module: undefined (with 'this')

// globalThis — works everywhere
console.log(globalThis); // window in browser, global in Node.js, etc.

// Use case: environment-agnostic code
function isNode() {
  return globalThis.process?.versions?.node !== undefined;
}

function isBrowser() {
  return typeof globalThis.document !== 'undefined';
}

// Safe polyfill setup
if (!globalThis.fetch) {
  globalThis.fetch = require('node-fetch'); // add fetch in older Node.js
}
```

---

### 20. Dynamic `import()`

> Import modules on demand at runtime — code splitting and lazy loading.

```javascript
// Static import — must be at top level, always loaded
import { add } from './math.js';

// Dynamic import() — on demand, returns a Promise
async function loadMath() {
  const math = await import('./math.js');
  console.log(math.add(1, 2)); // 3
}

// Real-world: lazy load heavy library only when needed
button.addEventListener('click', async () => {
  const { Chart } = await import('./chart-library.js');
  const chart = new Chart(ctx, config);
});

// Conditional import based on environment
const module = await import(
  process.env.NODE_ENV === 'development'
    ? './debug-utils.js'
    : './prod-utils.js'
);

// Named exports
const { formatDate, parseDate } = await import('./date-utils.js');
```

---
<a id="es2021-es12"></a>
## ES2021 (ES12) — 2021 &nbsp; <sup>[⬆ Back to Menu](#toc)</sup>

---

### 21. `String.prototype.replaceAll()`

> Replace all occurrences of a substring — no more regex workaround.

```javascript
const str = 'I love JavaScript. JavaScript is great!';

// Old way — needed regex with /g flag
str.replace(/JavaScript/g, 'TypeScript');

// replaceAll — much cleaner
str.replaceAll('JavaScript', 'TypeScript');
// 'I love TypeScript. TypeScript is great!'

// Works with strings (not regex)
'a.b.c'.replaceAll('.', '-'); // 'a-b-c'

// Note: replaceAll still accepts a RegExp — it must have the /g flag
str.replaceAll(/javascript/gi, 'TypeScript'); // case-insensitive replace all

// Common use: sanitize user input
function escapeHtml(str) {
  return str
    .replaceAll('&', '&amp;')
    .replaceAll('<', '&lt;')
    .replaceAll('>', '&gt;')
    .replaceAll('"', '&quot;');
}
```

---

### 22. `Promise.any()`

> Resolves on the **first fulfilled** Promise — the opposite of `Promise.all`.

```javascript
const p1 = Promise.reject('Server 1 down');
const p2 = Promise.resolve('Server 2 OK');
const p3 = Promise.resolve('Server 3 OK');

// Promise.any — first to RESOLVE wins
const result = await Promise.any([p1, p2, p3]);
console.log(result); // 'Server 2 OK' — first fulfilled

// Only rejects if ALL promises reject
try {
  await Promise.any([
    Promise.reject('Fail 1'),
    Promise.reject('Fail 2'),
    Promise.reject('Fail 3'),
  ]);
} catch (err) {
  console.log(err instanceof AggregateError); // true
  console.log(err.errors); // ['Fail 1', 'Fail 2', 'Fail 3']
}

// Use case: try multiple CDN endpoints, use whichever responds first
const data = await Promise.any([
  fetch('https://cdn1.example.com/data.json').then(r => r.json()),
  fetch('https://cdn2.example.com/data.json').then(r => r.json()),
  fetch('https://cdn3.example.com/data.json').then(r => r.json()),
]);
```

---

### 23. Logical Assignment Operators — `&&=`, `||=`, `??=`

> Combine logical operators with assignment — short-circuit evaluation.

```javascript
// &&= — assign only if left side is TRUTHY
let a = 1;
a &&= 2;         // a = 2 (a was truthy, so assign)
let b = 0;
b &&= 2;         // b = 0 (b was falsy, so NO assignment)
// Equivalent to: a = a && 2

// ||= — assign only if left side is FALSY
let x = null;
x ||= 'default'; // x = 'default' (x was falsy, so assign)
let y = 'hello';
y ||= 'default'; // y = 'hello' (y was truthy, so NO assignment)
// Equivalent to: x = x || 'default'

// ??= — assign only if left side is NULL or UNDEFINED
let name = null;
name ??= 'Guest'; // name = 'Guest' (null, so assign)
let count = 0;
count ??= 42;     // count = 0 (0 is NOT null/undefined, so NO assignment)
// Equivalent to: count = count ?? 42

// Real-world: initialize object properties lazily
const cache = {};
function getUser(id) {
  cache[id] ??= fetchUser(id); // only fetch if not cached
  return cache[id];
}
```

---

### 24. Numeric Separators — `_`

> Use underscores as visual separators in large numbers — humans can read them.

```javascript
// Hard to read
const million    = 1000000;
const bytes      = 1073741824;
const pi         = 3.14159265358979;

// Easy to read with separators
const million    = 1_000_000;
const bytes      = 1_073_741_824; // 1 GB
const pi         = 3.141_592_653_589_79;

// Works with all number types
const hex   = 0xFF_EC_D9_12;
const binary = 0b1010_0001_1000_0101;
const bigint = 9_007_199_254_740_991n;

// Separator is purely visual — no effect on value
1_000 === 1000 // true
```

---

### 25. `WeakRef` and `FinalizationRegistry`

> Hold a weak reference to an object — doesn't prevent garbage collection.

```javascript
// WeakRef — garbage collector can still collect the object
let obj = { name: 'bigData', size: '500MB' };
const ref = new WeakRef(obj);

// Access the object (if still alive)
const deref = ref.deref();
if (deref) {
  console.log(deref.name); // 'bigData' — still alive
} else {
  console.log('Object was garbage collected');
}

// Nullify the strong reference — obj may now be GC'd
obj = null;

// FinalizationRegistry — run a callback when object is collected
const registry = new FinalizationRegistry((value) => {
  console.log(`${value} was garbage collected`);
});

let target = { data: '...' };
registry.register(target, 'myTarget');
target = null; // may trigger callback eventually
```

---
<a id="es2022-es13"></a>
## ES2022 (ES13) — 2022 &nbsp; <sup>[⬆ Back to Menu](#toc)</sup>

---

### 26. `Array.prototype.at()`

> Access array elements by index — supports negative indices from the end.

```javascript
const fruits = ['apple', 'banana', 'cherry', 'date'];

// Traditional
fruits[0];               // 'apple'
fruits[fruits.length - 1]; // 'date' — verbose for last element

// .at() — cleaner
fruits.at(0);   // 'apple'
fruits.at(-1);  // 'date' — last element
fruits.at(-2);  // 'cherry' — second to last
fruits.at(10);  // undefined (out of range)

// Works on strings and TypedArrays too
'hello'.at(-1); // 'o' — last character

// Common pattern: last item
const last = arr.at(-1);

// Practical use: circular indexing
const days = ['Mon', 'Tue', 'Wed', 'Thu', 'Fri'];
const dayIndex = /* some calculation */ -1;
console.log(days.at(dayIndex)); // 'Fri'
```

---

### 27. `Object.hasOwn()`

> Modern replacement for `Object.prototype.hasOwnProperty.call()`.

```javascript
const user = { name: 'Akshay', age: 30 };

// Old, verbose way
Object.prototype.hasOwnProperty.call(user, 'name'); // true
user.hasOwnProperty('name');                         // true — but unsafe!

// Why unsafe? Object might not inherit from Object.prototype
const nullProto = Object.create(null); // no prototype!
nullProto.key = 'value';
nullProto.hasOwnProperty('key'); // TypeError! hasOwnProperty doesn't exist

// Object.hasOwn() — safe, always works
Object.hasOwn(user, 'name');      // true
Object.hasOwn(user, 'toString');  // false — inherited, not own
Object.hasOwn(nullProto, 'key');  // true ✅ — works on null-proto objects

// Common use: checking if a key was explicitly set
if (Object.hasOwn(config, 'timeout')) {
  applyTimeout(config.timeout);
}
```

---

### 28. Top-Level `await`

> Use `await` directly in ES modules without wrapping in an `async` function.

```javascript
// In an ES module (.mjs or type="module") — top-level await is allowed

// Without top-level await — needed an IIFE
(async () => {
  const config = await fetch('/config.json').then(r => r.json());
  startApp(config);
})();

// With top-level await — clean
const config = await fetch('/config.json').then(r => r.json());
startApp(config);

// Import with top-level await — conditional imports
const module = await (
  process.env.NODE_ENV === 'production'
    ? import('./prod.js')
    : import('./dev.js')
);

// Important: top-level await blocks the importing module
// Other modules importing THIS module wait until this module is done
```

---

### 29. Class Fields — Public, Private, and Static

> Declare class fields directly in the class body — no constructor required.

```javascript
class BankAccount {
  // Public instance field — with default
  currency = 'INR';

  // Private instance field — prefix with #
  #balance = 0;
  #owner;

  // Static field
  static interestRate = 0.035;

  // Private static field
  static #totalAccounts = 0;

  constructor(owner, initialBalance = 0) {
    this.#owner = owner;
    this.#balance = initialBalance;
    BankAccount.#totalAccounts++;
  }

  // Private method
  #validateAmount(amount) {
    if (amount <= 0) throw new Error('Amount must be positive');
  }

  deposit(amount) {
    this.#validateAmount(amount);
    this.#balance += amount;
    return this;
  }

  withdraw(amount) {
    this.#validateAmount(amount);
    if (amount > this.#balance) throw new Error('Insufficient funds');
    this.#balance -= amount;
    return this;
  }

  // Static method
  static getTotalAccounts() {
    return BankAccount.#totalAccounts;
  }

  get balance() { return this.#balance; }
  get owner()   { return this.#owner; }
}

const acc = new BankAccount('Akshay', 1000);
acc.deposit(500).withdraw(200);
console.log(acc.balance);  // 1300
console.log(acc.#balance); // SyntaxError — private!
console.log(BankAccount.getTotalAccounts()); // 1
```

---

### 30. `Error.cause` — Chained Errors

> Attach the original error when rethrowing — preserves error context.

```javascript
// Without cause — you lose the root error
try {
  JSON.parse('invalid');
} catch (err) {
  throw new Error('Failed to parse config'); // root cause lost!
}

// With cause — chain errors
try {
  JSON.parse('invalid json');
} catch (err) {
  throw new Error('Failed to parse config', { cause: err });
}

// Access the cause
try {
  // above code
} catch (err) {
  console.log(err.message);       // 'Failed to parse config'
  console.log(err.cause.message); // 'Unexpected token...'
}

// Practical use: wrap low-level errors with context
async function loadUserProfile(id) {
  try {
    const res = await fetch(`/api/users/${id}`);
    return await res.json();
  } catch (err) {
    throw new Error(`Could not load profile for user ${id}`, { cause: err });
  }
}
```

---
<a id="es2023-es14"></a>
## ES2023 (ES14) — 2023 &nbsp; <sup>[⬆ Back to Menu](#toc)</sup>

---

### 31. `Array.findLast()` and `findLastIndex()`

> Find elements from the end of an array — the reverse of `find` and `findIndex`.

```javascript
const nums = [1, 2, 3, 4, 5, 4, 3];

// find/findIndex — from the START
nums.find(n => n > 3);      // 4  (index 3)
nums.findIndex(n => n > 3); // 3

// findLast/findLastIndex — from the END
nums.findLast(n => n > 3);      // 4  (index 5 — the second 4)
nums.findLastIndex(n => n > 3); // 5

// Practical use: find the last error in a log
const logs = [
  { level: 'info', msg: 'Starting' },
  { level: 'error', msg: 'DB timeout' },
  { level: 'info', msg: 'Retrying' },
  { level: 'error', msg: 'Failed again' },
  { level: 'info', msg: 'Shutdown' },
];
const lastError = logs.findLast(log => log.level === 'error');
// { level: 'error', msg: 'Failed again' }
```

---

### 32. Immutable Array Methods — `toSorted`, `toReversed`, `toSpliced`, `with`

> New non-mutating versions of existing array methods — copy-first approach.

```javascript
const nums = [3, 1, 4, 1, 5, 9, 2, 6];

// toSorted — sorted COPY (sort() mutates original)
const sorted = nums.toSorted((a, b) => a - b);
console.log(sorted); // [1, 1, 2, 3, 4, 5, 6, 9]
console.log(nums);   // [3, 1, 4, 1, 5, 9, 2, 6] — unchanged!

// toReversed — reversed COPY (reverse() mutates)
const reversed = nums.toReversed();
console.log(reversed); // [6, 2, 9, 5, 1, 4, 1, 3]
console.log(nums);     // unchanged!

// toSpliced — spliced COPY (splice() mutates)
const spliced = nums.toSpliced(2, 1, 99); // remove 1 at index 2, insert 99
console.log(spliced); // [3, 1, 99, 1, 5, 9, 2, 6]
console.log(nums);    // unchanged!

// with — return copy with one element replaced
const updated = nums.with(0, 100); // replace index 0 with 100
console.log(updated); // [100, 1, 4, 1, 5, 9, 2, 6]
console.log(nums);    // unchanged!

// Why this matters:
// - Functional/React state patterns — never mutate state
// - Pipeline transformations — chain without side effects
const pipeline = data
  .toSorted((a, b) => a.date - b.date)
  .toReversed()
  .with(0, { ...data[0], pinned: true });
```

---

### 33. `Array.from` with Changeable Length (Shebang `#!` in scripts)

```javascript
// Hashbang (Shebang) — ES2023 formally specifies it
#!/usr/bin/env node
// Node.js script comment — allows direct execution
// Now formally part of spec
```

---
<a id="es2024-es15"></a>
## ES2024 (ES15) — 2024 &nbsp; <sup>[⬆ Back to Menu](#toc)</sup>

---

### 34. `Object.groupBy()` and `Map.groupBy()`

> Group array elements into an object/Map by a key returned from a callback.

```javascript
const products = [
  { name: 'Apple',  category: 'Fruit',  price: 1.5 },
  { name: 'Carrot', category: 'Veggie', price: 0.8 },
  { name: 'Banana', category: 'Fruit',  price: 0.5 },
  { name: 'Broc',   category: 'Veggie', price: 1.2 },
  { name: 'Cherry', category: 'Fruit',  price: 3.0 },
];

// Object.groupBy — group into a plain object
const byCategory = Object.groupBy(products, p => p.category);
// {
//   Fruit:  [ { Apple... }, { Banana... }, { Cherry... } ],
//   Veggie: [ { Carrot... }, { Broc... } ]
// }

// Access a group
byCategory['Fruit'].forEach(p => console.log(p.name)); // Apple, Banana, Cherry

// Group by computed key
const byPriceRange = Object.groupBy(products, p => {
  if (p.price < 1) return 'cheap';
  if (p.price < 2) return 'moderate';
  return 'expensive';
});

// Map.groupBy — when you need non-string keys
const byLength = Map.groupBy(products, p => p.name.length);
// Map { 5 => [...], 6 => [...], ... }

// Old way — had to do this manually with reduce
const manual = products.reduce((acc, p) => {
  acc[p.category] ??= [];
  acc[p.category].push(p);
  return acc;
}, {});
```

---

### 35. `Promise.withResolvers()`

> Create a Promise with its `resolve` and `reject` externally accessible.

```javascript
// Old way — extract resolve/reject via closure (verbose)
let resolve, reject;
const promise = new Promise((res, rej) => {
  resolve = res;
  reject = rej;
});

// Promise.withResolvers() — clean
const { promise, resolve, reject } = Promise.withResolvers();

// Use case: resolve from outside (deferred pattern)
function createTimeout(ms) {
  const { promise, resolve, reject } = Promise.withResolvers();
  const id = setTimeout(() => resolve('timeout!'), ms);
  // Optionally expose cancel
  return { promise, cancel: () => { clearTimeout(id); reject('cancelled'); } };
}

const { promise: timer, cancel } = createTimeout(5000);
// Cancel before it fires
cancel();

// Use case: convert event-based API to Promise
function waitForEvent(emitter, event) {
  const { promise, resolve, reject } = Promise.withResolvers();
  emitter.once(event, resolve);
  emitter.once('error', reject);
  return promise;
}
```

---

### 36. `ArrayBuffer` — `resize()` and `transfer()`

> Resize or transfer the ownership of an `ArrayBuffer`.

```javascript
// Resizable ArrayBuffer
const buf = new ArrayBuffer(1024, { maxByteLength: 4096 });
console.log(buf.byteLength); // 1024

buf.resize(2048); // grow it
console.log(buf.byteLength); // 2048

buf.resize(512);  // shrink it
console.log(buf.byteLength); // 512

// Transfer — move the buffer to a new ArrayBuffer (detaches original)
const buf2 = buf.transfer(); // transfer and clear original
console.log(buf.detached); // true — original is detached
console.log(buf2.byteLength); // 512 — new buffer has the data
```

---
<a id="es2025-es16"></a>
## ES2025 (ES16) — 2025 &nbsp; <sup>[⬆ Back to Menu](#toc)</sup>

---

### 37. `Set` Methods — Union, Intersection, Difference

> Mathematical set operations are now built into JavaScript's `Set`.

```javascript
const a = new Set([1, 2, 3, 4, 5]);
const b = new Set([3, 4, 5, 6, 7]);

// union — all elements from both sets
a.union(b); // Set { 1, 2, 3, 4, 5, 6, 7 }

// intersection — only elements in both
a.intersection(b); // Set { 3, 4, 5 }

// difference — elements in a but not in b
a.difference(b); // Set { 1, 2 }

// symmetricDifference — elements in either but not both
a.symmetricDifference(b); // Set { 1, 2, 6, 7 }

// isSubsetOf — is a a subset of b?
new Set([3, 4]).isSubsetOf(b); // true

// isSupersetOf — is a a superset of b?
a.isSupersetOf(new Set([1, 2])); // true

// isDisjointFrom — do they share no elements?
new Set([8, 9]).isDisjointFrom(a); // true

// Real-world: find common users between two teams
const teamA = new Set(['Alice', 'Bob', 'Carol']);
const teamB = new Set(['Bob', 'Dave', 'Carol']);
const shared = teamA.intersection(teamB); // Set { 'Bob', 'Carol' }
```

---

### 38. `Iterator` Helper Methods

> New methods on iterators for lazy, memory-efficient transformations.

```javascript
// Iterators now have map, filter, take, drop, etc.
// They are LAZY — only compute values as needed

function* numbers() {
  let n = 0;
  while (true) yield n++; // infinite sequence
}

const iter = numbers();

// take — get first N items without loading all
const first5 = iter.take(5).toArray(); // [0, 1, 2, 3, 4]

// map on iterator
const doubled = numbers().map(n => n * 2).take(4).toArray(); // [0, 2, 4, 6]

// filter on iterator
const evens = numbers().filter(n => n % 2 === 0).take(5).toArray(); // [0, 2, 4, 6, 8]

// flatMap on iterator
const pairs = numbers().flatMap(n => [n, n * 10]).take(6).toArray();
// [0, 0, 1, 10, 2, 20]

// drop — skip first N items
const from10 = numbers().drop(10).take(5).toArray(); // [10, 11, 12, 13, 14]

// reduce on iterator
const sum = [1, 2, 3, 4, 5].values().reduce((a, b) => a + b, 0); // 15

// forEach on iterator
numbers().take(3).forEach(n => console.log(n)); // 0, 1, 2

// Important: lazy evaluation — filter+map doesn't process until consumed
const pipeline = numbers()
  .filter(n => n % 2 === 0)  // not evaluated yet
  .map(n => n ** 2)           // not evaluated yet
  .take(4);                   // not evaluated yet
pipeline.toArray();            // NOW it evaluates: [0, 4, 16, 36]
```

---

### 39. `Promise.try()`

> Wrap a synchronous or async function into a Promise — handles both sync throws and async rejections uniformly.

```javascript
// Problem: mixing sync and async error handling
function mayThrowSyncOrAsync(input) {
  if (!input) throw new Error('No input'); // sync error
  return fetch('/api/' + input);           // may reject asynchronously
}

// Without Promise.try — sync error escapes .catch()
Promise.resolve()
  .then(() => mayThrowSyncOrAsync(null)) // sync throw -- caught by .catch below
  .catch(err => console.error(err));     // this works, but it's awkward

// With Promise.try — guaranteed to return a Promise, catches both
Promise.try(() => mayThrowSyncOrAsync(null))
  .catch(err => console.error(err)); // catches BOTH sync throws and async rejects

// Equivalent to wrapping in async function
async function wrapper() {
  return mayThrowSyncOrAsync(null);
}
wrapper().catch(err => console.error(err));

// Real use case: plugin/callback system where the callback might be sync or async
async function runPlugin(plugin, data) {
  return Promise.try(() => plugin.process(data)); // safely wraps whatever plugin does
}
```

---

### 40. `RegExp.escape()`

> Escape a string for safe use as a literal pattern in a RegExp.

```javascript
// Problem: user input in regex can break the pattern
const userInput = 'hello.world'; // . is special in regex!
const regex = new RegExp(userInput); // matches 'helloXworld' too — bug!

// RegExp.escape — escapes all special regex characters
const safe = RegExp.escape(userInput); // 'hello\\.world'
const safeRegex = new RegExp(safe);    // matches only 'hello.world'

// Real-world: search/highlight with user input
function highlight(text, searchTerm) {
  const pattern = new RegExp(RegExp.escape(searchTerm), 'gi');
  return text.replace(pattern, `<mark>$&</mark>`);
}

highlight('Price: $100.00', '$100.00');
// 'Price: <mark>$100.00</mark>' — $ and . are properly escaped
```

---

## 🗂️ Quick Comparison Reference

### Promise Combinators

| Method | Resolves when | Rejects when | Returns |
|--------|--------------|--------------|---------|
| `Promise.all` | All fulfill | **Any** rejects | Array of values |
| `Promise.allSettled` | All settle | Never | Array of `{status, value/reason}` |
| `Promise.race` | First settles (either) | First settles (rejected) | First value/reason |
| `Promise.any` | **First fulfills** | All reject | First value / `AggregateError` |

### `||` vs `??` vs `?.`

| Operator | Triggers on | Use for |
|----------|-------------|---------|
| `\|\|` | Any falsy (`0`, `''`, `false`, `null`, `undefined`) | Default for truly "empty" values |
| `??` | Only `null` / `undefined` | Default that preserves `0`, `false`, `''` |
| `?.` | `null` / `undefined` in chain | Safe property/method access |

### Mutating vs Immutable Array Methods (ES2023)

| Mutating (old) | Immutable copy (ES2023) |
|----------------|------------------------|
| `sort()` | `toSorted()` |
| `reverse()` | `toReversed()` |
| `splice()` | `toSpliced()` |
| `arr[i] = v` | `with(i, v)` |

### `find` vs `findLast`

| Method | Direction | Returns |
|--------|-----------|---------|
| `find(fn)` | Left → Right | First match |
| `findIndex(fn)` | Left → Right | Index of first match |
| `findLast(fn)` | Right → Left | Last match |
| `findLastIndex(fn)` | Right → Left | Index of last match |

---

## 🎯 Interview Quick-Fire

```javascript
// 1. Optional chaining + nullish coalescing combo
const city = user?.address?.city ?? 'Unknown';

// 2. Object transform pipeline
const result = Object.fromEntries(
  Object.entries(obj)
    .filter(([, v]) => v !== null)
    .map(([k, v]) => [k, String(v)])
);

// 3. Flatten + transform
const allTags = posts.flatMap(post => post.tags);

// 4. Group by category
const grouped = Object.groupBy(items, item => item.type);

// 5. Parallel async with error resilience
const results = await Promise.allSettled([fetch(url1), fetch(url2)]);
const successes = results
  .filter(r => r.status === 'fulfilled')
  .map(r => r.value);

// 6. Private class field
class Counter {
  #count = 0;
  increment() { this.#count++; }
  get value() { return this.#count; }
}

// 7. Debounce with logical assignment
opts.delay ??= 300; // only set if null/undefined

// 8. findLast pattern
const lastFailed = jobs.findLast(j => j.status === 'failed');

// 9. Immutable sort
const sorted = [...array].sort(); // old way
const sorted = array.toSorted(); // ES2023 way

// 10. Promise.withResolvers deferred pattern
const { promise, resolve } = Promise.withResolvers();
eventEmitter.once('ready', resolve);
await promise;
```

---

> **Study tip:** Focus on `?.`, `??`, `async/await`, `Promise.all/allSettled/any`, `Object.groupBy`, and class private fields — these come up most in modern JS interviews. Know the difference between `||` and `??`, and between mutating and immutable array methods.

---
<a id="es2026-es17"></a>
## ES2026 (ES17) — 2026 &nbsp; <sup>[⬆ Back to Menu](#toc)</sup>

> Officially approved by ECMA International on **June 30, 2026**. Focus: practical API improvements that reduce boilerplate, improve numeric precision, and make binary data handling first-class.

---
### 41. Temporal API — Modern Date & Time

> The long-awaited replacement for `Date` — immutable, timezone-aware, unambiguous. Reached **Stage 4 in March 2026** (ships in Chrome 144, Firefox 139, Node.js 26).

#### Why `Date` is broken

```javascript
// Problems with the old Date object:
const d = new Date('2024-07-17');
d.getMonth(); // 6 — 0-indexed! July = 6 🤦
d.setFullYear(2025); // MUTATES the object — side-effect bug
new Date('2024-7-17'); // Invalid in some environments — parsing inconsistent
new Date('2024-07-17'); // UTC midnight, but displayed in LOCAL time zone — confusing
```

#### Key Temporal Types

```javascript
// Temporal uses distinct types for distinct concepts — no ambiguity

Temporal.PlainDate      // date only, no time, no timezone
Temporal.PlainTime      // time only, no date, no timezone
Temporal.PlainDateTime  // date + time, no timezone
Temporal.ZonedDateTime  // date + time + timezone (most real-world use)
Temporal.Instant        // a precise moment in time (UTC-based)
Temporal.Duration       // a length of time (years, months, days, hours...)
Temporal.PlainYearMonth // year + month only (e.g. a billing period)
Temporal.PlainMonthDay  // month + day only (e.g. a birthday)
```

#### `Temporal.Now` — Current date/time

```javascript
// Get the current moment
Temporal.Now.instant();           // Instant (UTC)
Temporal.Now.zonedDateTimeISO();  // ZonedDateTime in your local timezone
Temporal.Now.plainDateISO();      // PlainDate today (local tz)
Temporal.Now.plainTimeISO();      // PlainTime right now (local tz)
Temporal.Now.timeZoneId();        // 'Asia/Kolkata' — string ID
```

#### `Temporal.PlainDate` — Date without time

```javascript
// Create — explicit, no ambiguity
const date = Temporal.PlainDate.from({ year: 2026, month: 7, day: 17 });
const date2 = Temporal.PlainDate.from('2026-07-17'); // ISO string

// Properties — all 1-indexed (finally!)
date.year;      // 2026
date.month;     // 7  ← not 6! Months are 1-indexed
date.day;       // 17
date.dayOfWeek; // 5 (1=Mon … 7=Sun)

// Arithmetic — returns a NEW object (immutable!)
const tomorrow = date.add({ days: 1 });       // 2026-07-18
const nextMonth = date.add({ months: 1 });    // 2026-08-17
const lastWeek = date.subtract({ weeks: 1 }); // 2026-07-10

// Compare
date.equals(date2);            // true
Temporal.PlainDate.compare(date, tomorrow); // -1 (date < tomorrow)

// Format
date.toString(); // '2026-07-17'
date.toLocaleString('en-IN', { dateStyle: 'long' }); // '17 July 2026'
```

#### `Temporal.ZonedDateTime` — Full datetime with timezone

```javascript
// The type you'll use most in real apps
const meeting = Temporal.ZonedDateTime.from({
  year: 2026, month: 7, day: 17,
  hour: 10, minute: 30,
  timeZone: 'Asia/Kolkata'
});

meeting.timeZoneId; // 'Asia/Kolkata'
meeting.hour;       // 10
meeting.offset;     // '+05:30'

// Convert to another timezone
const inNY = meeting.withTimeZone('America/New_York');
inNY.hour; // 1 (previous day, EST is -4:30 from IST)

// Arithmetic respects DST transitions automatically
const afterDST = meeting.add({ months: 3 }); // handles daylight saving correctly
```

#### `Temporal.Duration` — Lengths of time

```javascript
const duration = Temporal.Duration.from({ hours: 2, minutes: 30 });

duration.hours;   // 2
duration.minutes; // 30
duration.total('minutes'); // 150

// Arithmetic with dates
const start = Temporal.PlainDate.from('2026-01-01');
const end   = Temporal.PlainDate.from('2026-07-17');
const diff  = start.until(end); // Duration
diff.total('days'); // 197

// Human-readable
duration.toLocaleString('en', { style: 'long' }); // '2 hours, 30 minutes'
```

#### Comparison: `Date` vs `Temporal`

```javascript
// OLD — mutable, confusing months, timezone issues
const old = new Date(2026, 6, 17); // month is 0-indexed — July = 6!
old.setDate(old.getDate() + 7);    // mutates old! Bug-prone.

// NEW — immutable, clear, explicit
const now = Temporal.PlainDate.from({ year: 2026, month: 7, day: 17 }); // 1-indexed
const next = now.add({ days: 7 }); // new object, now is unchanged
```

> 💡 **Interview tip:** Key selling points of Temporal: **immutability**, **1-indexed months**, **explicit timezone handling**, **distinct types per concept** (date vs time vs zoned vs instant), and **correct DST-aware arithmetic**.

---

### 42. `Math.sumPrecise()`

> Sum an iterable of numbers with full floating-point precision — no more accumulation errors.

```javascript
// The classic JavaScript floating-point problem
0.1 + 0.2;                    // 0.30000000000000004 ❌
[0.1, 0.2, 0.3].reduce((a, b) => a + b, 0); // 0.6000000000000001 ❌

// Math.sumPrecise — uses compensated summation algorithm
Math.sumPrecise([0.1, 0.2, 0.3]); // 0.6 ✅ — exact!

// Works with any iterable
Math.sumPrecise(new Set([1, 2, 3]));       // 6
Math.sumPrecise([1e20, 1, -1e20]);         // 1 ✅ (naive sum gives 0 due to precision loss)

// Generator-based
function* range(n) { for (let i = 1; i <= n; i++) yield i; }
Math.sumPrecise(range(100)); // 5050 — exact

// Real-world: financial totals
const lineItems = [19.99, 9.99, 4.99, 0.03];
Math.sumPrecise(lineItems); // 35.00 ✅ — critical for money

// Old workaround — manually scale to integers and divide
const total = lineItems.reduce((sum, n) => sum + Math.round(n * 100), 0) / 100;
```

> 💡 **Interview tip:** `Math.sumPrecise` uses a compensated summation algorithm (similar to Kahan summation) to minimize floating-point rounding errors across any iterable — not just arrays.

---

### 43. `Error.isError()`

> Reliably check if a value is an Error — works across iframes, workers, and realms.

```javascript
// The problem: instanceof breaks across realms (different iframes/workers)
const err = new Error('oops');
err instanceof Error; // true — works in same realm

// In an iframe or worker:
const frameError = iframe.contentWindow.Error;
new frameError('cross-realm') instanceof Error; // false! Different Error constructor

// Error.isError — works across ALL realms
Error.isError(new Error('oops'));      // true
Error.isError(new TypeError('type'));  // true — subclasses too
Error.isError({ message: 'oops' });   // false — plain object, not a real Error
Error.isError('string error');        // false
Error.isError(null);                  // false

// Works cross-realm
Error.isError(new iframe.contentWindow.Error('cross')); // true ✅

// Practical use: error boundary / logging
function logError(value) {
  if (Error.isError(value)) {
    console.error(`[${value.name}] ${value.message}`, value.stack);
  } else {
    console.error('Unknown error:', value);
  }
}
```

---

### 44. `Array.fromAsync()`

> Build an array from an **async iterable** — the async version of `Array.from()`.

```javascript
// Array.from only works with synchronous iterables
Array.from([1, 2, 3]); // [1, 2, 3]

// Array.fromAsync — handles async iterables
async function* asyncGen() {
  yield await Promise.resolve(1);
  yield await Promise.resolve(2);
  yield await Promise.resolve(3);
}

// Must await — returns a Promise
const arr = await Array.fromAsync(asyncGen());
console.log(arr); // [1, 2, 3]

// With a mapping function (like Array.from's second arg)
const doubled = await Array.fromAsync(asyncGen(), x => x * 2);
console.log(doubled); // [2, 4, 6]

// Real-world: consume a paginated API as an async iterable
async function* fetchAllPages(url) {
  let page = 1;
  while (true) {
    const res = await fetch(`${url}?page=${page++}`);
    const { items, hasMore } = await res.json();
    yield* items;
    if (!hasMore) break;
  }
}

const allProducts = await Array.fromAsync(fetchAllPages('/api/products'));
console.log(allProducts); // flat array of every product across all pages

// Also works with sync iterables — just like Array.from
const fromSync = await Array.fromAsync([1, 2, 3]); // [1, 2, 3]
```

---

### 45. `Iterator.concat()`

> Combine multiple iterators into a single lazy sequence — no array creation needed.

```javascript
// Old way — spread into array (loads everything into memory)
const combined = [...iter1, ...iter2, ...iter3];

// Iterator.concat — lazy, no intermediate array
const combined = Iterator.concat(iter1, iter2, iter3);

// Works with any iterable
const all = Iterator.concat(
  [1, 2, 3],
  new Set([4, 5]),
  'abc'           // string is iterable → 'a', 'b', 'c'
);
all.toArray(); // [1, 2, 3, 4, 5, 'a', 'b', 'c']

// Chain with other iterator helpers (lazy throughout)
const result = Iterator.concat(
  getActiveUsers(),  // async generator
  getAdminUsers()
)
  .filter(u => u.age >= 18)
  .map(u => u.name)
  .take(10)
  .toArray();

// Real-world: combine log sources
const allLogs = Iterator.concat(
  readFile('app.log'),
  readFile('error.log'),
  readFile('access.log')
);
for (const line of allLogs) {
  processLogLine(line); // streams through — never all in memory at once
}
```

---

### 46. `Map.prototype.getOrInsert()` and `Map.prototype.getOrInsertComputed()`

> Get a value from a Map, inserting a default if the key is missing — eliminates repetitive `if (!map.has(k))` patterns.

```javascript
// The classic boilerplate pattern
if (!map.has('count')) map.set('count', 0);
map.get('count')++;

// getOrInsert — get value or set+get a default
const map = new Map();

// Returns existing value, or inserts+returns default
map.getOrInsert('count', 0); // 0 (inserted since 'count' was missing)
map.set('count', 5);
map.getOrInsert('count', 0); // 5 (returned existing — default ignored)

// getOrInsertComputed — default is computed lazily (fn only called if key missing)
map.getOrInsertComputed('users', () => []);
map.get('users').push('Akshay'); // ['Akshay']

// WeakMap gets the same methods
const wm = new WeakMap();
const obj = {};
wm.getOrInsert(obj, 'default');              // 'default'
wm.getOrInsertComputed(obj, () => new Map()); // new Map() — key didn't exist

// Real-world: word frequency counter
const freq = new Map();
for (const word of words) {
  freq.getOrInsert(word, 0);
  freq.set(word, freq.get(word) + 1);
}

// Or even cleaner — group items into arrays
const grouped = new Map();
for (const item of items) {
  grouped.getOrInsertComputed(item.category, () => []).push(item);
}
```

---

### 47. `Uint8Array` — Base64 and Hex Encoding

> Native Base64 and Hex conversion on binary data — no more manual atob/btoa workarounds.

```javascript
// Before ES2026 — awkward atob/btoa (string-based, not binary-safe)
const encoded = btoa('Hello'); // 'SGVsbG8='
const decoded = atob('SGVsbG8='); // 'Hello'

// ES2026 — Uint8Array gets native Base64 and Hex methods
const bytes = new Uint8Array([72, 101, 108, 108, 111]); // 'Hello'

// toBase64 / fromBase64
const b64 = bytes.toBase64();
console.log(b64); // 'SGVsbG8='

const restored = Uint8Array.fromBase64('SGVsbG8=');
console.log(restored); // Uint8Array [72, 101, 108, 108, 111]

// setFromBase64 — fill into an existing buffer
const target = new Uint8Array(10);
const { written } = target.setFromBase64('SGVsbG8=');
console.log(written); // 5 — bytes written

// toHex / fromHex
const hex = bytes.toHex();
console.log(hex); // '48656c6c6f' — hex string

const fromHex = Uint8Array.fromHex('48656c6c6f');
console.log(fromHex); // Uint8Array [72, 101, 108, 108, 111]

// Real-world: encode a file for upload or API
async function readAndEncode(file) {
  const buffer = await file.arrayBuffer();
  const bytes = new Uint8Array(buffer);
  return bytes.toBase64(); // send as base64 string in JSON
}

// Options: URL-safe alphabet, omit padding
bytes.toBase64({ alphabet: 'base64url', omitPadding: true });
// 'SGVsbG8' — URL-safe, no padding
```

---

### 48. JSON Improvements — `JSON.parse` Source Access & `JSON.rawJSON`

> Access the raw JSON source in revivers, and create raw JSON values that bypass `JSON.stringify` serialization.

```javascript
// JSON.parse reviver — now receives a 3rd `context` argument with raw source
const result = JSON.parse('{ "price": 9007199254740993 }', (key, value, context) => {
  // context.source = the raw JSON string for this value
  console.log(context.source); // '9007199254740993' — the exact original string
  // Without context, value would already be a JS number (possibly imprecise!)
  if (key === 'price') {
    return BigInt(context.source); // use raw source for precision
  }
  return value;
});
result.price; // 9007199254740993n — exact BigInt, not a rounded Number ✅

// JSON.rawJSON — create a "raw JSON" value that serializes as-is
const rawNum = JSON.rawJSON('9007199254740993');
JSON.stringify({ id: rawNum }); // '{"id":9007199254740993}' — no precision loss!

// Without JSON.rawJSON — precision is lost when stringifying large integers
const bigId = 9007199254740993;
JSON.stringify({ id: bigId }); // '{"id":9007199254740992}' ❌ wrong!

// Real-world: round-trip large IDs from a server (Twitter IDs, database IDs)
const response = await fetch('/api/posts');
const text = await response.text();
const posts = JSON.parse(text, (key, value, { source }) => {
  // Preserve large numeric IDs as BigInt
  if (key === 'id' && source.length > 15) return BigInt(source);
  return value;
});
```

---

## 🗂️ Quick Comparison Reference

### Promise Combinators

| Method | Resolves when | Rejects when | Returns |
|--------|--------------|--------------|---------|
| `Promise.all` | All fulfill | **Any** rejects | Array of values |
| `Promise.allSettled` | All settle | Never | Array of `{status, value/reason}` |
| `Promise.race` | First settles (either) | First settles (rejected) | First value/reason |
| `Promise.any` | **First fulfills** | All reject | First value / `AggregateError` |

### `||` vs `??` vs `?.`

| Operator | Triggers on | Use for |
|----------|-------------|---------|
| `\|\|` | Any falsy (`0`, `''`, `false`, `null`, `undefined`) | Default for truly "empty" values |
| `??` | Only `null` / `undefined` | Default that preserves `0`, `false`, `''` |
| `?.` | `null` / `undefined` in chain | Safe property/method access |

### Mutating vs Immutable Array Methods (ES2023)

| Mutating (old) | Immutable copy (ES2023) |
|----------------|------------------------|
| `sort()` | `toSorted()` |
| `reverse()` | `toReversed()` |
| `splice()` | `toSpliced()` |
| `arr[i] = v` | `with(i, v)` |

### `find` vs `findLast`

| Method | Direction | Returns |
|--------|-----------|---------|
| `find(fn)` | Left → Right | First match |
| `findIndex(fn)` | Left → Right | Index of first match |
| `findLast(fn)` | Right → Left | Last match |
| `findLastIndex(fn)` | Right → Left | Index of last match |

---

## 🎯 Interview Quick-Fire

```javascript
// 1. Optional chaining + nullish coalescing combo
const city = user?.address?.city ?? 'Unknown';

// 2. Object transform pipeline
const result = Object.fromEntries(
  Object.entries(obj)
    .filter(([, v]) => v !== null)
    .map(([k, v]) => [k, String(v)])
);

// 3. Flatten + transform
const allTags = posts.flatMap(post => post.tags);

// 4. Group by category
const grouped = Object.groupBy(items, item => item.type);

// 5. Parallel async with error resilience
const results = await Promise.allSettled([fetch(url1), fetch(url2)]);
const successes = results
  .filter(r => r.status === 'fulfilled')
  .map(r => r.value);

// 6. Private class field
class Counter {
  #count = 0;
  increment() { this.#count++; }
  get value() { return this.#count; }
}

// 7. Debounce with logical assignment
opts.delay ??= 300; // only set if null/undefined

// 8. findLast pattern
const lastFailed = jobs.findLast(j => j.status === 'failed');

// 9. Immutable sort
const sorted = array.toSorted(); // ES2023 — no mutation

// 10. Promise.withResolvers deferred pattern
const { promise, resolve } = Promise.withResolvers();
eventEmitter.once('ready', resolve);
await promise;

// 11. Precise sum (ES2026)
const total = Math.sumPrecise(lineItems); // no floating-point drift

// 12. getOrInsert grouping (ES2026)
const byType = new Map();
for (const item of items) {
  byType.getOrInsertComputed(item.type, () => []).push(item);
}

// 13. Array.fromAsync (ES2026)
const allRows = await Array.fromAsync(db.query('SELECT * FROM users'));
```

---

> **Study tip:** For ES2026 interviews specifically, be ready to explain `Math.sumPrecise` (floating-point precision), `Error.isError` (cross-realm checks), and `Array.fromAsync` (async iterables to arrays). The `Map.getOrInsert` pattern is a cleaner replacement for a very common `if (!map.has(k)) map.set(k, default)` idiom.
