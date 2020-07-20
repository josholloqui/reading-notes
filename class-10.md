# Class-10 Reading Notes

### JavaScript 

#### Chapt. 10 'Error Handling & Debugging
* The javascript interpreter processes one line of code at a time.
* When a statement needs data from another function, it stacks (or piles) the new function on top of the current task
* Each time a script enter a new execution context there are two phases of activity
* 1. Prepare
* 2. Execute
* If a error is generated it throws an exception  at that point the interpreter stops and looks for exception-handling code.
* Error objects 
* Debug the script to fix errors
* Handle errors gracefully
* note to self Refer back to debug workflow pg463
* Developer tools
* Can type in the console
Adding break point to help with debugging
* Can also use the debugger keyword 
* JavaScript has 7 different types of errors. Each creates its own error object which can tell you its line number and gives a description of the error
* If you know that you may get an error you can handle it gracefully using the try, catch, finally statements.