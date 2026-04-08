# Lecture 5 — System Models & CAP Theory
## MCQ Bank (40 Questions)

---

### Section 1: Two Generals Problem (Q1–Q6)

**Q1.** The Two Generals Problem demonstrates which fundamental limitation in distributed systems?

- A) Encrypted channels always solve coordination problems
- B) It is impossible to achieve guaranteed consensus over an unreliable communication channel
- C) Two nodes cannot share data without a central coordinator
- D) Replication always resolves message loss

---

**Q2.** In the Two Generals Problem outcome table, which combination results in "Army 2 Defeated"?

- A) Both armies attack
- B) Army 1 attacks, Army 2 does not attack
- C) Army 1 does not attack, Army 2 attacks
- D) Neither army attacks

---

**Q3.** In Solution 1 (General 1 always attacks and sends many messengers), what happens if ALL messengers are captured?

- A) General 2 attacks on its own and wins
- B) General 1 is safe because it did not attack
- C) General 2 does not know → General 1 attacks alone → General 1 loses
- D) General 2 retreats automatically

---

**Q4.** In Solution 2 (General 1 only attacks if a positive response is received), why is this still unsolvable?

- A) General 2 refuses to reply
- B) General 1 cannot send messages
- C) If General 2 knows and must respond, the confirmation message has the same delivery uncertainty — it creates the same problem now from General 2's perspective
- D) The acknowledgement always arrives too late

---

**Q5.** The key lesson of the Two Generals Problem ("No common knowledge") states:

- A) Generals should use shared encrypted keys
- B) The only way to know something is to communicate it, but that communication can always fail
- C) Generals must synchronize clocks before attacking
- D) Both generals must attack without any prior communication to ensure safety

---

**Q6.** In the e-commerce analogy of the Two Generals Problem, which outcome causes "Shop loses money"?

- A) Online Shop does not dispatch, Bank does not charge
- B) Online Shop dispatches, Bank charges
- C) Online Shop dispatches, Bank does NOT charge
- D) Online Shop does not dispatch, Bank charges

---

### Section 2: Byzantine Generals Problem (Q7–Q13)

**Q7.** The key difference between the Two Generals Problem and the Byzantine Generals Problem is:

- A) Byzantine has more armies but the same unreliable channel
- B) Byzantine assumes communication is reliable but nodes (generals) may be malicious traitors
- C) Byzantine assumes all generals are honest but only half the messages arrive
- D) Byzantine uses encrypted messages; Two Generals use plaintext

---

**Q8.** From General 3's point of view when General 2 says "General 1 said retreat," General 3 CANNOT determine:

- A) How many soldiers General 1 has
- B) Whether General 2 is lying OR whether General 1 actually said retreat and General 2 is honestly repeating it
- C) Whether General 2 received the message
- D) Whether the city is defended

---

**Q9.** Which correctly states the three assumptions of the Byzantine Generals Problem?

- A) Up to f generals are malicious; honest generals know who is malicious; malicious generals act independently
- B) Up to f generals are malicious; honest generals do NOT know who the malicious ones are; malicious generals may collude
- C) All generals are honest; messages can be lost; generals may be delayed
- D) Up to f generals crash permanently; the rest are fully honest; messages are unreliable

---

**Q10.** The Byzantine Generals theorem: to tolerate f malicious generals, the total number of generals needed is at least:

- A) 2f + 1
- B) f + 2
- C) 3f + 1
- D) 4f

---

**Q11.** According to the Byzantine Generals theorem, the fraction of generals that may be malicious must be strictly less than:

- A) 1/2
- B) 1/4
- C) 2/3
- D) 1/3

---

**Q12.** In the real-world Byzantine application shown in the lecture (server + 3 disks), the "generals" communicating via RPC to agree on a value are:

- A) Client processes sending HTTP requests
- B) Network routers forwarding packets
- C) Disks communicating with each other and the server to agree on the value of x
- D) Load balancers distributing traffic

---

**Q13.** Which correctly maps each thought experiment to its system assumption?

- A) Two Generals = faulty nodes, reliable network; Byzantine = honest nodes, faulty network
- B) Two Generals = honest nodes, faulty network; Byzantine = faulty (malicious) nodes, reliable network
- C) Both = faulty nodes AND faulty network
- D) Two Generals = faulty nodes AND faulty network; Byzantine = honest nodes, reliable messages

---

### Section 3: System Model — Network, Node & Timing Behavior (Q14–Q26)

