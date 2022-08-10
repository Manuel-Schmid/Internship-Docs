# REST API
### 1. What is REST?
REST stands for **RE**presentational **S**tate **T**ransfer. It's an architectural style for distributed hypermedia systems. 

In REST, data and functionality are considered resources and are accessed using Uniform Resource Identifiers (URIs).
The resources are acted upon by using a set of simple, well-defined operations and they have to be decoupled from their 
representation so that clients can access the content in various formats (e.g. HTML, XML, PDF, JSON, PNG, etc.).
It is important that every interaction with the server must be stateless.

    stateless:  Stateless means the computer or program does not keep any record of previous interactions and each 
                interaction request has to be handled based entirely on information that comes with it.

### 2. What is a REST resource?
A resource in REST can be any sort of information that we can name. For example, a REST resource can be a
document or image, a temporal service, a collection of other resources.
The state of the resource, at any particular time, is known as the resource representation.

### 3. What is an API?
What's an API?
An API is a set of definitions and protocols for building and integrating application software.
(Like a contract between an information provider and an information user)

### 4. REST APIs
When a client request is made via a REST(ful) API, it transfers a representation of the state of the resource to the requester.
Most of the time this representation is delivered in JSON but there are other possibilities. 

Commands:

    GET     // to retrieve a resource;
    PUT     // to change the state of or update a resource, which can be an object, file or block;
    POST    // to create a resource;
    DELETE  // to remove a resource.


### 5. Benefits
* Although REST has it's 6 main criteria which RESTful APIs need to conform to it is still considered easier to use than
protocols like SOAP.
* the guidelines can be implemented as needed -> makes REST APIs faster & more lightweight
* increased scalability (due to the server and client separation)
* higher flexibility & portability
* Works very well for IoT and mobile app development. 
* easy to integrate into existing websites.

### 6. Drawbacks / Challenges
* consequences of statelessness: since the requests are stateless the burden of maintaining the 
state lies on the client (client applications becomes heavy)
* Long response times and too much data 
* Redundant requests and/or data


