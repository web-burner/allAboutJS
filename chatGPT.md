# All About JS — Short, Clear Topic Guide

This guide follows the order of your notes. Repeated numbers and repeated topics are kept where they appear. Explanations are short, with illustrative code examples by topic group. Where your notes supplied code, I kept its overall structure and explained the concept around it.

## Milestone 3 — JavaScript fundamentals

### Module 13 — Variables and values

1. **Variable** — A named place to store a value.
2. **Ways to declare a variable** — Use const for values you will not reassign, let for values you will reassign, and var mainly when reading older code.
3. **Update a variable** — Assign a new value to a let or var variable.
4. **const** — Prevents reassignment of the variable binding; an object or array held by const can still be changed.
5. **Data types and typeof** — typeof reports the type of many JavaScript values.
6. **Number** — One type for integers and decimals.
7. **String** — Text written inside quotes.
8. **Boolean** — A true or false value.
9. **JavaScript keyword** — A reserved word with a language meaning, such as let, if, or return.
10. **Variable naming** — Use clear names; JavaScript names are case-sensitive and cannot start with a number.
11. **parseInt(value)** — Reads an integer from a string, such as parseInt("12px") returning 12.
12. **parseFloat(value)** — Reads a decimal number from a string.
13. **Decimals and fractions** — JavaScript Number can represent decimals, but binary floating-point can produce small rounding errors.
14. **toFixed(digits)** — Returns a string rounded to the requested decimal places.
15. **Arithmetic operators** — +, -, *, /, %, and ** mean add, subtract, multiply, divide, remainder, and exponent.
16. **Shorthand arithmetic** — Operators such as += update a variable using its current value.
17. **isNaN(value)** — Tests whether a value is Not-a-Number; Number.isNaN is stricter and often safer.
18. **undefined** — A value usually meaning that no value was assigned or a property is missing.
19. **null** — An intentional “no value” marker.
20. **Number** — The built-in numeric type and Number conversion helper; for example Number("42") gives 42.

~~~js
let score = 10;
score += 5;
const message = "Score: " + score;
console.log(score, typeof score, message);
~~~

### Module 14 — Conditions

21. **Greater than (>)** — True when the left value is larger.
22. **Less than (<)** — True when the left value is smaller.
23. **Equal (=)** — A single equals sign assigns a value; use === or == to compare values.
24. **Greater than or equal (>=)** — True when the left value is at least as large.
25. **Less than or equal (<=)** — True when the left value is no larger.
26. **Not equal (!=)** — Loose inequality; !== avoids type conversion and is usually preferred.
27. **AND (&&)** — True only when both conditions are truthy.
28. **OR (||)** — True when either condition is truthy.
29. **NOT (!) ** — Flips a truthy value to false or a falsy value to true.
30. **if/else** — Runs one block when a condition is true and another when false.
31. **Nested if/else** — A condition inside another condition.
32. **AND** — Combine requirements, for example age >= 18 && hasId.
33. **OR** — Accept either condition, for example isAdmin || isOwner.
34. **if/else if/else** — Checks several conditions in order, then uses a fallback.
35. **Nested if/else** — Useful for dependent decisions; avoid deep nesting when a clearer condition works.
36. **Ternary operator** — A compact expression: condition ? valueIfTrue : valueIfFalse.
37. **Logical NOT (!) ** — Use !condition to test the opposite, or !!value to convert to a boolean.

~~~js
const age = 20;
if (age >= 18 && age < 65) {
  console.log("Adult");
} else {
  console.log("Outside this range");
}
const label = age >= 18 ? "adult" : "minor";
~~~

### Module 15 — Loops and arrays

38. **for...of loop** — Visits each value in an iterable such as an array.
39. **while loop** — Repeats while its condition remains true.
40. **Increment (++)** — Adds one to a number.
41. **Infinite loop** — A loop whose condition never becomes false; it can freeze a program.
42. **Even number** — An integer divisible by 2; number % 2 === 0.
43. **Odd number** — An integer with remainder 1 when divided by 2.
44. **Sum** — The result of adding values.
45. **for loop** — Combines initialization, condition, and update in one loop header.
46. **Find even/odd values in a loop** — Check each value with remainder: value % 2.
47. **Find divisible values in a loop** — Use value % divisor === 0.
48. **Sum using a loop** — Start a total at 0 and add each value.
49. **break** — Exits the nearest loop immediately.
50. **continue** — Skips the rest of this iteration and moves to the next one.
51. **do...while** — Runs the body once before checking the condition.
52. **Array length** — The number of elements in an array.
53. **Array index** — A position number starting at 0.
54. **Read an array item** — Use arrayName[index].
55. **Set/update an item** — Assign to arrayName[index].
56. **push** — Adds an item to the end and returns the new length.
57. **pop** — Removes and returns the last item.
58. **shift** — Removes and returns the first item.
59. **unshift** — Adds item(s) at the start.
60. **Array method** — A built-in operation that reads or changes an array.
61. **includes** — Checks whether an array contains a value.
62. **indexOf** — Returns the first matching index, or -1 when absent.
63. **Array.isArray** — Checks whether a value is an array.
64. **join** — Combines array items into a string with a separator.
65. **concat** — Returns a new array combining arrays or values.
66. **slice** — Returns a shallow copy of a selected range; it does not change the original.
67. **splice** — Adds/removes items in place and changes the original array.

~~~js
const numbers = [2, 5, 8];
let sum = 0;
for (const number of numbers) {
  if (number % 2 === 0) sum += number;
}
console.log(sum, numbers.includes(5), numbers.slice(0, 2));
~~~

### Module 16 — Strings and objects

