* storing just the current state of the data in a domain, use an append-only store to record the full series of actions taken on that data
* Like a banking system stores all history
* Advantages
	* Excellent for real-time data reporting.
	- Great for fail-safety, data can be reconstituted from the event store.
	- Extremely flexible, any type of message can be stored.
	- Preferred way of achieving audit logs functionality for high compliance systems.
* Disadvantages
	* Requires an extremely efficient network infrastructure.
	- Requires a reliable way to control message formats, such as a schema registry.
	- Different events will contain different payloads.