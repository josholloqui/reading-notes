# using express routing
* Routing refers to how an application’s endpoints (URIs) respond to client requests.
* You define routing using methods of the Express app object that correspond to HTTP methods; for example, app.get() to handle GET requests and app.post to handle POST requests
* In fact, the routing methods can have more than one callback function as arguments. With multiple callback functions, it is important to provide next as an argument to the callback function and then call next() within the body of the function to hand off control to the next callback
* A route method is derived from one of the HTTP methods, and is attached to an instance of the express class.
* Route paths, in combination with a request method, define the endpoints at which requests can be made. Route paths can be strings, string patterns, or regular expressions.
* The characters ?, +, *, and () are subsets of their regular expression counterparts. The hyphen (-) and the dot (.) are interpreted literally by string-based paths.
* If you need to use the dollar character ($) in a path string, enclose it escaped within ([ and ]). For example, the path string for requests at “/data/$book”, would be “/data/([\$])book”.
* Route parameters are named URL segments that are used to capture the values specified at their position in the URL. The captured values are populated in the req.params object, with the name of the route parameter specified in the path as their respective keys.
* You can provide multiple callback functions that behave like middleware to handle a request. The only exception is that these callbacks might invoke next('route') to bypass the remaining route callbacks. You can use this mechanism to impose pre-conditions on a route, then pass control to subsequent routes if there’s no reason to proceed with the current route

# supertest
* Bookmarked supertest docs
* The motivation with this module is to provide a high-level abstraction for testing HTTP, while still allowing you to drop down to the lower-level API provided by superagent.
* You may pass an http.Server, or a Function to request() - if the server is not already listening for connections then it is bound to an ephemeral port for you so there is no need to keep track of ports.
* One thing to note with the above statement is that superagent now sends any HTTP error (anything other than a 2XX response code) to the callback as the first argument if you do not add a status code expect (i.e. .expect(302)
* If you are using the .end() method .expect() assertions that fail will not throw - they will return the assertion as an error to the .end() callback. In order to fail the test case, you will need to rethrow or pass err to done()

# using express middleware
* Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. The next middleware function is commonly denoted by a variable named next.
* Express is a routing and middleware web framework that has minimal functionality of its own: An Express application is essentially a series of middleware function calls.
* Execute any code.
* Make changes to the request and the response objects.
* End the request-response cycle.
* Call the next middleware function in the stack.

# express middleware
* Middleware functions are functions that have access to the request object (req), the response object (res), and the next middleware function in the application’s request-response cycle. These functions are used to modify req and res objects for tasks like parsing request bodies, adding response headers, etc.
* To restrict it to a specific route (and all its subroutes), provide that route as the first argument of app.use()
* One of the most important things about middleware in Express is the order in which they are written/included in your file; the order in which they are executed, given that the route matches also needs to be considered.

# express middleware list
* Bookmarked to use as reference