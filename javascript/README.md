# All About Javascript

Here are some key topics to learning JavaScript:

1. [Javascript](#intro-to-javascript)
    1. [What is JS](#what-is-javascript)
    2. [History of JS](#history-of-javascript)
    3. [Use cases of JS](#use-cases-for-javascript)
2. [The common confusion](#javascript-vs-java)
3. [Basics](#basics-of-javascript)
    1. [Datatypes](#datatypes)
    2. [Operators](#operators)
    3. [Variables](#variables)
    4. [String](#strings)
    5. [Arrays](#arrays)
    6. [Objects](#objects)
    7. [Variable Scope](#variable-scope)
4. [Control Flow](#control-flow)
5. [Function](#functions)
6. [Closures & Callbacks](#closures--callbacks)
7. [Functional Constructors](#functional-constructors)
8. [Prototypal Inheritance](#prototypal-inheritance)
9. [Modules](#modules)
10. [Async JS](#asynchronous-programming-and-apis)
11. [Promises](#promises)
12. [ES6 Features](#es6-features)
13. [Dom Manipulation and Events](#dom-manipulation-and-event-handling)
14. [Browser Developer Tools](#browser-developer-tools)
15. [Best Practices](#best-practices)
16. [More Best Practices](#best-practices-for-during-programming)

## Intro to Javascript

### What is JavaScript

JavaScript is a high-level, interpreted programming language that is primarily used to create interactive and dynamic web pages. It is a client-side language, which means that the code is executed by the user's browser rather than on a server. JavaScript is also used for server-side programming with technologies such as Node.js.

<p align="center">
<img src="https://user-images.githubusercontent.com/50291544/213943109-adcd807c-c1fc-4a33-a943-f9f771aaaa0f.png" height="325px" />
</p>

### History of JavaScript

JavaScript was first developed in 1995 by Brendan Eich at Netscape. It was originally called Mocha, then changed to LiveScript, and finally named JavaScript. It was standardized in the ECMAScript language specification, with the latest version being ES2021.

### Use cases for JavaScript

JavaScript is primarily used for web development and creating interactive user interfaces. This includes things like form validation, creating animations, and handling user events. JavaScript can also be used to create server-side applications using technologies like Node.js and can be used for things like automation, creating desktop and mobile apps using frameworks like Electron or React Native.

<p align="center">
<img src="https://user-images.githubusercontent.com/50291544/213943585-40a29806-eb15-4f9b-8a7f-f134dc70bc14.png" height="300px" />
</p>

### Javascript vs Java

JavaScript and Java are both programming languages, but they are used for different purposes and have some key differences.

Java is primarily used for building standalone applications and mobile apps, while JavaScript is primarily used for building interactive front-end web applications and browser scripts.

Javascript was originally named **Mocha**, but quickly became known as **LiveScript** and, later, **JavaScript**.

<p align="center">
<img src="https://user-images.githubusercontent.com/50291544/213943734-a6d903f9-228d-4ac5-b79f-754b8a6f55a2.jpg" height="300px" />
</p>

## Basics of Javascript

### Datatypes

In JavaScript, there are several different data types that can be used to store different types of values. These include:

E.g. `Numbers`, `String`, `Boolean`, `Array`, `Objects`, `Symbols`, `Function`, `Undefined`, `Null`, etc...

```js
// JavaScript has single type of number that is a 64-bit IEEE 754 double.
// Doubles have a 52-bit mantissa, which is enough to store integers
// up to about (9 x 10 ^ 15) precisely means upto 9 QUADRILLION numbers...

// numbers, int, double, float
8; // 8
8.0; // 8
8.3; // 8.3

8 + 8; // 16
8.0 + 8.0; // 16
8.3 + 8.3; // 16.6

8 - 8; // 0
5.5 - 0.2; // 5.3

8 ** 2; // 64  (8 to the power of 2)
8 ** 3; // 512 (8 to the power of 3)

8 / 2; // 4
8 / 3; // 2.6666666666666665

// strings
("Hello World!");
"Hello " + "World!"; // also gives "Hello World!"

"Hello World".length; // 11

"Hello World".charAt(0); // "H"
"Hello World".substring(0, 5); // "Hello"
"Hello World".substr(0, 5); // again "Hello"
"Hello World".slice(0, 5); // outputs the same thing again

"Hello-World".split("-"); // ["Hello", "World"]

// fun thing about number and string
1 + 1; // gives 2 as expected right!
1 + "1"; // gives 11, the childhood joke was correct
// this is known as type coercion,
// where JavaScript automatically converts the operands
// to the same data type before performing the operation.

// boolean
true; // 1, true,  enabled,  yes, on
false; // 0, false, disabled, no,  off

// special types
undefined; // danger: not to use :) means a variable is declared but not assigned any value
null; // this indicates a variable is assigned with no value
NaN; // it shows a variable is not a number

// to check types
typeof "hello"; // "string"

typeof 42; // "number"

typeof true; // "boolean"

typeof [1, 2, 3]; // "object" (arrays are considered objects in JavaScript)

typeof { fname: "Sobhan", lname: "Bera" }; // "object"

typeof null; // "object"

typeof undefined; // "undefined"
```

<p align="center">
<img src="https://user-images.githubusercontent.com/50291544/214041773-c7298a01-6fcf-420f-820a-3d4d5a69dd71.jpg" width="400" />
</p>

### Operators

Operators are used to perform operations on variables and data types.
JavaScript has various types of operators like arithmetic, comparison, and logical operators.

-   **Arithmetic operators**: used to perform mathematical operations, such as addition `(+)`, subtraction `(-)`, multiplication `(\*)`, division `(/)`, modulus `(%)`, and exponentiation `(**)`. For example:

    ```js
    let x = 5;
    let y = 2;
    console.log(x + y); // 7
    console.log(x - y); // 3
    console.log(x * y); // 10
    console.log(x / y); // 2.5
    console.log(x % y); // 1
    console.log(x ** y); // 25
    ```

-   **Comparison operators**: used to compare values, such as equality `(==)`, inequality `(!=)`, greater than `(>)`, less than `(<)`, greater than or equal to `(>=)`, and less than or equal to `(<=)`. For example:

    ```js
    let x = 5;
    let y = 2;
    console.log(x == y); // false
    console.log(x != y); // true
    console.log(x > y); // true
    console.log(x < y); // false
    console.log(x >= y); // true
    console.log(x <= y); // false
    ```

-   **Logical operators**: used to perform logical operations, such as and `(&&)`, or `(||)`, and not `(!)`. For example:

    ```js
    let x = true;
    let y = false;
    console.log(x && y); // false
    console.log(x || y); // true
    console.log(!x); // false
    ```

-   **Assignment operators**: used to assign values to variables, such as the basic assignment operator `(=)`, as well as compound assignment operators `(+=, -=, *=, /=, %=, **=)`. For example:

    ```js
    let x = 5;
    x = x + 2;
    console.log(x); // 7

    let y = 5;
    y += 2;
    console.log(y); // 7
    ```

-   **Conditional (ternary) operator**: used to perform a ternary operation, a shorthand for an if-else statement. The syntax is: `condition ? statement1 : statement2`. For example:

    ```js
    let x = 5;
    let y = 2;
    let min = x < y ? x : y;
    console.log(min); // 2
    ```

-   **Unary operators**: which operate on only one operand, like `typeof`, `delete`, `void`, and others. For example:

    ```js
    let x = "hello";
    console.log(typeof x); // string

    let y = { a: 1 };
    delete y.a;
    console.log(y); // {}
    ```

-   **Spread operator**: It allows the elements of an iterable to be expanded in places where zero or more arguments for function calls or elements for array literals are expected.

    ```js
    let arr = [1, 2, 3];
    console.log(...arr); // 1 2 3
    console.log(Math.max(...arr)); // 3
    ```

<p align="center">
<img src="https://user-images.githubusercontent.com/50291544/214043116-3b94baf0-3cc1-4cc1-9994-2ab588893ba1.png" height="400" />
</p>

### Variables

In JavaScript, variables are used to store data. They are used to store different types of values such as numbers, strings, arrays, and objects. Variables can be declared using the keyword "var", "let" or "const".

-   The `var` keyword is used to declare a variable in JavaScript. Variables declared with "var" are function scoped, which means they are only accessible within the function where they are declared.
-   The `let` keyword is similar to "var", but variables declared with "let" are block-scoped. This means they are only accessible within the block of code where they are declared.
-   The `const` keyword is used to declare a variable which cannot be reassigned.

```js
var a = "hello";
let b = "world";
console.log(a, b); // output will be "hello world"

// you can change the value of any variable declared using
// let and var keyword
a = "how are";
b = "you";
console.log(a, b); // now output will be "how are you"

const SCREEN_WIDTH = 29;
console.log(SCREEN_WIDTH); // output will be 29

SCREEN_WIDTH = 30; // Error: Attempted to assign to readonly property.
```

JavaScript variables don't have to be explicitly declared with a type, and the same variable can hold different types of values at different times.

```js
let a = 8; // here a is integer
console.log(a); // 8 - without error

a = "Hello World!"; // now a is a string
console.log(a); // output without error here too
```

<p align="center">
<img src="https://user-images.githubusercontent.com/50291544/214043879-f04dac18-86f1-485c-aaf0-ace481b207dc.jpg" height="325" />
</p>

### Strings

Strings are used to represent text. They can be declared using single or double quotes, and you can use the same quotes inside the string as long as they are escaped.

```js
let str1 = "Hello World!";
let str2 = "Hey!";
```

JavaScript provides several built-in methods for working with strings, such as:

-   **length**: returns the number of characters in a string
-   **indexOf(substr)**: returns the index of the first occurrence of a substring within a string
-   **substring(start, end)**: returns a portion of a string
-   **toUpperCase() / toLowerCase()**: returns the string in all uppercase or lowercase letters
-   **split(delimiter)**: splits a string into an array of substrings based on a delimiter
-   **replace(oldValue, newValue)**: replaces all occurrences of a string with another string

```js
let str = "Hello World!";
console.log(str.length); // 12

console.log(str.charAt(0)); // "H"

console.log(str.indexOf("World")); // 6

console.log(str.substring(6, 11)); // "World"

console.log(str.toUpperCase()); // "HELLO WORLD!"
console.log(str.toLowerCase()); // "hello world!"

console.log(str.split(" ")); // ["Hello", "World!"]

console.log(str.replace("World", "JavaScript")); // "Hello JavaScript!"

let str1 = "Hello";
let str2 = "World!";
console.log(str1.concat(" ", str2)); // "Hello World!"

let str = "    Hello World!    ";
console.log(str.trim()); // "Hello World!"

let str = "Hello";
console.log(str.repeat(3)); // "HelloHelloHello"
```

JavaScript also supports template literals, which allow you to include expressions inside strings using the ${expression} syntax.

```js
let name = "Sobhan";
let age = 20;
console.log(`My name is ${name} and I am ${age} years old.`);
// Output: My name is Sobhan and I am 20 years old.
```

**Fun Thing about strings in JS.**

```js
// fun time now
1; // 1
1 + 2; // 3
1 + 2 + 3; // 6
1 + 2 + 3 + 4; // 10
"1" + 2 + 3 + 4 + 5; // "12345"
```

<p align="center">
<img src="https://user-images.githubusercontent.com/50291544/213945966-0b1b0dad-83fa-489f-bd19-16857e492302.png" height="300" />
</p>

### Arrays

In JavaScript, arrays are used to store a collection of values.
They can be declared using square brackets, and values are separated by commas.

```js
let arr = [1, 2, 3, 4, 5];
console.log(arr); // [1, 2, 3, 4, 5]
```

JavaScript provides several built-in methods for working with arrays, such as:

-   **push(element)**: adds one or more elements to the end of an array
-   **pop()**: removes the last element of an array
-   **shift()**: removes the first element of an array
-   **unshift(element)**: adds one or more elements to the beginning of an array
-   **slice(start, end)**: returns a new array with a selected range of elements
-   **splice(start, deleteCount, item1, item2, ...)**: removes and/or adds new elements to an array
-   **reverse()**: reverses the order of elements in an array
-   **sort()**: sorts the elements of an array in alphabetical or numerical order
-   **forEach(function)**: calls a function for each element in an array
-   **map(function)**: creates a new array by calling a function for each element in an array
-   **filter(function)**: creates a new array with all elements that pass a test
-   **reduce(function)**: applies a function to each element in an array, and returns a single value

```js
let arr = [1, 2, 3];
arr.push(4);
console.log(arr); // [1, 2, 3, 4]

let arr = [1, 2, 3];
arr.pop();
console.log(arr); // [1, 2]

let arr = [1, 2, 3];
arr.shift();
console.log(arr); // [2, 3]

let arr = [1, 2, 3];
arr.unshift(0);
console.log(arr); // [0, 1, 2, 3]

let arr = [1, 2, 3];
arr.unshift(0);
console.log(arr); // [0, 1, 2, 3]

let arr = [1, 2, 3, 4, 5];
arr.splice(2, 1, 6);
console.log(arr); // [1, 2, 6, 4, 5]

let arr = [1, 2, 3];
arr.reverse();
console.log(arr); // [3, 2, 1]

let arr = [3, 2, 1];
arr.sort();
console.log(arr); // [1, 2, 3]

let arr = [1, 2, 3];
arr.forEach(function (element) {
    console.log(element);
});
// Output: 1, 2, 3

let arr = [1, 2, 3];
let newArr = arr.map(function (element) {
    return element * 2;
});
console.log(newArr); // [2, 4, 6]

let arr = [1, 2, 3, 4, 5];
let newArr = arr.filter(function (element) {
    return element % 2 === 0;
});
console.log(newArr); // [2, 4]

let arr = [1, 2, 3, 4];
let sum = arr.reduce(function (accumulator, currentValue) {
    return accumulator + currentValue;
});
console.log(sum); // 10
```

### Objects

In JavaScript, objects are used to store and organize data.
They are a collection of key-value pairs, where each key is a string and each value can be any data type,
including another object.

There are several ways to create objects in JavaScript:

-   **Object literals**: Objects can be created using curly braces {} and key-value pairs separated by a colon. For example:

    ```js
    let obj = {
        key1: "value1",
        key2: "value2",
        key3: "value3",
    };
    ```

-   **Object constructor**: Objects can be created using the built-in Object constructor. For example:

    ```js
    let obj = new Object();
    obj.key1 = "value1";
    obj.key2 = "value2";
    obj.key3 = "value3";
    ```

-   **`Object.create()`**: Objects can be created using the Object.create() method. For example:

    ```js
    let obj = Object.create(null);
    obj.key1 = "value1";
    obj.key2 = "value2";
    obj.key3 = "value3";
    ```

You can access the properties of an object using dot notation or bracket notation. For example:

```js
console.log(obj.key1); // "value1"
console.log(obj["key1"]); // "value1"
```

You can also add, modify, and delete properties of an object using the same notation. For example:

```js
obj.key4 = "value4";
obj.key1 = "new value1";
delete obj.key2;
```

JavaScript objects are also commonly used to store functions, which are known as methods. For example:

```js
let obj = {
    x: 5,
    y: 2,
    add: function () {
        return this.x + this.y;
    },
};
console.log(obj.add()); // 7
```

Objects have several built-in methods that can be used to manipulate and interact with their properties. Here are a few examples:

-   **`Object.keys(obj)`**: Returns an array of the object's own enumerable property names.

    ```js
    let obj = { a: 1, b: 2, c: 3 };
    console.log(Object.keys(obj)); // ["a", "b", "c"]
    ```

-   **`Object.values(obj)`**: Returns an array of the object's own enumerable property values.

    ```js
    let obj = { a: 1, b: 2, c: 3 };
    console.log(Object.values(obj)); // [1, 2, 3]
    ```

-   **`Object.freeze(obj)`**: Freezes an object, making it immutable so that other code can't delete or change any properties.

    ```js
    let obj = { a: 1, b: 2 };
    Object.freeze(obj);
    obj.a = 3; // This will have no effect
    console.log(obj.a); // 1
    ```

-   **`Object.isFrozen(obj)`**: Returns a Boolean indicating if an object is frozen.

    ```js
    let obj = { a: 1, b: 2 };
    console.log(Object.isFrozen(obj)); // false
    Object.freeze(obj);
    console.log(Object.isFrozen(obj)); // true
    ```

-   **`Object.seal(obj)`**: Seals an object, making it non-extensible so that new properties can't be added, but existing properties can still be modified.

    ```js
    let obj = { a: 1, b: 2 };
    Object.seal(obj);
    obj.c = 3; // This will have no effect
    console.log(obj.c); // undefined
    obj.a = 4; // This will change the property
    console.log(obj.a); // 4
    ```

-   **`Object.isSealed(obj)`**: Returns a Boolean indicating if an object is sealed.

    ```js
    let obj = { a: 1, b: 2 };
    console.log(Object.isSealed(obj)); // false
    Object.seal(obj);
    console.log(Object.isSealed(obj)); // true
    ```

<p align="center">
<img src="https://user-images.githubusercontent.com/50291544/214042839-c34eac70-2ff8-4867-bc19-d8d657500940.jpg" height="250" />
</p>

### Variable Scope

In JavaScript, variables have a scope, which determines the accessibility or visibility of those variables within the code. There are two types of scope in JavaScript: global scope and local scope.

1. **Global Scope**: Variables declared outside of any function or block are in the global scope. They can be accessed and modified from any part of the code, and their value is retained throughout the lifetime of the program.

```js
let globalVariable = "I'm a global variable";

function myFunction() {
    console.log(globalVariable); // "I'm a global variable"
}

myFunction();
```

2. **Local Scope**: Variables declared inside a function or block are in the local scope. They can only be accessed and modified within the function or block where they are declared, and their value is retained only for the duration of the function or block's execution.

```js
function myFunction() {
    let localVariable = "I'm a local variable";
    console.log(localVariable); // "I'm a local variable"
}

myFunction();
console.log(localVariable); // ReferenceError: localVariable is not defined
```

In JavaScript, you can use the var, let, and const keywords to declare variables, each one with different behaviors on the scope:

-   **`var`**: Variables declared with var have function scope. This means that they are accessible within the function where they are declared and its inner functions, but not outside of it.

-   **`let and const`**: Variables declared with let and const have block scope. This means that they are only accessible within the block where they are declared, if declared inside a function, they can't be accessed outside of it.

_It's important to understand how variable scope works, as it can affect the behavior of your code and can lead to unexpected results if not used properly._

### Control Flow

Control flow refers to the order in which statements in a program are executed.
There are several types of control flow statements that can be used in JavaScript:

E.g. `if-else`, `switch`, and `loops` are used to control the flow of execution in a program.

-   **`if` statements**: used to make a decision based on a condition. For example:

    ```js
    let x = 10;
    if (x > 5) {
        console.log("x is greater than 5");
    }
    ```

-   **`if...else` statements**: used to make a decision based on a condition, with a separate block of code to execute if the condition is false. For example:

    ```js
    let x = 3;
    if (x > 5) {
        console.log("x is greater than 5");
    } else {
        console.log("x is less than or equal to 5");
    }
    ```

-   **`switch` statements**: used to make a decision based on multiple conditions. For example:

    ```js
    let x = "red";
    switch (x) {
        case "red":
            console.log("x is red");
            break;
        case "blue":
            console.log("x is blue");
            break;
        default:
            console.log("x is neither red nor blue");
    }
    ```

-   **`while` loops**: used to repeat a block of code while a certain condition is true. For example:

    ```js
    let x = 0;
    while (x < 5) {
        console.log(x);
        x++;
    }
    ```

-   **`do...while` loops**: similar to while loops, but the block of code is executed at least once before the condition is checked. For example:

    ```js
    let x = 0;
    do {
        console.log(x);
        x++;
    } while (x < 5);
    ```

-   **`for` loops**: used to repeat a block of code a certain number of times. For example:

    ```js
    for (let i = 0; i < 5; i++) {
        console.log(i);
    }
    ```

-   **`for...in` loops**: used to iterate over the properties of an object. For example:

    ```js
    let obj = { a: 1, b: 2, c: 3, d: 4 };
    for (let key in obj) {
        console.log(key + ": " + obj[key]);
    }

    // a: 1
    // b: 2
    // c: 3
    ```

### Functions

In JavaScript, a function is a block of code that can be reused throughout your program.
Functions are defined using the `function` keyword and can take one or more arguments.
Here are some key points about functions in JavaScript:

-   **Syntax**: Functions are defined using the `function` keyword, followed by the function name, a list of arguments in parentheses, and a block of code in curly braces.

    ```js
    function myFunction(arg1, arg2) {
        // code to be executed
    }
    ```

-   **Arguments**: Functions can take one or more arguments, which are passed to the function when it is called. The arguments can be of any data type.

    ```js
    function myFunction(arg1, arg2) {
        console.log(arg1 + arg2);
    }
    myFunction(5, 2); // 7
    ```

-   **Return values**: Functions can return a value using the return keyword. If a function does not have a return statement, it returns undefined by default.

    ```js
    function myFunction(arg1, arg2) {
        return arg1 + arg2;
    }
    console.log(myFunction(5, 2)); // 7
    ```

-   **Function expressions**: Functions can also be defined as function expressions, which are assigned to a variable. This is also called anonymous function.

    ```js
    let myFunction = function (arg1, arg2) {
        return arg1 + arg2;
    };
    console.log(myFunction(5, 2)); // 7
    ```

-   **Arrow functions**: ES6 introduced arrow functions which are shorthand notation for function expressions. they are also called lambda function.

    ```js
    let myFunction = (arg1, arg2) => arg1 + arg2;
    console.log(myFunction(5, 2)); // 7
    ```

-   **Higher-order functions**: Functions in JavaScript can take other functions as arguments or return functions as values. This is known as Higher-order functions.

    ```js
    function myFunction(arg1, arg2, callback) {
        return callback(arg1, arg2);
    }
    console.log(myFunction(5, 2, (x, y) => x + y)); // 7
    ```

-   **Default parameters**: In JavaScript, you can assign a default value to a function parameter. This default value will be used if the function is called without passing a value for that parameter.

    ```js
    function myFunction(arg1, arg2 = 2) {
        return arg1 + arg2;
    }
    console.log(myFunction(5)); // 7
    ```

<p align="center">
<img src="https://user-images.githubusercontent.com/50291544/214045534-ea3aad6b-99aa-4316-a568-b21ecf9f0609.png" height="225" />
</p>

### Closures & Callbacks

In JavaScript, closures and callbacks are two related concepts that are often used together when working with asynchronous code.

-   **Closures**: A closure is a function that has access to the variables in its parent scope, even after the parent function has completed execution. Closures allow you to create functions that have access to specific variables, even when they are invoked outside of their parent scope.

```js
function myFunction() {
    let myVar = "I'm a closure";

    return function () {
        console.log(myVar);
    };
}

let myClosure = myFunction();
myClosure(); // "I'm a closure"
```

-   **Callbacks**: A callback function is a function that is passed as an argument to another function and is called when the first function has completed its task. Callbacks are widely used in JavaScript, and are the oldest way to handle async code.

```js
function myFunction(callback) {
    setTimeout(() => {
        callback("Hello, world!");
    }, 1000);
}

myFunction((response) => {
    console.log(response); // "Hello, world!"
});
```

_Closures and callbacks are often used together because they both allow you to create functions that can be invoked at a later time, and can have access to specific variables. Closures are often used to create callback functions that have access to specific variables, even when they are invoked outside of their parent scope._

_As a best practice, it's good to keep your code organized and readable by using closures and callbacks in a proper way, and avoid callbacks hell, which can make your code difficult to understand and maintain._

### Functional Constructors

A function constructor is a special type of function in JavaScript that is used to create objects.
It is a regular function that is invoked with the new keyword to create an object and initialize its properties and methods.

Here is an example of a simple function constructor:

```js
function Person(name) {
    this.name = name;
    this.greet = function () {
        console.log("Hello, my name is " + this.name + ".");
    };
}

let person = new Person("Vidhanshu");
console.log(person.name); // "Vidhanshu"
person.greet(); // "Hello, my name is Vidhanshu."
```

In this example, the `Person` function constructor is defined to take a single argument, `name`,
which is used to initialize the `name` property of the object. The function also has a method, `greet`,
which logs a message to the console. When the `new` keyword is used to create a new instance of the `Person` object,
the `name` argument is passed to the constructor function, and the properties and methods are initialized.

Function constructors are commonly used in JavaScript to create objects that have similar properties and methods.
They provide a way to create objects with a consistent structure, and to define the behavior of those objects in a single place.

_Function constructors are powerful, but also comes with a cost, that is,
every object created with a function constructor has it's own copy of the function.
It's better to use prototypes for methods._

_It is also important to note that function constructors should be named
with a capital letter to indicate that they are intended to be used with the new keyword._

### Prototypal Inheritance

In JavaScript, every object has a prototype property, which is a reference to another object.
When a property or method is accessed on an object and it is not found,
the JavaScript runtime looks for that property or method on the object's prototype.
If it is not found there, it looks on the prototype's prototype, and so on, until it reaches the
Object.prototype object at the top of the prototype chain.

Here is an example of how prototypal inheritance works in JavaScript:

```js
let animal = {
    eats: true,
};

let rabbit = {
    jumps: true,
};

// __proto__ is a special property found in each and every object in JS
rabbit.__proto__ = animal;

console.log(rabbit.eats); // true
```

In this example, the `rabbit` object has its own `jumps` property, but it does not have an `eats` property.
However, it can access the `eats` property from its prototype, which is the `animal` object.

<!-- ### Classes & Inheritance -->

### Modules

Modules in JavaScript are a way to organize and reuse code.
A module is a file that contains JavaScript code, and can be imported and exported by other files.
This allows you to split your code into smaller, more manageable pieces, and to share common functionality across multiple parts of your application.

JavaScript has two main ways of working with modules:

-   **CommonJS**: CommonJS is a module system used in Node.js to handle dependencies. In CommonJS, modules are defined using the exports object. To import a module, you use the require() function.

    ```js
    // myModule.js
    exports.myValue = 5;
    exports.myFunction = function () {
        console.log("Hello, world!");
    };

    // main.js
    const myModule = require("./myModule.js");
    console.log(myModule.myValue); // 5
    myModule.myFunction(); // "Hello, world!"
    ```

-   **ES6 Modules**: ES6 modules is a new way to handle modules in JavaScript, and is supported in modern browsers. In ES6, modules are defined using the export keyword, and imported using the import keyword.

    ```js
    // myModule.js
    export const myValue = 5;
    export function myFunction() {
        console.log("Hello, world!");
    }

    // main.js
    import { myValue, myFunction } from "./myModule.js";
    console.log(myValue); // 5
    myFunction(); // "Hello, world!"
    ```

With both of these systems, you can export and import variables, functions, classes and other types of data.
Also, you can use `export default `to export a single value by default,
and you can use `import myModule from './myModule'` to import the default export.

Modules are useful for structuring your code, and make it easier to manage dependencies and maintain your codebase over time.
They allow you to split your code into smaller, more manageable pieces, and to share common functionality

### Asynchronous programming and APIs

Asynchronous programming is a way of writing code that allows it to handle multiple tasks at the same time,
rather than executing tasks one after the other in a synchronous manner.
This is particularly useful when working with tasks that take a long time to complete, such as network requests or file I/O operations.

JavaScript has several ways to handle asynchronous code, including:

-   **Callbacks**: A callback function is a function that is passed as an argument to another function and is called when the first function has completed its task. Callbacks are widely used in JavaScript, and are the oldest way to handle async code.

    ```js
    function myFunction(callback) {
        setTimeout(() => {
            callback("Hello, world!");
        }, 1000);
    }

    myFunction((response) => {
        console.log(response); // "Hello, world!"
    });
    ```

-   **Promises**: Promises are objects that represent the eventual completion (or failure) of an asynchronous operation, and its resulting value. Promises provide a way to handle async code in a more elegant and easy to reason about way, by allowing you to attach callbacks to the promise that will be called when the promise is resolved or rejected.

    ```js
    let promise = new Promise((resolve, reject) => {
        setTimeout(() => {
            resolve("Hello, world!");
        }, 1000);
    });

    promise.then((response) => {
        console.log(response); // "Hello, world!"
    });
    ```

-   **Async/await**: Async/await is a more recent addition to JavaScript, and provides a way to write async code using a more synchronous-looking syntax. Async/await is built on top of promises and makes it easier to reason about async code.

    ```js
    async function myFunction() {
        let response = await new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve("Hello, world!");
            }, 1000);
        });
        console.log(response); // "Hello, world!"
    }

    myFunction();
    ```

<p align="center">
<img src="https://user-images.githubusercontent.com/50291544/214175741-d6e43b00-9a09-40fd-be6e-2799799b93a3.png" height="270" />
</p>

### Promises

Promises in JavaScript are objects that represent the eventual completion (or failure) of an asynchronous operation, and its resulting value. Promises provide a way to handle async code in a more elegant and easy to reason about way, by allowing you to attach callbacks to the promise that will be called when the promise is resolved or rejected.

Here is an example of a simple promise:

```js
let promise = new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve("Hello, world!");
    }, 1000);
});

promise.then((response) => {
    console.log(response); // "Hello, world!"
});
```

In this example, a new promise is created using the `Promise` constructor. The constructor takes a single argument,
a function called the executor. The executor function takes two arguments, `resolve` and `reject`,
which are functions that can be used to resolve or reject the promise.
In this example, the promise is resolved with the string "Hello, world!" after one second using `setTimeout` function.

Once the promise is created, you can attach callbacks to it using the `.then()` method. The `.then()` method takes a single argument,
a callback function that will be called when the promise is resolved.
The callback function takes a single argument, the value that the promise was resolved with.

You can also attach callbacks for when the promise is rejected using the `.catch()` method.

```js
let promise = new Promise((resolve, reject) => {
    setTimeout(() => {
        reject(new Error("Something went wrong!"));
    }, 1000);
});

promise
    .then((response) => {
        console.log(response);
    })
    .catch((error) => {
        console.log(error); // "Error: Something went wrong!"
    });
```

Promises also allows to chain multiple promises together using `.then()` method,
which makes it easy to handle multiple async operations in a more readable and maintainable way.

<p align="center">
<img src="https://user-images.githubusercontent.com/50291544/214176241-f85a27fe-afd7-48f6-93fb-885f952f910f.png" height="350px" />
</p>

### ES6 features

ECMAScript 6 (ES6) is the latest version of JavaScript, which introduces new features such as arrow functions,
template literals, destructuring, and more. These features make the code more concise, readable, and expressive.

Some of the other important features are:

1. **let and const**

```js
let x = 5;
x = 6;
console.log(x); // 6

const y = 7;
y = 8; // TypeError: Assignment to constant variable.
console.log(y);
```

2. **Template literals**

    ```js
    let name = "John";
    console.log(`Hello, ${name}!`); // "Hello, John!"
    ```

3. **Arrow functions**

    ```js
    let myFunction = (x, y) => x + y;
    console.log(myFunction(5, 2)); // 7
    ```

4. **Destructuring assignment**

    ```js
    let myArray = [1, 2, 3];
    let [a, b, c] = myArray;
    console.log(a); // 1
    console.log(c); // 3
    console.log(b); // 2
    ```

5. **Classes**

    ```js
    class Person {
        constructor(name) {
            this.name = name;
        }
        greet() {
            console.log(`Hello, my name is ${this.name}.`);
        }
    }
    let john = new Person("John");
    john.greet(); // "Hello, my name is John."
    ```

6. **Modules**

    ```js
    // myModule.js
    export const myValue = 5;
    export function myFunction() {
        console.log("Hello, world!");
    }

    // main.js
    import { myValue, myFunction } from "./myModule.js";
    console.log(myValue); // 5
    myFunction(); // "Hello, world!"
    ```

7. **Promises**

    ```js
    function getData() {
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                resolve({ data: "Hello, world!" });
            }, 1000);
        });
    }
    getData().then((response) => console.log(response.data)); // "Hello, world!"
    ```

8. **Spread operator and rest parameters**

    ```js
    let myArray = [1, 2, 3];
    let myOtherArray = [4, 5, ...myArray];
    console.log(myOtherArray); // [4, 5, 1, 2, 3]

    function myFunction(x, y, ...args) {
        console.log(x); // 1
        console.log(y); // 2
        console.log(args); // [3, 4, 5]
    }
    myFunction(1, 2, 3, 4, 5);
    ```

<p align="center">
<img src="https://user-images.githubusercontent.com/50291544/214176475-a870da5d-7a3a-46b5-9068-8aecdbbcf9c0.png" height="300px" />
</p>

### DOM manipulation and event handling

The Document Object Model (DOM) is an interface used to access and manipulate the content of a web page. JavaScript can be used to interact with the DOM, for example, to change the content, style, or layout of a page. Event handling is used to respond to user interactions with a web page, such as clicks, mouseovers, and key presses.

### Browser developer tools

Browser developer tools are built-in tools that allow developers to inspect and debug web pages. These tools can be used to inspect the DOM, view network requests, and debug JavaScript code. They can also be used to test and optimize web pages for performance.

Here are some of the key features of browser developer tools:

1. **Inspect Element**: Allows you to inspect the HTML and CSS of a web page, and see how the page is rendered in the browser. You can also edit the HTML and CSS directly in the browser, and see the changes in real-time.

2. **Javascript Console**: Allows you to interact with JavaScript code running on a web page. You can input JavaScript commands, view and track errors and logs, and debug JavaScript code.

3. **Network**: Allows you to monitor and analyze the network traffic on a web page. You can see the request and response headers, view the timing of the requests, and see the resources that are loaded on the page.

4. **Performance**: Allows you to measure the performance of a web page and identify bottlenecks. You can track the CPU and memory usage, view the call stack and profile the performance of JavaScript code.

5. **Application**: Allows you to view and manage the storage, cookies and other data that a website uses.

6. **Security**: Allows you to inspect security-related information such as certificate details, cookies, and other sensitive information.

7. **Audits**: Allows you to analyze web pages and identify performance, accessibility and best practices issues.

8. **Device Mode**: Allows you to test your website's design and functionality on different devices and screen sizes.

All these features can be accessed via the developer tools, which can be opened by right-clicking on a web page and selecting "Inspect" or by using the keyboard shortcut (F12 or Cmd+Opt+I on Mac) in most modern browsers.

In addition to these features, most browser developer tools also provide additional functionality such as the ability to take screenshots and record videos of the web page, and the ability to debug mobile devices remotely.

## Best Practices

1. **Keep Learning & Keep Practicing**.
2. **Share Your Knowledge**.
3. **Read Documentation**: This may not seem exciting at first, but trust me, it is the most comprehensive and valuable resource you will find for learning in this domain. Just read what you want to implement.
4. **Stay current**: What you learn today may quickly become obsolete, so it's important to stay informed and adapt with the rapid changes in technology.

## Best Practices for During Programming

1. **Write Readable Code**: Just use comments wherever needed. _Something is better than nothing_.
2. **Use Code Formatters**: Code formatters will format your code to look good.
3. **Use Version Control**: Git to track changes to your code, collaborate with others, and revert to previous versions if needed.
4. **Write DRY Code**: DRY stands for _Don't Repeat Yourself_.

<p align="center">
<img src="https://user-images.githubusercontent.com/50291544/214037879-f2f4abbb-ab0b-47fb-a818-2d5e0aa1df6f.png" height="225" />
</p>

<br />
<p>
<h6 align="center">
Remember that learning JavaScript requires practice, and bootcamp is just a start.
You should keep practicing and experimenting with the language in order to become proficient.
And if you have any question or need help don't hesitate to ask me.
</h6>
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/50291544/213941920-cbd2316f-77f3-4e40-9c8f-0d7a87684158.gif" width="400px" />
</p>

<br />
<p align="center">
<b>!!! ENJOY PROGRAMMING !!!</b>
</p>

<!-- ![high-level-language](https://user-images.githubusercontent.com/50291544/213943109-adcd807c-c1fc-4a33-a943-f9f771aaaa0f.png) -->
<!-- ![js-usages](https://user-images.githubusercontent.com/50291544/213943585-40a29806-eb15-4f9b-8a7f-f134dc70bc14.png) -->
<!-- ![js-vs-java](https://user-images.githubusercontent.com/50291544/213943734-a6d903f9-228d-4ac5-b79f-754b8a6f55a2.jpg) -->
<!-- ![js_integer+string=string](https://user-images.githubusercontent.com/50291544/213945781-b04356f8-388d-4777-8e52-dd49da1ab5c1.jpg) -->
<!-- ![datatype](https://user-images.githubusercontent.com/50291544/213945966-0b1b0dad-83fa-489f-bd19-16857e492302.png) -->
<!-- ![drycode](https://user-images.githubusercontent.com/50291544/214037879-f2f4abbb-ab0b-47fb-a818-2d5e0aa1df6f.png) -->
<!-- ![null-undefined](https://user-images.githubusercontent.com/50291544/214041773-c7298a01-6fcf-420f-820a-3d4d5a69dd71.jpg) -->
<!-- ![everything-is-obj](https://user-images.githubusercontent.com/50291544/214042839-c34eac70-2ff8-4867-bc19-d8d657500940.jpg) -->
<!-- ![operators](https://user-images.githubusercontent.com/50291544/214043116-3b94baf0-3cc1-4cc1-9994-2ab588893ba1.png) -->
<!-- ![variables](https://user-images.githubusercontent.com/50291544/214043879-f04dac18-86f1-485c-aaf0-ace481b207dc.jpg) -->
<!-- ![no-meme](https://user-images.githubusercontent.com/50291544/214045534-ea3aad6b-99aa-4316-a568-b21ecf9f0609.png) -->
<!-- ![async](https://user-images.githubusercontent.com/50291544/214175741-d6e43b00-9a09-40fd-be6e-2799799b93a3.png) -->
