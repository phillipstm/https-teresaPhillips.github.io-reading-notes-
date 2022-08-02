# REST


## How I explained REST to my brother
<https://gist.github.com/brookr/5977550>

**Who is Roy Fielding?**

He helped write the first web servers, that sent documents across the internet… and then he did a ton of research explaining why the web works the way it does. His name is on the specification for the protocol that is used to get pages from servers to your browser.

**Why don’t the techniques that we use today work well when we need to be able to talk to all of the machines in the world?**

They weren't designed to be used like that. When Fielding and his colleagues started building the web, being able to talk to any machine anywhere in the world was a primary concern. But most of the techniques developers later used to get computers to talk to each other didn't have those requirements.

We need to be able to talk to all machines about all the stuff that's on all the other machines. So we need some way of having one machine tell another machine about a resource that might be on yet another machine.

**What is the HTTP protocol that Fielding and his friends created?**

HTTP—this protocol Fielding and his friends created—is all about applying verbs to nouns. For instance, when you go to a web page, the browser does an HTTP GET on the URL you typed in and back comes a web page.

**What does a GET do?**

Browsers pretty much just GET stuff. They don't do a lot of other types of interaction with resources. This is a problem because it has led many people to assume that HTTP is just for GET'ing. But HTTP is actually a general purpose protocol for applying verbs to nouns.

**What does a POST do?**

If one system needs to add something to another system, it would use an HTTP verb of POST.

**What does PUT do?**

If a system wants to replace something in another system, it uses an HTTP verb of PUT.

**What does PATCH do?**

To do a partial update, it'll hopefully use PATCH.

## API Keys

**Geocoding API** <https://locationiq.com/>

Did you get your API key? **Yes**


**Weather Bit API** <https://www.weatherbit.io/>

Did you get your API key?**Yes**

**Yelp API Docs** <https://www.yelp.com/developers/documentation/v3/business_search>

Did you get your API key?**Yes**

**The Movie DB API Docs** <https://developers.themoviedb.org/3/getting-started/introduction>

Did you get your API key?**Yes**

## Things I want to know more about

How to write the code that can be read by computers in a way that will be able to make them more interconnected.