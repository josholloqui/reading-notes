# MVC
* Model–view–controller (usually known as MVC) is a software design pattern[1] commonly used for developing user interfaces that divides the related program logic into three interconnected elements. This is done to separate internal representations of information from the ways information is presented to and accepted from the user.[
* Traditionally used for desktop graphical user interfaces (GUIs), this pattern has become popular for designing web applications.[4] Popular programming languages like JavaScript, Python, Ruby, PHP, Java, C#, and Swift have MVC frameworks that are used for web or mobile application development straight out of the box.
* Model The central component of the pattern. It is the application's dynamic data structure, independent of the user interface.[5] It directly manages the data, logic and rules of the application.
* View Any representation of information such as a chart, diagram or table. Multiple views of the same information are possible, such as a bar chart for management and a tabular view for accountants.
* Controller Accepts input and converts it to commands for the model or view

# Architecting Single Page Applications
* The state represents every piece of data that changes in an application.
* You visit an URL, that’s state, make an Ajax call to retrieve a list of movies, that’s state again, you persist info to local storage, ditto, state.
* The domain describes the state and holds the business logic. It represents the core of our application and should be agnostic to the view layer. Angular, React, Vue, it shouldn’t matter, we should be able to use our domain regardless of the framework we choose.
* The store layer The data which results from creating and updating articles represents our application’s state.
* The store holds the articles and performs the add, remove and update immutable operations on them.
* Application services This layer is useful for doing all kinds of operations which are adjacent to the state flow like Ajax calls to retrieve data from the server or state projections.
* The view layer Right now we have a fully working application, agnostic of any framework, ready to be put to life by React.

# React MVC
* This year (2019), React went through one of its biggest changes with React v16.8: The One With Hooks.
* Shotgun surgery: one change results in many components needing edited
* Divergent changes: one component needs multiple edits to accomodate one change
* Duplicated code: same code structure in multiple components that requires parallel edits for a change
* Primitive obsession: reluctance to create useful data types which results in repetitive low-level logic
* Repeated conditionals: same conditional switching logic in different components
* The guiding light of Model View Controller (MVC) is separating presentation from domain. Why is that important to do? Our application’s “domain” is where we model our perception of the problem and its solution. By making this code separate—without reference to any UI—it could be modeled more correctly, tested more deeply, and presented more numerously.
* Sadly, “model” is a hugely overloaded term (especially in the object-oriented patterns space). In this case, we will define it more similarly to the broader concept of a “data model”: a construct to contain your domain-specific data and logic. Ideally, a model would have no idea a UI even existed
* A Presentation Layer of Controller and View React Components
* A UI-Agnostic Data Model
* We’re categorizing components by (a) what they know about and (b) what they can do. We group components into two categories:

1. Controller Components
1. View Components

* A “controller component” knows a lot about the rest of the world. It knows how to access and update “domain data” (application state) and how to choose and execute “domain logic”.
* Contrast that with a “view component”, which should be agnostic of most things a controller would know about. A view component shouldn’t know anything about application state (reading or writing), network protocols, or non-UI providers farther up the chain. Views shouldn’t know what protocol you use to speak to a backend or the format that data takes. Views shouldn’t know about your custom state contexts and providers for sharing domain data (application state).

# Reconciliation
* When you use React, at a single point in time you can think of the render() function as creating a tree of React elements. On the next state or props update, that render() function will return a different tree of React elements. React then needs to figure out how to efficiently update the UI to match the most recent tree.
* If we used this in React, displaying 1000 elements would require in the order of one billion comparisons. This is far too expensive. Instead, React implements a heuristic O(n) algorithm based on two assumptions:

Two elements of different types will produce different trees.
The developer can hint at which child elements may be stable across different renders with a key prop.
* Because React relies on heuristics, if the assumptions behind them are not met, performance will suffer.

The algorithm will not try to match subtrees of different component types. If you see yourself alternating between two component types with very similar output, you may want to make it the same type. In practice, we haven’t found this to be an issue.
Keys should be stable, predictable, and unique. Unstable keys (like those produced by Math.random()) will cause many component instances and DOM nodes to be unnecessarily recreated, which can cause performance degradation and lost state in child components.
Is