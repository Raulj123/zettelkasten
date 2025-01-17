## Monoliths 
* Self contained and Independent application 
* Advantages 
	* Simple to develop/debug
	* Fast and reliable communication
	* Easy monitoring and testing
	* Supports Acid transaction 
* Disadvantages
	* Maintenance becomes hard as the codebase grows
	- Tightly coupled application, hard to extend
	- Requires commitment to a particular technology stack
	- On each update, the entire application is redeployed
	
## Modular Monoliths
* Build and deploy single app, but build it in a way that breaks up the code into independent modules for each features needed.
* Need some examples between Modular vs monolithic 

## Microservices
 *  consists of a collection of small, autonomous services where each service is self-contained and should implement a single business capability within a bounded context
 * Each service has a separate codebase, which can be managed by a small development team
 *  Services can be deployed independently and a team can update an existing service without rebuilding and redeploying the entire application
 * Services are responsible for persisting their own data or external state (database per service)
 * ## Characteristics 
	 * Loosely Coupled: : Services should be loosely coupled so that they can be independently deployed and scaled
	 * Highly maintainable: Service should be easy to maintain and test because services that cannot be maintained will be rewritten.
	 * **Resilience & Fault tolerance**: Services should be designed in such a way that they still function in case of failure or errors. In environments with independently deployable services, failure tolerance is of the highest importance
* Advantages 
	* [Loosely coupled services](https://stackoverflow.com/questions/2832017/what-is-the-difference-between-loose-coupling-and-tight-coupling-in-the-object-o)
	* Services deployed Independently 
	* Highly agile 
	* Improves fault tolerance and data isolation 
* ## Best Practices 
	* Model services around the business domain.
	- Services should have loose coupling and high functional cohesion.
	- Isolate failures and use resiliency strategies to prevent failures within a service from cascading.
	- Services should only communicate through well-designed APIs. Avoid leaking implementation details.
	- Data storage should be private to the service that owns the data
	- Avoid coupling between services. Causes of coupling include shared database schemas and rigid communication protocols.
	- Decentralize everything. Individual teams are responsible for designing and building services. Avoid sharing code or data schemas.
	- Fail fast by using a [[Circuit Breaker]] to achieve fault tolerance.
	- Ensure that the API changes are backward compatible
* ## Pitfalls 
	* Service boundaries are not based on the business domain.
	- Underestimating how hard is to build a distributed system.
	- Shared database or common dependencies between services.
	- Lack of Business Alignment.
	- Lack of clear ownership.
	- Lack of idempotency.
	- Trying to do everything ACID instead of BASE
	- Lack of design for fault tolerance may result in cascading failures.

## Service-oriented architecture (SOA)
*  defines a way to make software components reusable via service interfaces
* These interfaces utilize common communication standards and focus on maximizing application service reusability whereas microservices are built as a collection of various smallest independent service units focused on team autonomy and decoupling
* Still meh about this




