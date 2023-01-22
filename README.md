<p align="center" >
  <img width="200" height="200" src="https://user-images.githubusercontent.com/115108831/213843365-56fa4f2d-b9d5-4997-88bf-7eb59bb405bb.png">
</p>

# 40 JavaScript Essential Concepts (Updating the repo everyday)


For anyone starting with Web Development, It is important to know the basics of JavaScript, but it can be confusing to figure out just where to start. That’s where this repository comes in. This repo will explain 40 of the most essential concepts that every developer should know to become a successful Javascript programmer. From data types and variables to functions and classes, this repository will cover the key concepts that one needs to know in order to master Javascript.

<br/>
<br/>


## Data types in JavaScript 
#### Primitive Data Types

- Number: Used to hold decimal value.
```js
  x = 2
```
- String: Used to hold sequence of characters.
```js
  name = "Toronto Dev"
```
- Undefined: Means value is not assigned.
```js
  console.log(x) // Output to web console: undefined.
```
- Boolean: A data type accepts true, false
```js
  let isOn = true;
```

- Null: A data type can only hold **null** value.
```js
  let x = null;
  console.log("Value of x" + x)
```

- BigInt: Represents whole numbers larger than 2<sup>53</sup>-1.
```js
  let number = BigInt(565656565656565656656565656565656565634) 
```
- Symbol: A built-in object whose constructor return a unique symbol.
```js
  let symbol1 = Symbol()
  let symbol1 = Symbol('baz')
  let symbol1 = Symbol('baz')
```

Primitives types are **immutable** which means they cannot be modified after creation.
- These are stored by value
```js
  let string = "who invented World Wide Web"
  string = 'Sir Tim Berners-Lee'     // We replaced the value of string variable

  // However, We cannot ALTER only REPLACE, like the example below.
  let string = 'Sir Tim Berners-Lee'
  string[0] = 's'  // Outpust -> 'Sir Tim Berners-Lee'
```


#### Non-Primitive Data types
These are the Data Types Derived from primitive Data.
- Object: A Javascript entity having properties and methods.
          Everything in JS is an object.
          
```js
   // Creating object with the name person
   let person = {
        firstName: "Toronto",
        lastName: "Dev",
   };

   console.log(`${person.firstName} ${person.lastName}`)
```

- Array: Collection of items stored at contiguous memory locations.
```js
  // Empty array
  var x = new array()
  
  // Array with single numeric argument
  var y = new array(10)
  
  // Explicit values
  var z = new Array(1, 3, "Toronto")
```
Non-primitive are **mutable**, these can be modified after creation.
- These are stored by the reference
```js
  let arr = ['Toronto', 'Melbourne', 'New Delhi']
  arr[1] = 'Sydney'                // We are mutating the state of variable arr using index
```

#### The typeof operator
This operator returns a string that tells the type of js variable.
```js
  typeof "G`day" // string
  typeof 0      // number
  typeof null // object
  typeof 1n    // BigInt
  typeof true  // boolean
  typeof undefined // undfined
  typeof Symbol("id")  symbol
  typeof {}   // object
```

<br/>
<br/>

## Call Stacks in JavaScript 

A call stack is a mechanism for an interpreter (like the JS interpreter in a web browser) to keep **track** of its place in a script that calls *multiple functions* — what function is being currently run and what other functions are called within that function.

Every time you invoke a function, it gets added or *pushed* to the top of call stack. When the function returns, its removed or  *popped* out of call stack. It is like a real stack in data structure where data is pushed and popped and follows the Last In First Out (LIFO) principle.

LIFO — When we say that the call stack follows the data structure principle of Last In, First Out (LIFO), it means that the last function that gets pushed into the stack is the first to be pop out, when the function returns.

### Call Stacks example
```js
function greetings() {
 sayHello();
}

function sayHello() {
  return "Hello!";
}

// Call the function greetings()
greetings();
```


