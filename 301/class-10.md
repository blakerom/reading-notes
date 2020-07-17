# Call-Stack

A Call stack is a mechanism for interpreting. It keeps track of its place in a script that calls multiple functions.
If a stack takes up more space than assigned to it, it will result in a stack overflow error.

```js
function greeting() {
   sayHi();
}
function sayHi() {
   return "Hi!";
}

// Invoke the `greeting` function
greeting();
```
All of the functions will be ignored until the greeting function invocation line is read. Then it will interpret the function.

Add the greeting function to the call stack list will then invoke the sayHi function adding it to the list. After the lines invoked are finished interpreting it goes back to the previous line and removes the function call from the list until it is empty.


