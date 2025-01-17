* Event-Driven Architecture (EDA) is about using events as a way to communicate within a system
*  Generally, leveraging a [[Message Broker]] to publish and consume events asynchronously

## What is an event?
* data point that represents state changes in a system
* only notifies the system of a particular state change

## Components
* Event producers: Publishes an event to the router
* Event routers: Filters and pushes the events to consumers
* Event consumers: Uses events to reflect changes in the system ![[event-driven-architecture.webp]]

## Patterns
* [[Sagas]]
* [[Publish-Subscribe]]
* [[Event Sourcing]]
* [[Command and Query Responsibility Segregation (CQRS)]]

## Advantages 
- Decoupled producers and consumers.
- Highly scalable and distributed.
- Easy to add new consumers.
- Improves agility.

## Challenges 
- Guaranteed delivery.
- Error handling is difficult.
- Event-driven systems are complex in general.
- Exactly once, in-order processing of events.

### examples
Used tech to implement this shi
* NATS
* Apache Kafka
* Amazon EventBridge
* Amazon SNS
* Google PubSub