# Read: Class 26

## An Intro to Webpack
* The entire dev community was involved in a constant quest of improving the overall user and developer experience around using and building javascript/web applications. Therefore, we saw a lot of new libraries and frameworks introduced.
*  the introduction of JavaScript modules, as writing encapsulated small chunks of code was the new trend. Eventually all of this lead to a situation where we had 4x or 5x he of files in the overall application package.
* Not only was the overall size of the application a challenge, but also there was a huge gap in the kind of code developers were writing and the kind of code browsers could understand.
* Webpack is a static module bundler.
* dependency graph which consists of various modules which your webapp would require to function as expected.
* ReactJS is a UI library which is very helpful in building intelligent complex UIs, and create-react-app is a CLI tool for setting up or bootstrapping a boilerplate dev setup
* adding a webpack.config.js file in the root of our application structure
* applications are limitless

## Webpack Concepts 
* Since version 4.0.0, webpack does not require a configuration file to bundle your project
* An entry point indicates which module webpack should use to begin building out its internal dependency graph. webpack will figure out which other modules and libraries that entry point depends on (directly and indirectly)
* The output property tells webpack where to emit the bundles it creates and how to name these files. It defaults to ./dist/main.js for the main output file and to the ./dist folder for any other generated file.
* Out of the box, webpack only understands JavaScript and JSON files. Loaders allow webpack to process other types of files and convert them into valid modules that can be consumed by your application and added to the dependency graph.
* At a high level, loaders have two properties in your webpack configuration:

1. The test property identifies which file or files should be transformed.
1. The use property indicates which loader should be used to do the transforming.

* In order to use a plugin, you need to require() it and add it to the plugins array. Most plugins are customizable through options. Since you can use a plugin multiple times in a configuration for different purposes, you need to create an instance of it by calling it with the new operator.
* By setting the mode parameter to either development, production or none, you can enable webpack's built-in optimizations that correspond to each environment. The default value is production.
* webpack supports all browsers that are ES5-compliant (IE8 and below are not supported). webpack needs Promise for import() and require.ensure(). If you want to support older browsers, you will need to load a polyfill before using these expressions.

## Rendering Elements
* React elements are immutable. Once you create an element, you can’t change its children or attributes. An element is like a single frame in a movie: it represents the UI at a certain point in time.
* React Only Updates What’s Necessary

## React Hello World
* React is a JavaScript library
```
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

## Introducing JSX
* JSX, and it is a syntax extension to JavaScript. We recommend using it with React to describe what the UI should look like. JSX may remind you of a template language, but it comes with the full power of JavaScript.
* JSX produces React “elements”
* React separates concerns with loosely coupled units called “components” that contain both.
* React doesn’t require using JSX, but most people find it helpful as a visual aid when working with UI inside the JavaScript code. It also allows React to show more useful error and warning messages.
* You can put any valid JavaScript expression inside the curly braces in JSX. For example, 2 + 2, user.firstName, or formatName(user) are all valid JavaScript expressions.
* JSX expressions become regular JavaScript function calls and evaluate to JavaScript objects.
* It is safe to embed user input in JSX
* Babel compiles JSX down to React.createElement() calls
