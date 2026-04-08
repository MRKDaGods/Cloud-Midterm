# Lecture 4 — Resource Management
## MCQ Bank (40 Questions)

---

### Section 1: General Problem & Goal

**Q1.** Which of the following best describes why VMs alone cannot provide elastic computing?

- A) VMs are too slow to run modern workloads
- B) A VM created with a fixed resource (e.g., 8 GB RAM) cannot dynamically scale that resource on its own
- C) VMs do not support networking
- D) VMs require a dedicated physical machine each

---

**Q2.** A hypervisor can share CPU and Memory across VMs, but it CANNOT efficiently manage which of the following?

- A) RAM partitioning between VMs
- B) CPU scheduling for guest OSes
- C) Middleware platforms like MapReduce job placement
- D) Network interface allocation

---

**Q3.** Which of the following frameworks are cited as examples of diverse cloud applications that a single framework cannot efficiently manage together?

- A) Apache, Nginx, MySQL, PostgreSQL
- B) MapReduce, Ray, DynamoDB, HDFS
- C) Docker, Kubernetes, Terraform, Ansible
- D) Hadoop, Spark, Kafka, Flink

---

**Q4.** The primary goal of cloud resource management is to:

- A) Minimize the number of running VMs at all times
- B) Maximize hardware procurement
- C) Maximize utilization while maintaining the Service Level Agreement (SLA)
- D) Ensure every user gets dedicated physical machines

---

### Section 2: Cloud Economics & Workload

**Q5.** Cloud workloads are described as "not consistent." Which statement is TRUE regarding cloud provider planning?

- A) Cloud providers build infrastructure to match minimum expected demand
- B) Cloud providers predict demand to plan for future expansions
- C) Cloud workloads are fully predictable on a minute-by-minute basis
- D) Demand is always highest during weekends

---

**Q6.** Peak demand in cloud systems can vary on what time granularity, making it hardest to predict?

- A) Yearly basis
- B) Monthly basis
- C) Weekly basis
- D) Minute-by-minute basis

---

**Q7.** According to the Laws of Cloudonomics, Law 1 states "Utility services cost less." This is because:

- A) Cloud providers use cheaper hardware
- B) Customers pay only for what they use
- C) Cloud providers receive government subsidies
- D) Cloud eliminates the need for software licensing

---

**Q8.** Law 3 of Cloudonomics — "Peak of the sum is less than the sum of peaks" — means:

- A) Cloud providers must over-provision to handle all user peaks simultaneously
- B) Individual tenant peaks happen at the same time in multi-tenancy
- C) Cloud providers can deploy less total capacity because aggregate peaks are averaged over time in multi-tenancy
- D) Single-tenant systems are more cost-efficient than multi-tenant systems

---

**Q9.** Law 4 of Cloudonomics states "Aggregate demand is smoother than individual." The practical benefit of this is:

- A) Cloud providers need less staff
- B) Cloud providers can operate at higher efficiencies and lower cost since demand is more predictable
- C) Individual tenants get better performance guarantees
- D) Storage costs decrease linearly with scale

---

**Q10.** Law 5 of Cloudonomics relates to economies of scale. In the context of the NVIDIA H100 GPU example:

- A) Cloud providers lose money renting GPUs below cost
- B) An H100 GPU costing ~$40,000 can achieve return on investment in ~60 days via AWS pricing of $39–$49/hr
- C) GPU cloud pricing always exceeds on-premise costs
- D) Law 5 only applies to CPU resources, not GPUs

---

**Q11.** Law 6 of Cloudonomics states "Superiority in numbers is important against bad actors." This refers to:

- A) Cloud providers employing large security teams
- B) Using many encryption keys simultaneously
- C) Cloud providers being better able to defend against bots and DDoS attacks due to large-scale infrastructure
- D) Multi-factor authentication across all users

---

**Q12.** Law 8 of Cloudonomics — "Dispersion is inverse square of latency" — implies:

- A) Doubling the number of servers halves the latency
- B) Reducing latency by half requires four times the number of resources
- C) Latency decreases linearly with geographic distribution
- D) Dispersion only applies to storage systems

