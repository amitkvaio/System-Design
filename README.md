# System-Design
System Design is the process of planning and defining the architecture of a software system. It focuses on how different components like databases, APIs, caching, load balancers, and microservices interact to build a scalable, reliable, and maintainable system.

* Prepare **point-wise notes** on **System Design basics + Top Interview Questions** (like the 30 I listed).
* Keep the language **simple and clear**.
* Add **examples wherever useful**.
* Provide the document in **Word (.docx)** or **PDF** so we can keep it as our interview prep guide.

---

# 📘 System Design – Quick Notes

## 1. What is System Design?

* Process of planning and creating the architecture of a software system.
* Goal → Build a system that is **scalable, reliable, and maintainable**.
* Example: Designing YouTube (video upload, streaming, recommendations).

---

## 2. Key Concepts in System Design

* **Scalability** → System grows with traffic (vertical vs horizontal).
* **Reliability** → System works even when parts fail.
* **Availability** → System is up and responding most of the time.
* **Performance** → Low latency, high throughput.
* **Consistency** → Data is same everywhere.
* **Fault Tolerance** → System survives failures.

---

## 3. Common Components

* **Load Balancer** → Distributes traffic to multiple servers.
* **Cache (Redis, Memcached)** → Speeds up reads.
* **Database (SQL, NoSQL)** → Stores data.
* **Message Queue (Kafka, RabbitMQ)** → Handles async tasks.
* **CDN** → Serves static content globally.
* **API Gateway** → Entry point for microservices.

---

## 4. Most Asked System Design Questions

* Design **URL Shortener** (bit.ly).
* Design **Chat System** (WhatsApp).
* Design **News Feed** (Facebook/Instagram).
* Design **E-commerce System** (Amazon/Flipkart).
* Design **Payment System** (PayPal).
* Design **Distributed Cache**.
* Design **File Storage System** (Google Drive, Dropbox).

---

## 5. Important Patterns

* **CAP Theorem** (Consistency, Availability, Partition Tolerance).
* **Sharding** → Split DB into smaller parts.
* **Replication** → Copy data for reliability.
* **Rate Limiting** → Restrict API requests.
* **Circuit Breaker** → Stop cascading failures.
* **Saga Pattern** → Handle distributed transactions.
* **CQRS + Event Sourcing** → Separate read/write & keep audit history.
---
