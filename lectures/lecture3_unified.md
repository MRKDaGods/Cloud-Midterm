# Lecture 3 — Cloud Computing Networking
## Unified Questions and Answers

Each question is followed by its answer and topic from the answer key.

### Section 1: Network Basics

**Q1.** A network is best defined as:
- A) A single device connected to the internet
- B) A group of connected devices that communicate with each other to share data and resources
- C) A software application used to transfer files
- D) A protocol for encoding binary data


**Answer:** **B** — A group of connected devices that communicate to share data and resources
**Topic:** Network Definition

---

**Q2.** Which of the following is NOT listed as a network property?
- A) Devices
- B) Group
- C) Bandwidth
- D) Share data/resources


**Answer:** **C** — Bandwidth (not a listed network property; the 4 properties are Devices, Group, Communicate, Share data/resources)
**Topic:** Network Properties

---

**Q3.** In the context of this course, which THREE areas are the focus of the networking lecture?
- A) Software Engineering, Networks, Web
- B) Networking basics, Networks inside Data Centers, Virtual Networks
- C) TCP/IP, OSI, Ethernet
- D) VMs, Containers, Physical Networks


**Answer:** **B** — Networking basics, Networks inside Data Centers, Virtual Networks
**Topic:** Course Focus

---

### Section 2: Communication Models (OSI & TCP/IP)

**Q4.** The OSI model was developed by which organization?
- A) IEEE
- B) IETF
- C) ISO
- D) 3GPP


**Answer:** **C** — ISO
**Topic:** OSI Model

---

**Q5.** How many layers does the OSI model have?
- A) 4
- B) 5
- C) 6
- D) 7


**Answer:** **D** — 7
**Topic:** OSI Layers

---

**Q6.** How many layers does the TCP/IP model have?
- A) 3
- B) 4
- C) 5
- D) 7


**Answer:** **B** — 4
**Topic:** TCP/IP Layers

---

**Q7.** Which of the following best describes the TCP/IP model compared to OSI?
- A) More complex and theoretical
- B) Simpler structure and protocol-driven (practical)
- C) Standardized by ISO
- D) Has more layers than OSI


**Answer:** **B** — Simpler structure and protocol-driven (practical)
**Topic:** TCP/IP vs OSI

---

**Q8.** In the TCP/IP model, which OSI layers are merged into the "Application Layer"?
- A) Physical and Data Link
- B) Network and Transport
- C) Application, Presentation, and Session
- D) Transport and Network


**Answer:** **C** — Application, Presentation, and Session
**Topic:** TCP/IP Mapping

---

**Q9.** In the TCP/IP model, which OSI layers are merged into the "Network Access (Link Layer)"?
- A) Application, Presentation, Session
- B) Transport and Network
- C) Data Link and Physical
- D) Session and Transport


**Answer:** **C** — Data Link and Physical
**Topic:** TCP/IP Mapping

---

**Q10.** What is the correct mapping of the "Internet Layer" in TCP/IP to the OSI model?
- A) Transport Layer
- B) Data Link Layer
- C) Network Layer
- D) Application Layer


**Answer:** **C** — Network Layer
**Topic:** TCP/IP Mapping

---

**Q11.** When loading "www.google.com", the sequence starts at which layer on the HOST side?
- A) Physical Layer
- B) Network Layer
- C) Application Layer (HTTP)
- D) Transport Layer


**Answer:** **C** — Application Layer (HTTP)
**Topic:** Communication Example

---

**Q12.** When a browser sends an HTTP request to load www.google.com, what is the FIRST step at the network level?
- A) Open TCP connection (Handshake)
- B) Send TCP message of the request
- C) Ask DNS for target IP
- D) Send IP packet to destination


**Answer:** **C** — Ask DNS for target IP
**Topic:** HTTP Request Flow

---

**Q13.** In the TCP connection process (Handshake), which two messages are exchanged?
- A) GET and POST
- B) SYN and SYN-ACK
- C) PUSH and ACK
- D) FIN and FIN-ACK


**Answer:** **B** — SYN and SYN-ACK
**Topic:** TCP Handshake

---

**Q14.** At the Network Layer, what does the system do when sending a SYN packet?
- A) Calls DNS for IP resolution
- B) Makes a System Call for NIC access to send data
- C) Waits for an HTTP response
- D) Opens a socket on port 443


**Answer:** **B** — Makes a System Call for NIC access to send data
**Topic:** System Calls

---

**Q15.** After the TCP handshake, what does the client do next?
- A) Render the HTML page
- B) Ask DNS again
- C) Send TCP message of the actual request with sequence IDs
- D) Close the connection


**Answer:** **C** — Send TCP message of the actual request with sequence IDs
**Topic:** HTTP Request Flow

---

**Q16.** TCP acknowledgment packets (ACKs) travel at which layer?
- A) Application Layer (HTTP)
- B) Data Link Layer
- C) Network Layer (IP packets carrying TCP data)
- D) Physical Layer only


**Answer:** **C** — Network Layer (IP packets carrying TCP ACK data)
**Topic:** TCP/IP Layers

---

**Q17.** In the full communication model diagram (slide 11), NFS is an example of a protocol at which layer?
- A) Transport Layer
- B) Network Layer
- C) Application Layer
- D) Data Link Layer


**Answer:** **C** — Application Layer
**Topic:** Layer Protocols

---

**Q18.** Which transport-layer protocols are shown in the TCP/IP model?
- A) HTTP and FTP
- B) UDP and TCP
- C) IP and ICMP
- D) ARP and RARP


**Answer:** **B** — UDP and TCP
**Topic:** Transport Protocols

---

**Q19.** ARP (Address Resolution Protocol) sits between which two layers in the TCP/IP model?
- A) Application and Transport
- B) Transport and Internet
- C) Internet and Network Interface
- D) Physical and Data Link


**Answer:** **C** — Internet and Network Interface
**Topic:** ARP Position

---

**Q20.** Which routing protocols are shown in the Internet Layer?
- A) HTTP, FTP, SMTP
- B) UDP, TCP
- C) RIP, OSPF, BGP, EGP
- D) Ethernet, Wi-Fi


**Answer:** **C** — RIP, OSPF, BGP, EGP
**Topic:** Routing Protocols

---

### Section 3: Application Layer (Layer 5 in TCP/IP)

**Q21.** The Application Layer answers which fundamental question?
- A) How raw bits are transferred?
- B) How data reaches the destination?
- C) How to provide network services to end-user applications?
- D) How to provide end-to-end communication?


**Answer:** **C** — How to provide network services to end-user applications?
**Topic:** App Layer

---

**Q22.** Application Layer protocols are used by:
- A) NICs and modems
- B) APIs
- C) IP routing tables
- D) Physical switches


