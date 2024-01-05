# Application-Programming-Interfaces-(API)

## What is API:
- An Application Programming Interface (API) is a contract that allows code to talk to other code. APIs are the building blocks of modern software because they allow for the sharing of resources and services across applications, organizations, and devices.

## Why are APIs important?
- APIs help developers integrate exciting features and build automation without reinventing the wheel
ex: using a Weather API instead of launching your weather balloons

- APIs allow enterprises to open up their product for faster innovation
ex: apps that interact with Twitter or Meta APIs by posting on your behalf or reading tweets

- APIs can be products themselves
ex: Software as a Service (SaaS) products like Stripe's payment APIs or Twilio's text messaging and email APIs

## Type of APIs
  **1. Hardware APIs**
  - Interface for software to talk to hardware.
    Example: How your phone's camera talks to the operating system.

  **2. Software Library APIs**
  - Interface for directly consuming code from another code base.
    Example: Using methods from a library you import into your application.

 **3.  Web APIs**
  - Interface for communicating across code bases over a network.
    Example: Fetching current stock prices from a finance API over the internet.

## Some of the API 
  - REST (Representational State Transfer)
  - GraphQL
  - WebSockets
  - webhooks
  - SOAP (Simple Object Access Protocol)
  - gRPC (Google Remote Procedure Call)
  - MQTT (MQ Telemetry Transport)

## Access
 - APIs also vary in the scope of who can access them.

     **Public APIs (aka Open APIs)**
    - Consumed by anyone who discovers the API

    **Private APIs**
    - Consumed only within an organization and not made public

    **Partner APIs**
    - Consumed between one or more organizations that have an established relationship


#### Request methods
  - When we make an HTTP call to a server, we specify a request method that indicates the type of operation we are about to perform. These are also called HTTP verbs.

Some common HTTP request methods correspond to the CRUD operations mentioned earlier. You can see a list of more methods here.

###### Method name  - Operation
  - GET	Retrieve data (Read)
  - POST	Send data (Create)
  - PUT/PATCH	Update data (Update) (PUT usually replaces an entire resource, whereas PATCH usually is for partial updates)
  - DELETE	Delete data (Delete)

#### Request URL
  - In addition to a request method, a request must include a request URL that indicates where to make the API call. A request URL has three parts: a protocol (such as http:// or https://), host (location of the server), and a path (route on the server). In REST APIs, the path often points to a reference entity, like "books".
    
```javascript
// Protocol	    Host	                            Path
    https://	    library-api.postmanlabs.com	        /books
```

##### Request-Response pattern
  ![image](https://github.com/GayashanDeshapriya/Application-Programming-Interfaces-API-/assets/94686812/c62097db-4bed-4255-8535-cea830f7b3e0)
  - The client is the agent making a request. A client could be a browser or an application you have coded
  - The request is sent over a network to some server.
  - The server interpreted the request (GET /books) and sent the appropriate response over the network back to the client

##### Query parameters
- Query parameters are added to the end of the path. They start with a question mark ?, followed by the key-value pairs in the format: <key>=<value>. For example, this request might fetch all photos that have landscape orientation:
     - GET https://some-api.com/photos?orientation=landscape

- If multiple query parameters exist, each is separated by an ampersand &. Below are two query parameters to specify the orientation and size of the photos to be returned:
     - GET https://some-api.com/photos?orientation=landscape&size=500x400

##### Path Variable
   - Another way of passing request data to an API is via path variables (a.k.a. "path parameters"). A path variable is a dynamic section of a path and is often used for IDs and entity names such as usernames.

###### Path Variable syntax
- The path variable comes immediately after a slash in the path. For example, the GitHub API allows you to search for GitHub users by providing a username in the path in place of {username} below: 
    GET https://api.github.com/users/{username}

| Path Variable          | Query Parameters                                        |
|------------------------|---------------------------------------------------------|
| ex: /books/abc123      | ex: /books?search=borges&checkedOut=false              |
| Located directly after a slash in the path. It can be anywhere on the path | Located only at the end of a path, right after a question mark? |
| Accepts dynamic values | Accepts defined query keys with potentially dynamic values. |
| Often used for IDs or entity names | Often used for options and filters                       |


### Authorization
  - Think about why you might not want an API to have completely open endpoints that anyone can access publicly. It would allow unauthorized people to access data they shouldn't see, or allow bots to flood an API with thousands of calls per second and shut it down.
  - There are multiple methods for authorizing a request. Some examples are
            - Basic Auth (username and password)
            - OAuth (delegated authorization)
            - API Keys (secret strings registered to a developer from an API portal).

## GraphQL

# Some ways to make API request 
 - **01. XMLHttpReuest**
 - **02. JQuery.get()**
 - **03. Javascript.fetch()**

**01.XMLHttpReuest**
```javascript
var= request = new XMLHttpRequest();
request.open('GET, 'http://hplusupport.com/api/product');
request.onload=function(){
    var response =request.response;
    var parseData=JSON.parse(response);
    console.log(parseData);
}
request.send();
```
**02. JQuery.get()** 
```javascript
$.get('http://hplusupport.com/api/product', function(response) {
 console.log(response)
}
```
**03. fetch()** 
```javascript
fetch('http://hplusupport.com/api/product) //connect and make a request(default in GET )
// then allow us to chain together multiple methods or actions that we want to do with the response
.then(           
 function(response) {
  return response.json(); //take the response and take the data as JSON
}
)
.then(
 function(respData){
  console.log(respData);
}
)
```
