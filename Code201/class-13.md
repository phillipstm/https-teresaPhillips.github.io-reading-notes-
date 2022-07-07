# Local Storage

1. What is JSON?


JSON is an open standard file format and data interchange format that uses human-readable text to store and transmit data objects consisting of attribute–value pairs and arrays. It is a common data format with diverse uses in electronic data interchange, including that of web applications with servers. Wikipedia

2 What is data persistence?


Persistent data in the field of data processing denotes information that is infrequently accessed and not likely to be modified. Static data is information, for example a record, that does not change and may be intended to be permanent. It may have previously been categorized as persistent or dynamic. Wikipedia

3. What is local storage?

Web storage, sometimes known as DOM storage, provides web apps with methods and protocols for storing client-side data. Web storage supports persistent data storage, similar to cookies but with a greatly enhanced capacity and no information sent in the HTTP request header. Wikipedia


4. Where is local storage stored?

LocalStorage provides at least 5MB of data storage across all major web browsers. This a lot more than the 4KB (maximum size) that we can store in cookies. On the users computer



## Local Storage and How To Use It On Websites
https://www.smashingmagazine.com/2010/10/local-storage-and-how-to-use-it/


1. Why would a developer use local storage for a web application?

 1 Caching data from the Web when it takes a long time to get it. It speeds up the time it takes to load the page.

 The following code (which uses jQuery) provides the main functionality for this. If local storage is supported and there is a key called thewholefrigginworld, then call the render() method, which displays the information. Otherwise, show a loading message and make the call to the Geo API using getJSON(). Once the data has loaded, store it in thewholefrigginworld and call render() with the same data:

 if(localStorage && localStorage.getItem('thewholefrigginworld')){
  render(JSON.parse(localStorage.getItem('thewholefrigginworld')));
} else {
  $('#list').html('


  2 It can maintain the state of an interface as crude as storing the entire HTML or as clever as maintaining an object with the state of all of your widgets.



2. What information should not be stored in local storage?

Passwords and sensitive personal information.


3. Local storage can store what type of data? How would you convert it to that type before storing?

Local storage can only store strings in the different keys. This means that when you have an object, it will not be stored the right way.

You would want to convert it to JSON it would look very similar to object literal syntax but it isn't an object.

You can work around this by using the native JSON.stringify() and JSON.parse() methods:

var car = {};
car.wheels = 4;
car.doors = 2;
car.sound = 'vroom';
car.name = 'Lightning McQueen';
console.log( car );
localStorage.setItem( 'car', JSON.stringify(car) );
console.log( JSON.parse( localStorage.getItem( 'car' ) ) );

The above produces the information you would expect to see in the console. Rather than just displaying object.


## Bookmark/Skim

“The Past, Present, and Future of Local Storage for Web Applications”
http://diveinto.html5doctor.com/storage.html


### Things I want to more about?

What does my local storage say about me.