68. **String length** — Number of UTF-16 code units in the string.
69. **String element access** — Read a character with text[index] or text.at(index).
70. **toLowerCase** — Returns a lowercase copy.
71. **toUpperCase** — Returns an uppercase copy.
72. **trim** — Returns a copy without whitespace at the start or end.
73. **Strings are immutable** — String methods return new strings; they do not edit the original.
74. **String slice** — Returns part of a string without changing the original.
75. **split** — Splits a string into an array using a separator.
76. **join** — Joins an array of strings into one string.
77. **concat** — Combines strings; + or template strings are also common.
78. **includes** — Checks whether a string contains another string.
79. **Reverse a string** — There is no built-in reverse for strings; split, reverse, then join.
80. **Object** — A collection of named properties.
81. **Properties and values** — A property is a key; its value is the data stored under that key.
82. **Primitive/non-primitive** — Primitives include numbers and strings; objects and arrays are reference values.
83. **Dot notation** — Read/write a known property with object.key.
84. **Bracket notation** — Use object[key], useful for dynamic or unusual property names.
85. **Set a property** — Assign a value to an existing or new key.
86. **Update a property** — Assign a different value to an existing key.
87. **Object.keys** — Returns an array of an object's own enumerable keys.
88. **Object.values** — Returns the corresponding values.
89. **Nested object** — An object stored as a property of another object.
90. **delete** — Removes a property from an object.
91. **for...in** — Iterates enumerable property names; check ownership when inherited properties matter.
92. **Object literal** — The usual direct form: const user = { name: "Ari" }.
93. **new keyword** — Calls a constructor to create an instance, e.g. new Date().
94. **Object.create** — Creates an object with a chosen prototype.

~~~js
const user = { name: "Ari", address: { city: "Kuala Lumpur" } };
user.name = "Mina";
console.log(user["address"].city);
console.log(Object.keys(user), Object.values(user));
~~~

## Milestone 4 — Arrays, functions, and problem solving

### Module 18 — Traversing and copying arrays

95. **Loop through an array with for...of** — Read one array value per iteration.
96. **Reverse with unshift** — Build a new array by adding each old value to its front.
97. **reverse()** — Reverses an array in place and returns that same array.
98. **sort()** — Sorts an array in place; provide a comparator for numeric sorting.
99. **Ascending/descending** — Compare values with a sort callback, e.g. (a, b) => a - b or b - a.
100. **Array of objects** — An array where each entry is an object, often used for records.
101. **Access an object in an array** — Read array[index].property.
102. **2D array** — An array whose elements are arrays.
103. **Access a 2D array item** — Use array[row][column].
104. **Copy an array** — Make a new shallow array so later edits to its top-level positions are separate.
105. **Array.from()** — Creates an array from an iterable or array-like value.
106. **Copy with concat** — Use oldArray.concat() to create a shallow copy.
107. **Copy with spread** — Use [...oldArray] for a shallow copy.

### Module 19 — Functions

108. **Function** — A reusable block of code that can receive values and return a result.
109. **Declare a function** — Use a function declaration, function expression, or arrow function.
110. **Parameter** — A named input in a function definition.
111. **Multiple parameters** — Separate inputs with commas.
112. **Argument** — The actual value passed when calling a function.
113. **Arguments vs parameters** — Parameters are names in the definition; arguments are values at the call.
114. **return** — Sends a result back and ends that function call.
115. **Store a return value** — Assign the function call result to a variable.
116. **Conditional odd/even return** — Return a different value depending on number % 2.
117. **Parameter types** — Inputs may be required, defaulted, rest parameters, or destructured.
118. **Sum an array with a function** — Loop through values or use reduce to accumulate them.
119. **Return even array values** — Use filter with a remainder check.

~~~js
function sum(values) {
  return values.reduce((total, value) => total + value, 0);
}
const evenNumbers = [1, 2, 3, 4].filter((number) => number % 2 === 0);
~~~

### Module 20 — Problem solving part 1

120. **Inches to feet** — Divide inches by 12.
121. **Miles to kilometers** — Multiply miles by 1.60934.
122. **Leap year** — Divisible by 4, except century years unless divisible by 400.
123. **Average of odd numbers** — Filter odd values, sum them, then divide by their count; handle an empty result.
124. **Remove duplicates** — Set removes repeated primitive values: [...new Set(values)].
125. **Math object** — Provides common numeric functions and constants.
126. **Math.abs** — Returns a non-negative distance from zero.
127. **Math.round** — Rounds to the nearest integer.
128. **Math.ceil** — Rounds upward to the next integer.
129. **Math.floor** — Rounds downward to the previous integer.
130. **Math.random** — Returns a pseudo-random number from 0 inclusive to 1 exclusive.
131. **Minimum number** — Math.min(a, b) returns the smallest input.
132. **Maximum number** — Math.max(a, b) returns the largest input.
133. **Date and time** — Date represents a moment in time.
134. **Today/specific date** — new Date() is now; pass a date string or timestamp for a chosen date.
135. **Get/set date parts** — Date methods read or change day, date, month, and year; month indexes start at 0.
136. **Get time** — Date methods can read hours/minutes or return milliseconds since the epoch.
137. **toLocaleDateString** — Formats a date for a locale.
138. **toLocaleTimeString** — Formats a time for a locale.
139. **toLocaleString** — Formats date and time for a locale.
140. **Swap variables/destructuring** — Destructuring can swap values: [a, b] = [b, a].

### Module 21 — Problem solving part 2

141. **Highest marks** — Track the student with the greatest score or sort/compare records.
142. **Maximum in an array** — Use Math.max(...numbers) for a modest array or loop for any size.
143. **Wood calculation** — Multiply each material count by its wood-per-item rate, then add.
144. **Cheapest phone** — Use reduce or sort to compare prices in an array of objects.
145. **Shopping cart total** — Sum each item's price multiplied by quantity.
146. **Multi-layer discounts** — Apply each discount in order to the current price.
147. **Calculator calling functions** — One function can select and call an operation function.
148. **Validate function inputs** — Check types and allowed ranges before calculating.

### Module 22.5 — Bonus objects

149. **Nested object** — Access deeper data with chained keys, e.g. user.address.city.
150. **Object values can be arrays, objects, or functions** — Objects can group related data and behavior.
151. **arguments object** — In regular functions, arguments is array-like; use rest parameters for a real array and clearer behavior.
152. **Search matching products** — Use find for one match or filter for all matches.

## Milestone 5 — Interactive JavaScript and the DOM

### Module 24 — Tour of the DOM

