Source is https://www.youtube.com/watch?v=-W9F__D3oY4

## 🧠 CS75 Lecture 9: Scalability – Comprehensive System Design Test

---

### **SECTION 1: Hosting & Scaling Models**

**1. What is the main disadvantage of shared hosting for growing websites?**
A) It’s more expensive than dedicated servers
B) You cannot run any PHP code
C) You share resources with other customers, leading to performance issues
D) Your IP address is blocked in most countries

**2. What is a VPS (Virtual Private Server)?**
A) A physical server you install in your home
B) A lightweight server running in your browser
C) A virtual machine with its own OS slice on a shared host
D) A cloud-based load balancer

**3. What is the main benefit of using Amazon EC2 over traditional hosting?**
A) It guarantees zero downtime
B) It allows scaling based on demand with per-minute billing
C) It offers unlimited bandwidth for free
D) It comes preinstalled with all web frameworks

---

### **SECTION 2: Vertical vs. Horizontal Scaling**

**4. What is vertical scaling?**
A) Adding more web servers
B) Adding more databases
C) Upgrading a single server’s hardware
D) Moving data into the cloud

**5. What is the primary limitation of vertical scaling?**
A) Software crashes more frequently
B) Hardware upgrades are limited and eventually hit a ceiling
C) Disk space becomes infinite
D) It always requires cloud support

**6. What is horizontal scaling?**
A) Adding more RAM to a server
B) Adding more application features
C) Distributing load across multiple servers
D) Using only client-side rendering

---

### **SECTION 3: Load Balancing & DNS**

**7. What role does a load balancer play in horizontal scaling?**
A) Encrypting user sessions
B) Directing incoming traffic to appropriate backend servers
C) Storing static files
D) Handling database writes

**8. What is a drawback of round-robin DNS load balancing?**
A) It doesn't work with HTTPS
B) It leads to duplicate IP addresses
C) It can't adjust for uneven load distribution
D) It uses too much memory

**9. Why is caching problematic with round-robin DNS?**
A) DNS is encrypted
B) Cached IPs may direct the same user to the wrong backend server
C) Browsers disable DNS caching by default
D) It prevents TLS negotiation

**10. How can sticky sessions be implemented without shared storage?**
A) By saving session IDs in the web page title
B) By assigning session state to a CDN
C) By using cookies to store server identifiers or session keys
D) By encoding user state in JavaScript variables

---

### **SECTION 4: Sessions, Storage, and Redundancy**

**11. Why is storing sessions locally on a web server problematic in a load-balanced environment?**
A) It creates file permission issues
B) It exposes user data to frontend code
C) Users might be routed to different servers and lose session continuity
D) Sessions expire too quickly

**12. What is one solution to centralizing session storage?**
A) Replicating the HTML codebase
B) Encrypting sessions client-side
C) Using a shared file system or database accessible by all servers
D) Generating a static version of each session

**13. What is a single point of failure in the context of centralized session storage?**
A) Any one user with a large session
B) Any server with too much RAM
C) A file or DB server that, if it crashes, takes down session access for all servers
D) A slow front-end router

---

### **SECTION 5: RAID & Redundancy**

**14. What does RAID stand for?**
A) Rapid Access Internet Distribution
B) Redundant Array of Independent Disks
C) Really Awesome Internal Disk
D) Remote Access Intelligent Drive

**15. Which RAID level mirrors data across two drives for redundancy?**
A) RAID 0
B) RAID 5
C) RAID 1
D) RAID 10

**16. What is a major downside of RAID 0?**
A) Slower writes
B) No performance boost
C) Loss of data if one drive fails
D) It is incompatible with SSDs

**17. Which RAID level can survive two simultaneous disk failures?**
A) RAID 1
B) RAID 5
C) RAID 6
D) RAID 0

---

### **SECTION 6: Database Replication**

**18. What is the purpose of master-slave replication in databases?**
A) Allow bidirectional writes
B) Provide redundancy and scale read performance
C) Prevent SQL injection
D) Automatically update indexes

**19. In a master-master setup, what happens if one master goes down?**
A) The database stops responding entirely
B) The other master can continue serving both reads and writes
C) All slaves are promoted to masters
D) Query performance doubles

**20. Why is read-scaling more practical than write-scaling in relational databases?**
A) Writes require hardware acceleration
B) Reads can be distributed across replicated slaves
C) Writes are stateless
D) Reads can only happen on the master

---

### **SECTION 7: Partitioning & Caching**

**21. What is database partitioning (sharding)?**
A) Cloning a database for testing
B) Backing up data daily
C) Splitting data across multiple machines based on a key like user ID
D) Writing queries faster using SSDs

**22. What’s a potential drawback of simple partitioning (e.g., Harvard and MIT databases)?**
A) Data gets lost during insert
B) Cross-partition features are hard to implement
C) It slows down database writes
D) It inflates schema sizes

