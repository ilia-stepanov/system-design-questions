Source is https://web.archive.org/web/20220602114024/https://www.lecloud.net/post/7994751381/scalability-for-dummies-part-2-database

## 🧠 **Scalability for Dummies – Part 2: Database – System Design Test**

---

**1. What performance bottleneck does the article say you will eventually face after scaling your web servers?**
A) Slow frontend rendering
B) Load balancer overload
C) Application memory limits
D) Database performance degradation

---

**2. What is the suggested traditional path (Path #1) when your MySQL database becomes a bottleneck?**
A) Switch immediately to a NoSQL database
B) Move session data to Redis
C) Scale vertically and implement master-slave replication
D) Split the application into microservices

---

**3. In Path #1, what is the role of master-slave replication?**
A) To reduce deployment time
B) To store backups across regions
C) To scale read queries across replicas
D) To automatically shard the data

---

**4. According to the article, what are the long-term effects of choosing Path #1?**
A) The system becomes stateless
B) Maintenance becomes cheaper
C) You can scale without rewriting code
D) Efforts become increasingly expensive and complex

---

**5. What database design techniques are mentioned as inevitable in Path #1?**
A) REST APIs and webhooks
B) Normalization and foreign keys
C) Sharding, denormalization, and SQL tuning
D) CDN integration and autoscaling

---

**6. Why is it better to choose Path #2 early while the dataset is still small?**
A) NoSQL databases require fewer indexes
B) Migration is easier before codebase becomes too large
C) Relational models are deprecated
D) You can enable GPU acceleration

---

**7. What does Path #2 suggest about JOIN operations?**
A) They should be replaced with recursive SQL queries
B) They should be cached using Redis
C) They should be avoided and moved to the application layer
D) They are optimized automatically by NoSQL databases

---

**8. What is the advantage of using NoSQL (e.g., MongoDB, CouchDB) in Path #2?**
A) Automatic normalization of data
B) Better performance for large, denormalized datasets
C) No need for backups
D) Full ACID compliance by default

---

**9. What change must developers make if JOINs are removed from database queries?**
A) Move aggregation to the frontend
B) Perform data joining logic inside the application code
C) Use CSV files for lookups
D) Add stored procedures

---

**10. Even with a switch to NoSQL, what eventual problem is anticipated?**
A) Storage corruption
B) Rate-limiting by the cloud provider
C) Query latency due to growing request volume
D) Cache invalidation errors

---

**11. What does the article suggest as the next step after a successful switch to NoSQL?**
A) Setting up multi-master replication
B) Enabling time-series indexing
C) Introducing a caching layer
D) Moving to a multi-cloud setup

---

**12. Which of the following best summarizes Path #2?**
A) Add more memory to the database instance
B) Normalize all tables to the 5th normal form
C) Avoid joins, denormalize data, use NoSQL, and cache results
D) Outsource query execution to third-party APIs

---

**13. What mindset shift is needed to adopt Path #2 successfully?**
A) Trust the database to handle scaling
B) Focus only on frontend optimization
C) Move responsibility of data structure and relations to the application
D) Avoid caching and rely on raw queries

---

## ✅ **Answer Key**

1. D
2. C
3. C
4. D
5. C
6. B
7. C
8. B
9. B
10. C
11. C
12. C
13. C
