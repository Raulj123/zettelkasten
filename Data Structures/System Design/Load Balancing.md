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
