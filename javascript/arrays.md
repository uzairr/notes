# Arrays

An array is useful because it stores multiple values into a single, organized data structure. 

## Examples

### 1. Array Creation
```bash
// creates a `donuts` array with three strings
var donuts = ["glazed", "powdered", "jelly"];

// creates a `mixedData` array with mixed data types
var mixedData = ["abcd", 1, true, undefined, null, "all the things"];

// creates a `arraysInArrays` array with three arrays
var arraysInArrays = [[1, 2, 3], ["Julia", "James"], [true, false, true, false]];

var arraysInArrays = [
  [1, 2, 3], 
  ["Julia", "James"], 
  [true, false, true, false]
];
```

### 2. Indexing
```bash
var donuts = ["glazed", "powdered", "sprinkled"];
console.log(donuts[0]); // "glazed" is the first element in the `donuts` array

console.log(donuts[3]); // the fourth element in `donuts` array does not exist!
```

### 3. Quiz
1. Create an array called sourceFamily and add "Julia", "James", and your name to the array. Then, print the sourceFamily to the console using console.log
2. Create an array called crew to organize the Serenity’s crew and set it equal to the variables below . You don't need to type out the actual strings, just use the provided variables.
```bash
var captain = "Mal";
var second = "Zoe";
var pilot = "Wash";
var companion = "Inara";
var mercenary = "Jayne";
var mechanic = "Kaylee";
```
3. Starting with this array of prices, change the prices of the 1st, 3rd, and 7th elements in the array.
```bash
var prices = [1.23, 48.11, 90.11, 8.50, 9.99, 1.00, 1.10, 67.00];
```
Afterwards, print out the prices array to the console.

4. You can find the length of an array by using its length property.
```
var donuts = ["glazed", "powdered", "sprinkled"];
console.log(donuts.length);
```
5. Find the length of the following:
```
var inventory = [
  ["gold pieces", 25],
  ["belt", 4],
  ["ring", 1],
  ["shoes", 2]
];
```

### 4. Push
You can use the `push()` method to add elements to the end of an array.

```bash
var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon sugar", "sprinkled"];
donuts.push("powdered"); // pushes "powdered" onto the end of the `donuts` array

var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon sugar", "sprinkled"];
donuts.push("powdered"); // the `push()` method returns 7 because the `donuts` array now has 7 elements
```

### 5. Pop
Alternatively, you can use the `pop()` method to remove elements from the end of an array.

```bash
var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon sugar", "sprinkled", "powdered"];

donuts.pop(); // pops "powdered" off the end of the `donuts` array
donuts.pop(); // pops "sprinkled" off the end of the `donuts` array
donuts.pop(); // pops "cinnamon sugar" off the end of the `donuts` array

var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller", "cinnamon sugar", "sprinkled", "powdered"];
donuts.pop(); // the `pop()` method returns "powdered" because "powdered" was the last element on the end of `donuts` array
```

### 6. Quiz
We’ve decided to replace some of the `donuts` in the donuts array.
```bash
var donuts = ["glazed", "strawberry frosted", "powdered", "Boston creme"];

donuts.pop();
donuts.pop();
donuts.pop();
donuts.push("maple walnut");
donuts.pop();
donuts.push("sprinkled");
```
What does the donuts array look like after the above changes?

### 7. Splice
`splice()` is another handy method that allows you to add and remove elements from anywhere within an array.

```bash
var donuts = ["glazed", "chocolate frosted", "Boston creme", "glazed cruller"];
donuts.splice(1, 1, "chocolate cruller", "creme de leche"); // removes "chocolate frosted" at index 1 and adds "chocolate cruller" and "creme de leche" starting at index 1

var donuts = ["cookies", "cinnamon sugar", "creme de leche"];

donuts.splice(-2, 0, "chocolate frosted", "glazed");

Check the output of donuts after the above changes and anticipate how splice actually worked here!
```

### 8. Quiz
James was creating an array with the colors of the rainbow, and he forgot some colors. The standard rainbow colors are usually listed in this order:
```
var rainbow = ["Red", "Orange", "Yellow", "Green", "Blue", "Purple"];
```
but James had this:
```
var rainbow = ["Red", "Orange", "Blackberry", "Blue"];
```
Using only the splice() method, insert the missing colors into the array, and remove the color "Blackberry" by following these steps:

- Remove "Blackberry"
- Add "Yellow" and "Green"
- Add "Purple"

### 9. Quiz
Consider the following array.
```
var team = ["Oliver Wood", "Angelina Johnson", "Katie Bell", "Alicia Spinnet", "George Weasley", "Fred Weasley", "Harry Potter"];
```
Create a function called `hasEnoughPlayers()` that takes the team array as an argument and returns true or false depending on if the array has at least seven players.

### 10. Quiz
In an earlier exercise, you created a crew array to represent Mal’s crew from the hit show Firefly.
```
var captain = "Mal";
var second = "Zoe";
var pilot = "Wash";
var companion = "Inara";
var mercenary = "Jayne";
var mechanic = "Kaylee";

var crew = [captain, second, pilot, companion, mercenary, mechanic];
```
Later in the show, Mal takes on three new crew members named "Simon", "River", and "Book". Use the push() method to add the three new crew members to the crew array.

