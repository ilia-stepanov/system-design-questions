Source is https://web.archive.org/web/20220530193911/https://www.lecloud.net/post/7295452622/scalability-for-dummies-part-1-clones

## 🧠 **Scalability for Dummies – Part 1: Clones – System Design Test**

---

**1. What is the primary responsibility of the load balancer in a scalable web architecture?**
A) Store user session data
B) Monitor CPU load of servers
C) Distribute incoming requests across multiple servers
D) Ensure SSL encryption of all traffic

---

**2. Why can the same user (e.g., Steve) be served by different servers for different requests?**
A) Because servers fail randomly
B) Because the load balancer assigns requests dynamically
C) Because users change their IP addresses
D) Because cookies route users to different servers

---

**3. What is the key requirement for all application servers in a scalable system?**
A) Each should store logs locally
B) Each should run different microservices
C) Each should have a backup database
D) Each should have the same codebase and avoid storing user data locally

---

**4. What is a major problem with storing session or user data locally on application servers?**
A) It increases memory usage
B) It requires more disk space
C) It causes inconsistent behavior when requests hit different servers
D) It reduces CPU efficiency

---

**5. Where should user session data be stored in a scalable system?**
A) On each server’s local disk
B) In the browser's localStorage
C) In a centralized data store
D) In a configuration file

---

**6. Why is Redis a preferred option for storing session data in many architectures?**
A) It has a simpler API than SQL
B) It stores data on hard disks
C) It is optimized for text storage
D) It provides fast, in-memory access for session data

---

**7. What does the article mean by “external” session store?**
A) Hosted outside the company’s firewall
B) Not physically located on any of the application servers
C) Installed on a backup server
D) Part of the frontend stack

---

**8. What is the consequence of having different application servers with different code versions?**
A) Higher latency
B) Users will be routed to staging environments
C) Risk of bugs and inconsistent behavior
D) More resource-efficient deployments

---

**9. What tool is recommended in the article for managing code deployment across all servers?**
A) Terraform
B) Jenkins
C) Capistrano
D) Docker Compose

---

**10. What is a notable challenge when deploying code to many servers at once?**
A) The database must also be redeployed
B) The load balancer must be restarted
C) Some servers may still serve outdated code if not updated properly
D) Redis must be flushed

---

**11. Why is Capistrano effective despite its learning curve?**
A) It integrates with system logs
B) It automates database schema migrations
C) It handles blue-green deployments
D) It ensures all servers get the latest code consistently

---

**12. What is an AMI in AWS, as described in the article?**
A) Amazon Migration Interface
B) Amazon Machine Image used to clone servers
C) Advanced Memory Index
D) API Management Instance

---

**13. What’s the benefit of creating an AMI after setting up a stateless application server?**
A) It ensures the server only runs on Windows
B) It improves network latency
C) It can be used to spawn identical application servers quickly
D) It compresses all static assets

---

**14. What deployment pattern is implied by the use of cloned servers and a load balancer?**
A) Monolithic
B) Vertical scaling
C) Horizontal scaling
D) Edge computing

---

**15. Why must all application servers avoid storing profile pictures or other user-specific files locally?**
A) It increases storage costs
B) These files cannot be indexed
C) It prevents consistent user experiences across requests
D) It slows down the load balancer

---

**16. What type of scalability challenge is addressed by ensuring “every server contains exactly the same codebase”?**
A) Fault tolerance
B) Data durability
C) Consistency across distributed systems
D) Cache invalidation

---

**17. What term best describes the architecture where any application server can handle any user’s request independently?**
A) Peer-to-peer
B) Stateless architecture
C) Stateful microservice
D) Monolithic server model

---

**18. Why is horizontal scaling easier with stateless servers?**
A) They use more memory per user
B) They require fewer CPU cores
C) They can be replaced or added without user impact
D) They automatically replicate user sessions

---

**19. What is the ultimate purpose of making a server “cloneable”?**
A) Enable real-time analytics
B) Allow fast recovery and seamless scaling
C) Increase local storage performance
D) Support A/B testing environments

---

**20. What does the article recommend doing *after* setting up a stateless clone?**
A) Creating a Docker image
B) Creating a backup schedule
C) Creating an AMI and deploying it
D) Running an antivirus scan

---

## ✅ **Answer Key**

1. C
2. B
3. D
4. C
5. C
6. D
7. B
8. C
9. C
10. C
11. D
12. B
13. C
14. C
15. C
16. C
17. B
18. C
19. B
20. C
