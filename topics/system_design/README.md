# System Design Preparation Guide 🏗️

A blueprint for tackling both Low-Level Design (LLD / Machine Coding) and High-Level Design (HLD) interview rounds.

---

## 🏛️ High-Level Design (HLD) Framework (45 mins)

When designing large scale distributed systems:

1. **Step 1: Clarify Requirements & Scope (5 mins)**
   - Functional: What core actions can users take?
   - Non-Functional: High availability vs Consistency (CAP), latency SLA (e.g. < 100ms), throughput, durability.
   - Out of scope items.

2. **Step 2: Back-of-the-Envelope Estimation (5 mins)**
   - DAU / MAU, read-to-write ratio.
   - QPS (Queries per second) = $\frac{\text{Daily Requests}}{86400}$.
   - Storage requirements over 5 years.
   - Network bandwidth (inbound and outbound).

3. **Step 3: High-Level Architecture & API Design (15 mins)**
   - REST / gRPC API contracts.
   - Database schema (SQL vs NoSQL).
   - Component block diagram: Clients $\to$ CDN / DNS $\to$ Load Balancer $\to$ API Gateway $\to$ Microservices $\to$ Cache (Redis) $\to$ Database (Primary-Replica) + Message Queue (Kafka/RabbitMQ).

4. **Step 4: Deep Dive & Bottlenecks (15 mins)**
   - Database scaling (Sharding, Partition keys, Replication lag).
   - Caching strategies (Cache-aside, Write-through, Eviction policies like LRU).
   - Rate limiting, failure recovery, single points of failure (SPOF).

### Classic HLD Problems:
- URL Shortener (TinyURL)
- Distributed Rate Limiter
- Notification Service
- Instagram / Twitter Newsfeed
- Ride Sharing Service (Uber / Lyft)

---

## 📐 Low-Level Design (LLD / Machine Coding)

Focuses on writing clean, modular, extensible code adhering to OOP & SOLID principles within 90–120 minutes.

### Standard Template:
1. Identify Entities and Actors.
2. Define Interfaces, Abstract Classes, and Enumerations.
3. Apply appropriate Design Patterns (Factory, Strategy, Observer, State).
4. Implement Thread-Safe Concurrency where applicable.
5. Write simple unit tests / driver `main()` method.

### Classic LLD Problems:
- Parking Lot System
- LRU / LFU Cache
- Snake and Ladder Game
- Splitwise Expense Sharing App
- Movie Ticket Booking System (BookMyShow)
