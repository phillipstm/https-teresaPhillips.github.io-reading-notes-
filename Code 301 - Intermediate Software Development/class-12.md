# CRUD-Create, Read, Update, Delete

## Status Codes Based On REST Methods

**In your own words, describe what each group of status code represents:**

**100’s =** Is an informational status code. It lets the client know that the header information was recieved but the transmition will likely fail, or computer will need to use another protocol to complete.

**200’s =** A success code. That let's the client know that it was transmitted successfully. But doesn't mean that it was processed just that it meant all validation when sent.

**300’s =** This let's the client know the request has been redirected. It could be temporary or permanent, but client needs to send request to a new location.

**400’s =** These are client side facing errors. Many reasons could include wrong url, timeouts, authentication, incorrect data.

**500’s =** Server error code. Usually point to overwhelmed server or unreachable server.

**What is a status code 202?** It is an aknowledgement that a asynchronous request was recieved and meant validation at time of transmit. It doesn't mean that request will complete.

**What is a status code 308?** This is a permanent redirect. Do not use the url anymore.

**What code would you use if an update didn’t return data to a client?** Status Code 204 is the correct display for a client update that didn't complete.

**What code would you use if a resource used to exist but no longer does?** 410 Gone - This is like 404 but we know that the resource existed in the past, but it got deleted or somehow moved, and we don’t know where.

**What is the ‘Forbidden’ status code?** 403 Forbidden - The client has authorized or doesn’t need to authorize itself, but still has no permissions to access the resource.

## Build A REST API With Node.js, Express, & MongoDB - Quick - First 20 minutes

<https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw>

**Why do we need to pull our MongoDB database string out of our server and put it into our .env?**

**What is middleware?** It's code that runs before once it's passed to your serer but before it's passed to it's route.

**What does app.use(express.json()) do?**

**What does the /:id mean in a route?** It is passing a paramater to update.

**What is the difference between PUT and PATCH?** Put updates all information. Patch just updates the new information given from the user and leaves the other data untouched.

**How do you make a default value in a schema?** Make it a model class of the object and then make it a requirement when calling the object.

**What does a 500 error status code mean?** There is an actual error on database not with the client or the API.

**What is the difference between a status 200 and a status 201?** The 201 code means that it is an async request and that it successfully created an object. Otherwise it will default to 200 which just means sucessful request.

## Things I want to know more about

I think I want to watch the video again. He droppped a lot of useful info but way to fast to take it all in one shot.