**Answer:** **B** — APIs
**Topic:** App Layer

---

**Q23.** Which of the following is NOT listed as an Application Layer protocol in the lecture?
- A) HTTP
- B) WebSocket
- C) TCP
- D) SSH


**Answer:** **C** — TCP (TCP is a Transport Layer protocol, not Application)
**Topic:** App Layer Protocols

---

**Q24.** Which protocol is used for file sharing according to the lecture's Application Layer?
- A) HTTP
- B) NFS
- C) SMTP
- D) WebSocket


**Answer:** **B** — NFS
**Topic:** App Layer Protocols

---

### Section 4: Transport Layer (Layer 4)

**Q25.** The Transport Layer answers which fundamental question?
- A) How raw bits are transferred?
- B) How data reaches the destination?
- C) How to provide end-to-end communication?
- D) How to provide network services to applications?


**Answer:** **C** — How to provide end-to-end communication?
**Topic:** Transport Layer

---

**Q26.** In the Transport Layer, TCP/UDP ports identify:
- A) The physical location of a server
- B) Which application is sending/receiving the data
- C) The MAC address of the destination
- D) The routing path through the internet


**Answer:** **B** — Which application is sending/receiving the data
**Topic:** Ports

---

**Q27.** TCP is characterized as:
- A) Connectionless
- B) Connection-oriented
- C) Broadcast-based
- D) Stateless


**Answer:** **B** — Connection-oriented
**Topic:** TCP

---

**Q28.** UDP is characterized as:
- A) Connection-oriented
- B) Reliable with ACKs
- C) Connectionless
- D) Requires handshake


**Answer:** **C** — Connectionless
**Topic:** UDP

---

**Q29.** What does TCP prioritize over UDP?
- A) Speed and efficiency
- B) Reliability
- C) Lower overhead
- D) Broadcast capability


**Answer:** **B** — Reliability
**Topic:** TCP vs UDP

---

**Q30.** What does UDP prioritize over TCP?
- A) Reliability
- B) Ordered delivery
- C) Efficiency
- D) Error correction


**Answer:** **C** — Efficiency
**Topic:** TCP vs UDP

---

**Q31.** In the TCP handshake, which of the following is the correct sequence?
- A) SYN → ACK → SYN-ACK
- B) SYN-ACK → SYN → ACK
- C) SYN → SYN-ACK → SYN (confirmation)
- D) ACK → SYN → SYN-ACK


**Answer:** **C** — SYN → SYN-ACK → SYN (confirmation/ACK)
**Topic:** TCP Handshake

---

**Q32.** In a UDP exchange, the server can:
- A) Only send one response
- B) Wait for a SYN before responding
- C) Send multiple responses without establishing a connection
- D) Only receive but never send


**Answer:** **C** — Send multiple responses without establishing a connection
**Topic:** UDP

---

**Q33.** Source port 50000 in the slide example is associated with:
- A) Email communicating
- B) FTP Uploading
- C) Web browsing
- D) SSH tunneling


**Answer:** **C** — Web browsing (Source port 50000)
**Topic:** Transport Layer Example

---

### Section 5: Network Layer (Layer 3)

**Q34.** The Network Layer answers which fundamental question?
- A) How to provide end-to-end communication?
- B) How data reaches the destination?
- C) How raw bits are transferred?
- D) How to provide network services?


**Answer:** **B** — How data reaches the destination?
**Topic:** Network Layer

---

**Q35.** Private IP addresses in a home/office network are generated by:
- A) The ISP
- B) The DHCP Server (assigned dynamically) via the Router
- C) The modem directly from the internet
- D) Each device independently


**Answer:** **B** — The DHCP Server (assigned dynamically) via the Router
**Topic:** Private IPs

---

**Q36.** Public IP addresses are generated by:
- A) The DHCP server on the router
- B) The ISP
- C) The DNS server
- D) The local switch


**Answer:** **B** — The ISP
**Topic:** Public IPs

---

**Q37.** What does DHCP stand for?
- A) Dynamic Host Connection Protocol
- B) Dynamic Host Configuration Protocol
- C) Distributed Host Communication Protocol
- D) Direct Hardware Configuration Protocol


**Answer:** **B** — Dynamic Host Configuration Protocol
**Topic:** DHCP

---

**Q38.** In the slide example, the private IPs shown (192.168.1.1 to 192.168.1.4) are generated by:
- A) The ISP
- B) The DNS server
- C) The Router
- D) Each device itself


**Answer:** **C** — The Router
**Topic:** Private IPs

---

**Q39.** What does NAT stand for?
- A) Network Access Technology
- B) Network Address Translator
- C) Node Allocation Table
- D) Network Aggregation Tool


**Answer:** **B** — Network Address Translator
**Topic:** NAT

---

**Q40.** NAT's primary function is:
- A) Routing messages between application-layer services
- B) Translating private IPs to public IPs and vice versa
- C) Encrypting all network traffic
- D) Assigning MAC addresses to devices


**Answer:** **B** — Translating private IPs to public IPs and vice versa
**Topic:** NAT Function

---

**Q41.** In the DNS resolution process for "www.example.com", which server provides the final authoritative IP address?
- A) Root DNS Server
- B) ISP's Recursive Server
- C) Top Level Domain (TLD) DNS Server
- D) Authoritative DNS Server


**Answer:** **D** — Authoritative DNS Server
**Topic:** DNS Resolution

---

**Q42.** What is the correct sequence of DNS resolution steps?
- A) Ask Root → Ask TLD → Ask Authoritative → Get IP from Recursive Server
- B) Ask Recursive → Ask Root → Ask TLD → Ask Authoritative → Return IP to client
- C) Ask Authoritative directly
- D) Ask TLD → Ask Root → Get IP


**Answer:** **B** — Ask Recursive → Ask Root → Ask TLD → Ask Authoritative → Return IP
**Topic:** DNS Flow

---

**Q43.** In the lecture example, the DNS resolution query returns IP:
- A) 192.168.1.1
- B) 82.129.80.111
- C) 142.251.142.206
- D) 217.64.213.12


**Answer:** **D** — 217.64.213.12
**Topic:** DNS Example

---

**Q44.** How do routers determine the path for an IP packet?
- A) They broadcast to all connected devices
- B) Each router has a routing table to pass the message to the next best node
- C) They always use the shortest physical path
- D) The DNS server provides routing instructions


**Answer:** **B** — Each router has a routing table to pass the message to the next best node
**Topic:** Routing

---

**Q45.** IP routing at the network layer involves packets traveling through:
- A) A single dedicated path predetermined at connection start
- B) Multiple routers, each forwarding to the next best node
- C) Only the ISP's infrastructure
- D) A direct physical cable from source to destination