153. **Link HTML to CSS** — A link element loads an external stylesheet.
154. **Link JavaScript to HTML** — A script element with src loads an external script.
155. **DOM** — The browser's object model of the page that JavaScript can inspect and change.
156. **document** — The page's main DOM entry point.
157. **getElementsByTagName** — Finds matching elements and returns a live HTMLCollection.
158. **Loop an HTMLCollection** — for...of can visit each element.
159. **getElementsByClassName** — Finds elements with a class; returns a live collection.
160. **getElementById** — Finds the element with a matching id.
161. **innerText** — Reads or sets rendered text.
162. **querySelectorAll** — Returns a static NodeList matching a CSS selector.
163. **NodeList vs HTMLCollection** — Both hold node references; HTMLCollection is usually live, while querySelectorAll's NodeList is static.
164. **querySelector** — Returns the first element matching a CSS selector, or null.
165. **Dynamic style** — Change style properties or, usually, toggle CSS classes.
166. **getAttribute** — Reads an HTML attribute.
167. **setAttribute** — Adds or changes an HTML attribute.
168. **innerText** — Sets visible text without treating it as HTML.
169. **innerHTML** — Reads/writes markup; only use trusted content to avoid injection risks.
170. **classList** — add, remove, or toggle CSS classes.
171. **NodeList** — A list-like collection of DOM nodes.
172. **HTMLCollection** — A live list-like collection of elements.
173. **parentNode** — Gets a node's parent.
174. **childNodes** — Gets all child nodes, including text nodes.
175. **createElement** — Creates a new DOM element.
176. **appendChild/append** — Adds node(s) at the end of an element.

### Module 25 — Events

177. **Event** — A signal that something happened, such as a click or key press.
178. **Event types** — Common groups are mouse, keyboard, form, focus, and load events.
179. **Inline event** — An HTML attribute like onclick; addEventListener is generally easier to maintain.
180. **addEventListener** — Registers a function to run for a named event.
181. **onclick()** — Usually means calling a function; for handling clicks, use an event listener or onclick property.
182. **element.onclick = function** — Assigns one click handler property.
183. **element.onclick = functionName** — Assigns a named function as the handler, without calling it.
184. **getElementById + addEventListener** — Find the target element, then attach its handler.
185. **Mouse/keyboard/form events** — Events describe user input such as click, keydown, submit, or change.
186. **event.target** — The element where the event originated.
187. **event.key** — The key value for keyboard events.
188. **event.type** — The event name, such as click or submit.
189. **Named function** — A function with a name, useful for reuse and debugging.
190. **Anonymous function** — A function expression without its own name.
191. **Callback function** — A function passed to be called later by another function.
192. **Input value** — Read text input using input.value.
193. **Comment box** — Read the form input, create a text node/element, and append it to the comments area.
194. **Delete confirmation** — Ask for confirmation or provide an undo step before removing data.
195. **mouseenter** — Fires when the pointer enters an element.
196. **mousemove** — Fires as the pointer moves over an element.
197. **mouseout** — Fires when the pointer leaves an element or one of its descendants.
198. **focus** — Fires when an element receives focus.
199. **blur** — Fires when an element loses focus.
200. **keydown** — Fires when a key is pressed down.
201. **keyup** — Fires when a key is released.
202. **Event bubbling** — An event travels from its target up through ancestor elements.
203. **Event object** — Contains details about the event and methods to control it.
204. **stopPropagation** — Stops the event from continuing through the propagation path.
205. **stopImmediatePropagation** — Also stops other listeners on the same element from running.
206. **Event delegation** — Handle many child events with one listener on a shared parent.
207. **tagName** — The element's tag name, usually uppercase in HTML documents.
208. **removeChild** — Removes a child node from its parent.

~~~js
const list = document.querySelector("#items");
list.addEventListener("click", (event) => {
  if (event.target.tagName === "BUTTON") {
    event.target.closest("li").remove();
  }
});
~~~

### Module 26 — Forms, styles, and browser APIs

209. **Connect Tailwind CSS** — Add and configure Tailwind so its utility classes are included in the page.
210. **Connect DaisyUI** — Add its plugin/theme on top of Tailwind.
211. **Login form with Tailwind/DaisyUI** — Build the form UI with utility classes and components.
212. **Style and listen to login form** — Attach submit handling with addEventListener.
213. **Connect a JS folder** — Use a correct relative script path.
214. **Login button behavior** — Read input values, validate them, then handle success/failure.
215. **type="button"** — A button that does not submit its form by default.
216. **e.preventDefault()** — Prevents the browser's default event action, such as form navigation.
217. **Check mobile number and PIN** — Validate values before continuing; client checks do not replace server-side security.
218. **window.location.href** — Reads or changes the current page URL.
219. **Navbar style** — Use CSS classes and responsive layout rules.
220. **e.target.tagName** — Reads the clicked element's tag.
221. **e.target.className** — Reads or sets the element's class attribute.
222. **e.target.id** — Reads or sets the element's id.
223. **closest** — Finds the nearest ancestor (or self) matching a selector.
224. **navigator** — Browser APIs and information are exposed through this object.
225. **clipboard** — The Clipboard API can read/write clipboard data with browser permission/security requirements.
226. **writeText()** — Writes text to the clipboard; usually call navigator.clipboard.writeText(text).
227. **then/catch** — Handle a promise's success and failure.
228. **isArray** — Array.isArray(value) checks for an array.
229. **isNaN** — Tests whether a value is not a valid number; prefer Number.isNaN for strict checking.

## Milestone 6 — ES6 and JavaScript behavior

