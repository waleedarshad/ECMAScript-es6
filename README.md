# ECMAScript(es6)

EcmaScript is the standardized scripting language that JavaScript implement. The current version of EcmaScript supported in modern browsers is ES5. ES5 has lot of short comings which javascript community put great effort to remove in ES6 Which is the latest standard for writing javascript apps.

ES6 provides lots of feature over es5 like classes, destructing, anonymous funcitons and templates literal, spreat operator.
Let discuss some of the es6 feature with examples
 
* Default Parameters in ES6
* Template Literals in ES6
* Multi-line Strings in ES6
* Destructuring Assignment in ES6
* Enhanced Object Literals in ES6
* Arrow Functions in ES6
* Block-Scoped Constructs Let and Const
* Classes in ES6

# Default Parameters
  // Basic syntax
 
  function multiply (a, b = 2) {
    return a * b;
  }
  
  multiply(5); // 10

  // Default parameters are also available to later default parameters

  function foo (num = 1, multi = multiply(num)) {
    return [num, multi];
  }
  
  foo(); // [1, 2]
  foo(6); // [6, 12]

# Template literals
Template literals are enclosed by the back-tick (` `) (grave accent) character instead of double or single quotes. Template literals can contain place holders. These are indicated by the Dollar sign and curly braces (${expression})

**Example

const firstName = 'Jane';
console.log(`Hello ${firstName}! How are you today?`);

** Output:  Hello Jane! How are you today?

# Multi-line Strings
we use backslash to breakdown string into mutiple line
** Example

var my_string = 'Lorem ipsum dolor sit amet, \  
consectetur adipiscing elit, sed do eiusmod tempor \  
incididunt ut labore et dolore magna aliqua. Ut enim\  
 ad minim veniam'
 
 # Destructuring Assignment
 
const obj = { first: 'Jane', last: 'Doe' };

const {first, last} = obj;

** output

console.log(first) // jane

console.log(last) // Doe
# Enhanced Object Literals 

ES6 introduces features to make the syntax even more succinct and increasingly more capable of constructing a complex data object in its initialization.

function getCar(make, model, value) {
    return {
        // with property value shorthand
        // syntax, you can omit the property
        // value if key matches variable
        // name
        make,
        model,
        value
    };
}

which is equivalent

function getCar(make, model, value) {
    return {
        make: make,
        model: model,
        value: value
    };
}



# Arrow Functions 
The “fat” arrow => (as opposed to the thin arrow ->) was chosen to be compatible with CoffeeScript, whose fat arrow functions are very similar.

Specifying parameters:

    () => { ... } // no parameter
     x => { ... } // one parameter, an identifier
(x, y) => { ... } // several parameters


const squares = [1, 2, 3].map(function (x) { return x * x });

const squares = [1, 2, 3].map(x => x * x);

** These two are equivalent ** 


# Const and let scope variable

Const and let are replacement of *var* and come with some significant difference
###
The difference between let and const is that once you bind a value/object to a variable using const, you can't reassign to that variable. 


const something = {};

something = 10; // Error.

--------------------------------

let somethingElse = {};

somethingElse = 1000; // This is fine.


# Classes