**Answer:** **B** — Multiple routers, each forwarding to the next best node
**Topic:** Routing

---

### Section 6: Data Link Layer (Layer 2)

**Q46.** The Data Link Layer answers which fundamental question?
- A) How to provide end-to-end communication?
- B) How data reaches the destination?
- C) How is data transferred?
- D) How to provide network services?


**Answer:** **C** — How is data transferred?
**Topic:** Data Link Layer

---

**Q47.** Which IEEE standard corresponds to Ethernet?
- A) IEEE 802.11
- B) IEEE 802.15.1
- C) IEEE 802.3
- D) IEEE 802.15.4


**Answer:** **C** — IEEE 802.3
**Topic:** Ethernet Standard

---

**Q48.** Which IEEE standard corresponds to Wi-Fi?
- A) IEEE 802.3
- B) IEEE 802.11
- C) IEEE 802.15.1
- D) IEEE 802.15.4


**Answer:** **B** — IEEE 802.11
**Topic:** Wi-Fi Standard

---

**Q49.** Which standard corresponds to Bluetooth?
- A) IEEE 802.3
- B) IEEE 802.11
- C) IEEE 802.15.4
- D) IEEE 802.15.1


**Answer:** **D** — IEEE 802.15.1
**Topic:** Bluetooth Standard

---

**Q50.** Which standard corresponds to Zigbee?
- A) IEEE 802.15.1
- B) IEEE 802.15.4
- C) IEEE 802.11
- D) 3GPP LTE R8


**Answer:** **B** — IEEE 802.15.4
**Topic:** Zigbee Standard

---

**Q51.** 3GPP LTE R8 corresponds to which mobile generation?
- A) 2G
- B) 3G
- C) 4G
- D) 4.5G


**Answer:** **C** — 4G
**Topic:** 3GPP Standards

---

**Q52.** 3GPP LTE R10 corresponds to which mobile generation?
- A) 3G
- B) 4G
- C) 4.5G
- D) 5G


**Answer:** **B** — 4G
**Topic:** 3GPP Standards

---

**Q53.** 3GPP LTE R13 corresponds to which mobile generation?
- A) 4G
- B) 5G
- C) 4.5G
- D) 3G


**Answer:** **C** — 4.5G
**Topic:** 3GPP Standards

---

**Q54.** In an Ethernet frame, what is the purpose of the Preamble field?
- A) Error detection using a hash code
- B) Synchronization and notification for the receiver
- C) Identifying the destination MAC address
- D) Specifying payload size


**Answer:** **B** — Synchronization and notification for the receiver
**Topic:** Ethernet Frame

---

**Q55.** What does SFD stand for in an Ethernet frame, and what is its value?
- A) Start Frame Delimiter — "10101011"
- B) Source Frame Data — "11001100"
- C) Signal Frame Detection — "11111111"
- D) Start Frame Data — "10101010"


**Answer:** **A** — Start Frame Delimiter — "10101011"
**Topic:** Ethernet Frame

---

**Q56.** How many bytes is a MAC address in an Ethernet frame?
- A) 4 bytes
- B) 2 bytes
- C) 6 bytes
- D) 8 bytes


**Answer:** **C** — 6 bytes
**Topic:** MAC Address

---

**Q57.** In an Ethernet frame, the CRC field is:
- A) 7 bytes — synchronization
- B) 2 bytes — payload size
- C) 4 bytes — 32-bit hash code for error detection
- D) 6 bytes — MAC address


**Answer:** **C** — 4 bytes — 32-bit hash code for error detection
**Topic:** Ethernet Frame CRC

---

**Q58.** The Length field in an Ethernet frame indicates:
- A) The duration of the transmission
- B) The payload size
- C) The source IP address
- D) The number of hops


**Answer:** **B** — The payload size
**Topic:** Ethernet Frame

---

**Q59.** The data payload in an Ethernet Type II frame is:
- A) Fixed at 512 bytes
- B) 46 to 1500 bytes
- C) 7 bytes
- D) Always exactly 1500 bytes


**Answer:** **B** — 46 to 1500 bytes
**Topic:** Ethernet Payload

---

**Q60.** In an Ethernet Type II frame, the total frame size is:
- A) 14 to 512 bytes
- B) 64 to 1518 bytes
- C) 128 to 2048 bytes
- D) 46 to 1500 bytes


**Answer:** **B** — 64 to 1518 bytes
**Topic:** Ethernet Frame Size

---

**Q61.** The MAC Header in an Ethernet Type II frame consists of:
- A) Destination MAC + Source MAC + EtherType = 14 bytes
- B) Preamble + SFD = 8 bytes
- C) Source MAC + CRC = 10 bytes
- D) Destination IP + Source IP = 8 bytes


**Answer:** **A** — Destination MAC + Source MAC + EtherType = 14 bytes
**Topic:** Ethernet MAC Header

---

**Q62.** Manchester encoding in the Data Link layer is used for:
- A) Routing packets between networks
- B) Encoding/Decoding bits for transmission
- C) Compressing payload data
- D) Assigning IP addresses dynamically


**Answer:** **B** — Encoding/Decoding bits for transmission
**Topic:** Manchester Encoding

---

**Q63.** Newer Ethernet protocols have:
- A) Fewer signal levels
- B) Only binary encoding
- C) Multiple signal levels (more than two)
- D) No encoding at all


**Answer:** **C** — Multiple signal levels (more than two)
**Topic:** Ethernet Encoding

---

**Q64.** In simplex transmission mode:
- A) Data can flow in both directions simultaneously
- B) Data flows only in one direction
- C) Data alternates directions on a shared medium
- D) Data is broadcast to all nodes


**Answer:** **B** — Data flows only in one direction
**Topic:** Simplex

---

**Q65.** Full-duplex transmission means:
- A) Data flows in one direction only
- B) Both parties can send and receive simultaneously
- C) Only one party can transmit at a time
- D) Data is sent in half-speed alternating bursts


**Answer:** **B** — Both parties can send and receive simultaneously
**Topic:** Full-Duplex

---

**Q66.** Half-duplex transmission means:
- A) Data flows only one direction permanently
- B) Both ends can communicate but only one at a time, sharing the medium
- C) Full simultaneous bidirectional communication
- D) Data sent in broadcast mode


**Answer:** **B** — Both ends can communicate but only one at a time
**Topic:** Half-Duplex

---

### Section 7: Physical Layer (Layer 1)

**Q67.** The Physical Layer answers which fundamental question?
- A) How to provide end-to-end communication?
- B) How data reaches the destination?
- C) How raw bits are transferred over physical media?
- D) How to provide network services?


