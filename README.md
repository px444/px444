# Aditya Kumar

Software Engineer focused on backend infrastructure, network middleware, and concurrency engineering. Building low-latency services in **Go** and systems algorithms in **C++**.

[LinkedIn](https://linkedin.com/in/adityakumar9319) · [Email](mailto:adityakr.swe@gmail.com)

---

### Core Technical Focus

- **Languages:** Go, C++, C, SQL
- **Systems & Backend:** High-concurrency services, reverse proxies, multi-tier caching, race synchronization, token-bucket rate limiting
- **Low-Level Fundamentals:** POSIX systems programming, memory management, TCP/IP sockets, Linux internals

---

### Featured Projects

#### [SynapseGateway](https://github.com/px444/SynapseGateway)
*Asynchronous AI reverse proxy and caching middleware in Go*

- Implemented a two-tier caching architecture: L1 exact SHA-256 hash lookup and L2 768-dimensional vector cache using cosine similarity.
- Bypasses upstream model calls on cache hits, reducing request latency from ~1,200ms to <5ms.
- Designed thread-safe mutex pools to prevent cache stampedes and added automated failover across upstream providers.

#### [RateLimiter](https://github.com/px444/rate-limiter)
*High-throughput token-bucket reverse proxy in Go*

- Built an in-memory token-bucket rate limiter with per-IP state isolation.
- Benchmarked at 10,000+ req/sec using `testing.B` with zero data races (`go test -race` verified).
- Implemented an asynchronous background cleaner to sweep expired client buckets and prevent memory growth under burst traffic.

---

### Foundations

- **Data Structures & Algorithms:** 150+ problems solved in modern C++ (graphs, trees, bit manipulation, DP).
- **Tooling:** Linux / Bash, Git CLI, Docker, GDB, Valgrind.
