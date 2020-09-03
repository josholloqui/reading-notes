# TDD

### Promise
* A Promise is a proxy for a value not necessarily known when the promise is created. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason
* A promise can be pending, fulfilled, or rejected
* Pending: initial state, neither fulfilled nor rejected
* Fulfilled: meaning that the operation completed successfully
* Rejected: meaning that the operation failed
* promise.then(), promise.catch(), and promise.finally() are used to associate further action with a promise that becomes settled
* Promise() creates a new Promise object

### Destructuring 
* The destructuring assignment syntax is a JavaScript expression that makes it possible to unpack values from arrays, or properties from objects, into distinct variables
* Two variables values can be swapped in one destructuring expression.
```let a = 1; let b = 3; [a, b] = [b, a]; ```
* It's always been possible to return an array from a function. Destructuring can make working with an array return value more concise
* You can ignore return values that you're not interested in
* When destructuring an array, you can unpack and assign the remaining part of it to a variable using the rest pattern
* Super useful to destruct to access what you need and you can pick and choose what is needed.

### Spread 
* Spread syntax (...) allows an iterable such as an array expression or string to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected, or an object expression to be expanded in places where zero or more key-value pairs (for object literals) are expected
* Without spread syntax, to create a new array using an existing array as one part of it, the array literal syntax is no longer sufficient and imperative code must be used instead using a combination of push(), splice(), concat(), etc. With spread syntax this becomes much more succinct
* Just like spread for argument lists, ... can be used anywhere in the array literal, and may be used more than once

### Rest
* The rest parameter syntax allows us to represent an indefinite number of arguments as an array
* A function's last parameter can be prefixed with ... which will cause all remaining (user supplied) arguments to be placed within a "standard" JavaScript array. Only the last parameter can be a "rest parameter"
* rest parameters are only the ones that haven't been given a separate name (i.e. formally defined in function expression), while the arguments object contains all arguments passed to the function
* the arguments object is not a real array, while rest parameters are Array instances, meaning methods like sort, map, forEach or pop can be applied on it directly
* the arguments object has additional functionality specific to itself (like the callee property)
* Rest parameters have been introduced to reduce the boilerplate code that was induced by the arguments

### TDD, Where Did It All Go Wrong
* Good reference point to refer back to.
* very informative test test test
* Test Behavior
* "The test becomes the first consumer of your code" really made more sense to me about test wen put into this perspective 

### What the heck is the event loop anyway?
* super useful video with a fantastic explanation of event loops definitely bookmarked