230. **const** — Block-scoped binding that cannot be reassigned.
231. **let** — Block-scoped binding that can be reassigned.
232. **var** — Function-scoped legacy declaration; avoid for new code.
233. **const arrays/objects** — The binding stays fixed, but their contents can still be mutated.
234. **Default parameter (=)** — Supplies a value when an argument is missing or undefined.
235. **Template string** — Backtick-delimited string supporting interpolation and multiple lines.
236. **Newline (\n)** — Inserts a line break in a string.
237. **variable** — Inserts an expression inside a template string.
238. **Arrow function** — A shorter function syntax with lexical this.
239. **Multiple parameters** — Separate parameter names with commas.
240. **Arrow body (=>)** — Use braces for statements; a single expression may be returned implicitly.
241. **Function declaration** — A named function declaration, available throughout its scope due to hoisting rules.
242. **Function expression** — A function stored in a variable or passed as a value.
243. **Anonymous arrow function** — An arrow function without a separate function name.
244. **Implicit return** — An expression-bodied arrow returns that expression automatically.
245. **Arrow this behavior** — Arrow functions inherit this from the surrounding scope; they do not create their own.
246. **Arrow arguments behavior** — Arrow functions have no own arguments object; use rest parameters.
247. **Spread operator (...)** — Expands iterable items or enumerable object properties into a new context.
248. **Array maximum** — Math.max(...numbers) works for smaller arrays; reduce avoids large argument lists.
249. **Copy array** — Spread or Array.from makes a shallow copy.
250. **Spread array in a function call** — Passes array entries as separate arguments.
251. **Copy object** — Use {...object} for a shallow copy.
252. **Destructuring** — Extracts values from arrays or properties from objects.
253. **Object destructuring** — Uses property names as variable names by default.
254. **Array destructuring** — Uses position/index order.
255. **Alias** — Rename a destructured value, e.g. const { name: userName } = user.
256. **Object.keys** — Gets property names.
257. **Object.values** — Gets property values.
258. **Object.entries** — Gets [key, value] pairs.
259. **delete** — Removes an object property.
260. **Object.seal** — Prevents adding/removing properties, but existing writable values can change.
261. **Object.freeze** — Prevents direct changes to an object's own properties; it is shallow.
262. **Access object value** — Use dot or bracket notation.
263. **Dot/bracket notation** — Choose brackets for a computed key or keys that are not valid identifiers.
264. **Optional chaining (?)** — ?. safely stops a property chain when the left side is null or undefined.
265. **map/filter/find/forEach/reduce** — Transform, select many, find one, run side effects, or accumulate values.
266. **class** — Syntax for creating objects with shared methods and constructor logic.
267. **constructor** — Initializes each class instance.
268. **Class properties** — Data associated with a class or its instances.
269. **Class method** — A function defined on a class's prototype.
270. **this** — Refers to a value determined by how a function is called; class methods usually use their instance.
271. **instanceof** — Checks whether an object inherits from a constructor's prototype.
272. **Inheritance** — Lets one class reuse/extend another class's behavior.
273. **Prototype inheritance** — JavaScript objects can inherit properties through a prototype chain.
274. **extends** — Declares a derived class.
275. **super(...)** — Calls the parent constructor; in a derived constructor it must run before using this.
276. **Encapsulation** — Keeps implementation details behind a controlled interface.
277. **Data types** — JavaScript values have types such as string, number, boolean, bigint, symbol, undefined, and object.
278. **Primitive** — An immutable value type such as string, number, boolean, bigint, symbol, null, or undefined.
279. **Non-primitive** — Objects, including arrays and functions, are reference values.
280. **Immutable** — A value cannot be changed in place; strings and primitives are immutable.
281. **Mutable** — An object can have properties/elements changed.
282. **Find null/undefined** — typeof null is "object" (a historical quirk); use value === null or value === undefined.
283. **Truthy/falsy** — Conditions coerce values; false, 0, "", null, undefined, and NaN are falsy.
284. **Double equals (==)** — Compares after coercion in many cases.
285. **Triple equals (===)** — Compares without coercing types; generally preferred.
286. **Implicit conversion** — JavaScript may convert types automatically during operations.
287. **Block/global scope** — let/const are block scoped; global bindings are available broadly, subject to modules and runtime.
288. **Hoisting** — Declarations are processed before execution, but initialization behavior differs by declaration type.
289. **Temporal dead zone** — Accessing let/const before their declaration throws a ReferenceError.
290. **Callback** — A function supplied to another function to run later.
291. **Pass by value/reference** — Parameters receive values; object values are references, so mutation can affect the same object.
292. **arguments keyword** — Array-like input collection in regular functions; rest parameters are clearer.
293. **Closure** — A function retains access to variables from the scope where it was created.
294. **Increment/decrement (++/--)** — Increase/decrease a number by one.

### Internet and data exchange

295. **Internet** — A global network of connected devices and networks.
296. **How the internet works** — Devices send packets using shared protocols through routers and networks.
297. **IP address** — A numeric address used to identify a network interface.
298. **IPv4/IPv6** — Two IP formats; IPv6 provides a much larger address space.
299. **DNS** — The Domain Name System maps domain names to network records such as IP addresses.
300. **How DNS works** — Resolvers query DNS servers/cache to find the needed record.
301. **HTTP** — A request/response protocol used by web clients and servers.
302. **HTTP layers** — Web traffic uses HTTP on top of transport/network protocols; HTTP itself defines requests and responses.
303. **HTTPS** — HTTP protected by TLS encryption and server authentication.
304. **JSON** — A text format for exchanging structured data.
305. **JSON.stringify()** — Converts a JavaScript value to JSON text.
306. **JSON.parse()** — Converts valid JSON text to a JavaScript value.
307. **Fetch JSON** — fetch returns a promise; check the response and parse it with response.json().
308. **Show data on click** — Attach a click handler and render the loaded value.
309. **Display post titles** — Map the posts array to title elements.
310. **Display styled cards** — Map data into repeated card markup and style with CSS.
311. **To-do list and conditional rendering** — Store tasks in state and show elements based on task state.
312. **GET** — Requests a resource.
313. **POST** — Sends data, often to create a resource.
314. **PUT** — Replaces a resource representation.
315. **PATCH** — Partially updates a resource.
316. **DELETE** — Requests resource removal.
317. **Status codes** — 200 success; 301/302 redirect; 404 not found; 500 server error; 503 unavailable.
318. **async/await** — Syntax for working with promises in an async function.
319. **Synchronous** — Work proceeds one step at a time; each step finishes before the next.
320. **Asynchronous** — Work can finish later while the program handles other tasks.
321. **Modal** — A dialog layer that asks the user to interact before returning to the page.
322. **Utterance/speech** — SpeechSynthesisUtterance represents text for the browser speech synthesis API.

### JavaScript engine and asynchronous behavior

