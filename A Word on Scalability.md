

## 🧠 *A Word on Scalability* – System Design Test

---

**1. What does the phrase “that doesn’t scale” often signal in technical discussions?**
A) The service has reached peak performance
B) The developers prefer to optimize later
C) The system's architecture limits its ability to grow
D) The code is difficult to understand

---

**2. How is scalability positively defined in the article?**
A) A system that performs the same regardless of input
B) A system that reduces load when more users arrive
C) A system that maintains speed by using GPU acceleration
D) A system that shows performance growth proportional to resource increase

---

**3. In distributed systems, why might we add resources aside from performance?**
A) To make the UI faster
B) To reduce the number of servers
C) To improve reliability through redundancy
D) To cut down database queries

---

**4. What is a key design requirement for achieving scalability?**
A) Using only the latest hardware
B) Having a central master node
C) Designing with scaling in mind from the beginning
D) Avoiding all redundancy in system design

---

**5. What can happen to algorithms not designed for scale when load or data grows?**
A) They will adapt automatically
B) They become more efficient
C) Their cost may increase drastically
D) They reduce server utilization

---

**6. What challenge does heterogeneity introduce in scale-out systems?**
A) It forces all servers to be restarted frequently
B) It makes resource allocation faster
C) Some nodes outperform others, possibly breaking uniform algorithms
D) It eliminates the need for load balancing

---

**7. How should architects deal with the reality of heterogeneity?**
A) By avoiding hardware upgrades
B) By isolating old nodes
C) By designing algorithms that can adapt to node differences
D) By standardizing all machines to the slowest node

---

**8. According to the article, what is necessary to achieve good scalability?**
A) Wait until the system breaks before fixing
B) Rely on default settings and frameworks
C) Architect systems with growth, redundancy, and diversity in mind
D) Outsource traffic to third-party CDNs only

---

## ✅ **Answer Key with Explanations**

1. **C** – The phrase is used to critique systems whose architecture can't support increased load or size.
2. **D** – Scalability is defined as performance increasing proportionally with added resources.
3. **C** – Redundancy is added to improve *reliability*, not just performance.
4. **C** – Scalability must be considered from the start, not as an afterthought.
5. **C** – Algorithms not built for scale may “explode in cost” under larger workloads.
6. **C** – Heterogeneous systems include nodes of varying power; uniform algorithms may fail or underutilize faster nodes.
7. **C** – Adaptable algorithms can better utilize heterogeneous infrastructure.
8. **C** – Proper architecture includes planning for growth, failure tolerance, and non-uniform infrastructure.
