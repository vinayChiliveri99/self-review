# Loops
In a programming language loops are used to iterate over data. By which we can traverse and transform data.

## 1. for 

This is one of the basic loop in a programming language, **for** is used to iterate over a data structure or on a data sequentially.
To loop through a block of code number of times.

Syntax :

``` js
for(initialization; condition; increment/decrement) { 
    // inner blocks for execution
}
```

The for loop contains 3 parts - 
  - initialization : initialize a iterator with any value (mostly starts with zero)
  - condition : a condition is checked, if the condition is true only then the inner block executes, else it comes out of the loop.
  - increment/decrement : this can be any value (mostly uses +1 or -1 as to visit every element in a data structre).

`Sample Code`

``` js
const array = [1, 2, 3, 4, 5];

for(let index = 0; index < array.length; index++) {
  console.log(array[index]);
}

output : 1 2 3 4 5 (each element in a new line).
```

## 2. forEach

forEach is a kind of higher order function at the same time it acts as a enhanced for loop, which calls a function 
for every element in an array.

Syntax :

``` js
array.forEach(function(element, index, array)) {
  // inner blocks for execution
}
```
The forEach takes a callback function as a argument and this function is executed for every element in an array, 
which can take a maximum of 3 parameters.

- element : the current element.
- index : the index of the current element.
- array : the original array (Not used that frequently)

`Sample Code 1 :`

```js
const array = [1, 2, 3, 4, 5]

array.forEach(printing);

function printing(elemenet, index) {
  console.log('Element at index ${index} is ${element}');
}

output -

Element at index 0 is 1
Element at index 1 is 2
Element at index 2 is 3
Element at index 3 is 4
Element at index 4 is 5

```

`Sample Code 2 : with the usage of array in callback function`

``` js
const numbers = [1, 2, 3, 4, 5]

numbers.forEach(function(number, index, array) {
  array[index] = number * 3;
});

console.log(numbers)

output -

[3, 6, 9, 12, 15]

```

In the above example we used forEach to modify the original array itself.

## 3. for .. in

The for .. in loop in JavaScript is used to loop on objects.
By using this loop, we can access the key, value pairs in an object.

Syntax :

```js
for(key in object) {
    // inner blocks for execution.
}
```
`Sample Code : `

```js
let car = {
    model : 'audi x4',
    car_make : 'audi',
    make_year : 2015,
    price : 100000000
};

// now to iterate over this data we can use for in loop.

for(key in car) {
    console.log(key + ' is ' + car[key]);
}


Output - 
model is audi x4
car_make is audi
make_year is 2015
price is 100000000
```
In this way we can access both key and value pairs from the object using **for .. in** loop