**Answer:** **C** — How raw bits are transferred over physical media?
**Topic:** Physical Layer

---

**Q68.** Which of the following is NOT listed as a physical media example in the lecture?
- A) Optical Fibers
- B) Physical Cables
- C) Radio Frequency
- D) Satellite Links


**Answer:** **D** — Satellite Links (not mentioned; optical fibers, physical cables, radio frequency are listed)
**Topic:** Physical Media

---

**Q69.** Which hardware components handle data conversion and raw transmission at the Physical Layer?
- A) Routers and switches
- B) NICs and modems
- C) Firewalls and load balancers
- D) DNS servers and gateways


**Answer:** **B** — NICs and modems
**Topic:** Physical Layer Devices

---

### Section 8: Network Devices

**Q70.** A Network Interface Card (NIC) operates at which layer?
- A) Network Layer
- B) Data Layer
- C) Physical Layer
- D) Application Layer


**Answer:** **C** — Physical Layer
**Topic:** NIC

---

**Q71.** How does a computer send/receive data through a NIC?
- A) Through HTTP requests only
- B) Via the PCI Bus connecting Host DMA, Memory, and Net Send/Recv DMA to the network
- C) By directly accessing the router's routing table
- D) Using DNS system calls


**Answer:** **B** — Via the PCI Bus connecting Host DMA, Memory, and Net Send/Recv DMA
**Topic:** NIC Architecture

---

**Q72.** A Modem's primary function is:
- A) Routing packets between networks
- B) Broadcasting data to all devices
- C) Converting digital data (Computer) to analogue (Fiber/Coaxial) and vice versa
- D) Assigning dynamic IP addresses


**Answer:** **C** — Converting digital data to analogue and vice versa
**Topic:** Modem

---

**Q73.** "Modem" is short for:
- A) Modern Networking Device
- B) Modulator/Demodulator
- C) Module/Demodule
- D) Motor/Demotivator


**Answer:** **B** — Modulator/Demodulator
**Topic:** Modem

---

**Q74.** A Repeater operates at which layer?
- A) Network Layer
- B) Data Link Layer
- C) Physical Layer
- D) Application Layer


**Answer:** **C** — Physical Layer
**Topic:** Repeater

---

**Q75.** What does a Repeater do?
- A) Routes packets between different networks
- B) Amplifies/Regenerates the signal strength within the same network
- C) Translates private IPs to public IPs
- D) Directs traffic only to the intended destination


**Answer:** **B** — Amplifies/Regenerates the signal strength within the same network
**Topic:** Repeater

---

**Q76.** A Hub is best described as:
- A) A multi-port connector that sends data only to the destination device
- B) A multi-port Repeater that broadcasts data to all attached devices
- C) A device that routes messages between networks
- D) A device that converts analogue to digital signals


**Answer:** **B** — A multi-port Repeater that broadcasts data to all attached devices
**Topic:** Hub

---

**Q77.** A Hub operates at which layer?
- A) Data Layer
- B) Network Layer
- C) Physical Layer
- D) Application Layer


**Answer:** **C** — Physical Layer
**Topic:** Hub

---

**Q78.** When Host A wants to send a message to Host E through a Hub (5 hosts connected), the Hub will:
- A) Send only to Host E
- B) Send to Host A and Host E only
- C) Broadcast to ALL connected hosts (B, C, D, E)
- D) Look up a routing table and forward selectively


**Answer:** **C** — Broadcast to ALL connected hosts (B, C, D, E)
**Topic:** Hub Behavior

---

**Q79.** A Bridge operates at which layer?
- A) Physical Layer
- B) Data Layer (Data Link)
- C) Network Layer
- D) Application Layer


**Answer:** **B** — Data Layer (Data Link)
**Topic:** Bridge

---

**Q80.** A Bridge is characterized as:
- A) A multi-port repeater
- B) A two-port connector that passes messages to the target segment
- C) A device that routes between different IP networks
- D) A multi-network connector


**Answer:** **B** — A two-port connector that passes messages to the target segment
**Topic:** Bridge

---

**Q81.** What does a Bridge join?
- A) Different IP networks
- B) Any two sub-networks or host segments
- C) Application layer services
- D) Physical cables to wireless networks


**Answer:** **B** — Any two sub-networks or host segments
**Topic:** Bridge

---

**Q82.** A Switch operates at which layer?
- A) Physical Layer
- B) Data Layer (Data Link)
- C) Network Layer
- D) Application Layer


**Answer:** **B** — Data Layer (Data Link)
**Topic:** Switch

---

**Q83.** The key difference between a Switch and a Hub is:
- A) A Switch operates at the Physical layer; a Hub does not
- B) A Switch sends data only to the destination device; a Hub broadcasts to all
- C) A Switch cannot handle multiple ports
- D) A Hub uses MAC addresses; a Switch does not


**Answer:** **B** — A Switch sends data only to the destination; a Hub broadcasts to all
**Topic:** Switch vs Hub

---

**Q84.** When Host A sends a message to Host E through a Switch:
- A) All connected hosts receive the message
- B) Only Host E receives the message
- C) The message is dropped if Host E is offline
- D) The message is broadcast then filtered by each host


**Answer:** **B** — Only Host E receives the message
**Topic:** Switch Behavior

---

**Q85.** A Router operates at which layer?
- A) Physical Layer
- B) Data Layer
- C) Network Layer
- D) Application Layer


**Answer:** **C** — Network Layer
**Topic:** Router

---

**Q86.** A Router is best described as:
- A) A two-port connector between sub-networks
- B) A multi-port repeater
- C) A multi-network connector that moves data between networks and provides traffic control
- D) A device that converts analogue to digital


**Answer:** **C** — A multi-network connector that moves data between networks and provides traffic control
**Topic:** Router

---

**Q87.** In the Router diagram, what separates the two sub-networks?
- A) A Bridge
- B) A Switch
- C) A Router connecting 192.168.1.X and 41.68.220.X
- D) A Hub


**Answer:** **C** — A Router connecting 192.168.1.X and 41.68.220.X
**Topic:** Router Example

---

**Q88.** A NAT device operates at which layer?
- A) Physical Layer
- B) Data Layer
- C) Network Layer
- D) Application Layer


**Answer:** **C** — Network Layer
**Topic:** NAT

---

**Q89.** In the NAT example, a host with source IP 10.0.0.1 sends a packet to 200.100.10.1. After passing through the NAT (Router+NAT at 150.150.0.1), the source IP in the packet reaching the server becomes:
- A) 10.0.0.1
- B) 200.100.10.1
- C) 150.150.0.1
- D) 192.168.1.1