323. **JavaScript** — A programming language used in browsers and server runtimes.
324. **High abstraction** — Hides low-level machine details behind accessible language features.
325. **Garbage collection** — Runtime reclaims memory that is no longer reachable.
326. **JIT compiled** — Engines may compile frequently used code during execution for speed.
327. **Call stack memory** — Stack frames track active function calls and local execution.
328. **Multi-paradigm** — JavaScript supports procedural, functional, and object-oriented styles.
329. **Prototype-based** — Objects can inherit from other objects through prototypes.
330. **Dynamically typed** — A variable can hold values of different types at different times.
331. **V8 engine** — Google's JavaScript engine used in Chrome and Node.js.
332. **Execution context** — Runtime environment for global code or a function call.
333. **Call stack** — Last-in, first-out stack of function calls currently executing.
334. **Single-threaded with async APIs** — JavaScript runs a main execution thread, while host APIs handle many asynchronous operations.
335. **setTimeout/clearTimeout** — Schedule one callback after a minimum delay; clearTimeout cancels it using its timer ID.
336. **Promise.all** — Waits for all promises to fulfill, or rejects when one rejects.
337. **Promise states** — pending, fulfilled (resolved), or rejected.
338. **async/await** — await pauses that async function until a promise settles; it does not block the whole JavaScript thread.
339. **try/catch** — Catches synchronous errors and errors thrown while awaiting promises.
340. **Promise hell** — Deeply nested promise callbacks; chaining or async/await improves readability.
341. **setInterval/clearInterval** — Repeats a callback on a timer until cleared.
342. **Event loop/concurrency** — Runtime schedules queued callbacks when the call stack is available.
343. **Event queue** — Holds callbacks waiting for the event loop to run them.

### Local storage

344. **localStorage** — Browser storage that persists across reloads for the same origin.
345. **setItem** — Saves a string by key.
346. **getItem** — Reads a stored string; returns null when absent.
347. **removeItem** — Removes a stored key.
348. **JSON.stringify for storage** — Convert objects to strings before storing.
349. **Store/read objects** — stringify on save, parse on read, and handle missing or invalid data.
350. **JSON.parse from storage** — Converts a stored JSON string back to a value.

~~~js
const saved = localStorage.getItem("cart");
const cart = saved ? JSON.parse(saved) : [];
localStorage.setItem("cart", JSON.stringify(cart));
~~~

## Milestone 7 — React core concepts

### React overview list

352. **React** — A JavaScript library for building user interfaces from components.
353. **Component** — A reusable piece of UI, usually a function returning JSX.
354. **Capitalized component name** — React treats lowercase JSX names as HTML tags.
355. **JSX markup** — HTML-like syntax transformed into JavaScript.
356. **XML** — A markup format with explicit tags; JSX resembles XML syntax.
357. **JSX rules** — Return one root, close tags, use valid expressions, and use React attribute names.
358. **Fragment** — Groups sibling JSX without adding a DOM element.
359. **camelCase attributes** — JSX uses names like onClick and className.
360. **Curly braces** — Insert a JavaScript expression in JSX.
361. **Return JSX** — A component returns its UI inside parentheses when multiline.
362. **Style in JSX** — Use className or a JavaScript style object with camelCase properties.
363. **Set a parameter** — Function components receive props as their first parameter.
364. **Props** — Inputs passed from a parent component.
365. **Read props** — Use props.name or destructure { name }.
366. **Destructuring** — Pull properties into local variables.
367. **Read-only props/conditional rendering** — Props should not be changed by the receiving component; choose UI based on conditions.
368. **Six conditional rendering approaches** — if, if/else, ternary, &&, ||, or a variable holding selected JSX.
369. **map method** — Converts each array item to a new result.
370. **Return a component with map** — Map data to JSX elements.
371. **Pass values with map** — Supply each item as a prop and use a stable key.
372. **vite.config** — Vite project configuration, including plugins.
373. **package.json** — Project metadata, scripts, and dependency versions.
374. **index.html** — Vite's HTML entry document.
375. **ESLint** — Finds likely code problems and style issues.
376. **src folder** — Holds application source files.

### Module 36 — React core concept part 1

377. **What is React?** — React builds interfaces from components and updates the DOM efficiently using its rendering system.
378. **Create a React project** — Use Vite's project generator, choose React and JavaScript, then install dependencies.
379. **What is a component?** — A UI building block that returns JSX.
380. **Component types** — Common types include function components and class components; function components are standard in modern React.
381. **Component syntax** — Capitalize its name, return JSX, and export it if other files need it.

~~~jsx
const Component = () => {
    return (
        <div>

        </div>
    );
};

export default Component;
~~~

382. **What is JSX?** — A JavaScript syntax extension for describing UI with markup-like elements.
383. **JSX rules** — Return one root element or fragment, close tags, and use JSX attribute names.
384. **Dynamic JSX content** — Put JavaScript expressions inside curly braces.
385. **Style with a variable** — Pass a style object or a class name.

~~~jsx
const Component = () => {
  const comStyle = { border: "2px solid red" };
  return <div style={comStyle}></div>;
};

export default Component;
~~~

386. **Props example** — A parent passes attributes; the child reads them from props.

~~~jsx
function App() {
  return (
    <>
      <Player name="Shaon"></Player>
      <Player name="Sajjat"></Player>
    </>
  );
}

const Player = (props) => {
  return <p>name: {props.name}</p>;
};

export default App;
~~~

387. **Pass/read props and defaults** — Destructure properties in the parameter; default values can be supplied there.

~~~jsx
function App() {
  return (
    <>
      <Player name="Shaon" game="Football"></Player>
      <Player name="Sajjat" game="Football"></Player>
    </>
  );
}

const Player = ({ name, game }) => {
  return (
    <>
      <p>name: {name}</p>
      <p>name: {game}</p>
    </>
  );
};
~~~

388. **Read-only props/conditional rendering** — Export and import components across files; choose UI with a condition without mutating props.
389. **Six ways to conditionally render** — if, if/else, ternary, &&, ||, and a variable containing JSX.
390. **Render lists with map** — Map array entries to components and provide a stable key, preferably a unique data id.

~~~jsx
function App() {
    const players = ["Sakib", "Tamim", "Mushfiq", "Mahmudullah", "Mashrafi"];

    return (<>
    {players.map((player, ind) => (
    <Players key={ind} player={player}></Players>
    ))}</>);
}
~~~

### Module 37 — State, events, effects, and data

391. **vite.config.js** — Configures Vite and its plugins.
392. **package.json** — Lists scripts, installed packages, and version ranges.
393. **ESLint** — Reports code issues such as unused variables or syntax problems.
394. **App.jsx** — Often the top-level application component; project structure can vary.
395. **React event handling** — Pass a handler to onClick; wrap it in an arrow when you need to pass arguments.

~~~jsx
function App() {
  const handleEvent = (name) => {
    console.log("Hello " + name);
  };
  return (
    <>
      <button
        style={{ border: "1px solid tomato", padding: "10px" }}
        onClick={() => handleEvent("Shaon")}
      >
        Event Button
      </button>
    </>
  );
};
~~~

