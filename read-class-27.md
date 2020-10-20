# setState Explained
* React components can, and often do, have state. State can be anything, but think of things like whether a user is logged in or not and displaying the correct username based on which account is active. Or an array of blog posts. Or if a modal is open or not and which tab within it is active.
* setState() is the only legitimate way to update state after the initial state setup. Let’s say we have a search component and want to display the search term a user submits.
* The reconciliation process is the way React updates the DOM, by making changes to the component based on the change in state. When the request to setState() is triggered, React creates a new tree containing the reactive elements in the component (along with the updated state)
* Object.assign() is used to copy data from a source object to a target object. If the data being copied from the source to the target all have same keys, like in our example, the last object wins
* When building React applications, there are times when you’ll want to calculate state based the component’s previous state. You cannot always trust this.state to hold the correct state immediately after calling setState(), as it is always equal to the state rendered on the screen.
* Update to a component state should be done using setState()
* You can pass an object or a function to setState()
* Pass a function when you can to update state multiple times
* Do not depend on this.state immediately after calling setState() and make use of the updater function instead.

# Lists and Keys
* we use the map() function to take an array of numbers and double their values.
* You can build collections of elements and include them in JSX using curly braces {}
* Keys help React identify which items have changed, are added, or are removed
* Keys only make sense in the context of the surrounding array.
8 Keys used within arrays should be unique among their siblings

# Typechecking Props
* As your app grows, you can catch a lot of bugs with typechecking. For some applications, you can use JavaScript extensions like Flow or TypeScript to typecheck your whole application. But even if you don’t use those, React has some built-in typechecking abilities. To run typechecking on the props for a component, you can assign the special propTypes property
* With PropTypes.element you can specify that only a single child can be passed to a component as children.
* You can define default values for your props by assigning to the special defaultProps

# Components and Props
* The simplest way to define a component is to write a JavaScript function
* Components can refer to other components in their output. This lets us use the same component abstraction for any level of detail. A button, a form, a dialog, a screen: in React apps, all those are commonly expressed as components.
* Whether you declare a component as a function or a class, it must never modify its own props.

# Handling Events
* React events are named using camelCase, rather than lowercase.
* With JSX you pass a function as the event handler, rather than a string.

# Snapshot testing 
* Snapshot tests are a very useful tool whenever you want to make sure your UI does not change unexpectedly.
* A similar approach can be taken when it comes to testing your React components. Instead of rendering the graphical UI, which would require building the entire app, you can use a test renderer to quickly generate a serializable value for your React tree