**23. What is Memcached used for?**
A) Encrypting SQL queries
B) Backing up user data
C) Storing frequently accessed data in RAM for faster access
D) Generating static HTML

**24. What happens in Memcached when the cache is full?**
A) It crashes
B) It overwrites the entire dataset
C) It evicts the least recently used data
D) It sends alerts to Redis

---

### **SECTION 8: Global Load Balancing & Fault Tolerance**

**25. What is “High Availability” in system design?**
A) A form of database indexing
B) A way to ensure minimal downtime through redundancy
C) An encryption strategy for sessions
D) A cloud-only strategy

**26. What is an “active-passive” load balancer setup?**
A) Both load balancers are used equally
B) One handles traffic while the other stands by
C) Both load balancers send traffic simultaneously
D) Each handles a specific port

**27. What can happen if DNS TTLs are cached for too long during a data center outage?**
A) Load increases on the new server
B) Users keep trying to access the offline data center
C) Browsers block the site permanently
D) Cookies expire immediately

---

### **SECTION 9: Security & Final Design**

**28. What traffic should generally be allowed through a web-facing firewall?**
A) Only port 22 (SSH)
B) Port 3306 (MySQL)
C) TCP 80 and 443
D) UDP 143 and 110

**29. Why should internal traffic (e.g., MySQL) be blocked from the public internet?**
A) It reduces memory usage
B) It saves bandwidth
C) It prevents external attackers from querying your database
D) It increases disk write speed

**30. Why is SSL termination often done at the load balancer?**
A) To avoid installing certificates on all backend servers
B) To encrypt Redis data
C) To reduce DNS latency
D) Because load balancers don't use TLS

--

Here’s the **answer key with explanations** for each correct answer in the CS75 Lecture 9: Scalability test:

---

## ✅ **Answer Key with Explanations**

1. **C** – *Shared hosting* places multiple customers on the same machine, which leads to performance degradation when one user consumes excessive resources.
2. **C** – A *VPS* gives you your own OS environment on a shared physical machine, allowing more control and isolation.
3. **B** – *EC2* allows dynamic provisioning and billing per usage minute, enabling you to scale up/down based on traffic.
4. **C** – *Vertical scaling* means improving a single machine by upgrading its CPU, RAM, etc.
5. **B** – You can only upgrade hardware so far; eventually, you hit limits in cost and capability.
6. **C** – *Horizontal scaling* adds more servers, distributing load and reducing reliance on a single machine.
7. **B** – A *load balancer* evenly distributes traffic across backend servers to optimize performance.
8. **C** – *Round-robin DNS* does not account for server load, which can result in uneven traffic distribution.
9. **B** – Due to *DNS caching*, users may repeatedly hit the same server, defeating load balancing.
10. **C** – By storing a *server ID or session key* in a cookie, the user can be routed consistently to the same server.
11. **C** – If session data is on one server, and the user is routed elsewhere, they may lose access to their session state.
12. **C** – A *shared store* like Redis or a shared filesystem makes session data available to all servers.
13. **C** – If the central session server fails, the entire session layer breaks, creating a single point of failure.
14. **B** – *RAID* stands for Redundant Array of Independent Disks – used for performance and fault tolerance.
15. **C** – *RAID 1* duplicates data to two disks, ensuring availability if one fails.
16. **C** – *RAID 0* improves performance via striping but offers no redundancy – one disk fails, data is lost.
17. **C** – *RAID 6* can tolerate two drive failures thanks to double parity.
18. **B** – In *master-slave replication*, slaves mirror the master, allowing *redundancy* and *read scaling*.
19. **B** – *Master-master* allows bidirectional writes, so if one fails, the other can handle requests.
20. **B** – *Reads* can be duplicated across many slaves easily; *writes* are trickier due to conflict resolution.
21. **C** – *Partitioning* (sharding) splits the database across servers using a user attribute like ID range.
22. **B** – Cross-server communication (e.g. messaging a user on another shard) requires complex syncing.
23. **C** – *Memcached* stores key-value pairs in RAM for fast access, reducing DB load.
24. **C** – *Least Recently Used (LRU)* eviction policy ensures old, unused entries are removed when full.
25. **B** – *High availability* means system redundancy (e.g. failover mechanisms) to minimize downtime.
26. **B** – In *active-passive*, one load balancer is on standby until the other fails.
27. **B** – A long TTL means users may keep trying to access a failed data center due to outdated IP cache.
28. **C** – Only HTTP (80) and HTTPS (443) should be open externally for a typical web app.
29. **C** – Exposing *MySQL* externally is a security risk – attackers could attempt to query or inject.
30. **A** – *SSL termination* at the load balancer centralizes certificate handling and reduces backend load.