396. **useState** — Returns a state value and a setter; calling the setter requests a re-render.

~~~jsx
function App() {
  const [count, setCount] = useState(0);
  const handleEvent = (name) => {
    console.log("Hello " + name);
    const newCount = count + 1;
    setCount(newCount);
  };
  return (
    <>
      <button
        style={{ border: "1px solid tomato", padding: "10px" }}
        onClick={() => handleEvent("Shaon")}
      >
        Event {count}
      </button>
    </>
  );
}
~~~

397. **Suspense** — Shows fallback UI while a supported child is waiting for a resource.
398. **fallback** — The placeholder React renders while the suspended content is not ready.
399. **use hook** — In supported React versions, reads a promise or context during rendering.
400. **Dynamic data with use()** — Fetch/create a promise, pass it to a child, then read the resolved value with use().
401. **Load data with async/await** — await fetch and response.json() inside an async function; handle errors and HTTP status.
402. **useEffect** — Runs side effects after rendering, such as subscriptions or client-side data loading.
403. **Effect dependencies** — Values read from outside the effect belong in the dependency array; an empty array means run after mount, and omitted dependencies mean run after every render.

### JavaScript fundamentals recap for React (the source repeats numbering 352–376)

352. **let/const** — Choose variable declarations based on whether reassignment is needed.
353. **if/else** — Branch the program based on a condition.
354. **Logical conditions** — Combine checks with && and ||.
355. **Array** — Ordered collection of values.
356. **Array properties/string trim** — length belongs to arrays and strings; trim is a string method, not an array method.
357. **Array index** — Use a zero-based position.
358. **Array/string methods** — push/pop/shift/unshift edit arrays; slice/splice select or edit; case methods, includes, map, forEach, filter, find, and reduce handle strings/arrays.
359. **Loops** — for, for...in, for...of, while, and do...while repeat work in different ways.
360. **Function/return** — Reusable logic can return a result.
361. **Function arguments** — Values supplied when a function is called.
362. **Object access** — Read a property's value using dot or bracket notation.
363. **Update object values** — Assign a new value to the property.
364. **Template string** — Embed expressions in a string.
365. **Arrow function** — A compact function form with lexical this.
366. **Rest parameter** — Collect remaining arguments into an array with ...name.
367. **Spread** — Expands values into arrays, objects, or function calls.
368. **Destructuring** — Extract values from arrays or objects.
369. **JSON stringify/parse** — Convert between JS values and JSON text.
370. **fetch** — Make HTTP requests and receive a promise.
371. **Object keys/values** — Object.keys/values return arrays.
372. **Array add/remove with spread** — Create a new array with additions or filtered-out items.
373. **Truthy/falsy** — Values are coerced to booleans in conditions.
374. **Ternary/AND/OR shortcuts** — Compactly choose or conditionally show values.
375. **localStorage/sessionStorage** — Browser storage; sessionStorage is scoped to a tab session.
376. **Dot/bracket notation** — Brackets allow computed keys.

### Modules 38–42 — Projects, modules, storage, and UI libraries

404. **Projects** — Combine components, fetch, props, state, suspense, map, keys, optional chaining, styling, conditions, toggles, lifted state, and deployment; treat state arrays immutably with a copied array.
405. **ES modules** — export makes values available to other files; import brings them in.

~~~js
function sum(a, b) {
  return a + b;
}
function subtract(a, b) {
  return a - b;
}

export { sum, subtract };
~~~

406. **Relative path** — A file path written from the current file, such as ../utils/helper.js.
407. **Data/storage project** — Load JSON/API data, render it, save selected ids or cart data in localStorage, parse on read, and update saved data when items are removed.
408. **imgbb** — Image hosting can provide a URL; do not expose private API keys in client code.
409. **Install Tailwind** — Add Tailwind packages to the React project.
410. **Vite plugin** — Configure the Tailwind plugin in Vite when required by the chosen setup.
411. **Import Tailwind CSS** — Include the Tailwind entry stylesheet in the app.
412. **Google fonts** — Load a chosen font in CSS or the HTML document.
413. **DaisyUI** — Add its plugin/configuration so its component classes and themes are available.
414. **Lucide React/icons** — Install icon components and import only those used.
415. **Custom navbar** — Build navigation with links, responsive layout, and styling.
416. **Boolean state toggle** — Store whether a menu is open.
417. **NOT toggle** — setOpen(!open) flips a boolean; functional state update is safer when based on prior state.
418. **Show/hide menu** — Render the menu conditionally from open state.
419. **Pricing cards** — Map fake or real plan data into reusable cards.
420. **Loader** — Show progress or placeholder UI while work is pending.
421. **Display pricing cards** — Render plan data consistently with a component and shared styles.
422. **Recharts install** — Add the chart library dependency.
423. **Choose a chart** — Select a chart type that fits the data.
424. **Chart data** — Provide an array of objects as the chart's data.
425. **dataKey** — Names the object field that supplies a chart series.
426. **XAxis/YAxis** — Set dataKey to the fields used for chart labels and values.
427. **Axios** — HTTP client whose response object includes data, status, and headers.
428. **axios.get** — Returns a promise; read its response.data property.
429. **Flatten chart data** — Convert nested API records to the simple shape the chart expects.
430. **React awesome components** — Reusable third-party components can speed up common UI work; review package quality and accessibility.

## Milestone 8 — React Router

431. **SPA** — Single-page app updates views without a full document reload for each route.
432. **MPA** — Multi-page app loads separate documents for different pages.
433. **Install React Router** — Add the routing package used by the project.
434. **RouterProvider/createBrowserRouter** — Create a route configuration and provide it to the app.
435. **Declare routes** — Match paths to elements/components.
436. **Path navigation** — A route path selects a page component.
437. **Children/nested route** — Child pages render within a parent layout, usually at Outlet.
438. **Link/NavLink** — Navigate without a full page reload; NavLink can expose active state.
439. **Active class** — Style the current route based on NavLink's active state.
440. **Loader/useLoaderData** — Load route data before rendering and read it in the route component.
441. **Suspense data loading** — Wrap promise-reading UI with Suspense and provide fallback.
442. **Dynamic route** — Put a parameter such as :userId in the path.
443. **Params and loader** — Read route params and use them to request the matching record.
444. **Show dynamic details** — Render a detail page from the id-specific data.
445. **useNavigate** — Navigate in response to code, such as going back with -1.
446. **useNavigation** — Read whether route navigation is pending and show progress UI.
447. **useParams** — Read dynamic values from the current route.
448. **Load inside component** — Fetch locally when the data is component-specific; handle loading and errors.
449. **404 route** — A wildcard path can render a not-found page.
450. **Navigate component** — Redirect declaratively when a condition is true.
451. **useLocation** — Read current pathname, search, hash, and navigation state.

