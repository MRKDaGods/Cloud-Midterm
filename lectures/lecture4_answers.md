# Lecture 4 — Resource Management
## Answer Key

| Q   | Answer | Topic |
|-----|--------|-------|
| 1   | **B** — A VM created with fixed resources cannot dynamically scale on its own | General Problem |
| 2   | **C** — Middleware platforms like MapReduce job placement | General Problem |
| 3   | **B** — MapReduce, Ray, DynamoDB, HDFS | Diverse Workloads |
| 4   | **C** — Maximize utilization while maintaining the SLA | Resource Mgmt Goal |
| 5   | **B** — Cloud providers predict demand to plan for future expansions | Workload Variability |
| 6   | **D** — Minute-by-minute basis | Workload Variability |
| 7   | **B** — Customers pay only for what they use | Cloudonomics Law 1 |
| 8   | **C** — Cloud providers can deploy less total capacity; aggregate peaks are averaged over time in multi-tenancy | Cloudonomics Law 3 |
| 9   | **B** — Cloud providers can operate at higher efficiencies and lower cost since demand is more predictable | Cloudonomics Law 4 |
| 10  | **B** — An H100 GPU costing ~$40,000 achieves ROI in ~60 days at $39–$49/hr AWS pricing | Cloudonomics Law 5 |
| 11  | **C** — Cloud providers better defend against bots and DDoS attacks due to large-scale infrastructure | Cloudonomics Law 6 |
| 12  | **B** — Reducing latency by half requires four times the number of resources | Cloudonomics Law 8 |
| 13  | **C** — Proximity to major cities is NOT a criterion; greenfield sites prioritize cheap power/land and low environment impact | Cloudonomics Law 10 |
| 14  | **C** — The programming language used by the provider | SLA |
| 15  | **C** — 8.76 hours/year downtime | SLA Availability |
| 16  | **C** — 10% off their bill | Amazon S3 SLA |
| 17  | **C** — 0.000125 (p^n = 0.05^3) | SLA Replication |
| 18  | **D** — ~1 (essentially 100%) | SLA Replication |
| 19  | **D** — Deterministic task assignment is NOT a scheduler responsibility | Scheduler Role |
| 20  | **B** — Maximize throughput | Scheduler Goals |
| 21  | **C** — EDF or RMA | Real-Time Scheduling |
| 22  | **B** — Achieve fairness across limited shared resources | Fair Queuing |
| 23  | **B** — \|Ωa(t)/wa − Ωb(t)/wb\| | Fairness Definition |
| 24  | **B** — Maximize the minimum share to each request not fully serviced | Max-Min Fairness |
| 25  | **B** — Small tasks get needed resources; large tasks split remaining capacity | Max-Min Fairness |
| 26  | **B** — Task 1 demands 2 but gets 2.5 — it receives 0.5 CPU excess, which is unfair | Max-Min Example |
| 27  | **C** — 2.7 and 2.7 (Task 1 gets 2, Task 2 gets 2.6, remaining 5.4 / 2 = 2.7 each) | Max-Min Example |
| 28  | **B** — Tree structure where bandwidth fraction B = wi / Σwj | SFQ Structure |
| 29  | **B** — q / wa | SFQ Quantum |
| 30  | **B** — Sa(i) = max[v(τi), Fa(i−1)], where Sa(i) = 0 initially | SFQ Algorithm |
| 31  | **B** — Smallest virtual start time; highest weight if tied | SFQ Selection |
| 32  | **C** — v(t) = max over all threads of Fx (when CPU is idle) | SFQ Virtual Time |
| 33  | **C** — Fb(0) = Sb(0) + q/wb = 0 + 12/4 = **3** | SFQ Example |
| 34  | **B** — Fa(0) = Sa(0) + q/wa = 0 + 12/1 = **12** (a runs from t=3 finishing at t=15 in wall time, but Fa(0)=12 in virtual time) | SFQ Example |
| 35  | **B** — Scalability bottleneck, hard to diversify, and complex | Mesos |
| 36  | **B** — Low utilization; cannot adapt to real-time demand changes | Statistical Partition |
| 37  | **B** — Presents available resources to frameworks one-at-a-time (pessimistic concurrency); frameworks decide which to accept | Mesos Resource Offers |
| 38  | **B** — Receives resource offers from Mesos Master and decides which resources to use | Mesos Architecture |
| 39  | **B** — Leader election and failover among Mesos Master replicas | Mesos ZooKeeper |
| 40  | **C** — Lock-free optimistic concurrency control with per-framework Cell State copies and atomic commits | Omega |

---

## Key Concepts Summary

### SLA Availability Numbers (must memorize)
| Availability | Annual Downtime |
|---|---|
| 99% | 3.65 days |
| 99.9% | 8.76 hours |
| 99.99% | 52.56 minutes |

### SFQ Algorithm Steps (per iteration i at real time τi)
1. `Sa(i) = max[v(τi), Fa(i−1)]`  — initial Sa = 0
2. Select thread with **smallest Sa(i)**; break ties by **highest weight**
3. `Fa(i) = Sa(i) + q/wa`
4. Update virtual time: `v(t) = Sa(i)` if CPU busy; `v(t) = max(Fx)` if CPU idle

### Max-Min Fairness Algorithm
1. Divide capacity equally among all tasks
2. If any task gets **more than its demand** → cap it at its demand
3. Redistribute leftover capacity equally among remaining unsatisfied tasks
4. Repeat until all capacity is assigned

### Mesos vs Omega vs Borg Comparison
| System | Scheduling Model | Concurrency | Key Innovation |
|---|---|---|---|
| **Mesos** | Two-level (Master + Framework Scheduler) | Pessimistic (one at a time) | Resource Offers; Fine-grained sharing |
| **Omega** | Shared-State (per-framework schedulers) | Optimistic (atomic commit) | Cell State copies; no central scheduler |
| **Borg** | Centralized BorgMaster + Borglet agents | Priority-based with preemption | Handles prod/non-prod; Paxos replication |

### Borg Architecture Components
- **BorgMaster**: Centralized controller (replicated via Paxos), manages job lifecycle, health checks
- **Scheduler**: Scans pending queue, assigns rank/priority, round-robins same-rank jobs, feasibility check & scoring
- **Borglet**: Linux process on each machine, starts/stops jobs, manages local resources, reports health
- **Cell**: Set of machines managed as a single unit

### Kubernetes ↔ Borg Mapping
| Borg | Kubernetes |
|---|---|
| BorgMaster | Kube-api-server / etcd |
| Scheduler | Kube-scheduler |
| Borglet | Kubelet |
| Alloc | Pod |
| Borg Container | Docker |
| Cell | Namespace |
| Job / Task | Pod / Deployment / Labels |
