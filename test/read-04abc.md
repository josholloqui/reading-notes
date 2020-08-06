# Read 04a: URL Search Params, URL Hash, & Hash Change Event

* The URLSearchParams interface defines utility methods to work with the query string of a URL.
* The toString() method of the URLSearchParams interface returns a query string suitable for use in a URL.
* The hashchange event is fired when the fragment identifier of the URL has changed (the part of the URL beginning with and following the # symbol).
* use the hashchange event in an addEventListener method
* use the onhashchange event handler property

# Read 04b: Regular Expressions (Regex)
* Keep this cheatsheet a must
* regex  useful in extracting information from any text by searching for one or more matches of a specific search pattern
* will definitely have to come back to a reread and save these cheatsheets
* data validation
* data scraping
* data wrangling
* string parsing
* string replacement
* syntax highlightning, file renaming, packet sniffing and many other applications involving strings

# Read 04c: Asynchronous JavaScript, Promises, and fetch
* JavaScript is synchronous by default, and is single threaded
* Asynchronous means that things can happen independently of the main program flow
* Programs internally use interrupts, a signal that’s emitted to the processor to gain the attention of the system
* You can’t know when a user is going to click a button, so what you do is, you define an event handler for the click event.
* A callback is a simple function that’s passed as a value to another function, and will only be executed when the event happens
* Callbacks are used everywhere, not just in DOM events
* too much nesting makes things very compliocated
* A promise is commonly defined as a proxy for a value that will eventually become available
* Promises are one way to deal with asynchronous code, without writing too many callbacks in your code
* promise it will start in pending state.
* the caller function waits for it to either return the promise in a resolved state, or in a rejected state, but the function continues its execution while the promise does it work
* Read promises again note to self
* fetch() makes network request to a url and returns a promise
* That promise resolves with a response object when the remote server responds with headers
* To read the response body, we have to call a response method on it, like text() or json(), which will return another promise whose resolve value is the body of the response