~~~jsx
const router = createBrowserRouter([
  {
    path: "/",
    Component: Root,
    children: [
      { index: true, element: <h1>Welcome Home</h1> },
      { path: "mobile", element: <h1>All Mobiles are here</h1> },
      { path: "laptop", element: <h1>All Laptops are here</h1> },
    ],
  },
]);
~~~

## React Router forms, context, and authentication

452. **onSubmit** — Handles form submission.
453. **Event object** — Gives the handler form and event details.
454. **Prevent default** — Call preventDefault() to stop the browser's standard form navigation when handling it in React.
455. **Form action/FormData** — A form action can receive FormData; read named fields with get().
456. **Controlled field** — React state is the source of truth; pass value and onChange.
457. **Ways to read form data** — Use event target values, FormData, or controlled state.
458. **Controlled field** — Updates React state as the user types.
459. **Uncontrolled field** — The DOM holds the current value; a ref can read it when needed.
460. **useRef value** — Read an input with ref.current.value after the element mounts.
461. **Custom hook naming** — Custom hooks start with use and can share stateful logic.
462. **Return value and handler** — A custom input hook can return the current value and its change handler.
463. **Use the hook in inputs** — Connect the returned value/handler to fields and prevent form reload on submit.
464. **Product form/table** — Lift product state to a parent; pass an add handler down and product data to the table.
465. **Family component tree** — Parent/child nesting describes component relationships.
466. **Props drilling** — Passing props through layers that do not need them can become cumbersome.
467. **Context API** — Share values with descendants without passing props at every level.

~~~jsx
export const AssetContext = createContext("");

function App() {
  const asset = "Diamond";

  return (
    <>
      <h2>React Form</h2>
      <AssetContext.Provider value={asset}>
        <ProductManagement></ProductManagement>
      </AssetContext.Provider>
    </>
  );
}

export default App;
~~~

468. **Authentication** — Verifies who a user is.
469. **Authorization** — Determines what an authenticated user is allowed to do.
470. **Encryption** — Transforms data so it cannot be read without the right key; use HTTPS and secure credential handling.

### Firebase authentication project notes

471. **Google sign-in setup** — Create the app, install/configure Firebase, enable Google provider, call signInWithPopup, observe auth state, display user info, and provide sign-out. Configure OAuth callback settings for providers.
472. **Register/sign-in form** — Registration creates an account; sign-in uses an existing account.
473. **Register a new user** — Collect credentials and call the provider's account creation method.
474. **Email/password setup** — Create Firebase project/app, install SDK, initialize auth, and enable email/password in Firebase settings.
475. **Error message** — Show a useful error from the failed operation; don't assume a particular property name without checking the error object.
476. **Client validation** — Give immediate feedback, but enforce important rules on a trusted server/provider too.
477. **Success message** — Confirm successful completion to the user.
478. **Regular expression** — A pattern matcher used for format checks.
479. **Password pattern checks** — Test minimum length, uppercase, number, and symbol as shown in the supplied pattern example.
480. **Show/hide password** — Toggle the input type between password and text.
481. **Checkbox state** — Read a checkbox with e.target.checked.
482. **Sign in with email/password** — Call the Firebase sign-in method and handle its promise.
483. **Email verification** — Send a verification message for the signed-in user.
484. **Check verified email** — Read emailVerified before granting app-specific access.
485. **Password reset** — Send a reset email to the supplied address.
486. **Update profile** — Update display name/photo URL with Firebase's profile method.

487. **Auth project setup** — Create the app, router, styling, pages, links, Firebase project, and configuration.
488. **Firebase auth setup** — Enable the provider, connect the form handler, and call account creation.
489. **Auth context/provider** — Put shared auth state/actions in context and wrap the app so components can use it.
490. **Create user through context** — Expose a function that accepts email/password and calls Firebase.
491. **Sign in through context** — Expose sign-in action and listen for auth changes to keep user state current.
492. **Auth observer cleanup** — Start the observer in useEffect and return its unsubscribe function to avoid a stale subscription.
493. **Sign out/private pages** — Call signOut, reset forms if needed, and protect user-only routes.
494. **Private route/loading** — Render protected children for signed-in users; otherwise show loading or redirect to login.
495. **Return after login** — Save the original location and navigate back after successful sign-in.
496. **Deploy/auth environment** — Configure SPA rewrites and Firebase authorized domains; put public build-time config in env variables but never treat client env values as secrets.
497. **date-fns** — Utility library for parsing and formatting dates.
498. **Firebase hosting setup** — Install Firebase CLI and select the hosting project.
499. **Firebase login** — Authenticate the CLI account.
500. **Firebase init** — Connect hosting settings to the local project.
501. **Select hosting** — Choose the Hosting feature during setup.
502. **Choose project/SPA mode** — Select the correct Firebase project and enable rewrite behavior for a client-side router.
503. **Build folder** — Vite commonly outputs production files to dist; confirm the configured output folder.
504. **Build/deploy** — Build the app, then deploy the configured output using Firebase CLI.

## Milestone 9 — Node and Express

505. **First Express server** — Initialize a Node project, install Express, create the app, define a port and route, listen, then run with Node or a watcher.
506. **Get all/single API data** — Return JSON data from routes; use a route parameter such as :id and validate/convert it before lookup.
507. **Load server data in React** — Fetch through a loader/component and configure CORS on the server when browser origins differ.

## Milestone 10 — Backend and database integration

### Module 53 — Node, Express, and APIs

