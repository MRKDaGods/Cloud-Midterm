# Lecture 5 — System Models & CAP Theory
## Answer Key

---

### Section 1: Two Generals Problem

**Q1. B**
The Two Generals Problem proves it is impossible to guarantee consensus over an unreliable channel — no matter how many messages are exchanged, there is always uncertainty about the last unacknowledged message.

**Q2. C**
Army 1 does NOT attack, Army 2 attacks alone → Army 2 is defeated.
Table: (Not Attack / Not Attack = Nothing) | (Attack / Not Attack = Army 1 Defeated) | **(Not Attack / Attack = Army 2 Defeated)** | (Attack / Attack = City Captured)

**Q3. C**
If all messengers are captured → General 2 never receives the message → General 2 does not attack → General 1 attacks alone → General 1 loses.

**Q4. C**
The confirmation (ACK) message suffers the same delivery uncertainty. If General 2 sends "agreed" but it gets lost, General 2 knows and attacks but General 1 does not attack — same fail-state, now from General 2's side. This is the infinite regress of acknowledgements.

**Q5. B**
The only way to share knowledge in a distributed system is through communication, and that communication channel is unreliable — so true "common knowledge" is unachievable.

**Q6. C**
Online Shop **dispatches** goods but Bank does **NOT charge** → the shop delivers without receiving payment → Shop loses money.

---

### Section 2: Byzantine Generals Problem

**Q7. B**
In the Byzantine Generals Problem, the channel is assumed reliable but some nodes (generals) may be active traitors that lie or send conflicting messages. In the Two Generals Problem, the channel is the problem, not the nodes.

**Q8. B**
General 3 cannot tell if General 2 is actively lying (Byzantine fault) OR if General 1 actually said "retreat" and General 2 is faithfully relaying it. Both produce the same observable message.

**Q9. B**
Three assumptions: (1) up to f generals are malicious, (2) honest generals do NOT know who the malicious ones are, (3) malicious generals may collude.

**Q10. C**
Theorem: **3f + 1** total generals needed to tolerate f malicious ones.
Example: to tolerate 1 traitor, need at least 4 generals.

**Q11. D**
Less than **1/3** of generals may be malicious. (i.e., at most ⌊(n−1)/3⌋ traitors in a group of n.)

**Q12. C**
The disks communicate via RPC with the server and with each other to agree on the value of x — analogous to the generals agreeing on an attack plan.

**Q13. B**
- **Two Generals** = honest nodes, faulty (unreliable) network
- **Byzantine** = faulty (malicious) nodes, reliable network

---

### Section 3: System Model — Network, Node & Timing Behavior

**Q14. B**
Reliable links: messages always delivered, no loss, no fabrication — but reordering is allowed.

**Q15. B**
Fair-loss links: messages can be lost, duplicated, or reordered, but have a non-zero probability of delivery. Retrying eventually gets through.

**Q16. B**
Arbitrary (adversarial) links: a malicious active adversary interferes with the link (eavesdrop, modify, drop, spoof, replay). The real internet is modeled this way.

**Q17. B**
Fair-loss → Reliable: use **retry + de-duplicate**. Retrying ensures eventual delivery; de-duplication handles duplicates from retries.

**Q18. C**
Arbitrary → Fair-loss: use a **cryptographic protocol such as TLS**. TLS prevents an adversary from modifying/spoofing messages; if adversary just drops messages, we're back to fair-loss behavior (which retrying can handle).
Note: TLS cannot fix an adversary that decides to drop ALL messages.

**Q19. C**
Network partition: nodes are running fine, but some links between them are cut or severely degraded — messages get dropped or delayed. This is distinct from node crashes.

**Q20. B**
- **Crash-stop**: crashes → stops permanently, no recovery.
- **Crash-recovery**: crashes → loses in-memory state → may resume execution later (persistent state on disk may survive).

**Q21. C**
Byzantine (fail-arbitrary): the node deviates arbitrarily from its algorithm. This includes crashing, but also sending wrong/conflicting/malicious messages.

**Q22. B**
Synchronous: (1) message latency ≤ known upper bound, (2) nodes execute at a known speed. Both properties together define a synchronous system.

**Q23. B**
Partially synchronous: asynchronous for some finite (but unknown) period, then synchronous. Models real-world systems that are usually well-behaved but can have temporary disruptions.

**Q24. C**
Network congestion causing message queueing is a **network** timing violation.
(A, B, D are all node-level timing violations.)

**Q25. D**
"Stop the world" garbage collection pauses is a **node** timing violation — the node pauses execution.
(A, B, C are all network-level timing violations.)

**Q26. C**
Without RTOS, OS scheduling is not guaranteed. Context switching, GC pauses, and page faults can cause nodes to deviate from expected execution speeds — this is why timing violations happen in practice.

---

### Section 4: System Failure Concepts

**Q27. B**
- **Fault** = some PART of the system not working (node fault or network fault)
- **Failure** = the system AS A WHOLE is not working (service outage)
A fault may or may not cause a failure (fault-tolerant systems tolerate faults without failing).

**Q28. B**
The five concepts are: **Failure** (service outage), **Availability** (ready immediately), **Reliability** (run without failure), **Safety** (continue during faults), **Maintainability** (ability to repair).

