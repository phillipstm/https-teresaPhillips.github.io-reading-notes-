# APIs

## API Design Best Practices

<https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design>

A well-designed web API should aim to support:

**Platform independence.** Any client should be able to call the API, regardless of how the API is implemented internally. This requires using standard protocols, and having a mechanism whereby the client and the web service can agree on the format of the data to exchange.

**Service evolution.** The web API should be able to evolve and add functionality independently from client applications. As the API evolves, existing client applications should continue to function without modification. All functionality should be discoverable so that client applications can fully use it.

**What does REST stand for?**

Representational State Transfer (REST)

**REST APIs are designed around a ____.**

**Resources**, which are any kind of object, data, or service that can be accessed by the client

**What is an identifier of a resource? Give an example.**

A resource has an identifier, which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:

<https://adventure-works.com/orders/1>

**What are the most common HTTP verbs?**

The most common operations are GET, POST, PUT, PATCH, and DELETE.

**GET** retrieves a representation of the resource at the specified URI. The body of the response message contains the details of the requested resource.

**POST** creates a new resource at the specified URI. The body of the request message provides the details of the new resource. Note that POST can also be used to trigger operations that don't actually create resources.

**PUT** either creates or replaces the resource at the specified URI. The body of the request message specifies the resource to be created or updated.

**PATCH** performs a partial update of a resource. The request body specifies the set of changes to apply to the resource.

**DELETE** removes the resource at the specified URI.

**What should the URIs be based on?**

Resource URIs should be based on nouns (the resource) and not verbs (the operations on the resource).

**Give an example of a good URI.**

<https://adventure-works.com/orders> // Good

<https://adventure-works.com/create-order> // Avoid

**What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?**

An API may require a client application to send multiple requests to find all of the data that it requires. Instead, you might want to denormalize the data and combine related information into bigger resources that can be retrieved with a single request.

**What status code does a successful GET request return?**

A successful GET method typically returns HTTP status code 200 (OK). 

**What status code does an unsuccessful GET request return?**

If the resource cannot be found, the method should return 404 (Not Found).

**What status code does a successful POST request return?**

If a POST method creates a new resource, it returns HTTP status code 201 (Created).

**What status code does a successful DELETE request return?**

If the delete operation is successful, the web server should respond with HTTP status code 204 (No Content), indicating that the process has been successfully handled, but that the response body contains no further information.

### Book mark and review

RegExr - Pay particular attention to the cheatsheet
<https://regexr.com/>

Regex Tutorial
<https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285>

Regex 101
<https://regex101.com/>

#### Things I want to know more about

Use HATEOAS to enable navigation to related resources.
<https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design#use-hateoas-to-enable-navigation-to-related-resources>

Chatty I/O <https://docs.microsoft.com/en-us/azure/architecture/antipatterns/chatty-io/>

Extraneous Fetching <https://docs.microsoft.com/en-us/azure/architecture/antipatterns/extraneous-fetching/>