**Answer:** **C** — 150.150.0.1 (the Router+NAT's public IP replaces the private source IP)
**Topic:** NAT Translation

---

**Q90.** When the server at 200.100.10.1 responds back through NAT, the destination IP in the packet arriving at the host is:
- A) 150.150.0.1
- B) 200.100.10.1
- C) 10.0.0.1
- D) 192.168.0.1


**Answer:** **C** — 10.0.0.1 (NAT reverses the translation on inbound traffic)
**Topic:** NAT Translation

---

**Q91.** An Access Point operates at which layer?
- A) Physical Layer
- B) Data Layer
- C) Network Layer
- D) Application Layer


**Answer:** **C** — Network Layer
**Topic:** Access Point

---

**Q92.** Which of the following roles does an Access Point NOT perform?
- A) Switch
- B) DHCP server
- C) DNS resolver for external domains
- D) Firewall


**Answer:** **C** — DNS resolver for external domains (Access Point acts as switch, DHCP, router, firewall)
**Topic:** Access Point Roles

---

**Q93.** A Gateway operates at which layer?
- A) Physical Layer
- B) Data Layer
- C) Network Layer
- D) Application (App) Layer


**Answer:** **D** — Application (App) Layer
**Topic:** Gateway

---

**Q94.** A Gateway is best described as:
- A) A two-port connector for sub-networks
- B) A multi-system connector for similar/dissimilar networks
- C) A device that amplifies signals
- D) A multi-port repeater


**Answer:** **B** — A multi-system connector for similar/dissimilar networks
**Topic:** Gateway

---

**Q95.** A Load Balancer operates at which layer?
- A) Transport Layer
- B) Network Layer
- C) Data Layer
- D) Application (App) Layer


**Answer:** **D** — Application (App) Layer
**Topic:** Load Balancer

---

**Q96.** The primary function of a Load Balancer is:
- A) Translating private IPs to public IPs
- B) Routing packets between networks
- C) Distributing incoming traffic across a group of servers
- D) Amplifying signal strength


**Answer:** **C** — Distributing incoming traffic across a group of servers
**Topic:** Load Balancer

---

**Q97.** A Firewall operates at which layer?
- A) Physical Layer
- B) Data Layer
- C) Network Layer
- D) Application (App) Layer


**Answer:** **D** — Application (App) Layer
**Topic:** Firewall

---

**Q98.** A Firewall's primary function is:
- A) Converting analogue to digital signals
- B) Distributing traffic across servers
- C) Routing between subnets
- D) Controlling incoming/outgoing traffic based on security rules


**Answer:** **D** — Controlling incoming/outgoing traffic based on security rules
**Topic:** Firewall

---

**Q99.** Which of the following correctly matches devices to their layers?
- A) Hub → Network Layer; Router → Data Layer
- B) Switch → Data Layer; Router → Network Layer; Load Balancer → App Layer
- C) Bridge → Physical Layer; Switch → Network Layer
- D) NIC → Data Layer; Modem → Application Layer


**Answer:** **B** — Switch → Data Layer; Router → Network Layer; Load Balancer → App Layer
**Topic:** Device-Layer Mapping

---

### Section 9: Network Topology

**Q100.** How many standard network topologies are shown in the lecture?
- A) 4
- B) 5
- C) 6
- D) 7


**Answer:** **D** — 7 (Point-to-point, Bus, Ring, Star, Tree, Mesh, Hybrid)
**Topic:** Network Topology

---

**Q101.** In which topology does data travel in a circular path through all devices?
- A) Bus
- B) Star
- C) Ring
- D) Mesh


**Answer:** **C** — Ring
**Topic:** Ring Topology

---

**Q102.** In which topology are all devices connected to a central device (hub/switch)?
- A) Bus
- B) Ring
- C) Tree
- D) Star


**Answer:** **D** — Star
**Topic:** Star Topology

---

**Q103.** In a Bus topology, all devices connect to:
- A) A central hub
- B) Each other directly
- C) A single shared backbone cable
- D) A ring of routers


**Answer:** **C** — A single shared backbone cable
**Topic:** Bus Topology

---

**Q104.** A Mesh topology is characterized by:
- A) One central device
- B) A linear backbone
- C) Every device connected to every other device
- D) A hierarchical tree structure


**Answer:** **C** — Every device connected to every other device
**Topic:** Mesh Topology

---

### Section 10: Cloud Network Structure

**Q105.** In a cloud data center, TOR stands for:
- A) Transfer Of Route
- B) Top-of-Rack
- C) Traffic Overhead Router
- D) Trunked Output Router


**Answer:** **B** — Top-of-Rack
**Topic:** TOR

---

**Q106.** TOR switches operate at what speed range?
- A) 100Mbps to 1Gbps
- B) 1 to 10Gbps
- C) 40 to 100Gbps
- D) 1Tbps


**Answer:** **B** — 1 to 10Gbps
**Topic:** TOR Speed

---

**Q107.** The primary function of TOR switches is to:
- A) Connect sectors together and the internet
- B) Connect racks to the internet directly
- C) Connect servers within the same rack together
- D) Route traffic between VMs globally


**Answer:** **C** — Connect servers within the same rack together
**Topic:** TOR Function

---

**Q108.** Core Switches in a cloud data center operate at approximately:
- A) 1Gbps
- B) 10Gbps
- C) 100Gbps
- D) 1Tbps


**Answer:** **C** — ~100Gbps
**Topic:** Core Switch Speed

---

**Q109.** Core Switches are used to:
- A) Connect servers within the same rack
- B) Connect racks together (within a sector)
- C) Connect sectors together and the internet
- D) Translate private IPs to public IPs


**Answer:** **B** — Connect racks together (within a sector)
**Topic:** Core Switch Function

---

**Q110.** Layer 3 Switches/Routers in a cloud data center are used to:
- A) Connect servers within racks
- B) Connect racks within a sector
- C) Connect sectors together and the internet
- D) Manage VLAN assignments


**Answer:** **C** — Connect sectors together and the internet
**Topic:** Layer 3 Switch Function

---

**Q111.** In-Rack traffic refers to communication:
- A) Between sectors
- B) Between servers in different racks within the same sector
- C) Between servers in the SAME rack
- D) Between the data center and the internet


**Answer:** **C** — Between servers in the SAME rack
**Topic:** In-Rack Traffic

---

**Q112.** East-West traffic in a cloud data center refers to:
- A) Traffic between sectors or the internet
- B) Traffic between servers in the SAME sector (different racks)
- C) Traffic between servers in the same rack
- D) Traffic from end-users to the data center


**Answer:** **B** — Between servers in the SAME sector (different racks)
**Topic:** East-West Traffic

---

