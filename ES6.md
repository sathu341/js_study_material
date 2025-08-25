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
    <code language="javascript">
      let age = 25;
age = 26; // ✅ allowed

const pi = 3.14;
pi = 3.1415; // ❌ Error

    </code>
  </pre>
</div>
