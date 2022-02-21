# 02-Express-REST-API

## Types of express middleware
- Application level middleware [app.use]
- Router level middleware [router.use]
- Built-in middleware [express.static,express.json,express.urlencoded]


### True or false: The route handler is middleware?
They are not middleware functions by definition.

### In what ways can a middleware function end the process and send data to the browser?
Middleware functions can perform the following tasks:

#### Execute any code.
#### Make changes to the request and the response objects.
#### End the request-response cycle.
#### Call the next middleware in the stack.

