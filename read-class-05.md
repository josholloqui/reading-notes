# Web Scraping JavaScript
* Javascript to interact with your browser, the browser provides a Runtime Environment
* Javascript is not the kind of programming language that can interact with or manipulate the computer or it's resources directly.
* NodeJS is a runtime environment that allows an application written in Javascript to make it possible to be run at on a server as well.
* NodeJS makes use of a single main thread and utilizes it to perform tasks in a Non-Blocking manner with the help of the Event Loop.
* Request is one of the most widely used HTTP clients in the Javascript ecosystem
* Superagent is another robust HTTP client that has support for promises and the async/await syntax sugar
* Puppeteer, as the name implies, allows you to manipulate the browser programmatically just like how a puppet would be manipulated by its puppeteer
* You could crawl a Single Page Application and generate pre-rendered content
* HTTP Clients such as Axios, Superagent, and Request are used to send HTTP requests to a server and receive a response.
* Cheerio abstracts the best out of JQuery for the sole purpose of running it in the server-side for web crawling but does not execute Javascript code.
* JSDOM creates a DOM per the standard Javascript specification out of an HTML string and allows you to perform DOM manipulations on it.
* Puppeteer and Nightmare are high-level browser automation libraries, that allow you to programmatically manipulate web applications as if a real person were interacting with it.

# MDN - querySelector
* The Document method querySelector() returns the first Element within the document that matches the specified selector, or group of selectors. If no matches are found, null is returned
* A DOMString containing one or more selectors to match. This string must be a valid CSS selector string; if it isn't, a SYNTAX_ERR exception is thrown.
* If the specified selector matches an ID that is incorrectly used more than once in the document, the first element with that ID is returned.
* To match against an ID or selectors that do not follow standard CSS syntax (by using a colon or space inappropriately, for example), you must escape the character with a backslash ("\"). As the backslash is also an escape character in JavaScript, if you are entering a literal string, you must escape it twice (once for the JavaScript string, and another time for querySelector()

# MDN - querySelectorAll
* The Document method querySelectorAll() returns a static (not live) NodeList representing a list of the document's elements that match the specified group of selectors.
* A DOMString containing one or more selectors to match against. This string must be a valid CSS selector string; if it's not, a SyntaxError exception is thrown. See Locating DOM elements using selectors for more information about using selectors to identify elements. Multiple selectors may be specified by separating them using commas.
* A non-live NodeList containing one Element object for each element that matches at least one of the specified selectors or an empty NodeList in case of no matches.
* Once the NodeList of matching elements is returned, you can examine it just like any array. If the array is empty (that is, its length property is 0), then no matches were found.
* querySelectorAll() behaves differently than most common JavaScript DOM libraries, which might lead to unexpected results.