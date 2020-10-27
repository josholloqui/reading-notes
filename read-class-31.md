# custom hooks  
* Building your own Hooks lets you extract component logic into reusable functions.
* When we want to share logic between two JavaScript functions, we extract it to a third function. Both components and Hooks are functions, so this works for them too!
* Is this code equivalent to the original examples? Yes, it works in exactly the same way. If you look closely, you’ll notice we didn’t make any changes to the behavior. All we did was to extract some common code between two functions into a separate function. Custom Hooks are a convention that naturally follows from the design of Hooks, rather than a React feature.
* Do I have to name my custom Hooks starting with “use”? Please do. This convention is very important. Without it, we wouldn’t be able to automatically check for violations of rules of Hooks because we couldn’t tell if a certain function contains calls to Hooks inside of it.
* Do two components using the same Hook share state? No. Custom Hooks are a mechanism to reuse stateful logic (such as setting up a subscription and remembering the current value), but every time you use a custom Hook, all state and effects inside of it are fully isolated.
*  other built-in Hooks in the Hooks API reference.

# hook rules
* Only Call Hooks at the Top Level
* Don’t call Hooks inside loops, conditions, or nested functions. Instead, always use * Hooks at the top level of your React function. By following this rule, you ensure that Hooks are called in the same order each time a component renders. That’s what allows React to correctly preserve the state of Hooks between multiple useState and useEffect calls. (If you’re curious, we’ll explain this in depth below.)
Don’t call Hooks from regular JavaScript functions. Instead, you can:

* ✅ Call Hooks from React function components.
* ✅ Call Hooks from custom Hooks
* We released an ESLint plugin called eslint-plugin-react-hooks that enforces these two rules.
* Note that you don’t need to worry about this problem if you use the provided lint rule. But now you also know why Hooks work this way, and which issues the rule is preventing.

# vustom hooks all you need to know
* Hooks have a lot of benefit to us as developers, and they are going to change the way we write components for the better. They already help us to write clearer and more concise code - it's like we went on a code diet and we lost a lot of weight and we look better and feel better. It brings out our jawline and makes us feel lighter on our toes. It's the one change that works for us
* Hooks do trim the fat. It cuts down and makes our code more readable, concise and clear
* Never call Hooks from inside a loop, condition or nested function
* Hooks should sit at the top-level of your component
* Only call Hooks from React functional components
* Never call a Hook from a regular function
* Hooks can call other Hooks
* Bookmarked site a lot of valuable information

# 10 essential hook
* useArray hook
* Array manipulation is what a dev goes through every weekday. Adding elements to an array or removing an element at a given index is a daily routine for us. useArray reduces this burden by providing us with various array manipulation methods. This hook is a part of the react-hanger package.
* react-use-form-state hook
Forms are everywhere, even in the smallest of applications we have to encounter forms and manage their state. Managing form state in React can be a bit unwieldy sometimes.
react-use-form-state is a small React Hook that attempts to simplify managing form state, using the native form input elements you are familiar with.
* react-fetch-hook
Making ajax calls is like the most basic and most performed task for a frontend developer. And the React community is quick enough to create a hook for this purpose too.
* useMedia hook
useMedia is a React sensor hook that tracks the state of a CSS media query. We all know the importance of the media queries and how much important is responsiveness for any site.
* react-useportal hook
React Portals provide a first-class way to render children into a DOM node that exists outside the DOM hierarchy of the parent component. And this hook helps us do that.
* react-firebase-hooks
We all appreciate the greatness of firebase and use it a lot in our projects, whether its for authentication or storage. And this hook is the one we really need.
* use-onClickOutside hook
An outside click is a way to know if the user clicks everything but a specific component. You may have seen this behavior when opening a dropdown menu or a modal or a dropdown list.
* useIntersectionObserver hook
A React hook for using intersection observers.
The Intersection Observer API provides a way to asynchronously observe changes in the intersection of a target element with an ancestor element or with a top-level document’s viewport.
* use-location hook
The name says it all, this hook is used for getting the location of the browser.
* use-redux hook
This one is for my redux readers. This hook returns the store and dispatch property.
