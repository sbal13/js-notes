## Loops and Iteration


```js
const stores = [
  {
    street: "123 Elm St",
    city: "Metropolis",
    state: "Kansas",
    phone: "812-734-9887",
    open: "8am - 7pm",
    pets: [
      {
        name: "Ace",
        age: 5,
        type: "dog",
        breed: "husky"
      },
      {
        name: "Rover",
        age: 7,
        type: "dog",
        breed: "doberman"
      },
      {
        name: "Selene",
        age: 3,
        type: "cat",
        breed: "maine coon"
      },
      {
        name: "Penny",
        age: 8,
        type: "cat",
        breed: "domestic short hair"
      },

    ]
  },
  {
    street: "28 Peru Street",
    city: "Islington",
    state: "Missouri",
    phone: "845678097",
    open: "8am - 7pm",
    pets: [
      {
        name: "Oberon",
        age: 5,
        type: "iguana",
        breed: "tropical green"
      },
      {
        name: "Logan",
        age: 6,
        type: "cat",
        breed: "long hair"
      },
    ]
  },
  {
    street: "139 James Street",
    city: "Pittsburgh",
    state: "Pennsylvania",
    phone: "582-224-9862",
    open: "8am - 7pm",
    pets: [
      {
        name: "Denver",
        age: 3,
        type: "dog",
        breed: "australian shepherd"
      },
      {
        name: "Midgard",
        age: 7,
        type: "snake",
        breed: "anaconda"
      },
      {
        name: "Ghost",
        age: 9,
        type: "dog",
        breed: "dachsund"
      },
    ]
  }
]
// collect all names of dogs in all pet stores
let dogs = [];

for (i = 0; i < stores.length; i++) {
  for (j = 0; j < stores[i].pets.length; j++) {
    if (stores[i].pets[j].type === "dog") {
      dogs.push(stores[i].pets[j].name)
    }
  } 
}


```


### Exercises

#### Questions

1. Objects and loops

Given an array of names as strings, write a loop that produces an array of objects each having sequential ids. Consider how you can use the index to produce ids

ex:
```js
// Given this array
[
  "Arthur",
  "Josiah",
  "Lauren",
  "Irina"
]

// Write a loop that produces an array structured like so:
[
  {id: 1, name: "Arthur"},
  {id: 2, name: "Josiah"},
  {id: 3, name: "Lauren"},
  {id: 4, name: "Irina"},
]
```

2. Conditional logic and loops

Given an array of objects containing pet information, return the pet with the greatest age. Think of strategies for keeping track of the oldest pet.

ex:
```js
// Given this array
[
  {age: 8, name: "Fido"},
  {age: 3, name: "Jerry"},
  {age: 12, name: "Denver"},
  {age: 5, name: "Alex"},
]

// Should return
{age: 12, name: "Denver"}
```

3. Functions and Loops

Given an array of pet objects, write a function called `filterByAge` that takes an integer as an argument and finds all pets with ages less than that integer.

ex:
```js
// Given this array...
[
  {age: 8, name: "Fido"},
  {age: 3, name: "Jerry"},
  {age: 12, name: "Denver"},
  {age: 5, name: "Alex"},
]

// ...calling the function with 7...
filterByAge(7)

// ...should return
[{age: 3, name: "Jerry"}, {age: 5, name: "Alex"}]
```

4. Nested arrays

Given the `stores` array above, write a loop that produces an array of all unique animal types. (no duplicates)

```js
// Should create array
["dog", "cat", "iguana", "snake"]
```

Note: If you're unsure of how to check whether a value is already in an array, look it up!

#### Answers