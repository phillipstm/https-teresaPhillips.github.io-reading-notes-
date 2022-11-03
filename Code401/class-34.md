# API Integration

## Review API Server Build

<https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/api-server/>

**Explain the different between a query string parameter and a path parameter.**

Query String-Would return an entire category of objects.
Query Parameter-Would filter the category based on argument given.

**What would our API URL with a path id parameter be given the following information:**
**Domain: <http://our-site.com>**
**v3**
**model name: stuff**
**id: things**

<http://our-site.com/api/v3/stuff/things>

**We have created a dynamic API with an “interface”. Describe how that interface works to a non-technical friend.**

Our interface works by sending a request to an API and based on user inputs and access rights returns data in real time.

## Review Auth Server Build

<https://codefellows.github.io/code-401-javascript-guide/curriculum/apps-and-libraries/auth-server/>

**Describe how you would use middleware to implement basic and bearer auth.**

I would use basic auth on the signin route to allow everyone access to read app. Bearer auth would need to be used if a user needs to function in other capacities.
The Basic Auth Middleware should at this point validate the user account in our database, and return an object with a re-authentication/bearer token and the user object or an error object

**Describe the handshake necessary to implement OAuth.**

Using a 3rd party api and app.get handles the handshake. Once the user has granted permission, invoke a GET on your /oauth route. The OAuth middleware should at this point complete the handshaking process, create/update a local user account in our database, and return an object with a re-authentication/bearer token and the user object

**Describe how Role Based Access Control works to a non-technical friend.**

Role Based Access Control assigns what a user is allowed to access based on the role they are in.

## Things I want to know more about

3rd party AuthO application