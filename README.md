# Application-Programming-Interfaces-(API)
### What is API:
- An Application Programming Interface (API) is a contract that allows code to talk to other code. APIs are the building blocks of modern software because they allow for the sharing of resources and services across applications, organizations, and devices.

### Why are APIs important?
- APIs help developers integrate exciting features and build automation without reinventing the wheel
ex: using a Weather API instead of launching your weather balloons

- APIs allow enterprises to open up their product for faster innovation
ex: apps that interact with Twitter or Meta APIs by posting on your behalf or reading tweets

- APIs can be products themselves
ex: Software as a Service (SaaS) products like Stripe's payment APIs or Twilio's text messaging and email APIs

### Type of API s
  #### Hardware APIs
  - Interface for software to talk to hardware.
    Example: How your phone's camera talks to the operating system.

#### Software Library APIs
  - Interface for directly consuming code from another code base.
    Example: Using methods from a library you import into your application.

#### Web APIs
  - Interface for communicating across code bases over a network.
    Example: Fetching current stock prices from a finance API over the internet.

##### Some of the API 
  - REST (Representational State Transfer)
  - GraphQL
  - WebSockets
  - webhooks
  - SOAP (Simple Object Access Protocol)
  - gRPC (Google Remote Procedure Call)
  - MQTT (MQ Telemetry Transport)

#### Access
 - APIs also vary in the scope of who can access them.

    ##### Public APIs (aka Open APIs)
    - Consumed by anyone who discovers the API

    ##### Private APIs
    - Consumed only within an organization and not made public

    ##### Partner APIs
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
  - In addition to a request method, a request must include a request URL that indicates where to make the API call. A request URL has three parts: a protocol (such as http:// or https://), host (location of the server), and path (route on the server). In REST APIs, the path often points to a reference entity, like "books".
    
```javascript
// Protocol	    Host	                            Path
    https://	    library-api.postmanlabs.com	        /books
```

##### Request-Response pattern
  ![image](https://github.com/GayashanDeshapriya/Application-Programming-Interfaces-API-/assets/94686812/c62097db-4bed-4255-8535-cea830f7b3e0)

