Source is https://web.archive.org/web/20230126233752/https://www.lecloud.net/post/9246290032/scalability-for-dummies-part-3-cache



## 🧠 **Scalability for Dummies – Part 3: Cache – System Design Test**

---

**1. What problem remains for users even after switching to a scalable database?**
A) Lack of disk space
B) Slow frontend rendering
C) Slow page requests due to large data fetching
D) Server authentication failures

---

**2. What type of caching does the author strongly recommend?**
A) File-based caching
B) Cached database queries
C) Cached cron jobs
D) Cached objects

---

**3. Why should you avoid file-based caching in scalable architectures?**
A) It has slower read speeds than SQL
B) It causes memory leaks
C) It complicates cloning and auto-scaling servers
D) It is not compatible with microservices

---

**4. What is the general structure of an in-memory cache like Redis or Memcached?**
A) Document store
B) Columnar database
C) Key-value store
D) Graph database

---

**5. What is the purpose of putting a cache between your application and your database?**
A) To increase database size
B) To reduce code complexity
C) To speed up read operations
D) To prevent SQL injection

---

**6. What kind of performance does Redis offer on a standard server?**
A) 100–200 operations/sec
B) 1,000 operations/sec
C) Several hundred thousand read operations per second
D) Less than Memcached

---

**7. What’s the issue with caching complex database query results (#1 - Cached Database Queries)?**
A) You can't invalidate expired keys
B) You must use joins in cache keys
C) It's difficult to invalidate cached results when one piece of data changes
D) It's only available in Redis Enterprise

---

**8. In cached database queries, what is typically used as the cache key?**
A) Primary key of the table
B) Column name
C) Hashed version of the query
D) Username

---

**9. What is the main advantage of cached objects over cached queries?**
A) It supports relational joins
B) It allows simpler cache invalidation
C) It requires fewer cache keys
D) It stores query plans instead of data

---

**10. In the example provided, what should be cached after the Product class assembles its data array?**
A) Only the product price
B) Just the customer reviews
C) The entire class instance or the full data array
D) A list of foreign key references

---

**11. What programming concept does the author relate object caching to?**
A) Dependency injection
B) RESTful endpoints
C) Class instances in OOP
D) Environment variables

---

**12. What feature does object caching enable that benefits performance significantly?**
A) Multi-threaded SQL queries
B) Asynchronous processing by worker servers
C) GPU acceleration for caching
D) Replication between cloud zones

---

**13. What is a good real-world example of what to cache as an object?**
A) Indexes of the database
B) Internal Docker logs
C) Fully rendered blog articles
D) Error messages

---

**14. What is the author’s favorite in-memory cache tool and why?**
A) Redis, because of persistence and data structures
B) Memcached, because of high availability
C) SQLite, because of simplicity
D) Cassandra, because of partitioning

---

**15. Why might someone still choose Memcached over Redis?**
A) It supports joins
B) It supports persistent storage
C) It scales easily
D) It has better security features

---

**16. What kind of data structures are natively supported by Redis but not Memcached?**
A) CSV and JSON
B) Tables and Views
C) Lists and Sets
D) Graphs and Trees

---

**17. What bold claim does the author make about clever Redis usage?**
A) It can outperform AWS Lambda
B) It eliminates the need for load balancers
C) It may let you eliminate your database entirely
D) It turns your backend into a frontend

---

**18. What caching behavior is recommended when data changes?**
A) Restart the cache server
B) Refresh the frontend
C) Invalidate and refresh the cached object
D) Clear all cache keys manually

---

---

## ✅ **Answer Key**

1. C
2. D
3. C
4. C
5. C
6. C
7. C
8. C
9. B
10. C
11. C
12. B
13. C
14. A
15. C
16. C
17. C
18. C
