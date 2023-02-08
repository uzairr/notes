# Functions

Functions is a usable chunk of code that can be used again and again.

## Examples

### 1. Reverse Function
```bash
function reverseString(reverseMe){
  var reversed = "";
  for ( var i = reverseMe.length - 1; i >= 0; i--) {
    reversed += reverseMe[i];
  }
  return reversed;
}
```
`
console.log(reverseString("Julia"));`

### 2. why functions usually return undefined
```bash
function sayHello() {
  var message = "Hello!"
  console.log(message);
}
```
`sayHello();`

If you tried pasting any of the functions above into the JavaScript console, you probably didn't notice much happen. In fact, you probably saw undefined returned back to you. undefined is the default return value on the console when nothing is explicitly returned using the special return keyword.

### 3. Return statements
```bash
function sayHello() {
  var message = "Hello!"
  return message;
}
```
`console.log(sayHello());`

In the sayHello() function above, a value is printed to the console with console.log, but not explicitly returned with a return statement. You can write a return statement by using the return keyword followed by the expression or value that you want to return.

### 4. Parameters vs Arguments

A parameter is always going to be a variable name and appears in the function declaration.

An argument is always going to be a value (i.e. any of the JavaScript data types - a number, a string, a boolean, etc.) and will always appear in the code when the function is called or invoked.
## Quiz
Check the output of the following code snippets:
```
function findAverage(x, y) {
  var answer = (x + y) / 2;
  return answer;
}

var avg = findAverage(5, 9);
```

## Knowledge Check
1. Declare a function called laugh() that returns "hahahahahahahahahaha!". Print the value returned from the laugh() function to the console.
2. Write a function called laugh() that takes one parameter, num that represents the number of "ha"s to return. e.g. ```console.log(laugh(3)); --> hahaha!```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)