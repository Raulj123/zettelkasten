It's easier to remember a name like `google.com` than something like `122.250.192.232`.

This brings us to Domain Name System (DNS) which is a hierarchical and decentralized naming system used for translating human-readable domain names to IP addresses.

DNS lookup involves the following eight steps:
![[how-dns-works.webp]]

# DNS Resolver
First stop in a DNS query. ==The recursive resolver acts as a middleman between a client and a DNS nameserver.== After receiving a DNS query from a web client, a recursive resolver will either respond with cached data, or send a request to a root nameserver, followed by another request to a TLD nameserver, and then one last request to an authoritative nameserver. After receiving a response from the authoritative nameserver containing the requested IP address, the recursive resolver then sends a response to the client.

# DNS root server
A root server ==accepts a recursive resolver's query which includes a domain name, and the root nameserver responds by directing the recursive resolver to a TLD nameserver==, based on the extension of that domain (`.com`, `.net`, `.org`, etc.).
# TLD nameserver
A TLD nameserver ==maintains information for all the domain names that share a common domain extension, such as== `.com`, `.net`, or whatever comes after the last dot in a URL.
* **Generic top-level domains**: These are domains like `.com`, `.org`, `.net`, `.edu`, and `.gov`.
- **Country code top-level domains**: These include any domains that are specific to a country or state. Examples include `.uk`, `.us`, `.ru`, and `.jp`.
#  Authoritative DNS server
The authoritative nameserver is usually the resolver's last step in the journey for an IP address. ==The authoritative nameserver contains information specific to the domain name it serves== (e.g. [google.com](http://google.com/)) and it can provide a recursive resolver with the IP address of that server found in the DNS A record, or if the domain has a CNAME record (alias) it will provide the recursive resolver with an alias domain, at which point the recursive resolver will have to perform a whole new DNS lookup to procure a record from an authoritative nameserver (often an A record containing an IP address). If it cannot find the domain, returns the NXDOMAIN message.

## Query Types
- **Recursive**: DNS does all the work for you.
- **Iterative**: You (or your computer) keep asking around until you find the answer.
- **Non-recursive**: The DNS already knows and tells you right away.
## DNS Zones, Caching, Reverse 
- **DNS Zones**: Neighborhoods of the internet, managed by someone.
- **DNS Caching**: A "notebook" to remember recent websites for faster browsing.
- **Reverse DNS**: Finding a name from an IP address (important for email security
