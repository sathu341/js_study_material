<div>
  <h1>Basic of ES6</h1>
<h3>let and Const</h3>
  <ul>
    <li>
let → block-scoped, can be reassigned, cannot be redeclared in the same scope.
    </li>
    <li>
const → block-scoped, cannot be reassigned, must be initialized at declaration.
</li>
    <li>
var (old) → function-scoped, hoisted (can cause bugs).
    </li>
  </ul>
  <pre>
    <code class="lanaguage-js">
      let age = 25;
age = 26; // ✅ allowed

const pi = 3.14;
pi = 3.1415; // ❌ Error
</code>

   
  </pre>
 <h2> Template Literals </h2>
<p>
  Backticks (`) allow embedded variables and multi-line strings.

Syntax: `Hello, ${name}`
</p>
<pre>
  <code class="language-js">
let name = "Sathish";
console.log(`Hello, ${name}! Welcome to ES6.`);
  </code>
  </pre>
  <div>
 <h3>Functions</h3>
 <h4>Arrow Functions</h4>
 <pre>
   <code class="language-js">
      //Shorter syntax, no separate this.

const add = (a, b) => a + b;
console.log(add(2, 3)); // 5

Default Parameters
function greet(name = "Guest") {
  return `Hello, ${name}`;
}
console.log(greet()); // Hello, Guest
   </code>
 </pre>

<h3>
Rest Parameters
</h3>
<pre>
  <code class="language-js">
    //Collects multiple arguments into an array.

function sum(...nums) {
  return nums.reduce((a, b) => a + b, 0);
}
console.log(sum(1, 2, 3)); // 6

  </code>
</pre>
<h3>
Spread Operator
</h3>
<h3>
Expands arrays/objects.
</h3>

<code class="language-js">
  
let arr1 = [1, 2], arr2 = [3, 4];
console.log([...arr1, ...arr2]); // [1,2,3,4]

let obj1 = {a:1}, obj2 = {b:2};
console.log({...obj1, ...obj2}); // {a:1, b:2}
</code>
<h4>
  3. Objects & Arrays
Destructuring
</h4>
<code class="language-js">
const person = { name: "John", age: 30 };
const { name, age } = person;

const numbers = [10, 20];
const [x, y] = numbers;
</code>
<h3>
Object Shorthand
  </h3>
  <code class="language-js">
let username = "Sathish", score = 100;
let player = { username, score };
console.log(player); // {username: "Sathish", score: 100}

for...of Loop

Iterates over iterable objects (arrays, strings, etc).

for (let num of [1,2,3]) {
  console.log(num);
}
</code>
<h3>
  4. Classes & Inheritance
</h3>

<pre>
Class Syntax
class Person {
  constructor(name) {
    this.name = name;
  }
  greet() {
    console.log(`Hi, I’m ${this.name}`);
  }
}
</pre>
<code class="language-js">
Inheritance
class Student extends Person {
  constructor(name, roll) {
    super(name);
    this.roll = roll;
  }
}
let s1 = new Student("Alice", 101);
s1.greet(); // Hi, I’m Alice
</code>

<h3>5. Modules </h3>
<pre>
  <code class="language-js">
Named Export

// file1.js
export const pi = 3.14;

// file2.js
import { pi } from './file1.js';


Default Export

// file1.js
export default function area(r) { return 3.14 * r * r; }

// file2.js
import area from './file1.js';
</pre>
</code>
<h3>6. Advanced Features</h3>
<code class="language-js">
Promises
let promise = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Success"), 1000);
});
promise.then(res => console.log(res)).catch(err => console.log(err));

Async/Await
async function fetchData() {
  let data = await promise;
  console.log(data);
}
fetchData(); // Success

Generators

Functions that can pause and resume.

function* count() {
  yield 1;
  yield 2;
  yield 3;
}
let gen = count();
console.log(gen.next().value); // 1
</code>
<h3>7. Collections
Set
</h3>

<code class="language-js">
Stores unique values.

let s = new Set([1,2,2,3]);
console.log(s); // {1,2,3}

WeakSet

Like Set, but only stores objects, and they are weakly held (garbage collected).

Map

Key-value pairs, keys can be any type.

let m = new Map();
m.set("a", 1);
m.set(2, "two");
console.log(m.get("a")); // 1

WeakMap

Keys must be objects, values are weakly held.
</code>
<pre>
  <code class="language-js">
//8. Other Features
Symbols

Unique identifiers.

let sym1 = Symbol("id");
let sym2 = Symbol("id");
console.log(sym1 === sym2); // false

String Methods
"hello".includes("he"); // true
"world".startsWith("wo"); // true

Number Methods
Number.isInteger(10); // true
Number.isNaN(NaN); // true

Array Methods
[1,2,3].find(n => n > 1); // 2
[1,2,3].findIndex(n => n === 2); // 1
Array.from("123"); // ["1","2","3"]
Array.of(5,10); // [5,10]

Object Methods
let obj = {a:1, b:2};
Object.keys(obj);   // ["a","b"]
Object.values(obj); // [1,2]
Object.entries(obj);// [["a",1],["b",2]]
  </code>
    </pre>
  </div>
</div>
