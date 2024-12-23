==A proxy server is an intermediary piece of hardware/software sitting between the client and the backend server.== It receives requests from clients and relays them to the origin servers. Typically, proxies are used to filter requests, log requests, or sometimes transform requests (by adding/removing headers, encrypting/decrypting, or compression).

# Types
1) [Forward Proxy](#Forward Proxy)
2) [Reverse Proxy](#Reverse Proxy])

# Froward Proxy
A forward proxy, often called a proxy, proxy server, or web proxy is a server that ==sits in front of a group of client machines. When those computers make requests to sites and services on the internet, the proxy server intercepts those requests and then communicates with web servers on behalf of those clients, like a middleman.==
# Reverse Proxy
A reverse proxy is a server that sits in front of one or more web servers, intercepting requests from clients. ==When clients send requests to the origin server of a website, those requests are intercepted by the reverse proxy server.==

# Okay? Differences 
*  forward proxy sits in front of a client and ensures that no origin server ever communicates directly with that specific client
* reverse proxy sits in front of an origin server and ensures that no client ever communicates directly with that origin server.

Well, no as a load balancer is useful when we have multiple servers. Often, load balancers route traffic to a set of servers serving the same function, while reverse proxies can be useful even with just one web server or application server. ==A reverse proxy can also act as a load balancer but not the other way around.==