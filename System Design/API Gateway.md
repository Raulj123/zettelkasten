* API management tool that sits between a client and a collection of backend services 
* Responsibilities
	* Authentication
	* monitoring
	* [[Load Balancing]]
	* [[Caching]]
	* throttling
	* logging, etc.
* ### Why we need it?
	* single entry point for all clients with some additional features and better management
* ### Features
	* Authentication
	* [[Service Discovery]]
	* Reverse [[Proxy]]
	* [[Caching]]
	* Security
	* Retry and [[Circuit Breaker]]
	* [[Load Balancing]]
	* Logging, Tracing
	* API composition
	* [[Rate Limiting]] and throttling
	* Versioning
	* Routing
	* IP whitelisting or backlisting

## Advantages
- Encapsulates the internal structure of an API.
- Provides a centralized view of the API.
- Simplifies the client code.
- Monitoring, analytics, tracing, and other such features.

## Disadvantages
- Possible single point of failure.
- Might impact performance.
- Can become a bottleneck if not scaled properly.
- Configuration can be challenging.

# Backend for Frontend (BFF) pattern
*  we create separate backend services to be consumed by specific frontend applications or interfaces
* sometimes the output of data returned by the microservices to the front end is not in the exact format or filtered as needed by the front end
*  get the required data from the appropriate service, format the data, and sent it to the frontend
* ## When to use?
	*  shared or general purpose backend service must be maintained with significant development overhead.
	- We want to optimize the backend for the requirements of a specific client.
	- Customizations are made to a general-purpose backend to accommodate multiple interfaces.
## Examples
* Amazon API Gateway
* Apigee API Gateway
* Azure API Gateway
* Kong API Gateway