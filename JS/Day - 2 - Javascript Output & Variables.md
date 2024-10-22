*`Programming With Rakib`*
*`Day-02 |Javascript Output & Variables`*

**Java-script output**
- Writing into an HTML element, using `innerHTML`.
- Writing into the HTML output using `document.write()`.
- Writing into an alert box, using `window.alert()`.
- Writing into the browser console, using `console.log()`.

**Using innerHTML**
```js
document.getElementById("demo").innerHTML = 5 + 6;
```
- To access an HTML element, JavaScript can use the *`document.getElementById(id)`* method.
- The `innerHTML` property defines the HTML content

**Using document.write()**
```html
<h1>My First Web Page</h1>  
<p>My first paragraph.</p>  
  
<script>  
document.write(5 + 6);  
</script>
```

Using document.write() after an HTML document is loaded, will **delete all existing HTML**:

```html
<h1>My First Web Page</h1>  
<p>My first paragraph.</p>  
  
<button onclick="document.write(5 + 6)">Try it</button>
```
`The document.write() method should only be used for testing.`

 **Using window.alert()**
 
 You can use an alert box to display dat:
```js
window.alert("Hello World");
```
You can skip the `window` keyword.

**Using console.log()**
For debugging purposes, you can call the `console.log()` method in the browser to display data.
```js
console.log("Hello World")
```


## Variables 

- variable like container 
- variable is machine of contain value 
- Variables are Containers for Storing Data
- variable value must be a data type -> we discuss letter about this 
- real life example: glass, box, bag, etc 

**JavaScript Variables can be declared in 4 ways:**
- Automatically
- Using `var`
- Using `let`
- Using `const`

`Automatically`
```js
x = 5;  
y = 6;  
z = x + y;
```

`using var`
```js
var x = 5;  
var y = 6;  
var z = x + y;
```
- The `var` keyword was used in all JavaScript code from 1995 to 2015.
- The `var` keyword should only be used in code written for older browsers.


`Using let`
```js
let x = 5;  
let y = 6;  
let z = x + y;
```
The `let` and `const` keywords were added to JavaScript in 2015.


`Using const`
```js
const x = 5;  
const y = 6;  
const z = x + y;
```

 **When to Use var, let, or const?**

1. Always declare variables

2. Always use `const` if the value should not be changed

3. Always use `const` if the type should not be changed (Arrays and Objects)

4. Only use `let` if you can't use `const`

5. Only use `var` if you MUST support old browsers.



**JavaScript Identifiers**

All JavaScript **variables** must be **identified** with **unique names**.

These unique names are called **identifiers**.

Identifiers can be short names (like x and y) or more descriptive names (age, sum, totalVolume).

The general rules for constructing names for variables (unique identifiers) are:

- Names can contain letters, digits, underscores, and dollar signs.
- Names must begin with a letter.
- Names can also begin with $ and _ (but we will not use it in this tutorial).
- Names are case sensitive (y and Y are different variables).
- Reserved words (like JavaScript keywords) cannot be used as names.
- JavaScript identifiers are case-sensitive.




**Declaring Variable**
```js
let a; //just declare variable 
a = 2 // assing value in a by (=) assingment operator 

let a, b, c, d; // declaring multiple variable 

let c = 12; //declaring variable & assign value at a time
```
