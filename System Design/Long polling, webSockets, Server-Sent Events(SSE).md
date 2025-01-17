# Long polling
* HTTP Long polling is a technique used to push information to a client as soon as possible from the server
* In Long polling, the server does not close the connection once it receives a request from the client. Instead, the server responds only if any new message is available or a timeout threshold is reached.
## Working (long polling)
Let's understand how long polling works:
1. The client makes an initial request and waits for a response.
2. The server receives the request and delays sending anything until an update is available.
3. Once an update is available, the response is sent to the client.
4. The client receives the response and makes a new request immediately or after some defined interval to establish a connection again.

## Advantages
* Easy to implement, good for small-scale projects.
- Nearly universally supported.

## Disadvantages
- Creates a new connection each time, which can be intensive on the server.
- Reliable message ordering can be an issue for multiple requests.
- Increased latency as the server needs to wait for a new request.

# WebSockets
*  full-duplex(both parties can communicate with each other simultaneously) communication channels over a single TCP connection
*  client establishes a WebSocket connection through a process known as the WebSocket handshake
* standardized way for the server to send content to the client without being asked and allowing for messages to be passed back and forth while keeping the connection open
## Working (WebSockets)
Let's understand how WebSockets work:
1. The client initiates a WebSocket handshake process by sending a request.
2. The request also contains an [HTTP Upgrade](https://en.wikipedia.org/wiki/HTTP/1.1_Upgrade_header) header that allows the request to switch to the WebSocket protocol (`ws://`).
3. The server sends a response to the client, acknowledging the WebSocket handshake request.
4. A WebSocket connection will be opened once the client receives a successful handshake response.
5. Now the client and server can start sending data in both directions allowing real-time communication.
6. The connection is closed once the server or the client decides to close the connection.

# Server-Sent Events(SSE)
* Server-Sent Events (SSE) is a way of establishing long-term communication between client and server that enables the server to proactively push data to the client.
* It is unidirectional, meaning once the client sends the request it can only receive the responses without the ability to send new requests over the same connection.
## Working (SSE)
Let's understand how server-sent events work:
1. The client makes a request to the server.
2. The connection between client and server is established and it remains open.
3. The server sends responses or events to the client when new data is available.