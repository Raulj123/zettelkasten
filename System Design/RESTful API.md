## What is a RESTful API?
RESTful API is an interface that two computer systems use to exchange information securely over the internet.

## What is an API?
* An application programming interface (API) defines the rules that you must follow to communicate with other software systems
* You can think of a web API as a gateway between clients and resources on the web

## Clients
Clients are users who want to access information from the web

## Resources
* Resources are the information that different applications provide to their clients.
*  Resources can be images, videos, text, numbers, or any type of data.
* The machine that gives the resource to the client is also called the server

## What is REST?
* Representational State Transfer (REST) is a software architecture that imposes conditions on how an API should work
* API developers can design APIs using several different architectures
*  you can use the terms REST API and RESTful API interchangeably

# Principles of the REST architectural style

## Uniform Interface
* **Identify resources**: Every resource has a unique URL (like an address for a file).
- **Understand resources**: The server sends extra info (metadata) so clients know what the resource is and how to update or delete it.
- **Process resources**: The server explains how to use the data by including helpful details in the message.
- **Discover more**: The server includes links to related resources so clients can find everything they need.

## Statelessness
Statelessness in REST means that the **server doesn’t remember anything** about previous requests.

## Layered System
A **layered system** in REST means the client doesn’t directly deal with the server—it can go through other layers (like security, caching, or load balancers) before reaching the server

## Cacheability
* RESTful web services support caching, which is the process of storing some responses on the client or on an intermediary to improve server response time.
*  RESTful web services control caching by using API responses that define themselves as cacheable or noncacheable.

## Code on demand
Return executable code to support a part of your application. _(optional)_

#  What does the RESTful API client request contain?

* ## Unique Resource Identifier 
	* The server identifies each resource with unique resource identifiers
	* server typically performs resource identification by using a Uniform Resource Locator (URL)
	* URL is also called the request endpoint and clearly specifies to the server what the client requires
* ## Method
	* Developers often implement RESTful APIs by using the Hypertext Transfer Protocol (HTTP). An HTTP method tells the server what it needs to do to the resource. The following are four common HTTP methods:
	* https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods
* ## Headers 
	* HTTP headers let the client and server pass additional information's with an HTTP request or response
	* ``` casesensitive : value ``` 
	* ### Grouped according to their contexts
		* General Headers: info about request/response
		* Request Headers: info about the request
		* Response Headers: info about the response
		* Entity Headers: info about the body
	* ### Categories of HTTP Headers
		* Authentication 
		* Caching
		* CORS
		* etc. so many
* ## Parameters
	* Path parameters that specify URL details.
	- Query parameters that request more information about the resource.
	- Cookie parameters that authenticate clients quickly.

# What are RESTful API authentication methods?
* ## HTTP auth
	* HTTP defines some authentication schemes that you can use directly when you are implementing REST API:
		* _**Basic authentication**_
			* In basic authentication, the client sends the user name and password in the request header. It encodes them with base64, which is an encoding technique that converts the pair into a set of 64 characters for safe transmission.
		*  _**Bearer authentication**_
			* The term bearer authentication refers to the process of giving access control to the token bearer. The bearer token is typically an encrypted string of characters that the server generates in response to a login request. The client sends the token in the request headers to access resources.
* ## API Keys
	*  server assigns a unique generated value to a first-time client. Whenever the client tries to access resources, it uses the unique API key to verify itself. API keys are less secure because the client has to transmit the key, which makes it vulnerable to network theft.
* ## OAuth
	* OAuth combines passwords and tokens for highly secure login access to any system
	* server first requests a password and then asks for an additional token to complete the authorization process
	* can check the token at any time and also over time with a specific scope and longevity

# What does the RESTful API server response contain?
REST principles require the server response to contain the following main components:
* ## Status Line
	* The status line contains a three-digit status code that communicates request success or failure. For instance, ==2XX codes indicate success,== but ==4XX and 5XX codes indicate errors==. ==3XX codes indicate URL redirection.==
* ## Message Body
	* The response body contains the resource representation.
	*  server selects an appropriate representation format based on what the request headers contain
	* Clients can request information in XML or JSON formats, which define how the data is written in plain text
* ## Headers 
	* Yea they can also have headers lol


No code generation, must use 3rd party libs(swagger)