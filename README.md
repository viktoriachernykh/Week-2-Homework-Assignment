# Homework Assignment

This assignment covers the first week of the Intermediate Bootcamp. This repository contains 2 test files, each covering a single task. The order of the tasks does not matter. **You can complete them in any order.** Try to complete as many of them as you can.

## Instructions

### Assignment 1: ShoppingCart

1. You must create a module named `ShoppingCart`. The module must export a `class`! In other words your `module.exports` is not an object, a string, or anything else, but only a class.
1. Given a brand new instance of the class in a variable `cart`, calling `cart.getItems()` should return an empty array.
1. The class should have a method `cart.addItem(itemName, quantity, price)`, which adds a new item to an internal array.
1. After adding items, a call to `cart.getItems()` should return an array that includes the added items.
1. Items in the array should be in this format:
   ```js
   {
     name: "Name of the item",
     quantity: 1,
     pricePerUnit: 99.99
   }
   ```
1. Calling `cart.clear()` should remove all items from the items array. Meaning, the next call to `getItems()` should return an empty array.
1. Calling `cart.total()` should return the total value of the shopping cart. Meaning, the sum of the cost of each cart item. The cost of each item is its `pricePerUnit` multiplied by the `quantity`. **Use `reduce`!**

### Assignment 2: transform

1.  You must create a module named `transform` that exports a function named `groupAdultsByAgeRange`. The test imports it like this:
    ```js
    const groupAdultsByAgeRange = require("./transform").groupAdultsByAgeRange;
    ```
    _Note: This is a named export_
1.  The exported `groupAdultsByAgeRange` should be a function.
1.  The function will be called with an array of objects as its argument. The objects represent people, with a property `name` and a property `age`. Your function should group each person **over the age of 18** into age ranges. Here are a few examples:

    ```js
    // Example 1
    groupAdultsByAgeRange([
      { name: "Henry", age: 9 },
      { name: "John", age: 20 }
    ]);
    // Should result in:
    const result = { "20 and younger": [{ name: "John", age: 20 }] };

    // Example 2
    groupAdultsByAgeRange([
      { name: "Anna", age: 31 },
      { name: "John", age: 32 },
      { name: "Hank", age: 60 }
    ]);
    // Should result in:
    const result2 = {
      "31-40": [
        { name: "Anna", age: 31 },
        { name: "John", age: 32 }
      ],
      "51 and older": [{ name: "Hank", age: 60 }]
    };
    ```

1.  Notice that the groups are only added to the resulting object if they are not empty. Make sure your function does the same.
1.  You should use a combination of `filter` and `reduce`. If your solution uses `for`-loops instead of `reduce` for creating the **final object**, you will receive partial points. The use of `for`-loops is allowed, but try to construct the returned "grouping" object using `reduce`.
1.  These are the groups that your code needs to return. Use the text as the name of the property:
    - `20 and younger`
    - `21-30`
    - `31-40`
    - `41-50`
    - `51 and older`

### Assignment 3: Fetching Data

Make an HTML page that fetches starwars data from an api and displays it:

1. Make an HTML file
2. Include a script
3. Fetch data about Luke Skywalker from the from the following url `https://swapi.co/api/people/1`
4. Display it on the page
5. Make a button with the text `DARTH VADER` on it
6. When you click the button it fetches data from `https://swapi.co/api/people/4/` and displays it on the page
