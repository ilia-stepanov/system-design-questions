Source is https://web.archive.org/web/20220926171507/https://www.lecloud.net/post/9699762917/scalability-for-dummies-part-4-asynchronism

## 🧠 **Scalability for Dummies – Part 4: Asynchronism – System Design Test**

---

**1. What real-world analogy does the article use to introduce the concept of asynchronism?**
A) Ordering coffee at a café
B) Waiting in line at a post office
C) Buying bread at a bakery
D) Getting your car washed

---

**2. Why is asynchronism important in a web service context?**
A) It removes the need for caching
B) It allows background processing to improve user experience
C) It eliminates server load
D) It reduces frontend code complexity

---

**3. What is the first paradigm of asynchronism described in the article?**
A) Lazy loading on the frontend
B) Doing background tasks during user login
C) Pre-computing results in advance
D) Parallelizing all frontend API calls

---

**4. What does “bake the breads at night and sell them in the morning” represent in web apps?**
A) Data compression
B) Multi-tenant architecture
C) Static site generation / pre-rendering
D) Session replication

---

**5. Which technique is commonly used to implement async #1 (pre-computing)?**
A) Load balancing
B) WebSocket streaming
C) Cronjobs that trigger rendering scripts
D) Blockchain event listeners

---

**6. What is the main benefit of hosting pre-rendered HTML files on S3 or a CDN?**
A) Encryption at rest
B) Automatic SEO optimization
C) Better analytics
D) Extremely scalable and responsive websites

---

**7. What type of content is best suited for pre-computing in advance?**
A) Personalized notifications
B) Frequently changing product availability
C) General, predictable content
D) Live chat messages

---

**8. What is the second paradigm of asynchronism described in the article?**
A) Polling from the backend every 10 seconds
B) Scheduling SQL backups
C) Handling dynamic, user-triggered tasks via job queues
D) Moving all logic to frontend

---

**9. What’s the role of the job queue in async #2?**
A) Delays frontend requests
B) Stores user sessions
C) Holds tasks until a worker picks them up
D) Validates user permissions

---

**10. What happens after a worker completes a job from the queue?**
A) It logs the task but does not respond
B) It clears the cache
C) It sends a “job done” signal that the frontend can check
D) It updates the user database schema

---

**11. What is the benefit of signaling “job in progress” immediately to the user?**
A) Increases CPU usage
B) Prevents Redis failures
C) Keeps the UI responsive and improves UX
D) Makes frontend code shorter

---

**12. Which of the following tools is explicitly recommended in the article for implementing async queues?**
A) Apache Kafka
B) RabbitMQ
C) MongoDB
D) Jenkins

---

**13. Which tools besides RabbitMQ are also mentioned for async processing?**
A) PostgreSQL and SQLite
B) Docker and Kubernetes
C) ActiveMQ and Redis
D) Prometheus and Grafana

---

**14. What data structure in Redis can be used for a job queue?**
A) Set
B) Hash
C) List
D) Stream

---

**15. What’s the main backend benefit of implementing asynchronism?**
A) Cost reduction through licensing
B) Infinite scalability of background workloads
C) Improved logging and monitoring
D) Better integration with SQL databases

---

**16. What’s the main frontend benefit of async processing?**
A) Richer animations
B) Automatic retries
C) Snappier response time and improved UX
D) Full offline functionality

---

**17. What’s the overall advice the author gives regarding time-consuming tasks?**
A) Cache them with Memcached
B) Avoid using frameworks
C) Always perform them asynchronously
D) Outsource them to third-party APIs

---

---

## ✅ **Answer Key**

1. C
2. B
3. C
4. C
5. C
6. D
7. C
8. C
9. C
10. C
11. C
12. B
13. C
14. C
15. B
16. C
17. C