---

**Q13.** Law 10 of Cloudonomics describes datacenter location criteria. Which of the following is NOT a criterion for "greenfield" sites?

- A) Located on network backbone
- B) Cheap access to power and cooling
- C) Proximity to major cities and populated areas
- D) Low impact on environment

---

### Section 3: Service Level Agreement (SLA)

**Q14.** Which of the following is NOT typically specified in an SLA?

- A) Availability (uptime)
- B) Response time (latency)
- C) The programming language used by the provider
- D) Responsibilities of each party

---

**Q15.** What is the maximum annual downtime permitted at 99.9% availability SLA?

- A) 3.65 days
- B) 52.56 minutes
- C) 8.76 hours
- D) 24 hours

---

**Q16.** Amazon S3's SLA is set at 99.9% availability. If uptime drops below 99.9% but stays above 99%, the customer receives:

- A) A full refund
- B) 25% off their bill
- C) 10% off their bill
- D) No compensation

---

**Q17.** To achieve high availability (e.g., 99.999%), cloud systems use replication. If a single server has failure probability p = 0.05, what is the probability that ALL servers in a 3-replica setup fail?

- A) 0.05
- B) 0.1426
- C) 0.000125
- D) 0.0000003125

---

**Q18.** In the SLA replication table with p = 0.05, using 20 replicas gives a probability of at least 1 server operational that is approximately:

- A) 0.95
- B) 0.99986
- C) 0.9999996875
- D) ~1 (essentially 100%)

---

### Section 4: Scheduling Fundamentals & Fair Queuing

**Q19.** Which of the following is NOT a property the scheduler is responsible for?

- A) Efficient: achieve high utilization
- B) Fair: all users access their paid resources
- C) Starvation-Free: no task waits indefinitely
- D) Deterministic: always assign tasks to the same machine

---

**Q20.** For a batch system, the scheduler's primary goal is to:

- A) Meet deadlines
- B) Maximize throughput
- C) Minimize latency
- D) Ensure availability

---

**Q21.** Which scheduling algorithm is most appropriate for real-time systems?

- A) Round Robin
- B) First Come First Served (FCFS)
- C) Earliest Deadline First (EDF) or Rate Monotonic Algorithm (RMA)
- D) Fair Queuing

---

**Q22.** Fair Queuing is a family of scheduling algorithms designed to:

- A) Prioritize high-weight tasks exclusively
- B) Achieve fairness across limited shared resources
- C) Guarantee zero latency for all tasks
- D) Replace the operating system scheduler entirely

---

**Q23.** According to the fairness definition in the lecture, a scheduler minimizes which expression for two runnable threads a and b?

- A) Ωa(t) × wa − Ωb(t) × wb
- B) |Ωa(t)/wa − Ωb(t)/wb|
- C) Ωa(t) + Ωb(t)
- D) wa/Ωa(t) + wb/Ωb(t)

---

### Section 5: Max-Min Fairness

**Q24.** The core principle of Max-Min Fairness is:

- A) Give all resources to the highest-priority task
- B) Maximize the minimum share allocated to each request not fully serviced
- C) Divide all resources equally regardless of demand
- D) Give larger tasks more resources proportionally

---

**Q25.** In Max-Min Fairness, small tasks:

- A) Are queued behind large tasks
- B) Get exactly their needed resources, while large tasks split the remaining capacity
- C) Always receive half the total cluster capacity
- D) Are rejected if resources are constrained

---

**Q26.** Given 4 tasks demanding CPUs {2, 2.6, 4, 5} with total capacity = 10, why is simply dividing resources equally (10/4 = 2.5 each) considered unfair?

- A) It gives Task 3 and Task 4 too few resources
- B) Task 1 receives more than it needs (demands 2, gets 2.5), which is excess
- C) It violates the SLA for all tasks
- D) It causes starvation for Task 2

---

**Q27.** In the Max-Min Fairness example with demands {2, 2.6, 4, 5} and capacity = 10, what is the final allocation for Task 3 and Task 4 after applying Max-Min Fairness correctly?

