Load balancing lets us distribute incoming network traffic across multiple resources ensuring high availability and reliability by sending requests only to resources that are online.
![[load-balancer-layers.webp]]
# Why?
* scale to meet high volumes, modern computing best practices 
* no single server is overworked 
* server goes down load balancer redirects traffic 
# Workload distribution

- **Host-based**: Routes based on **hostname** (e.g., `shop.` vs. `blog.`).
- **Path-based**: Routes based on the **URL path** (e.g., `/products` vs. `/checkout`).
- **Content-based**: Routes based on **request details** (e.g., user location or specific parameters).
# Layers 
- **Network Layer (Layer 4)**:
    - **Fast** and uses basic info like IPs/ports to route traffic.
    - These are often dedicated hardware devices that can operate at high speed.
- **Application Layer (Layer 7)**:
    - **Smart** and uses the full request to make routing decisions.
    - This allows the management of load based on a full understanding of traffic.
# Types
* **Software Load Balancers**: Easier, cost-effective, and flexible; ideal for custom configurations but require more setup. Available as installable solutions or managed cloud services.
- **Hardware Load Balancers**: Physical devices with high traffic capacity but expensive, less flexible, and require firmware updates and maintenance.

# What it does not do 
DNS does not check for server and network outages, or errors. It always returns the same set of IP addresses for a domain even if servers are down or inaccessible.

# Advantages 
- Scalability
- Redundancy
- Flexibility
- Efficiency
# Failure of a load balancer?
As you must've already guessed, the load balancer itself can be a single point of failure. To overcome this, a second or `N` number of load balancers can be used in a cluster mode.