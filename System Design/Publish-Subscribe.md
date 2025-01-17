* Similar to a message queue, publish-subscribe is also a form of service-to-service communication that facilitates asynchronous communication
* In a pub/sub model, any message published to a topic is pushed immediately to all the subscribers of the topic
* he publisher doesn't need to know who is using the information that it is broadcasting, and the subscribers don't need to know where the message comes from
*  bit different than message queues, where the component that sends the message often knows the destination it is sending to

## How it works
- A message topic provides a lightweight mechanism to broadcast asynchronous event notifications and endpoints that allow software components to connect to the topic in order to send and receive those messages.
- To broadcast a message, a component called a _publisher_ simply pushes a message to the topic.
- All components that subscribe to the topic (known as _subscribers_) will receive every message that was broadcasted.

* Amazon SNS
* Google Pub/Sub
