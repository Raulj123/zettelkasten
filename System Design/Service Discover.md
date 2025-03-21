* Service discovery is the technology to automatically detect services and devices on a computer network
* a networking standard that accomplishes the detection of networks by identifying resources
* ## Why we need it?
	*  modern microservices-based applications typically run in virtualized or containerized environments where the number of instances of a service and their locations change dynamically. Consequently, we need a mechanism that enables the clients of service to make requests to a dynamically changing set of ephemeral service instances

# Implementations
* ## Client-side discovery
	*  client obtains the location of another service by querying a [service registry](#Servvice Registry) which is responsible for managing and storing the network locations of all the services.
* ## Server-side discovery
	* intermediate component such as a load balancer. The client makes a request to the service via a load balancer which then forwards the request to an available service instance.

# Service Registry
* database containing the network locations of service instances to which the clients can reach out
# Service Registration
We also need a way to obtain service information, often known as service registration. Let's look at two possible service registration approaches:

### Self-Registration
When using the self-registration model, a service instance is responsible for registering and de-registering itself in the Service Registry. In addition, if necessary, a service instance sends heartbeat requests to keep its registration alive.

### Third-party Registration
The registry keeps track of changes to running instances by polling the deployment environment or subscribing to events. When it detects a newly available service instance, it records it in its database. The Service Registry also de-registers terminated service instances.

### Service Mesh
Service-to-service communication is essential in a distributed application but routing this communication, both within and across application clusters, becomes increasingly complex as the number of services grows. Service mesh enables managed, observable, and secure communication between individual services. It works with a service discovery protocol to detect services. [Istio](https://istio.io/latest/about/service-mesh) and [envoy](https://www.envoyproxy.io/) are some of the most commonly used service mesh technologies.

Here are some commonly used service discovery infrastructure tools:
- [etcd](https://etcd.io/)
- [Consul](https://www.consul.io/)
- [Apache Thrift](https://thrift.apache.org/)
- [Apache Zookeeper](https://zookeeper.apache.org/)