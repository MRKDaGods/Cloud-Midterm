# Lecture 1 — Introduction to Cloud Computing
## Answer Key

| Q  | Answer | Topic                        |
|----|--------|------------------------------|
| 1  | **B** — 1981 | History of Internet |
| 2  | **C** — 2000s | History of Internet |
| 3  | **C** — Google | History of Internet |
| 4  | **D** — 2006 | History of Internet |
| 5  | **B** — Single-core CPU, one at a time | Serial Computing |
| 6  | **C** — Multiple subtasks on multiple CPUs simultaneously | Parallel Computing |
| 7  | **B** — Multiple computers via network cooperating concurrently | Distributed Computing |
| 8  | **D** — Distributed Computing | Summary Diagram |
| 9  | **B** — Service delivery model for on-demand access to shared resources | NIST Definition |
| 10 | **C** — Elastic resource management | NIST Definition |
| 11 | **D** — Self-service | NIST Definition |
| 12 | **B** — Peer-to-peer architecture | Cloud Characteristics |
| 13 | **C** — 2 | Cloud Models |
| 14 | **C** — Where is your code deployed? | Deployment Model |
| 15 | **D** — Public Cloud | Deployment Models |
| 16 | **B** — Pay-per-use subscription over the internet | Public Cloud |
| 17 | **C** — Private Cloud | Deployment Models |
| 18 | **D** — Community Cloud | Deployment Models |
| 19 | **B** — Infrastructure built/managed by a community with a common goal | Community Cloud |
| 20 | **B** — Comprises two or more different deployment models | Hybrid Cloud |
| 21 | **C** — Computational/storage resources as a fully outsourced device | IaaS |
| 22 | **D** — PaaS (Integration and Middleware) | Service Models |
| 23 | **B** — Software applications as a service, reducing install/maintenance complexity | SaaS |
| 24 | **C** — EC2 Instance | AWS Services |
| 25 | **C** — DynamoDB | AWS Services |
| 26 | **D** — S3 | AWS Services |
| 27 | **B** — VPC | AWS Services |
| 28 | **D** — Cloud Functions | Cross-Cloud Comparison |
| 29 | **A** — Homogeneous (Grid); Heterogeneous (Cluster) | Grid/Cluster Computing |
| 30 | **C** — Bitcoin | Grid/Cluster Computing |
| 31 | **C** — Process near source, faster response, optimized resources, cleaner data | IoT/Edge/Fog |
| 32 | **C** — Cloud Layer | IoT/Edge/Fog |
| 33 | **D** — Different trustworthiness of data | Big Data |
| 34 | **C** — Virtualization (not a V of Big Data) | Big Data |
| 35 | **C** — 1-Server / M-Clients, 1-to-1 communication | Centralized Architecture |
| 36 | **C** — Distributed | Architecture Comparison |
| 37 | **B** — Multiple independent components collaborating to perform a service | P2P |
| 38 | **C** — Storm on East Coast destroying Virginia-based Amazon facilities | Cloud Vulnerabilities |
| 39 | **B** — Single config file exceeded limit → BGP routing protocol failure | Single Point of Failure |
| 40 | **C** — Internal DNS race condition (clean-up deleted records just applied by slow DNS enactor) | Cascading Failures |

---

## Quick-Reference Summary

### History Dates
- **1981** TCP/IP · **1984** DNS · **1986** Email
- **1995** Yahoo/eBay · **1996** yellowpages · **1998** Google
- **2004** Facebook · **2005** YouTube · **2006** Twitter
- **2006** AWS · **2010** Azure & GCP

### NIST Cloud Definition Keywords
| NIST Phrase | Meaning |
|---|---|
| Rapid provisioning | Elastic resource management |
| Minimal management effort | User-friendly |
| Minimal provider interaction | Self-service |
| Shared pool / on-demand | Not a technology — a service delivery model |

### Deployment Models
| Model | Key Trait |
|---|---|
| Public | Pay-per-use, internet-accessible, provider-managed |
| Private | Enterprise own DC, ingress firewall, better security |
| Community | Shared by a group with a common goal |
| Hybrid | Two or more models combined |

### Service Models
| Model | What it provides |
|---|---|
| IaaS | Compute + Storage hardware (e.g., EC2, EBS) |
| PaaS | OS + Middleware runtime (e.g., Elastic Beanstalk) |
| SaaS | Full software applications (e.g., Gmail) |

### Big Data 5 Vs
- **Volume** — Amount · **Velocity** — Speed · **Variety** — Types · **Value** — Usefulness · **Veracity** — Trustworthiness

### Architecture Communication Patterns
| Type | Servers | Clients | Communication |
|---|---|---|---|
| Centralized | 1 | M | 1-to-1 |
| Decentralized | N | M | 1-to-1 |
| Distributed | N | M | 1-to-n |

### Cloud Vulnerability Case Studies
| Incident | Root Cause | Type |
|---|---|---|
| June 2012 AWS | East Coast storm → facility damage | Natural Disaster |
| Nov 2025 Cloudflare | Config file limit → BGP failure (same code on all 330 DCs) | Single Point of Failure |
| Oct 2025 AWS | DNS race condition → DynamoDB → cascading services down | Cascading Failure |
