# Array Methods
* forEach() loops over an array's items
* includes() checks if an array includes the item passed in the method
* filter() creates a new array with only elements passed condition inside the provided function
* map() creates a new array by calling the provided function in every element
* reduce() applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value
* some() checks if at least one of an array's item passed the condition. If passed, it return 'true' otherwise 'false'
* every() checks if all of an array's items passed the condition. If passed, it return 'true' otherwise 'false'
* sort() used to arrange/sort an array's item either ascending or descending order
* Array.from() changes all thing that are array-like or iterable into true array especially when working with DOM, so that you can use other array methods like reduce, map, filter and so on
* Array.of() creates an array from every arguments passed into it

# Class Syntax 
* The basic syntax is
```
class MyClass {
  // class methods
  constructor() { ... }
  method1() { ... }
  method2() { ... }
  method3() { ... }
  ```
* use new MyClass() to create a new object with all the listed methods
* constructor() method is called automatically by new
* Sometimes people say that class is a “syntactic sugar” (syntax that is designed to make things easier to read, but doesn’t introduce anything new), because we could actually declare the same without class keyword at all
*  classes may include getters/setters, computed properties
* “Class fields” is a syntax that allows to add any properties

# MDN - Classes
* Classes are in fact "special functions", and just as you can define function expressions and function declarations, the class syntax has two components: class expressions and class declarations
* One way to define a class is using a class declaration. To declare a class, you use the class keyword with the name of the class
* function declarations are hoisted and class declarations are not
* A class expression is another way to define a class. Class expressions can be named or unnamed. The name given to a named class expression is local to the class's body. (it can be retrieved through the class's (not an instance's) name property, though)
* Bookmarked so much useful info on this doc about classes

# MVC Architecture
* Model View Controller is a predictable software design pattern that can be used across many frameworks with many programming languages, commonly Python, Ruby, PHP, JavaScript, and more
* Model: stores & manages data
* View: Graphical User Interface
* Controller: Brains of the application.
* Traditionally used for Graphical user interfaces (GUIs)
* Popular in web applications
* MVC responsibilities are divided between the client & server, compatible with web application architecture
* MVC is helpful design pattern when planning development
* Code reuse
* Extendable code
* MVC makes model classes reusable without modification
* highlighted somethings that stood out to me but there is so much more in the benefits of MVC