**Q14.** A "Reliable (perfect) link" guarantees which of the following?

- A) Zero latency and strict FIFO ordering
- B) Messages always go through with no loss or fabrication, though they may be reordered
- C) Messages are encrypted end-to-end
- D) Messages arrive in strict order with no reordering

---

**Q15.** Which network link type allows messages to be lost, duplicated, or reordered but guarantees eventual delivery if retried indefinitely?

- A) Reliable (perfect) link
- B) Fair-loss link
- C) Arbitrary (adversarial) link
- D) Synchronous link

---

**Q16.** An Arbitrary (adversarial) link is one where:

- A) Messages are occasionally delayed but always eventually delivered
- B) A malicious active adversary can eavesdrop, modify, drop, spoof, or replay messages — the real internet model
- C) Messages are delivered out of order but never dropped
- D) Messages may be duplicated but the content is never modified

---

**Q17.** How do you upgrade a Fair-loss link to behave like a Reliable link?

- A) Use TLS encryption
- B) Use retry + de-duplicate
- C) Increase network bandwidth
- D) Switch to UDP

---

**Q18.** How do you upgrade an Arbitrary (adversarial) link to behave like a Fair-loss link?

- A) Retry + de-duplicate
- B) Add redundant network paths
- C) Use a cryptographic protocol such as TLS
- D) Switch to a synchronous timing model

---

**Q19.** A "Network partition" is defined as:

- A) A node that crashes and loses all state
- B) A node sending Byzantine messages to other nodes
- C) Nodes running fine, but some links are interrupted causing messages to be dropped or significantly delayed
- D) A network running at maximum bandwidth causing queueing

---

**Q20.** What is the difference between "Crash-stop (fail-stop)" and "Crash-recovery (fail-recovery)" node behavior?

- A) Crash-stop nodes restart after crashing; crash-recovery nodes stop forever
- B) Crash-stop nodes stop executing forever after crashing; crash-recovery nodes may lose in-memory state but can resume executing later
- C) Crash-stop faults are from hardware failures; crash-recovery faults are from software bugs
- D) Both are identical in their effect on the system

---

**Q21.** A "Byzantine (fail-arbitrary)" node:

- A) Crashes permanently and sends no further messages
- B) Crashes and recovers, losing its in-memory state each time
- C) Deviates arbitrarily from its algorithm, which can include crashing OR malicious behavior
- D) Only fails under high load conditions

---

**Q22.** In "Synchronous" timing behavior, which TWO properties hold simultaneously?

- A) Messages can be delayed arbitrarily; nodes can pause arbitrarily
- B) Message latency is no greater than a known upper bound AND nodes execute at a known speed
- C) Message latency is bounded but node execution speed is unpredictable
- D) Node execution speed is known but message latency has no upper bound

---

**Q23.** "Partially Synchronous" timing behavior is best described as:

- A) Half the nodes are synchronous and half are asynchronous at all times
- B) The system behaves asynchronously for some finite, unknown period, and synchronously otherwise
- C) Messages are delivered at exactly half the maximum latency bound
- D) The system alternates between synchronous and asynchronous on a fixed schedule

---

**Q24.** Which of the following causes a NETWORK timing violation (not a node timing violation)?

- A) "Stop the world" garbage collection pause
- B) OS context switching at a critical moment
- C) Network congestion causing message queueing
- D) Page faults and memory thrashing

---

**Q25.** Which of the following causes a NODE timing violation (not a network timing violation)?

- A) Message loss requiring retry
- B) Network/route reconfiguration
- C) Network congestion causing queueing
- D) "Stop the world" garbage collection pauses

---

**Q26.** The lecture notes that most distributed systems do NOT use Real-time Operating Systems (RTOS). Why is this significant?

- A) It means distributed systems achieve perfect synchrony
- B) It means timing guarantees ARE available in most distributed systems
- C) It means node execution speed is NOT guaranteed, contributing to timing violations
- D) It means RTOS is incompatible with cloud environments

---

### Section 4: System Failure Concepts (Q27–Q32)

**Q27.** Which correctly maps Failure vs Fault?

- A) Failure = some part of the system not working; Fault = entire system not working
- B) Failure = entire system not working (service outage); Fault = some part of the system not working
- C) Both Failure and Fault mean the entire system is unavailable
- D) Failure is a network issue; Fault is a node issue

---

**Q28.** Which five concepts are listed under "Concepts" in the System Failure section?