- A) 2.5 and 2.5
- B) 4 and 4
- C) 2.7 and 2.7
- D) 3 and 3

---

### Section 6: Start-Time Fair Queuing (SFQ)

**Q28.** In Start-Time Fair Queuing (SFQ), processes are sorted for CPU bandwidth using a:

- A) Hash table ordered by arrival time
- B) Tree structure where bandwidth fraction B = wi / Σwj
- C) Round-robin queue with fixed time slices
- D) Min-heap ordered by remaining execution time

---

**Q29.** In SFQ, for a CPU with quantum slice q, thread a with weight wa is assigned CPU for a quantum of:

- A) q × wa
- B) q / wa
- C) q + wa
- D) q − wa

---

**Q30.** In SFQ, the Virtual Start Time for thread a at slice i is calculated as:

- A) Sa(i) = Fa(i−1) − v(τi)
- B) Sa(i) = max[v(τi), Fa(i−1)], where Sa(i) = 0 initially
- C) Sa(i) = min[v(τi), Fa(i−1)]
- D) Sa(i) = Sa(i−1) + q/wa

---

**Q31.** In SFQ, the scheduler selects the thread with the:

- A) Largest virtual finish time
- B) Smallest virtual start time (and highest weight if tied)
- C) Smallest weight
- D) Longest remaining burst time

---

**Q32.** In SFQ, when the CPU is idle, the virtual time v(t) is updated to:

- A) v(t) = 0
- B) v(t) = Sa(i) of the selected thread
- C) v(t) = max over all threads of Fx
- D) v(t) = the sum of all finish times

---

**Q33.** In the SFQ example with q=12, wa=1, wb=4: In Iteration 1, thread b is selected first because both Sa and Sb are 0 and b has higher weight. What is Fb(0)?

- A) 12
- B) 6
- C) 3
- D) 4

---

**Q34.** In the SFQ example (q=12, wa=1, wb=4), after Iteration 2 where thread a runs from t=3 to t=15, what is Fa(0)?

- A) 3
- B) 12
- C) 15
- D) 24

---

### Section 7: Mesos

**Q35.** A "Monolithic" (centralized) scheduler has which of the following as a key disadvantage?

- A) It allows frameworks to make all scheduling decisions
- B) It is a scalability bottleneck, hard to diversify, and complex
- C) It provides too much resource isolation between frameworks
- D) It cannot schedule batch jobs

---

**Q36.** "Statistical Partition" of resources (dedicating X machines to MapReduce) fails primarily because:

- A) MapReduce cannot schedule its own tasks
- B) It leads to low utilization and cannot adapt to demand changes in real-time
- C) It requires a centralized scheduler
- D) Frameworks cannot communicate with each other

---

**Q37.** Mesos introduces "Resource Offers." This mechanism:

- A) Forces all frameworks to use only resources offered by a central authority
- B) Presents available resources to frameworks and assigns them one-at-a-time (pessimistic concurrency) letting frameworks decide which to accept
- C) Uses optimistic concurrency to avoid a central resource manager
- D) Replaces the framework scheduler with a unified Mesos scheduler

---

**Q38.** In the Mesos architecture, what role does the Framework Scheduler play?

- A) It directly polls Borglet agents for task status
- B) It receives resource offers from the Mesos Master and decides which resources to use for its tasks
- C) It manages the Paxos persistent store
- D) It acts as standby master in case of failure

---

**Q39.** Mesos uses ZooKeeper quorum for which purpose?

- A) Storing user data
- B) Managing failover and leader election among Mesos Master replicas
- C) Running MapReduce jobs
- D) Providing DNS resolution for slave nodes

---

### Section 8: Omega & Borg

**Q40.** Omega improves over Mesos by replacing pessimistic concurrency with:

- A) A centralized monolithic scheduler
- B) Statistical partitioning per framework
- C) Lock-free optimistic concurrency control — each framework has its own scheduler and a local copy of the cluster state ("Cell State"), committing atomically
- D) A two-level scheduler with a mandatory resource broker

---