**Q29. B**
Single point of failure: a node or link whose fault alone causes the entire system to fail. Goal of fault-tolerant design: eliminate SPOF.

**Q30. B**
A perfect (timeout-based) failure detector can only work in a system where: (1) timing is synchronous (bounded latency), (2) nodes are fail-stop (crash and stay down), (3) links are reliable (no message loss). Without all three, you cannot distinguish a crash from a slow/delayed node.

**Q31. B**
Timeout-based detection cannot distinguish: (1) crashed node, (2) temporarily unresponsive/slow node, (3) messages lost in transit, (4) messages significantly delayed. All four look the same from the outside (no response within timeout).

**Q32. B**
Eventually perfect failure detector: may temporarily make false accusations (label a live node as failed) or miss crashes (not label a crashed node immediately), but **eventually** converges to correct labeling — crashed → labelled faulty; correct → not labelled faulty.

---

### Section 5: Replication

**Q33. C**
Replication can handle fail-stop and fail-recover faults because another replica takes over. It CANNOT handle Byzantine faults from software bugs — if all replicas run the same buggy code, all replicas produce the same wrong answer, and replication doesn't help.

**Q34. B**
If all replicas share the same power source, a power outage takes down ALL replicas simultaneously — the independence assumption fails completely, defeating the purpose of replication.

**Q35. D**
Hashing algorithm choice is not part of replication consistency overhead. The actual items are: P/B sync lag, cut-over timing, handling anomalies during switchover, and creating new replicas.

**Q36. C**
Replication factor = 3 means: 1 primary + 2 replicas. Fraction used for replication = 2/3 of total resources.
(Factor 2 → 1/2 overhead; Factor 3 → 2/3 overhead; Factor n → (n−1)/n overhead.)

**Q37. D**
**RAID 5**: stripping with **distributed** parity — parity is spread across all disks, no single dedicated parity disk (unlike RAID 3/4 which has a dedicated parity disk).
- RAID 0 = stripping only
- RAID 1 = mirroring
- RAID 3/4 = stripping with dedicated parity disk

---

### Section 6: CAP Theory

**Q38. C**
CAP Theorem (Brewer's theorem): any distributed system can guarantee at most **2 out of 3** of: Consistency, Availability, Partition Tolerance. You cannot have all three simultaneously.

**Q39. B**
Correct classification per the lecture:
| System | CAP Category | Reason |
|---|---|---|
| SQL Server, MySQL, PostgreSQL | **CA** | Traditional RDBMs prioritize consistency and availability on a single-node or tightly coupled setup; sacrifice partition tolerance |
| HBase, Redis, MongoDB | **CP** | Linearizable service — consistent and partition-tolerant; may refuse requests (sacrifice availability) during a partition |
| Cassandra, DynamoDB | **AP** | Eventually consistent — available and partition-tolerant; data may be temporarily inconsistent (sacrifice strong consistency) |

**Q40. A**
- **Consistency** = "All clients see the same data at the same time"
- **Partition Tolerance** = "System continues to operate despite network failures"
- **Availability** = "All clients can access the system at any time"

---

## Quick-Reference Summary Table

| Q# | Answer | Topic |
|----|--------|-------|
| Q1 | B | Two Generals: fundamental limitation |
| Q2 | C | Two Generals: outcome table |
| Q3 | C | Two Generals: Solution 1 failure |
| Q4 | C | Two Generals: Solution 2 failure |
| Q5 | B | Two Generals: no common knowledge |
| Q6 | C | Two Generals: e-commerce analogy |
| Q7 | B | Byzantine vs. Two Generals difference |
| Q8 | B | Byzantine: ambiguity from General 3's view |
| Q9 | B | Byzantine: three assumptions |
| Q10 | C | Byzantine: 3f+1 theorem |
| Q11 | D | Byzantine: < 1/3 threshold |
| Q12 | C | Byzantine applied: disks |
| Q13 | B | Mapping each problem to its assumption |
| Q14 | B | Reliable link definition |
| Q15 | B | Fair-loss link definition |
| Q16 | B | Arbitrary link definition |
| Q17 | B | Fair-loss → Reliable: retry + dedup |
| Q18 | C | Arbitrary → Fair-loss: TLS |
| Q19 | C | Network partition definition |
| Q20 | B | Crash-stop vs. crash-recovery |
| Q21 | C | Byzantine node behavior |
| Q22 | B | Synchronous timing: two properties |
| Q23 | B | Partially synchronous definition |
| Q24 | C | Network timing violation example |
| Q25 | D | Node timing violation example |
| Q26 | C | RTOS not used → timing not guaranteed |
| Q27 | B | Failure vs. Fault definitions |
| Q28 | B | Five system failure concepts |
| Q29 | B | Single point of failure |
| Q30 | B | Perfect failure detector conditions |
| Q31 | B | Timeout-based detector ambiguity |
| Q32 | B | Eventually perfect failure detector |
| Q33 | C | Replication cannot handle Byzantine bugs |
| Q34 | B | Independence assumption failure |
| Q35 | D | Consistency overhead items |
| Q36 | C | Replication factor 3 → 2/3 overhead |
| Q37 | D | RAID 5: distributed parity |
| Q38 | C | CAP: at most 2 of 3 |
| Q39 | B | CA/CP/AP system classification |
| Q40 | A | CAP property definitions |