- A) Failure, Fault, Node, Network, Timing
- B) Failure, Availability, Reliability, Safety, Maintainability
- C) Consistency, Availability, Partition Tolerance, Reliability, Safety
- D) Fault, Fault Tolerance, Replication, Detection, Recovery

---

**Q29.** A "Single point of failure" is defined as:

- A) A node that fails more than once per day
- B) A node or link whose fault leads to complete system failure
- C) A component that handles more than 50% of the traffic
- D) A backup replica that has not yet synced with the primary

---

**Q30.** A "Perfect failure detector" can ONLY exist under which specific combination?

- A) Asynchronous system with fair-loss links and crash-recovery nodes
- B) Synchronous system with fail-stop nodes and reliable links
- C) Partially synchronous system with Byzantine nodes
- D) Asynchronous system with crash-recovery nodes and fair-loss links

---

**Q31.** A timeout-based failure detector CANNOT distinguish between which four scenarios?

- A) Fast node, slow node, Byzantine node, idle node
- B) Crashed node, temporarily unresponsive node, lost messages, delayed messages
- C) Network partition, message duplication, node restart, Byzantine fault
- D) Fail-stop, fail-recover, Byzantine fault, correct node operation

---

**Q32.** An "Eventually perfect failure detector":

- A) Is 100% accurate at all times from the moment it starts
- B) May temporarily mislabel nodes (false positives or negatives) but eventually correctly identifies all crashed nodes as faulty
- C) Only works correctly inside a synchronous system
- D) Only detects Byzantine faults, not crash faults

---

### Section 5: Replication (Q33–Q37)

**Q33.** Which fault type CANNOT be handled by replication?

- A) Fail-stop faults (e.g., power outage)
- B) Fail-recover faults (e.g., network partition, unresponsive server)
- C) Byzantine faults caused by software bugs (since all replicas run the same buggy code)
- D) Both A and B, but not C

---

**Q34.** The "faults are independent" assumption in replication BREAKS in which scenario?

- A) A Byzantine node sends conflicting write requests
- B) All replicas are connected to the same power source (correlated failure takes all replicas down)
- C) A network partition isolates one replica from the others
- D) A software update slows down one replica

---

**Q35.** "Consistency Overhead" in replication includes all of the following EXCEPT:

- A) Delay/lag between Primary and Backup requiring P/B synchronization
- B) Deciding when to cut over from Primary to Backup
- C) Handling anomalies until the backup takes over
- D) Choosing which hashing algorithm to use for key-value lookups

---

**Q36.** If a system uses a replication factor of 3, what fraction of total resources is consumed by replication overhead (non-primary copies)?

- A) 1/3
- B) 1/2
- C) 2/3
- D) 3/4

---

**Q37.** Which RAID level uses "stripping with distributed parity" (parity spread across all disks, no single dedicated parity disk)?

- A) RAID 0
- B) RAID 1
- C) RAID 3/4
- D) RAID 5

---

### Section 6: CAP Theory (Q38–Q40)

**Q38.** The CAP theorem states that a distributed system can simultaneously guarantee at most:

- A) All three: Consistency, Availability, and Partition Tolerance
- B) Only one of the three properties at a time
- C) Exactly two of the three properties
- D) Two during normal operation and all three during network failures

---

**Q39.** Classify these systems by their CAP category (CA / CP / AP):
- SQL Server, MySQL, PostgreSQL
- HBase, Redis, MongoDB
- Cassandra, DynamoDB

- A) CA = HBase/Redis/MongoDB; CP = Cassandra/DynamoDB; AP = SQL Server/MySQL/PostgreSQL
- B) CA = SQL Server/MySQL/PostgreSQL; CP = HBase/Redis/MongoDB; AP = Cassandra/DynamoDB
- C) CA = Cassandra/DynamoDB; CP = SQL Server/MySQL/PostgreSQL; AP = HBase/Redis/MongoDB
- D) CA = HBase/Redis; CP = Cassandra/DynamoDB; AP = SQL Server/PostgreSQL

---

**Q40.** In CAP theory, match each property to its definition:
- "All clients see the same data at the same time"
- "System continues to operate despite network failures"
- "All clients can access the system at any time"

- A) Consistency / Partition Tolerance / Availability
- B) Availability / Consistency / Partition Tolerance
- C) Partition Tolerance / Availability / Consistency
- D) Consistency / Availability / Partition Tolerance

---
