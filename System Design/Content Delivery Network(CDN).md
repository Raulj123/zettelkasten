A content delivery network (CDN) is a geographically distributed group of servers that work together to provide fast delivery of internet content. Generally, static files such as HTML/CSS/JS, photos, and videos are served from CDN.

# why use?
Serving content from CDNs can significantly improve performance as users receive content from data centers close to them and our servers do not have to serve requests that the CDN fulfills.

# How it works
![[cdn.webp]]
- **Origin Server**: Contains the original content.
- **Edge Servers**: Distributed worldwide to cache content closer to users.
- **Content Delivery**: When a user requests content, the closest edge server delivers it instead of the origin server. This reduces latency and load on the origin server, improving website speed and scalability.
- **Example**: A request from the UK for a website hosted in the USA would be served from the nearest edge location in London, speeding up delivery to the user.
# Types
Push CDN:
Action: Content is uploaded to the CDN manually whenever changes occur.
Pro: Minimal traffic since only new or changed content is uploaded.
Best For: Sites with low traffic or infrequently updated content.

Pull CDN:
Action: Content is fetched from the origin server only when a request requires it.
Pro: Requires less maintenance and more evenly distributes traffic.
Best For: Sites with heavy traffic where content changes frequently.