**Q113.** North-South traffic refers to:
- A) Traffic between servers in the same rack
- B) Traffic between servers in the same sector
- C) Traffic between sectors or to/from the internet
- D) Internal VM-to-VM communication


**Answer:** **C** — Between sectors or to/from the internet
**Topic:** North-South Traffic

---

**Q114.** The correct hierarchy of cloud network structure from bottom to top is:
- A) Layer 3 Switch → Core Switch → TOR → Servers
- B) Servers → TOR → Core Switch → Layer 3 Switch
- C) Servers → Core Switch → TOR → Layer 3 Switch
- D) TOR → Servers → Core Switch → Layer 3 Switch


**Answer:** **B** — Servers → TOR → Core Switch → Layer 3 Switch
**Topic:** Cloud Network Hierarchy

---

### Section 11: Network Virtualization Concepts

**Q115.** In cloud data centers, virtual entities (VMs/Containers) communicate through:
- A) Direct physical NIC connections only
- B) PNIC (Physical NIC) via the Hypervisor Kernel and VM Network
- C) External routers only
- D) The internet backbone directly


**Answer:** **B** — PNIC via the Hypervisor Kernel and VM Network
**Topic:** Virtual Entities

---

**Q116.** Which of the following is TRUE about virtual networks in cloud data centers?
- A) Virtual networks must use dedicated physical resources
- B) Virtual networks are always public
- C) Virtual networks are isolated and can share the same underlying physical resources
- D) Each virtual network requires a separate physical switch


**Answer:** **C** — Virtual networks are isolated and can share the same underlying physical resources
**Topic:** Virtual Network Properties

---

**Q117.** A Network Hypervisor is best described as:
- A) A physical router with special firmware
- B) An abstraction layer that represents nodes/links in a virtual network and controls resources
- C) A software firewall
- D) A load balancer for VMs


**Answer:** **B** — An abstraction layer that represents nodes/links and controls resources
**Topic:** Network Hypervisor

---

**Q118.** Which of the following is NOT a function of the Network Hypervisor?
- A) Control bandwidth
- B) Control virtual network capacity
- C) Isolate and secure virtual networks
- D) Assign public IP addresses from the ISP


**Answer:** **D** — Assign public IP addresses from the ISP (not a hypervisor function)
**Topic:** Network Hypervisor Functions

---

**Q119.** Internal Virtualization addresses which question?
- A) How VMs on different servers communicate?
- B) How VMs on the SAME server communicate?
- C) How physical switches route VLAN traffic?
- D) How NAT translates between private and public IPs?


**Answer:** **B** — How VMs on the SAME server communicate?
**Topic:** Internal Virtualization

---

**Q120.** In Internal Virtualization, the VMM Hypervisor creates:
- A) Physical NICs and physical switches
- B) Virtual NICs (VNICs) and virtual switches
- C) TOR switches and Core switches
- D) VXLAN tunnels


**Answer:** **B** — Virtual NICs (VNICs) and virtual switches
**Topic:** Internal Virtualization

---

**Q121.** In Internal Virtualization, when a VM triggers a network system call (e.g., sendmsg()), the hypervisor:
- A) Ignores the call and passes it to the physical NIC directly
- B) Traps the system call and emulates the operation using Virtual NICs
- C) Broadcasts the call to all VMs on the server
- D) Escalates the call to the ISP router


**Answer:** **B** — Traps the system call and emulates the operation using Virtual NICs
**Topic:** System Call Emulation

---

**Q122.** A Virtual NIC defines:
- A) The routing table for the physical server
- B) The VM's connectivity and bandwidth
- C) The DNS configuration for the host
- D) The MAC addresses for physical switches


**Answer:** **B** — The VM's connectivity and bandwidth
**Topic:** Virtual NIC

---

**Q123.** In Internal Virtualization (Emulate Network Function), network requests are forwarded to the Hypervisor's virtual switch which then:
- A) Sends them directly to the physical NIC without inspection
- B) Routes network messages to the target Virtual NIC
- C) Broadcasts to all VMs on all servers
- D) Drops packets that have no routing entry


**Answer:** **B** — Routes network messages to the target Virtual NIC
**Topic:** Virtual Switch

---

**Q124.** In the Docker networking example, what subnet is created for the virtual network?
- A) 10.0.0.0/8
- B) 192.168.0.0/16
- C) 172.19.0.0/16
- D) 10.10.0.0/24


**Answer:** **C** — 172.19.0.0/16
**Topic:** Docker Networking

---

**Q125.** In the Docker networking example, what does Docker create to connect the virtual network to the external LAN?
- A) A physical bridge
- B) A virtual bridge (mybridge)
- C) A VXLAN tunnel
- D) A NAT gateway at the ISP


**Answer:** **B** — A virtual bridge (mybridge)
**Topic:** Docker Networking

---

**Q126.** External Virtualization addresses which question?
- A) How VMs on the SAME server communicate?
- B) How VMs on DIFFERENT servers communicate?
- C) How physical routers are configured?
- D) How DNS resolves VM hostnames?


**Answer:** **B** — How VMs on DIFFERENT servers communicate?
**Topic:** External Virtualization

---

**Q127.** In External Virtualization, the Hypervisor holds:
- A) Physical routing tables only
- B) Virtual iptables with the physical servers hosting the target VMs
- C) VLAN configuration for all external switches
- D) DNS records for all VMs


**Answer:** **B** — Virtual iptables with the physical servers hosting the target VMs
**Topic:** External Virtualization

---

### Section 12: VLAN

**Q128.** A VLAN (Virtual LAN) allows:
- A) Routing between different IP networks
- B) Grouping devices into separate, isolated sub-groups regardless of physical location
- C) Converting digital to analogue signals
- D) Distributing traffic across multiple servers


**Answer:** **B** — Grouping devices into separate, isolated sub-groups
**Topic:** VLAN Definition

---

**Q129.** Which IEEE standard defines the VLAN tagging in Ethernet frames?
- A) IEEE 802.3
- B) IEEE 802.11
- C) IEEE 802.1Q
- D) IEEE 802.15.1


**Answer:** **C** — IEEE 802.1Q
**Topic:** VLAN Standard

---

**Q130.** In the IEEE 802.1Q frame, the VLAN Tag (802.1Q Tag) is inserted between:
- A) Preamble and SFD
- B) Source Address and Length/Type fields
- C) Length/Type and Data fields
- D) Data and CRC


**Answer:** **B** — Between Source Address and Length/Type fields
**Topic:** 802.1Q Frame Position

---

**Q131.** The 802.1Q VLAN tag contains a VID field of how many bits?
- A) 3 bits
- B) 1 bit
- C) 12 bits
- D) 16 bits


