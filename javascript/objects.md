# Objects

JavaScript objects are containers for named values called properties

NOTE: `typeof` is an operator that returns the name of the data type that follows it:

## Examples

### 1. typeof usage
```
typeof "hello" // returns "string"
typeof true // returns "boolean"
typeof [1, 2, 3] // returns "object" (Arrays are a type of object)
typeof function hello() { } // returns "function"
```

### 2. Object Notation
```
var sister = {
  name: "Sarah", 
  age: 23,
  parents: [ "alice", "andy" ],
  siblings: ["julia"],
  favoriteColor: "purple",
  pets: true
};

// two equivalent ways to use the key to return its value
sister["parents"] // returns [ "alice", "andy" ]
sister.parents // also returns ["alice", "andy"]
```

### 3. Object containing function
```
var sister = {
  name: "Sarah",
  age: 23,
  parents: [ "alice", "andy" ],
  siblings: ["julia"],
  favoriteColor: "purple",
  pets: true,
  paintPicture: function() { return "Sarah paints!"; }
};

sister.paintPicture();
sister.name
```

### 4. Object literals, methods, and properties
```
var myObj = { 
  color: "orange",
  shape: "sphere",
  type: "food",
  eat: function() { return "yummy" }
};

myObj.eat(); // method
myObj.color; // property
```

### 5. Naming Conventions
Feel free to use upper and lowercase numbers and letters, but don't start your property name with a number. You don't need to wrap the string in quotes! If it's a multi-word property, use camel case. Don't use hyphens in your property names
```
var richard = {
  "1stSon": true;
  "loves-snow": true;
};

richard.1stSon // error
richard.loves-snow // error
```

### 6. Quizes
1. Create a `breakfast` object to represent the following menu item:
```
The Lumberjack - $9.95
eggs, sausage, toast, hashbrowns, pancakes
```
The object should contain properties for the `name`, `price`, and `ingredients.`

2. Using the given object:
```
var savingsAccount = {
  balance: 1000,
  interestRatePercent: 1,
  deposit: function addMoney(amount) {
    if (amount > 0) {
      savingsAccount.balance += amount;
    }
  },
  withdraw: function removeMoney(amount) {
    var verifyBalance = savingsAccount.balance - amount;
    if (amount > 0 && verifyBalance >= 0) {
      savingsAccount.balance -= amount;
    }
  }
};
```
add a `printAccountSummary()` method that returns the following account message:
```
Welcome!
Your balance is currently $1000 and your interest rate is 1%.
```

3. Create an object called `facebookProfile.` The object should have 3 properties, `name`, `numberOfFreinds`, `messages`
The object should also have 4 methods:

`postMessage(message)` - adds a new message string to the array
`deleteMessage(index)` - removes the message corresponding to the index provided
`addFriend()` - increases the friend count by 1
`removeFriend()` - decreases the friend count by 1

4. Here is an array of dount objects.
```
var donuts = [
  { type: "Jelly", cost: 1.22 },
  { type: "Chocolate", cost: 2.45 },
  { type: "Cider", cost: 1.59 },
  { type: "Boston Cream", cost: 5.99 }
];
```
Use the `forEach()` method to loop over the array and print out the following donut summaries using `console.log`

```
Jelly donuts cost $1.22 each
Chocolate donuts cost $2.45 each
Cider donuts cost $1.59 each
Boston Cream donuts cost $5.99 each
```