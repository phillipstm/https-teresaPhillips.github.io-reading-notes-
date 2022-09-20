# An introduction to NodeJS and Express

<https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction>

1.Explain middleware, answer as though I were a non-technical recruiter.

It's a web framework.

2.Express the most popular _Node_ _web_ _framework___.


3.Express is “unopinionated.” What does that mean?

Unopinionated frameworks, by contrast, have far fewer restrictions on the best way to glue components together to achieve a goal, or even what components should be used. They make it easier for developers to use the most suitable tools to complete a particular task, albeit at the cost that you need to find those components yourself.

 You can insert almost any compatible middleware you like into the request handling chain, in almost any order you like. You can structure the app in one file or multiple files, and using any directory structure

4.What is a module and why is modularity useful to us as developers?

A module is a JavaScript library/file that you can import into other code using Node's require() function. Express itself is a module, as are the middleware and database libraries that we use in our Express applications.

const express = require("express");
const app = express();


## What is NPM?

<https://docs.npmjs.com/getting-started/what-is-npm>

NPM----Node Package Manager

1.What version of npm are you running on your machine?

version---8

2.What command would you type to install a library/package called ‘jshint’ into your node project?

npx jshint

## What is TDD?

<https://www.agilealliance.org/glossary/tdd/>

TDD =**Test Driven Development**

1.Explain why tests are important. Please explain as though I were your non technical elder.

They ensure your code is functioning as expected and enable developers to test it before applying it. So it doesn't break a website.

2.What are three expected benefits of testing

**Significant reductions in defect rates, at the cost of a moderate increase in initial development effort.

**Overheads are more than offset by a reduction in effort in projects’ final phases.

**TDD leads to improved design qualities in the code, and more generally a higher degree of “internal” or technical quality, for instance improving the metrics of cohesion and coupling.

3.Name at lest 2 individual pitfalls and at least 2 team pitfalls commonly encountered while writing tests.

**forgetting to run tests frequently
**writing too many tests at once

**partial adoption – only a few developers on the team use TDD
**poor maintenance of the test suite – most commonly leading to a test suite with a prohibitively long running time

## CI/CD

<https://www.youtube.com/watch?v=xSv_m3KhUO8>

1.What are three benefits of Continuous Integration?

**When there is more than one dev working on a project.
**When making changes in a shared master dev branch.
**Ensures everyone's changes will integrate with the current version of the project.

2.What is the difference between Continuos Delivery and Continuous Deployment?

CDelivery- develop in a way you could deliver at anytime.

CDeployment- Deploy new features immediately

3.Explain how GitHub fits into this process assuming the listener comes from a non-technical background

It helps give a clear idea of which changes can be added to the main dev branch. It has ensured using tests have passed checks during build. 

## Bookmark and Review

nodeJS docs
<https://nodejs.org/en/docs/>

npm docs
<https://docs.npmjs.com/>

express docs
<https://expressjs.com/en/4x/api.html>

http status codes
<https://www.restapitutorial.com/httpstatuscodes.html>

supertest
<https://github.com/visionmedia/supertest>

### Things I want to know more about

<https://expressjs.com/en/resources/middleware.html> ----cheat sheet