```
var doctor = "Simon";
var sister = "River";
var shepherd = "Book";
```

### 11. Quiz
Check the use of the `reverse()` method on the following array:

```
var reverseMe = ["h", "e", "l", "l", "o"];

reverseMe.reverse()
```

Check the use of the `sort()` method on the following array:

```
var sortMe = [2, 1, 10, 7, 6];

sortMe.sort()
```

Consider the following array, removeFirstElement:

```
var removeFirstElement = ["a", "b", "c"];
```
Let's say that you want to modify (i.e., mutate) `removeFirstElement` by removing the first element within it. Which method(s) could you use?

Hint: Try ```shift()``` and ```splice()```

Check the use of the `sort()` method on the following array:

```
var turnMeIntoAString = ["s", "o", "u", "r", "c", "e", "k", "o", "d", "e", "s"];

turnMeIntoAString.join()
```

### 12. Array Loops
Once the data is in the array, you want to be able to efficiently access and manipulate each element in the array without writing repetitive code for each element.
```
var donuts = ["jelly donut", "chocolate donut", "glazed donut"];

// the variable `i` is used to step through each element in the array
for (var i = 0; i < donuts.length; i++) {
    donuts[i] += " hole";
    donuts[i] = donuts[i].toUpperCase();
}
```

### 13. ForEach
The `forEach()` method gives you an alternative way to iterate over an array, and manipulate each element in the array with an inline function expression.
```
var donuts = ["jelly donut", "chocolate donut", "glazed donut"];

donuts.forEach(function(donut) {
  donut += " hole";
  donut = donut.toUpperCase();
  console.log(donut);
});
```

```
for (var i = 0; i < donuts.length; i++) {
  donuts[i] += " hole";
  donuts[i] = donuts[i].toUpperCase();
  console.log(donuts[i]);
}
```

```
words = ["cat", "in", "hat"];
words.forEach(function(word, num, all) {
  console.log("Word " + num + " in " + all.toString() + " is " + word);
});
```

### 14. Quiz
Use the array's `forEach()` method to loop over the following array and add 100 to each of the values if the value is divisible by 3.
```
var test = [12, 929, 11, 3, 199, 1000, 7, 1, 24, 37, 4, 19, 300, 3775, 299, 36, 209, 148, 169, 299, 6, 109, 20, 58, 139, 59, 3, 1, 139];
```

### 15. Map
With the `map()` method, you can take an array, perform some operation on each element of the array, and return a new array.
```
var donuts = ["jelly donut", "chocolate donut", "glazed donut"];

var improvedDonuts = donuts.map(function(donut) {
  donut += " hole";
  donut = donut.toUpperCase();
  return donut;
});
```

### 16. Quiz
Use the `map()` method to take the array of bill amounts shown below, and create a second array of numbers called totals that shows the bill amounts with a 15% tip added.
```
var bills = [50.23, 19.12, 34.01, 100.11, 12.15, 9.90, 29.11, 12.99, 10.00, 99.22, 102.20, 100.10, 6.77, 2.22];
```
Print out the new totals array using `console.log`

*Note*: Check out the `toFixed()` method for numbers to help with rounding the values to a maximum of 2 decimal places. Note, that the method returns a string to maintain the "fixed" format of the number. So, if you want to convert the string back to a number, you can cast it or convert it back to a number:

### 17. 2D Arrays
Oftentimes, data is arranged in a grid like fashion like:
```
var donutBox = [
  ["glazed", "chocolate glazed", "cinnamon"],
  ["powdered", "sprinkled", "glazed cruller"],
  ["chocolate cruller", "Boston creme", "creme de leche"]
];

// here, donutBox.length refers to the number of rows of donuts
for (var row = 0; row < donutBox.length; row++) {
  console.log(donutBox[row]);
}

for (var row = 0; row < donutBox.length; row++) {
  // here, donutBox[row].length refers to the length of the donut array currently being looped over
  for (var column = 0; column < donutBox[row].length; column++) {
    console.log(donutBox[row][column]);
  }
}
```

### 18. Quiz
Use a nested for loop to take the numbers array below and replace all of the values that are divisible by 2 (even numbers) with the string "even" and all other numbers with the string "odd".

```
var numbers = [
    [243, 12, 23, 12, 45, 45, 78, 66, 223, 3],
    [34, 2, 1, 553, 23, 4, 66, 23, 4, 55],
    [67, 56, 45, 553, 44, 55, 5, 428, 452, 3],
    [12, 31, 55, 445, 79, 44, 674, 224, 4, 21],
    [4, 2, 3, 52, 13, 51, 44, 1, 67, 5],
    [5, 65, 4, 5, 5, 6, 5, 43, 23, 4424],
    [74, 532, 6, 7, 35, 17, 89, 43, 43, 66],
    [53, 6, 89, 10, 23, 52, 111, 44, 109, 80],
    [67, 6, 53, 537, 2, 168, 16, 2, 1, 8],
    [76, 7, 9, 6, 3, 73, 77, 100, 56, 100]
];
```