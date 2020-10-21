# Architectural Styles and Architectural Patterns
* In a few words, while Design Patterns impact a specific section of the code base, Architectural Patterns are high-level strategies that concern large-scale components, the global properties and mechanisms of a system.
* main difference is, an Architectural Pattern, as we said, is a way to solve a recurring architectural problem, while an Architectural Style is a name given to a recurrent Architectural Design. It doesn’t exist to solve a problem.
* A single architecture can contain several Architectural Styles, and each Architectural Style can make use of several Architectural Patterns. An Architecture Patterns can be a subset of an Architectural Styles targeting a specific scope.
* Idiom is also a term that we can regularly meet. An Idiom is a low-level pattern specific to a programming language. It describes how to implement particular aspects of the components or the relationships between them using the features of a given language.
* Presentation layer or UI layer
* Application layer or Service layer
* Business logic layer or Domain layer
* Data access layer or Persistence layer
* EDA, this pattern organizes a system around the production, detection and consumption of events. Such a system consists of event Emitters and event Consumers. Emitters are decoupled from Consumers, which are also decoupled from each other.
* An Emitter is an event source and only knows that the event has occurred. A Consumer needs to know an event has occurred and it has the responsibility of applying a reaction as soon as an event is presented.
* Consumers can subscribe to an event manager receives notifications when events are emitted and forward events to all registered Consumers.

# Container and Presentation Pattern
* containers : are stateful components that contain your business login
* presentations : are stateless components that present your data
* Container components “[a]re concerned with how things work”1. In this role they manage state, fetch data from APIs, setup event handlers, and pass information to other components via props.
* Presentation components “[a]re concerned with how things look”1. In this role they receive props and use those props to render and style DOM.

# Container Details
* When the Container/Presentation pattern first became popular all containers were class based components. At that time state and lifecycle methods were only available within class components. Since containers are responsible for managing state and fetching data (lifecycle methods) they were exclusively written as class components. This helped highlight the dichotomy between container components (classes) and presentational components (functions).
* To set state inside a class based container component use this.setState
* Dependent state changes (changes that do rely on knowing what the current state is) are done by passing a function to this.setState. That function receives current state and returns an object for update.
* Class based container components can fetch data inside lifecycle methods (NOTE: you should fetch data with a service function). If your component always needs to fetch some data, you can use componentDidMount to fetch your data right as your component is mounted.
* To initialize state use the useState hook. When using useState each piece of state should be a JavaScript primitive (string, number, boolean, null, undefined) or a simple array. You can use multiple useState hooks in a single component.
* Fetching data and setting the fetched data in state is considered a side effect. This is because by fetching data we are changing the state of our application.

# Presentation Details
* Presentational components are written as functional components. They return the markup that is going to get rendered to the DOM.
* When we pass props into our component we should use the prop-types package to specify the props our component receives. This gives us convenient warning messages if we forget to pass a prop or pass a prop with the wrong type.

# functional vs class components
* The most obvious one difference is the syntax. A functional component is just a plain JavaScript function which accepts props as an argument and returns a React element.
* A class component requires you to extend from React.Component and create a render function which returns a React element. This requires more code but will also give you some benefits which you will see later on.
* Because a functional component is just a plain JavaScript function, you cannot use setState() in your component. That’s the reason why they also get called functional stateless components. So everytime you see a functional component you can be sure that this particular component doesn’t have its own state.
* If you need a state in your component you will either need to create a class component or you lift the state up to the parent component and pass it down the functional component via props.
* The reason is the same like for state, all lifecycle hooks are coming from the React.Component which you extend from in class components.
* Functional component are much easier to read and test because they are plain JavaScript functions without state or lifecycle-hooks
* You end up with less code
* They help you to use best practices. It will get easier to separate container and presentational components because you need to think more about your component’s state if you don’t have access to setState() in your component
* The React team mentioned that there may be a performance boost for functional component in future React versions

# Conditional Rendering 
8 Conditional rendering in React works the same way conditions work in JavaScript. Use JavaScript operators like if or the conditional operator to create elements representing the current state, and let React update the UI to match them.

