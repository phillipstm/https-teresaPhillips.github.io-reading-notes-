# Express REST API

## Review: ES6 Classes

<https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes>

**Classes are a template for creating ____.**  

Objects

**Can a class declaration be hoisted?**

Yes, but they can't be called until intitialized, or it will return an reference error.

**How would you describe a constructor and contextual “this” to a non-technical friend?**

A constructor is a template to create a named object. Once it has been named anything that follows the name, wrapped in curly braces in the body of that line of code, the this is referring to that named object.

## Using Express Routing

<https://expressjs.com/en/guide/routing.html>

**Within Express, what does routing refer to?**

It refers to how a applications endpoints respond to a client request.

**What is the difference between a route path and a route method?**

Route methods load middleware functions at a path.
Route paths define the endpoints of requests made. They can be strings,string patterns, or regular expressions.

**When is it appropriate to add next as a parameter to a route handler and what must you do if next has been passed to your middleware as a parameter?**

It is appropriate to add next as a parameter to a route handler when you have multiple callback functions that behave like middleware to handle the request to bypass the remaining route callbacks.

## Express Routing

<https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4>

**What is an Express Router?**

It's like a mini-Express application. It provides routing APIs like .use, .get,.param, and route.

**By what mean do we initialize express.Router() in an express server?**

Npm install, once it's listed in package json as a dependency
{
        "name": "express-router-experiments",
        "main": "server.js",
        "dependencies": {
            "express": "~4.0.0"
        }
    }

**What do we use route middleware for?**

It's a way of doing things before a request is processed. Ex: Auth0, logging analytic, etc.

use router.use() to define middleware.

...

    // we'll create our routes here

    // get an instance of router
    var router = express.Router();

    // route middleware that will happen on every request
    router.use(function(req, res, next) {

        // log each request to the console
        console.log(req.method, req.url);

        // continue doing what we were doing and go to the route
        next();
    });

    // home page route (http://localhost:8080)
    router.get('/', function(req, res) {
        res.send('im the home page!');
    });

    // about page route (http://localhost:8080/about)
    router.get('/about', function(req, res) {
        res.send('im the about page!');
    });

    // apply the routes to our application
    app.use('/', router);

    ...

## Things I want to know more about

 method definitions.<https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Method_definitions>

Express Route Tester <https://expressjs.com/en/guide/routing.html#:~:text=Express%20Route%20Tester>

Response methods-Route handlers
<https://expressjs.com/en/4x/api.html#res.download>
res.download()**Prompt a file to be downloaded.
res.end()**End the response process.
res.json()**Send a JSON response.
res.jsonp()**Send a JSON response with JSONP support.
res.redirect()**Redirect a request.
res.render()**Render a view template.
res.send()**Send a response of various types.
res.sendFile()**Send a file as an octet stream.
res.sendStatus()**Set the response status code and send its string representation as the response body.
