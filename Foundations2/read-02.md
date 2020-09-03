# Components, Classes and Callbacks

### Atomic Design

#### Part 1
* Start big and work your way down
* Organisms are large sections that we can easily extract from the page
* For each Organism divide into Molecules
* Molecules are sections that we can easily extract from an Organism
* Organism can also contain other Organisms.
* Atomic design is like chemistry in a way
* Atoms include basic html elements like form labels
* Split the page design into large sections — Organisms
* Next, divide your Organisms into Molecules, Look out for sections that are repeated frequently
* Then, Extract your atoms from the Molecules. Remember elements that can’t be broken up any further

#### Part 2
* Separate our components into different folders representing the different atomic stages; atoms, molecules, and organisms
* Start small and work your way up
* For components to be reusable and composable, you have to make them as small and as independent as possible
* In order to achieve responsiveness, we’ll create an atom(i.e. component) called Flex that takes children as props. children in this scenario, is any number of elements/components we put in between the Flex tags.

#### Thinking In React
* Break the UI into a component hierarchy
* single responsibility principle, that is, a component should ideally only do one thing. If it ends up growing, it should be decomposed into smaller subcomponents.

#### Callbacks
* A callback is a function that is to be executed after another function (normally asynchronous) has finished executing
* Complex: In JavaScript, functions are objects. Because of this, functions can take functions as arguments, and can be returned by other functions. Functions that do this are called higher-order functions. Any function that is passed as an argument and subsequently called by the function that receives it, is called a callback function.
* JavaScript is an event driven language
* JavaScript functions are first-class objects, you can pass functions to other functions as variables
* JavaScript Callback Functions can be used synchronously or asynchronously

#### Classes
* “class” construct, that introduces great new features which are useful for object-oriented programming.
* First, a function created by class is labelled by a special internal property So it’s not entirely the same as creating it manually.
* Class methods are non-enumerable. A class definition sets enumerable flag to false for all methods in the "prototype"
* Just like literal objects, classes may include getters/setters, computed properties etc
* Just like functions, classes can be defined inside another expression, passed around, returned, assigned, etc.
* An object is an instance of a class

#### This
* Methods can reference the object as this
* The value of this is defined at run-time.
* When a function is declared, it may use this, but that this has no value until the function is called
* A function can be copied between objects
* When a function is called in the “method” syntax: object.method(), the value of this during the call is object