507. **Server** — A program/computer that receives requests and returns responses.
508. **Who runs a server?** — A server process runs on a computer or cloud environment.
509. **Computer server** — A machine configured to provide services over a network.
510. **Request/response** — Client sends a request; server returns a response.
511. **Different servers** — They may use different hardware, software, protocols, and roles.
512. **Server types** — Web, application, database, file, and other service servers.
513. **Database** — Organized persistent data managed for querying and updates.
514. **Three-tier architecture** — Separates presentation/client, application/server, and data/database layers.
515. **REST request methods** — HTTP methods such as GET, POST, PUT, and DELETE express operation intent.
516. **REST response formats** — APIs commonly return JSON; XML is also possible.
517. **GET** — Retrieve data.
518. **POST** — Send/create data.
519. **PUT** — Replace/update a resource.
520. **DELETE** — Remove a resource.
521. **POST flow** — Send JSON in fetch with method, headers, and body; parse the returned response.
522. **Request object** — req.body contains parsed body data; req.params contains path parameters.
523. **Response methods** — res.send/res.json send data; res.status sets status; res.sendStatus sends a status; res.set sets headers.
524. **Node.js** — JavaScript runtime built on V8 with server-side APIs.
525. **Node runtime** — Runs JavaScript outside the browser.
530. **Runtime** — The environment that executes a program.
531. **Runtime environment** — Runtime plus its APIs, libraries, and execution rules.
532. **Threads** — Independent execution paths; Node handles many I/O tasks asynchronously.
533. **Non-blocking I/O/event loop** — I/O can wait without blocking JavaScript from handling other work.
534. **Asynchronous Node.js** — Use callbacks, promises, and async/await for delayed operations.
535. **Event-driven Node.js** — Code responds to events such as requests or completed I/O.
536. **When to use Node** — Useful for network services and JavaScript-based tooling; choose it based on workload and requirements.
537. **Why Node is recommended** — Shared JavaScript ecosystem and strong I/O handling can suit many web services.
538. **Node features** — V8 runtime, package ecosystem, event loop, and asynchronous I/O APIs.
539. **Express** — A Node framework for routes and middleware.
540. **Middleware** — A function in the request/response pipeline that can inspect, modify, or end a request.

### Databases and MongoDB

541. **Data** — Recorded facts or values.
542. **Database** — A system for storing and retrieving data.
543. **DBMS** — Software for creating, querying, and managing databases.
544. **SQL vs NoSQL** — SQL databases use relational tables and schemas; NoSQL databases use several models and often flexible records.
545. **NoSQL types** — Document, key-value, wide-column, and graph databases.
546. **MongoDB** — A document database that stores BSON-like documents in collections.
547. **MongoDB advantages** — Flexible documents and a mature ecosystem; design still needs indexes, validation, and access controls.

### Module 53 recap — Express setup and client/server flow

548. **Install Express server** — Create a project, install express/cors, configure package scripts, create index.js, define app and port, add a route, and call app.listen.
549. **Fetch users/create form** — Expose a users route, fetch it from React, handle CORS as needed, render the records, and collect new user details.
550. **POST form data** — Prevent form navigation, collect fields, send JSON with fetch, and enable express.json() middleware on the server.

~~~js
app.use(express.json());

app.post("/users", (req, res) => {
  const newUser = req.body;
  res.send(newUser);
});
~~~

### Module 54 — MongoDB CRUD

551. **Create MongoDB server/database** — Set up a MongoDB Atlas deployment or local database.
552. **MongoDB** — A document-oriented database.
553. **Atlas setup** — Create a cluster/deployment and configure database access.
554. **Network/database access** — Configure allowed network connections and a database user with appropriate permissions.
555. **Connect Node to MongoDB** — Create a client using a URI, connect in an async function, handle errors, and keep the connection available for routes.

~~~js
async function run () {
  try{
      (await client.connect()).db('admin').command({ping:1});
      console.log('Database connect to server successfully')
  }finally{
      // client.close()
  }
}
run().catch(console.dir)
~~~

556. **Client-side POST** — Submit form data from React; receive it at an Express route and insert it in the database.
557. **insertOne/insertMany/bulkWrite** — Insert one document, many documents, or a batch of mixed operations.
558. **Read collection data** — find() creates a cursor; toArray() reads the results into an array.
559. **Delete by ObjectId** — Convert the URL id to ObjectId, call deleteOne, then remove the matching item from React state.
560. **Load one item by id** — Use a dynamic route, query with ObjectId, findOne, and show the result in a detail page.
561. **PUT/PATCH update** — Read the id/body, build a query and update document (often with $set), call updateOne, and return the result. upsert inserts only when configured and no record matches.
562. **MongoDB Compass** — Desktop GUI for connecting to and inspecting MongoDB deployments, including local ones.

### Module 55 — Smart Deals CRUD project

563. **Project setup** — Create the server folder, initialize npm, install Express/CORS/MongoDB, add middleware and routes, then test with an API client.
564. **MongoDB recap** — Connect a client, select database/collection, insert records, and test endpoints.
565. **Delete/update/get products** — Use route ids, ObjectId queries, CRUD collection methods, and return results.
566. **Sort/limit/skip/project** — Sort result order, cap result count, skip records for paging, and project only needed fields.
567. **Query parameters** — Values after ? in a URL filter requests; read them from req.query and build a safe query.

~~~js
app.get("/products", async (req, res) => {
  console.log(req.query);

  const email = req.query.email;
  const query = {};
  if (email) {
    query.email = email;
  }
  const cursor = productsCollection.find(query);
  const result = await cursor.toArray();

  res.send(result);
});
~~~

568. **Primary/foreign keys and bids** — A primary key identifies a record; a foreign key references another record. For MongoDB, keep related ids and validate ownership.
569. **React app structure and routes** — Separate pages, components, layouts, features, hooks, shared libraries, and assets; use layouts/Outlet for nested pages.
570. **Firebase AuthContext/provider** — Initialize Firebase, create auth context/provider, expose user/loading/actions, and subscribe to auth state.
571. **Register/social login** — Build the registration route, configure Google provider, call popup sign-in, handle errors, and protect private pages.
572. **Save users to database** — Post relevant profile data to the server, check for an existing user before insert, and avoid trusting client-supplied identity without server verification.

## Quick code reminders

- Use === for comparisons unless loose coercion is intentional.
- Use const by default and let when reassignment is needed.
- Do not mutate React state arrays/objects in place; make a copy and set the new state.
- Array.sort and reverse mutate their source; copy first when that matters.
- JavaScript objects are passed as values that refer to objects; avoid calling this pure pass-by-reference.
- await does not make the whole program synchronous; it suspends the current async function.
- Keep secrets and privileged database credentials on the server, never in browser code.

