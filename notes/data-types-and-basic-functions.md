## Data Types
- How we represent attributes

### Types:
* number
* string
* boolean
* undefined
* null

### "Truthiness"

In conditional logic, data types are evaluated (i.e. coerced) into a true or false value

- Numbers -> truthy EXCEPT 0 which is falsey
- Strings -> truthy EXCEPT "" which is falsey
- `undefined` and `null` -> falsey

## Data Structures

- How we represent collections of things

### Arrays
- Ordered
- Indexed starting at 0

* What are arrays good at representing?
  - In general they are good for representing things that are the same
* Examples
  - Lines of people
  - List of things
  - Books on a bookshelf
  - Products in a supermarket

### Objects
- Unordered
- Arbitrarily indexed

- What are objects good at representing?
  - Meant to represent things themselves/collections of attributes
* Examples
  - People
  - Tables
  - Shows

## Functions 

### Function Declaration
```js

function doSomething() { // method signature
  // method body
}
```

### Function vs Function Invocation
```js
// Just a function
doSomething

// Calling (i.e. invoking) a function
doSomething()
```

### Function Parameters and Return statements
```js
// value and tax are PARAMETERS -> parameters are how data gets into a function
function applyTax(value, tax){
  // the return value represents the product of the function (i.e. what you want to get OUT of the function)
  return value + value*tax
}

let a = applyTax(2.0, 0.06) // invoke the function, store in variable
```

### Exercises

#### Questions
```js
// 1. Representing real life in data
// Imagine you are creating an application meant for users to get information on what pets are available at a number of pet shops
// Consider what information would be most useful for a user. What would they need to know about shops themselves? What would they need to know about the pets?

// 2. Functions and conditional logic
// Write a function called validPassword that takes a string as an argument and checks that it is at least 8 characters long and console.logs "Too short" if it is too short or "Good to go!" if it passes your test
// Note: If you're note sure how to check the length of a string, look it up.

// 3. Return values
// Write a function called evenifier that takes an integer as an argument, checks to see if it's even. If it is, return that number. If it's not return that number multiplied by 2

// 4. Combining functions and objects
// Given an object with this structure

let person = {
  name: "Sai",
  age: 29,
  occupation: "Developer"
}

// write a function "whoAmI" that prints a string like this:
// "Hi, my name is Sai. I am 29 years old and I work as a Developer"


```
#### Answers
```js
// Write your answer here

// 1. 

let store = {
  street: "123 Elm St",
  city: "Metropolis",
  state: "Kansas",
  phone: "812-734-9887",
  open: "8am - 7pm"
}

let pet = {
  name: "Ace",
  age: 5,
  type: "dog",
  breed: "husky"
}

// 2.

function validPassword (string) {
    if (length.string > 7) {
      console.log("good to go")
    } else {
      console.log("too short")
    }
}

// 3.

function evenifier (number) {
    if (number % 2 == 0) {
      return number
    }
    else {
      return number*2
    }
}

// 4. 

let person = {
  name: "Sai",
  age: 29,
  occupation: "Developer"
}

function whoAmI () {
  console.log(`Hi, my name is person["name"]. I am  years person["age"] old and I work as a person["occupation"].`)
}
```