**Answer:** **C** — 12 bits
**Topic:** VLAN VID

---

**Q132.** In the 802.1Q tag, what does TPID stand for?
- A) Tagged Protocol Identification
- B) Tag Protocol IDentifier
- C) Transfer Protocol ID
- D) Trunk Port Identification


**Answer:** **B** — Tag Protocol IDentifier
**Topic:** 802.1Q Fields

---

**Q133.** The maximum number of VLANs supported by IEEE 802.1Q is:
- A) 256
- B) 1024
- C) 4096
- D) 65536


**Answer:** **C** — 4096 (2^12)
**Topic:** VLAN Limit

---

**Q134.** In a VLAN-aware network, devices in the SAME VLAN:
- A) Require inter-VLAN routing to communicate
- B) Cannot communicate without a router
- C) Form a group and communicate directly
- D) Must use VXLAN for communication


**Answer:** **C** — Form a group and communicate directly
**Topic:** VLAN Communication

---

**Q135.** Devices from DIFFERENT VLANs require:
- A) A new physical cable
- B) Inter-VLAN routing
- C) A Hub to broadcast between groups
- D) A modem to convert signals


**Answer:** **B** — Inter-VLAN routing
**Topic:** Inter-VLAN

---

**Q136.** Which of the following is listed as a PRO of VLANs?
- A) Simplifies configuration
- B) No need for managed switches
- C) Security through network traffic isolation
- D) No inter-VLAN routing needed


**Answer:** **C** — Security through network traffic isolation
**Topic:** VLAN Pros

---

**Q137.** Which of the following is listed as a CON of VLANs?
- A) Better security
- B) Interoperability issues with legacy/non-aware devices
- C) Reduced bandwidth
- D) Requires physical separation of networks


**Answer:** **B** — Interoperability issues with legacy/non-aware devices
**Topic:** VLAN Cons

---

### Section 13: VXLAN

**Q138.** Why is VXLAN needed over traditional VLAN (IEEE 802.1Q)?
- A) VLAN supports too many segments
- B) VLAN IDs are 12 bits (only 4096 segments) — not enough for cloud data centers
- C) VLAN cannot support Ethernet
- D) VLAN does not support multicast


**Answer:** **B** — VLAN IDs are 12 bits (only 4096 segments) — not enough for cloud
**Topic:** VXLAN Motivation

---

**Q139.** The "Overlay Network" in VXLAN refers to:
- A) The physical network connection moving data between switches
- B) The virtualized VLAN connection between two Layer-2 switches
- C) The TCP/IP stack on each VM
- D) The management network for the hypervisor


**Answer:** **B** — The virtualized VLAN connection between two Layer-2 switches
**Topic:** VXLAN Overlay

---

**Q140.** The "Underlay Network" in VXLAN refers to:
- A) The virtualized VLAN connection
- B) The VM-to-VM communication layer
- C) The physical network connection moving data from one switch to another
- D) The application-level virtual network


**Answer:** **C** — The physical network connection moving data from one switch to another
**Topic:** VXLAN Underlay

---

**Q141.** VXLAN virtualizes VLAN using which type of devices?
- A) Layer-1 Physical repeaters
- B) Layer-2 switches only
- C) Layer-3 Switches/Routers
- D) Application-layer gateways


**Answer:** **C** — Layer-3 Switches/Routers
**Topic:** VXLAN Devices

---

**Q142.** In VXLAN, the original Ethernet frame is encapsulated in:
- A) A TCP segment
- B) A UDP message with a VXLAN header
- C) An ICMP packet
- D) An HTTP request


**Answer:** **B** — A UDP message with a VXLAN header
**Topic:** VXLAN Encapsulation

---

**Q143.** The VXLAN header's primary purpose is to:
- A) Provide encryption for the data
- B) Identify servers in the same VXLAN group (VNI)
- C) Assign public IP addresses
- D) Perform NAT translation


**Answer:** **B** — Identify servers in the same VXLAN group (VNI)
**Topic:** VXLAN Header

---

**Q144.** VNI in VXLAN stands for:
- A) Virtual Network Infrastructure
- B) VXLAN Network Identifier
- C) Virtual Node Interface
- D) VLAN Network Index


**Answer:** **B** — VXLAN Network Identifier
**Topic:** VNI

---

**Q145.** In the VXLAN packet flow diagram (6 steps), in step 3 which entity encapsulates the original packet into a UDP/VXLAN packet?
- A) The destination VM
- B) The VTEP (VXLAN Tunnel Endpoint) on the source side
- C) The Layer 3 switch in the underlay
- D) The DNS server


**Answer:** **B** — The VTEP (VXLAN Tunnel Endpoint) on the source side
**Topic:** VXLAN Packet Flow

---

**Q146.** VTEP stands for:
- A) Virtual Tunnel Endpoint Protocol
- B) VXLAN Tunnel End Point
- C) Virtual Transfer Encoding Protocol
- D) VLAN Topology Extension Point


**Answer:** **B** — VXLAN Tunnel End Point
**Topic:** VTEP

---

### Section 14: DVS and VPC

**Q147.** A Distributed Virtual Switch (DVS) is:
- A) A physical switch distributed across multiple data centers
- B) Multiple Network Hypervisors emulating the operation of a switch across multiple host machines
- C) A Layer-3 router that handles VXLAN tunnels
- D) A software load balancer


**Answer:** **B** — Multiple Network Hypervisors emulating the operation of a switch across multiple host machines
**Topic:** DVS

---

**Q148.** Which of the following is a PRO of a DVS?
- A) Requires no configuration
- B) Provides virtual switch ports that are configurable (e.g., control data rate)
- C) Eliminates the need for physical switches
- D) Directly replaces Layer 3 routing


**Answer:** **B** — Provides virtual switch ports that are configurable (e.g., control data rate)
**Topic:** DVS Pros

---

**Q149.** In a DVS, LAN ports with the same attributes can form:
- A) A VXLAN
- B) A VLAN
- C) A VPC
- D) A NAT table


**Answer:** **B** — A VLAN
**Topic:** DVS-VLAN Relation

---

**Q150.** VPC stands for:
- A) Virtual Processing Cloud
- B) Virtual Private Cloud
- C) Virtualized Protocol Controller
- D) Variable Public Connection


**Answer:** **B** — Virtual Private Cloud
**Topic:** VPC

---

**Q151.** A VPC creates:
- A) Physical dedicated networks in public cloud
- B) Private virtual networks inside public cloud
- C) Public IP address pools for cloud customers
- D) Hardware-level isolation between data centers


**Answer:** **B** — Private virtual networks inside public cloud
**Topic:** VPC Definition

---

