A cache's primary purpose is to increase data retrieval performance by reducing the need to access the underlying slower storage layer.
- **Cache Basics**: A cache is a small, fast memory storing frequently accessed data for quicker retrieval.
- **Levels (L1, L2, L3)**: Data is stored and searched in a hierarchy of levels, starting with the fastest and smallest (L1) and moving to slower, larger levels (L2, L3, etc.).
- **Read/Write Process**:
    - **Reading**: Searches begin at L1. If not found, it moves to the next level until the data is located or missed.
    - **Writing**: If data isn’t found, it’s written into the cache for future quick access.
- **Blocks and Tags**: Data is stored in **blocks** with tags indicating its location for efficient searching.

# Hit or miss
#### Cache hit
- Data is successfully retrieved from the cache.
- **Types of Cache Hits**:
    - **Hot Cache**: Fastest, data retrieved from L1.
    - **Warm Cache**: Medium speed, data found in L2 or L3.
    - **Cold Cache**: Slowest, data found in lower levels (e.g., L3+).

#### **Cache Miss**:
- Data is not found in the cache, triggering a fetch from the main source.
- Once retrieved, the data is written to the cache for future access.
# Invalidation
Cache invalidation is a process where the computer system declares the cache entries as invalid and removes or replaces them.

# Caching systems 
- **Write-Through Cache**:
    - **Action**: Writes data to both the cache and the database simultaneously.
    - **Pro**: Ensures consistency between cache and database.
    - **Con**: Higher write latency due to dual writes.
- **Write-Around Cache**:
    - **Action**: Writes directly to the database, bypassing the cache.
    - **Pro**: Reduces write latency.
    - **Con**: Increases cache misses; data must be fetched from the database during read operations.
- **Write-Back Cache**:
    - **Action**: Writes data to the cache first, then asynchronously writes to the database.
    - **Pro**: Lower write latency and higher throughput for write-intensive applications.
    - **Con**: Risk of data loss if the cache fails before the data is written to the database