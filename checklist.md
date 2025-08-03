Here is a **step-by-step checklist** with guiding **questions** for each phase of the system design interview. Use this as your **mental flowchart** during interviews or practice — it ensures you don’t miss any critical part and keeps your approach structured and impressive.

---

## ✅ Step-by-Step System Design Interview Checklist

---

### **🟩 Step 1: Clarify Requirements and Scope**

**Goal:** Understand exactly what you're building and at what scale.

#### ✅ Ask Functional Requirements

* What are the core features of this system?
* What are the user roles and their key actions?
* Should we support real-time interactions? (e.g., messaging, notifications)
* Are there any specific workflows to support? (e.g., sign up → upload photo → follow user)

#### ✅ Ask Non-Functional Requirements

* What are the performance expectations (e.g., latency < 100ms)?
* What availability and uptime does the system require?
* Is data consistency critical, or is eventual consistency acceptable?
* What are the security/privacy concerns?
* Should the system scale globally or regionally?

#### ✅ Estimate Scale and Constraints

* How many users per day / per second?
* How much data is generated daily?
* Peak traffic vs average traffic?
* Are there any constraints? (e.g., real-time, GDPR, SLA targets, limited budget)

---

### **🟨 Step 2: Define High-Level Architecture**

**Goal:** Create a modular blueprint of system components and how they interact.

#### ✅ Identify Core Components

* What major services/modules do we need? (e.g., user service, feed service, media storage)
* Which ones are **read-heavy** and which are **write-heavy**?
* What are the external dependencies? (e.g., payment gateways, map APIs)

#### ✅ Define Communication Flow

* How do clients interact with the backend? (REST, GraphQL, WebSocket)
* How do backend services talk to each other? (sync HTTP calls, async queues)

#### ✅ Sketch the Architecture

* What are the main boxes and arrows? (clients, APIs, services, databases, queues)
* How do requests and data flow through the system?

---

### **🟦 Step 3: Design Data Models and Storage**

**Goal:** Define how data is structured and stored.

#### ✅ Model Core Entities

* What are the main data entities? (e.g., User, Post, Order, Message)
* What are the relationships between them?

#### ✅ Choose Storage Solutions

* SQL or NoSQL? Why?
* Do we need blob/object storage (e.g., images/videos)?
* Do we need search/indexing (e.g., ElasticSearch)?

#### ✅ Estimate and Plan for Data Size

* How much storage will we need after 1 year?
* Do we need sharding or partitioning?

---

### **🟧 Step 4: Add Performance & Scalability Components**

**Goal:** Make the system handle high load, low latency, and growth.

#### ✅ Add Caching Layers

* What are our hot paths for reads? Can we cache them?
* What caching system to use (Redis, Memcached)?
* How to handle cache invalidation?

#### ✅ Load Balancing & Horizontal Scaling

* Do we need a load balancer in front of each service?
* Are services stateless for easy scaling?
* What are our autoscaling strategies?

#### ✅ Use Asynchronous Processing Where Needed

* Any slow tasks to offload? (e.g., email, transcoding, image resize)
* Should we add a queue system (Kafka, RabbitMQ, SQS)?

---

### **🟥 Step 5: Ensure Reliability and Availability**

**Goal:** Prevent system failure and ensure graceful degradation.

#### ✅ Add Redundancy & Failover

* Do we replicate services and databases across zones/regions?
* What happens when a service or database goes down?

#### ✅ Handle Rate Limiting and Backpressure

* Do we need to protect services from abuse or traffic spikes?
* Should we use API throttling, circuit breakers?

#### ✅ Define Monitoring and Alerting

* How do we know if something breaks? (logs, metrics, traces)
* What are our SLAs/SLOs?

---

### **🟫 Step 6: Address Additional Concerns**

**Goal:** Round out the design with missing but important pieces.

#### ✅ Security

* How do we authenticate and authorize users?
* Do we encrypt data at rest and in transit?

#### ✅ Data Privacy & Compliance

* Do we need GDPR or HIPAA compliance?
* Do we need user audit logs or data deletion tools?

#### ✅ Cost Efficiency

* Are we using appropriate services for traffic patterns?
* Can we batch or compress data to save storage?

---

### **🟪 Step 7: Summarize and Discuss Trade-Offs**

**Goal:** Wrap up and show maturity in reasoning.

#### ✅ Review Coverage

* Did I address all functional and non-functional requirements?
* Did I miss any components (notifications, search, analytics)?

#### ✅ Call Out Trade-Offs

* Why did I choose SQL over NoSQL (or vice versa)?
* Why did I pick fan-out-on-write vs fan-out-on-read?
* What is the trade-off between consistency and availability?

#### ✅ Mention Future Improvements

* What would I improve or revisit if I had more time?
* How could we evolve this design as the user base grows?

---

Let me know if you want this in a printable template or Anki-style flashcards!
