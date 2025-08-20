# System-Design-Interview

---

# Top 30 System Design Interview Questions and Answers

## 1. What is System Design?

* **Definition**: Process of defining the architecture, components, modules, interfaces, and data for a system.
* **Goal**: Build a system that is **scalable, reliable, maintainable, and efficient**.
* **Example**: Designing YouTube involves video upload, streaming, caching, and recommendation system.

---

## 2. What is Scalability in System Design?

* **Scalability**: Ability of a system to handle increased load.
* **Types**:

  * Vertical Scaling (adding more power to one server).
  * Horizontal Scaling (adding more servers).
* **Example**: Adding more servers in a load-balanced cluster.

---

## 3. What is Latency vs Throughput?

* **Latency**: Time taken to process a single request.
* **Throughput**: Number of requests a system can process per second.
* **Trade-off**: Optimizing one may affect the other.
* **Example**:

  * Latency: Netflix video starts in 1 sec.
  * Throughput: Netflix streams 10M videos/sec.

---

## 4. Explain Load Balancer

* **Definition**: Distributes traffic across multiple servers.
* **Types**:

  * L4 (TCP/UDP).
  * L7 (Application level - HTTP/HTTPS).
* **Example**: Nginx, HAProxy, AWS ELB.

---

## 5. What is Caching? Why is it important?

* **Caching**: Storing frequently accessed data in memory to reduce DB load.
* **Benefits**: Faster response, less DB usage.
* **Example**: Redis, Memcached.

---

## 6. What are CAP Theorem and its trade-offs?

* **CAP Theorem**: A distributed system can only provide **2 out of 3**:

  * Consistency (all nodes have same data).
  * Availability (system always responds).
  * Partition Tolerance (system works despite network failures).
* **Example**:

  * CP: HBase.
  * AP: Cassandra.
  * CA: Single node SQL DB.

---

## 7. Difference between SQL and NoSQL in system design?

* **SQL**: Structured, relational, strict schema (MySQL, PostgreSQL).
* **NoSQL**: Unstructured, flexible schema, high scalability (MongoDB, Cassandra).
* **Example**:

  * Banking → SQL.
  * Social media posts → NoSQL.

---

## 8. What is CDN (Content Delivery Network)?

* **CDN**: Distributes content across global servers to reduce latency.
* **Use case**: Images, videos, static assets.
* **Example**: Cloudflare, Akamai.

---

## 9. Explain Message Queues

* **Definition**: Used for async communication between services.
* **Examples**: Kafka, RabbitMQ, AWS SQS.
* **Use case**: Order processing in e-commerce.

---

## 10. What is Event-driven Architecture?

* **Definition**: System where services react to events.
* **Benefits**: Loose coupling, scalability.
* **Example**: Payment service triggers notification service after transaction success.

---

## 11. Difference between Monolithic vs Microservices?

* **Monolithic**: Single codebase, tightly coupled.
* **Microservices**: Independent services communicating via APIs.
* **Trade-offs**: Microservices improve scalability but increase complexity.

---

## 12. What is Sharding?

* **Sharding**: Splitting a database into smaller parts (shards) to improve scalability.
* **Example**: Splitting users DB by region (Asia DB, Europe DB).

---

## 13. Explain Replication

* **Replication**: Copying data across multiple servers for fault tolerance.
* **Types**: Master-Slave, Master-Master.
* **Example**: MySQL replication for read-heavy workloads.

---

## 14. What is Rate Limiting?

* **Definition**: Controlling how many requests a user/system can make in a time period.
* **Use case**: Prevent abuse, API protection.
* **Example**: 100 API calls/min per user.

---

## 15. Explain Consistent Hashing

* **Definition**: A hashing technique that evenly distributes data across nodes in a scalable way.
* **Use case**: Load balancing, distributed caching.

---

## 16. What is Idempotency in APIs?

* **Definition**: Multiple identical requests produce the same result.
* **Example**: Payment API → charging once even if API is retried.

---

## 17. Difference between Synchronous and Asynchronous Communication

* **Sync**: Immediate response (REST).
* **Async**: Delayed, via queues/events (Kafka).
* **Use case**:

  * Sync → Login API.
  * Async → Notification email sending.

---

## 18. What is Database Indexing?

* **Definition**: Data structure that speeds up queries.
* **Trade-off**: Faster reads, slower writes.
* **Example**: Index on `user_id` column.

---

## 19. Explain Leader Election in Distributed Systems

* **Definition**: Choosing a single node as a leader to coordinate tasks.
* **Example**: Zookeeper does leader election.

---

## 20. What is Data Partitioning?

* **Definition**: Breaking large datasets into smaller partitions.
* **Types**: Range partitioning, Hash partitioning.

---

## 21. How do we design a URL Shortener like bit.ly?

* **Steps**:

  * API to shorten URL.
  * Store mapping in DB.
  * Redirect service.
  * Cache for fast lookup.

---

## 22. How do we design a Messaging System like WhatsApp?

* **Components**:

  * Messaging Queue (Kafka).
  * Storage (Cassandra).
  * Push Notifications.
  * End-to-end encryption.

---

## 23. How do we design a Feed System like Facebook/Instagram?

* **Steps**:

  * Store user posts.
  * Generate feed (push vs pull model).
  * Cache feed.
  * Ranking algorithm.

---

## 24. How do we design a Payment Gateway?

* **Steps**:

  * API for payment.
  * Connect to banks/payment processors.
  * Ensure **idempotency**.
  * Handle retries & failures.
  * Security: PCI-DSS, encryption.

---

## 25. What is Circuit Breaker in Microservices?

* **Definition**: Prevents cascading failures by stopping calls to failing service.
* **Example**: Netflix Hystrix, Resilience4j.

---

## 26. What is a Saga Pattern in Microservices?

* **Definition**: Manages distributed transactions using events/compensation.
* **Use case**: Order → Payment → Shipping. If payment fails, cancel order.

---

## 27. Explain CQRS (Command Query Responsibility Segregation)

* **Definition**: Separate write (command) and read (query) operations.
* **Benefit**: Optimized performance and scalability.

---

## 28. What is Event Sourcing?

* **Definition**: Store system state as a sequence of events.
* **Benefit**: Full audit history, replayability.
* **Example**: Banking transactions.

---

## 29. Explain API Gateway

* **Definition**: Entry point for all client requests in microservices.
* **Features**: Routing, authentication, rate limiting.
* **Example**: Spring Cloud Gateway, Kong.

---

## 30. How do we design a High-Availability System?

* **Principles**:

  * Redundancy.
  * Failover.
  * Replication.
  * Load balancing.
* **Example**: Active-passive DB setup with automatic failover.

---
