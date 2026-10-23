# Aditya Kumar

Software engineer obsessed with what happens between the network card and application code. Most of my time goes into building low-latency middleware in **Go** and exploring systems architecture in **C++**.

[LinkedIn](https://linkedin.com/in/adityakumar9319) · [Email](mailto:adityakr.swe@gmail.com)

---

### What I Care About

- **Low-Latency & Concurrency:** Eliminating lock contention, handling race conditions gracefully, and building services that don’t choke when traffic spikes.
- **Systems Plumbing:** Reverse proxies, token-bucket limiters, tiered caching architectures, and the Linux TCP stack.
- **Mechanical Sympathy:** Understanding cache lines, memory allocation overhead, and why simple code running close to the OS almost always beats over-abstracted frameworks.

---

### Key Work

#### [SynapseGateway](https://github.com/px444/SynapseGateway) — *AI Reverse Proxy & Semantic Caching Layer*
Upstream inference calls are slow and expensive. I built a Go reverse proxy to sit in front of models and drop response times dramatically:
- **Two-tier caching:** Fast L1 exact-match (SHA-256) paired with an L2 vector cache calculating cosine similarity on 768-dim embeddings.
- **Latency drop:** Slashes latency from ~1,200ms roundtrips to <5ms on cache hits.
- **Concurrency hardening:** Granular mutex synchronization to prevent thundering herds, plus upstream fallback routing when providers fail.

#### [RateLimiter](https://github.com/px444/rate-limiter) — *Sub-Millisecond Token-Bucket Proxy*
A lightweight HTTP reverse proxy built to withstand burst traffic without eating memory:
- Handles **10,000+ req/sec** verified via Go's `testing.B` benchmarks.
- Clean concurrency with zero data races (`go test -race` validated).
- Includes an active eviction daemon that quietly reclaims idle IP state so long-running sessions don't leak memory.

---

### Current Stack & Tools

- **Core:** Go, C++, C, SQL
- **Internals:** Concurrency (`sync`, goroutines), POSIX Threads, Linux Sockets, Memory Layout
- **Toolkit:** Linux, Git CLI, Docker, GDB, Valgrind

---

### What I’m Exploring Right Now

- Diving deeper into high-scale distributed system architectures (caching topologies, database sharding, and consensus).
- Analyzing memory allocation profiles and write-amplification tradeoffs in storage engines.
- Grinding out hard algorithmic problems in C++ (150+ solved on NeetCode/LeetCode with a focus on trees, graphs, and dynamic programming).
```