**Q152.** Which of the following components is found in a VPC (as shown in the AWS VPC example)?
- A) Physical TOR switches
- B) Internet Gateway, NAT Gateway, Route Tables, Subnets
- C) Manchester encoding circuits
- D) IEEE 802.3 Ethernet frames only


**Answer:** **B** — Internet Gateway, NAT Gateway, Route Tables, Subnets
**Topic:** VPC Components

---

**Q153.** In the AWS VPC example, a Public VPC Subnet has which IP range?
- A) 172.16.0.0/16
- B) 10.0.0.0/24
- C) 192.168.1.0/24
- D) 10.10.0.0/16


**Answer:** **B** — 10.0.0.0/24
**Topic:** AWS VPC Example

---

**Q154.** Which VPC component is identified as "Gateways" in the lecture?
- A) Route Tables
- B) Internet Gateway and NAT Gateway
- C) Subnets
- D) VPN Connection


**Answer:** **B** — Internet Gateway and NAT Gateway
**Topic:** VPC Gateways

---

**Q155.** Which VPC component is identified as "VLAN Segmentation" in the lecture?
- A) Internet Gateway
- B) NAT Gateway
- C) Route Tables (public/private subnets)
- D) VPN Gateway


**Answer:** **C** — Route Tables (public/private subnets representing VLAN segmentation)
**Topic:** VPC VLAN Segmentation

---

**Q156.** Which of the following is listed as a PRO of VPCs in the lecture?
- A) No need for any gateways
- B) Eliminates routing entirely
- C) Traffic Control (Gateways), Security & Isolation (VLAN), Flexible Network as a Service
- D) Requires dedicated physical hardware


**Answer:** **C** — Traffic Control, Security & Isolation, Flexible Network as a Service
**Topic:** VPC Pros

---

**Q157.** In the AWS VPC example, which service allows connectivity between the VPC and a Corporate Data Center?
- A) Internet Gateway
- B) NAT Gateway
- C) VPN Gateway + VPN Connection + Customer Gateway
- D) Load Balancer


**Answer:** **C** — VPN Gateway + VPN Connection + Customer Gateway
**Topic:** VPC-Corporate Connectivity

---

**Q158.** In a VPC, "Virtual Routers" correspond to which VPC component shown in the lecture diagram?
- A) Internet Gateway
- B) Subnets
- C) Route Tables
- D) VPN Connection


**Answer:** **C** — Route Tables
**Topic:** VPC Virtual Routers

---

### Section 15: Mixed Tricky Questions

**Q159.** Which device would you use to connect two physically separate office networks that use different IP address ranges?
- A) Hub
- B) Repeater
- C) Router
- D) Bridge


**Answer:** **C** — Router
**Topic:** Device Selection

---

**Q160.** A company wants to segment its employees into HR, Engineering, and Finance departments with isolated traffic, all sharing the same physical switches. Which technology should be used?
- A) VXLAN
- B) VLAN
- C) DVS
- D) VPC


**Answer:** **B** — VLAN
**Topic:** Technology Selection

---

**Q161.** A cloud provider needs to support millions of tenant virtual networks on the same physical infrastructure. Traditional VLANs (802.1Q) are insufficient because:
- A) VLANs are too fast
- B) VLAN IDs are limited to 4096 segments (12-bit VID)
- C) VLANs require dedicated physical hardware per tenant
- D) VLANs don't support Layer 3 routing


**Answer:** **B** — VLAN IDs are limited to 4096 segments (12-bit VID)
**Topic:** VXLAN vs VLAN

---

**Q162.** In the TCP/IP model, when a VM makes a `sendmsg()` system call, the hypervisor traps it at which conceptual layer?
- A) Application Layer
- B) Internet Layer
- C) Transport Layer
- D) Network Access Layer (using virtual NICs acting at the physical/data link boundary)


**Answer:** **D** — Network Access Layer (hypervisor intercepts at the virtual NIC level)
**Topic:** System Call & Virtualization

---

**Q163.** What is the correct order of events when a browser loads www.google.com, from first to last?
- A) Render HTML → Send HTTP → DNS → TCP SYN
- B) DNS query → TCP handshake → Send HTTP request → Wait for response → Render HTML
- C) TCP handshake → DNS query → Send HTTP → Render HTML
- D) Send HTTP → DNS → TCP handshake → Render HTML


**Answer:** **B** — DNS query → TCP handshake → Send HTTP request → Wait for response → Render HTML
**Topic:** HTTP Flow

---

**Q164.** Which of the following correctly pairs a network concept with its description?
- A) VTEP → physical router endpoint
- B) VXLAN Underlay → the virtual overlay tunnel
- C) PNIC → Physical Network Interface Card on the host server
- D) VNIC → the physical card in a Cloud switch


**Answer:** **C** — PNIC → Physical Network Interface Card on the host server
**Topic:** Terminology

---

**Q165.** In the cloud data center hierarchy, a server in Rack 1 communicating with a server in Rack 3 (same sector) produces what type of traffic?
- A) North-South
- B) In-Rack
- C) East-West
- D) Internet-bound


**Answer:** **C** — East-West
**Topic:** Traffic Types

---

**Q166.** Which IEEE 802.1Q sub-field is 3 bits and is used for Priority Code Point?
- A) CFI
- B) VID
- C) PRI
- D) TPID


**Answer:** **C** — PRI (Priority Code Point — 3 bits)
**Topic:** 802.1Q Fields

---

**Q167.** In an Ethernet frame, the Preamble is:
- A) 1 byte — Start Frame
- B) 7 bytes — Synchronization/Notification for Receiver
- C) 6 bytes — MAC Address
- D) 4 bytes — CRC


**Answer:** **B** — 7 bytes — Synchronization/Notification for Receiver
**Topic:** Ethernet Preamble

---

**Q168.** Which protocol at the Internet layer is responsible for mapping IP addresses to MAC addresses?
- A) ICMP
- B) ARP (Address Resolution Protocol)
- C) OSPF
- D) BGP


**Answer:** **B** — ARP (Address Resolution Protocol)
**Topic:** ARP

---

**Q169.** RARP (Reverse Address Resolution Protocol) does which of the following?
- A) Maps IP to MAC
- B) Maps MAC to IP
- C) Routes packets between networks
- D) Resolves domain names to IPs


**Answer:** **B** — Maps MAC to IP
**Topic:** RARP

---

**Q170.** In a DVS setup across 3 host machines, the virtual switch spans:
- A) Only one host machine
- B) The physical switch layer only
- C) All host machines through coordinated hypervisors
- D) The internet backbone


**Answer:** **C** — All host machines through coordinated hypervisors
**Topic:** DVS Architecture

---
